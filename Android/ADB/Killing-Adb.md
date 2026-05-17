______________________________________________________________________

## title: Kill Adb source: Local vault description: Kill stubborn ADB

# Kill ADB

## Get PID with ss command (port 5037 by default)

```bash
ss -ltnp | grep :5037
```

## Kill PID

```bash
kill -9 "PID"
```
