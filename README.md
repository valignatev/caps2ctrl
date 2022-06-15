## caps2ctrl

Simple capslock to ctrl mapper plugin for [interception tool](https://gitlab.com/interception/linux/tools)

## Usage
Install [interception tools](https://gitlab.com/interception/linux/tools)
Compile caps2ctrl: `./build.sh`

Put this to `/etc/interception/udevmon.yaml`:

```yaml
- JOB: intercept -g $DEVNODE | /path/to/caps2ctrl | uinput -d $DEVNODE
  DEVICE:
    EVENTS:
      EV_KEY: KEY_CAPSLOCK
```

Enable and start udevmon service

## License
Public Domain
