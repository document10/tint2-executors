## [volume-icon.sh](https://github.com/nwg-piotr/tint2-executors/blob/master/volume-icon.sh)

This script displays an appropriate volume icon, according to the current volume level. Assign scroll up/down command to increase/decrease level. Use `-l` argument to display level as text next to the icon.

![volume icon](http://nwg.pl/wiki-tint2-executors/icon-volume.png)

## Dependencies:

`alsa-utils`

## Command:

```
~/tint2-executors/volume-icon.sh [-l]
```

`-l` argument turns on textual level display.

## Sample executor:

```
#-------------------------------------
# Executor 3
execp = new
execp_command = ~/tint2-executors/volume-icon.sh -l
execp_interval = 3
execp_has_icon = 1
execp_cache_icon = 1
execp_continuous = 0
execp_markup = 1
execp_tooltip = Scroll ↓↑, middle click to mute
execp_lclick_command = rof -P zenity ~/tint2-executors/zenity-set-volume.sh
execp_rclick_command = rof pavucontrol
execp_mclick_command = amixer set Master toggle -q
execp_uwheel_command = amixer set Master 5%+ unmute -q
execp_dwheel_command = amixer set Master 5%- -q
execp_font = Monospace 9
execp_font_color = #eeeeee 100
execp_padding = 2 0
execp_background_id = 6
execp_centered = 0
execp_icon_w = 20
execp_icon_h = 20
```