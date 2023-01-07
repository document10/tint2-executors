## [battery-icon.sh](https://github.com/nwg-piotr/tint2-executors/blob/master/battery-icon.sh)

This script displays an appropriate battery icon, according to the current charge level and charging state. It has mainly aesthetic values: it should rather be used next to the built-in Tint2 battery indicator, not instead of it. However, you may use `-l` argument to display level as text next to the icon.

Note that the script __does not check if AC connected__, but if the battery is currently in "Charging" state. Opposites are "Not charging" (AC still plugged in) and "Discharging" (AC unplugged). I believe this way the icon is more useful at observing the charge/discharge cycle.

![battery icon](http://nwg.pl/wiki-tint2-executors/icon-battery.png)

## Dependencies:

`acpi`

## Command:

```sh
~/tint2-executors/battery-icon.sh [-l]
```

`-l` argument turns on textual level display

## Sample executor:

```
#-------------------------------------
# Executor 5
execp = new
execp_command = ~/tint2-executors/battery-icon.sh
execp_interval = 30
execp_has_icon = 1
execp_cache_icon = 1
execp_continuous = 0
execp_markup = 1
execp_tooltip = 
execp_lclick_command = b=$(acpi -b) && notify-send "$b"
execp_rclick_command = 
execp_mclick_command = 
execp_uwheel_command = 
execp_dwheel_command = 
execp_font_color = #000000 100
execp_padding = 0 0
execp_background_id = 6
execp_centered = 0
execp_icon_w = 20
execp_icon_h = 20
```