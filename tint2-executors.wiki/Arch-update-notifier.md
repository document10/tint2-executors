## [arch-update.sh](https://github.com/nwg-piotr/tint2-executors/blob/master/arch-update.sh)

If you didn't decide to install `pamac`, you may miss an icon to show that updates are available. I really enjoy
the [Arch Linux Updates Indicator GNOME extension](https://github.com/RaphaelRochet/arch-update) and took a look at its code. In contrary to the original, I decided to check both Arch repos and AUR at the same time.

![Arch update notifier](http://nwg.pl/wiki-tint2-executors/arch-update.png)

___
**NOTE:** This script and executor heavily rely on the terminal and AUR helper installed on your machine. Copying to / use from another location recommended.
___

## Dependencies:

`pacman-contrib`, `xfce4-terminal` or another terminal, `trizen` or another AUR helper, `libnotify` and a [notification server](https://wiki.archlinux.org/index.php/Desktop_notifications#Notification_servers) to see the updates list as a notification (optionally).

## Command: 

~/tint2-executors/arch-update.sh

## Customization:

1. In the [arch-update.sh](https://github.com/nwg-piotr/tint2-executors/blob/master/arch-update.sh) script line:
```
upd=$(/bin/sh -c "/usr/bin/checkupdates && /usr/bin/trizen -Qqu -a")
```
replace `trizen -Qqu -a` with your favourite AUR helper and an appropriate command.

2. In the executor below, in the left click command:
```
execp_lclick_command = xfce4-terminal -e 'sh -c "trizen -Syyu ; echo Finished, press enter to close; read; 
```

replace `xfce4-terminal` with your terminal and `trizen` with your AUR helper.

## Sample executor:
```
#-------------------------------------
# Executor 1
execp = new
execp_command = ~/tint2-executors/arch-update.sh
execp_interval = 1800
execp_has_icon = 1
execp_cache_icon = 0
execp_continuous = 0
execp_markup = 0
execp_tooltip = 
execp_lclick_command = xfce4-terminal -e 'sh -c "trizen -Syyu ; echo Finished, press enter to close; read; killall -SIGUSR1 tint2"'
execp_rclick_command = 
execp_mclick_command = 
execp_uwheel_command = 
execp_dwheel_command = 
execp_font_color = #f8e6e6 100
execp_padding = 0 0
execp_background_id = 0
execp_centered = 0
execp_icon_w = 26
execp_icon_h = 26
```