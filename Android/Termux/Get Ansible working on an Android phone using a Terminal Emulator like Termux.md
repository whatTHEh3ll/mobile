---
title: Get Ansible working on an Android phone using a Terminal Emulator like Termux
source: https://gist.github.com/kuttor/5540b0b7ee18ea62283068b03813693e
author:
published:
created: 2026-05-21
description: Get Ansible working on an Android phone using a Terminal Emulator like Termux - ansible-termux.sh
tags:
  - Android
  - guide
---
```
#!/data/data/com.termux/files/usr/bin/bash

yes | pkg upgrade && \

yes | pkg install \

    python \

    python-dev \

    libffi \

    libffi-dev \

    openssl \

    openssl-dev \

    libsodium \

    clang \

    cmake

# Install the latest Python package manager.

# The version of pip that comes with Python may be outdated.

pip install --upgrade pip

pip list --outdated --format=freeze | \

    grep -v '^\-e' | \

    cut -d = -f 1 | \

    xargs -n1 pip install -U && \

# The pynacl dependency originally did not install because

# it gave problems building dependencies'

pip install --upgrade pynacl

pip install --upgrade ansible
```

```
pkg install python
pip install --upgrade pip
pip install wheel
pkg install rust
export CARGO_BUILD_TARGET=aarch64-linux-android
pip install cryptography
pip install ansible
```

> ```
> pkg install python
> pip install --upgrade pip
> pip install wheel
> pkg install rust
> export CARGO_BUILD_TARGET=aarch64-linux-android
> pip install cryptography
> pip install ansible
> ```

👍

> ```
> pkg install python
> pip install --upgrade pip
> pip install wheel
> pkg install rust
> export CARGO_BUILD_TARGET=aarch64-linux-android
> pip install cryptography
> pip install ansible
> ```

Is not working anymore, because of an opaque pointers error during cryptography compilation.

```
#!/bin/bash

yes | pkg upgrade && \
yes | pkg install \
    openssl python rust build-essential
pip install --upgrade pip setuptools wheel
export CARGO_BUILD_TARGET=aarch64-linux-android
pip install --upgrade cryptography ansible pywinrm[credssp]
```

[@lexxxel](https://github.com/lexxxel) This worked for me in August. Tell me if it still works.

[@eggbean](https://github.com/eggbean) unfortunately no.

```
error: failed to prepare thin LTO module: Opaque pointers are only supported in -opaque-pointers mode (Producer: 'LLVM15.0.1' Reader: 'LLVM 15.0.1')

      error: could not compile \`cryptography-rust\` due to previous error

      Caused by:
        process didn't exit successfully: \`rustc --crate-name cryptography_rust --edition=2018 src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type cdylib --emit=dep-info,link -C opt-
```
```
=============================DEBUG ASSISTANCE=============================
          If you are seeing a compilation error please try the following steps to
          successfully install cryptography:
          1) Upgrade to the latest pip and try again. This will fix errors for most
             users. See: https://pip.pypa.io/en/stable/installing/#upgrading-pip
          2) Read https://cryptography.io/en/latest/installation/ for specific
             instructions for your platform.
          3) Check our frequently asked questions for more information:
             https://cryptography.io/en/latest/faq/
          4) Ensure you have a recent Rust toolchain installed:
             https://cryptography.io/en/latest/installation/#rust

          Python: 3.10.7
          platform: Linux-5.10.81-android12-9-24709469-abF936BXXU1AVHH-aarch64-with-libc
          pip: n/a
          setuptools: 65.3.0
          setuptools_rust: 1.5.2
          rustc: 1.63.0
          =============================DEBUG ASSISTANCE=============================

      error: \`cargo rustc --lib --message-format=json-render-diagnostics --manifest-path src/rust/Cargo.toml --target aarch64-linux-android --release -v --features 'pyo3/extension-module pyo3/abi3-py36' -- --crate-type cdylib\` failed with code 101
      [end of output]

  note: This error originates from a subprocess, and is likely not a problem with pip.
  ERROR: Failed building wheel for cryptography
Failed to build cryptography
ERROR: Could not build wheels for cryptography, which is required to install pyproject.toml-based projects
```

I can't use Ansible under termux directly because Ansible tried to use a strange tmp for path:

```
~ $ ansible -m setup localhost -vvv
...
<127.0.0.1> EXEC /bin/sh -c '( umask 77 && mkdir -p "\` echo ~u0_a510/.ansible/tmp \`"&& mkdir "\` echo ~u0_a510/.ansible/tmp/ansible-tmp-1677705385.2093754-32681-130593073141864 \`" && echo ansible-tmp-1677705385.2093754-32681-130593073141864="\` echo ~u0_a510/.ansible/tmp/ansible-tmp-1677705385.2093754-32681-130593073141864 \`" ) && sleep 0'
Using module file /data/data/com.termux/files/usr/lib/python3.11/site-packages/ansible/modules/setup.py
<127.0.0.1> PUT /data/data/com.termux/files/home/.ansible/tmp/ansible-local-32408cvqlt1ww/tmp60urci3t TO /data/.ansible/tmp/ansible-tmp-1677705385.2093754-32681-130593073141864/AnsiballZ_setup.py
<127.0.0.1> EXEC /bin/sh -c 'rm -f -r '"'"'~u0_a510/.ansible/tmp/ansible-tmp-1677705385.2093754-32681-130593073141864/'"'"' > /dev/null 2>&1 && sleep 0'
localhost | FAILED! => {
    "msg": "failed to transfer file to /data/.ansible/tmp/ansible-tmp-1677705385.2093754-32681-130593073141864/AnsiballZ_setup.py: [Errno 2] No such file or directory: b'/data/.ansible/tmp/ansible-tmp-1677705385.2093754-32681-130593073141864/AnsiballZ_setup.py'"
}
```

/data/.ansible is no valid path to write.

When using proot with Debian:
Most of my ssh connections fail. Some randomly get connected and the result is what is expected. Currently, I'm not able to invest enough time to figure out, what causes the issue.

TL;DR: Ansible under termux is not working on my z fold 4

[@lexxxel](https://github.com/lexxxel) I found that this issue occurs only when using `connection: local` in the playbook. (which is used by ansible -m ping localhost as well I think)
I guess this is a bug in termux as `echo ~u0_a510` is ideally supposed to give `/data/data/com.termux/files/home` but gives `/data`. (on linux echo ~username does give /home/username if a user named username exists)

I found two ways of working around it.

- One is to use ssh connection type and pass the localhost/127.0.0.1 from the inventory. (works only for ansible-playbook and doesn't apply for `ansible -m setup localhost`)
- Or patch ansible code to have this line added. (Works for me both ansible, ansible-playbook commands with connection: local)
```
diff --git a/plugins/connection/local.py b/plugins/connection/local.py
index 27afd10..e21c4df 100644
--- a/plugins/connection/local.py
+++ b/plugins/connection/local.py
@@ -42,6 +42,7 @@ class Connection(ConnectionBase):

     transport = 'local'
     has_pipelining = True
+    _remote_is_local = True

     def __init__(self, *args, **kwargs):
```

Related issues, urls

[@lexxxel](https://github.com/lexxxel) You may reset `ANSIBLE_REMOTE_TEMP` with the proper value such as:

```
export ANSIBLE_REMOTE_TEMP=$HOME/.ansible/tmp
```
