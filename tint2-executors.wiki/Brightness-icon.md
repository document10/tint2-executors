## [brightness-icon.sh](https://github.com/nwg-piotr/tint2-executors/blob/master/brightness-icon.sh)

This script displays an appropriate brightness icon, according to the current brightness level. Assign scroll up/down command to increase/decrease level. Use -l argument to display level as text next to the icon.

![brightness icon](http://nwg.pl/wiki-tint2-executors/icon-brightness.png)

## Dependencies:

`xorg-xbacklight` or `light-git` (AUR). Check the [project site](https://github.com/haikarainen/light) for info on other Linux distributions.
## Command:

```
~/tint2-executors/icon-brightness.sh [-l]
```

`-l` argument turns on textual level display.

## Sample executor:

For `light` package replace:
- `xbacklight -5` with `light -U 5`
- `xbacklight +5` with `light -A 5`

```
#-------------------------------------
# Executor 4
execp = new
execp_command = ~/tint2-executors/brightness-icon.sh -l
execp_interval = 3
execp_has_icon = 1
execp_cache_icon = 1
execp_continuous = 0
execp_markup = 1
execp_tooltip = Scroll ↓↑
execp_lclick_command = rof -P zenity ~/tint2-executors/zenity-set-brightness.sh
execp_rclick_command = rof arandr
execp_mclick_command = 
execp_uwheel_command = xbacklight +5
execp_dwheel_command = xbacklight -5
execp_font = Monospace 9
execp_font_color = #eeeeee 100
execp_padding = 2 0
execp_background_id = 6
execp_centered = 0
execp_icon_w = 20
execp_icon_h = 20
```