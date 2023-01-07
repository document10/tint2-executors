## [wifi-name.sh](https://github.com/nwg-piotr/tint2-executors/blob/master/wifi-name.sh)

Bash script to display the name of Wi-Fi network currently in use, labeled with an icon or text.

![wi-fi name](http://nwg.pl/wiki-tint2-executors/wifi-name.png)

## Command:

`~/tint2-executors/wifi-name.sh [-N] [-M'My custom name:']`

With no argument the command displays the network icon and current network name. Optionally you can replace the icon with default or custom label.

## Sample executor:

```
#-------------------------------------
# Executor 1
execp = new
execp_command = ~/tint2-executors/wifi-name.sh
execp_interval = 5
execp_has_icon = 1
execp_cache_icon = 1
execp_continuous = 0
execp_markup = 1
execp_lclick_command = 
execp_rclick_command = 
execp_mclick_command = 
execp_uwheel_command = 
execp_dwheel_command = 
execp_font = Monospace 9
execp_font_color = #eeeeee 100
execp_padding = 10 0
execp_background_id = 0
execp_centered = 0
execp_icon_w = 16
execp_icon_h = 16
```