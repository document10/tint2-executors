## [bbswitch-status-temp.sh](https://github.com/nwg-piotr/tint2-executors/blob/master/bbswitch-status-temp.sh)

Have you ever needed to know if your hybrid (Optimus) laptop is currently running Intel or Nvidia graphics? In GNOME [there was an extension for that](https://extensions.gnome.org/extension/1100/bumblebee-status). Out of boredom I took a look at its code, which resulted in this short script. It simply reads the `/proc/acpi/bbswitch` file and displays appropriate icon. Of course you need Bumblebee installed. The script uses the `nvidia-smi` package to display the NVIDIA icon with the temperature indication.

![bbswitch-status](http://nwg.pl/wiki-tint2-executors/icon-bbswitch-status-temp.png)

## Dependencies:

`nvidia-smi`

## Command:

`~/tint2-executors/bbswitch-status-temp.sh`

## Sample executor:

```
#-------------------------------------
# Executor 2
execp = new
execp_command = ~/tint2-executors/bbswitch-status-temp.sh
execp_interval = 3
execp_has_icon = 1
execp_cache_icon = 1
execp_continuous = 0
execp_markup = 1
execp_tooltip = 
execp_lclick_command = 
execp_rclick_command = 
execp_mclick_command = 
execp_uwheel_command = 
execp_dwheel_command = 
execp_font = Monospace 9
execp_font_color = #eeeeee 100
execp_padding = 5 0
execp_background_id = 0
execp_centered = 0
execp_icon_w = 24
execp_icon_h = 16
```