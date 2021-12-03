# Accelrotate

Tiny program for rotating devices based on accelerometer data. E.g. rotating screens on laptops.

## Install

```
$ pip install accelrotate
```

# Usage

```
$ accelrotate --help
Usage: accelrotate [OPTIONS] [[normal|inverted|left|right]]

Rotate display and devices based on accelerometer data.
Requires: xinput, xrandr, xsetwacom (for --wacom flag)

Options:
  -d, --no-display  do not rotate display
  -l, --loop        continuesly check rotation in loop every X second where
  -w, --wacom TEXT  rotate wacom devices that match name pattern  [default:
                    wacom]
  -x, --xorg TEXT   rotate Xorg devices that match name pattern  [default:
                    touchscreen|touch digitizer|trackpoint|mouse]
  --help            Show this message and exit.
```

Either a loop or single rotation can be executed:

```
# rotate devices and screen
$ accelrotate --display -x "touchscreen|trackpoint" left 
$ accelrotate 
```
