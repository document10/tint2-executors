## [bbswitch-status.sh](https://github.com/nwg-piotr/tint2-executors/blob/master/bbswitch-status.sh)

Have you ever needed to know if your hybrid (Optimus) laptop is currently running Intel or Nvidia graphics? In GNOME [there was an extension for that](https://extensions.gnome.org/extension/1100/bumblebee-status). Out of boredom I took a look at its code, which resulted in this short script. It simply reads the `/proc/acpi/bbswitch` file and displays appropriate icon. Of course you need Bumblebee installed.

![bbswitch-status](http://nwg.pl/wiki-tint2-executors/bumblebee-status-on-off.png)

## Command:

`~/tint2-executors/bbswitch-status.sh`

## Sample executor:

```
#-------------------------------------
# Executor 4
execp = new
execp_command = ~/tint2-executors/bbswitch-status.sh
execp_interval = 2
execp_has_icon = 1
execp_cache_icon = 1
execp_continuous = 0
execp_markup = 0
execp_tooltip = 
execp_lclick_command = 
execp_rclick_command = 
execp_mclick_command = 
execp_uwheel_command = 
execp_dwheel_command = 
execp_font_color = #ffffff 100
execp_padding = 0 0
execp_background_id = 0
execp_centered = 1
execp_icon_w = 30
execp_icon_h = 30
```