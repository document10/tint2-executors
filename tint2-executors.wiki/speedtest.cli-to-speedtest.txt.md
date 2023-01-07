## [speedtest.sh](https://github.com/nwg-piotr/tint2-executors/blob/master/speedtest.sh)

This script collects data on the Internet connection speed over time, and saves them additively to the ~/speedtest.txt file.

![speedtest-cli >> txt](http://nwg.pl/wiki-tint2-executors/speedtest-cli-txt.png)

## Dependencies:
`speedtest-cli`, optionally `libnotify` and a [notification server](https://wiki.archlinux.org/index.php/Desktop_notifications#Notification_servers) (in my case `xfce4-notifyd`).

## Command:
`~/tint2-executors/speedtest.sh`

## Sample executor:
(Check and save results every half an hour)

```
#-------------------------------------
# Executor 6
execp = new
execp_command = ~/tint2-executors/./speedtest.sh
execp_interval = 1800
execp_has_icon = 0
execp_cache_icon = 1
execp_continuous = 0
execp_markup = 1
execp_lclick_command = 
execp_rclick_command = 
execp_mclick_command = 
execp_uwheel_command = 
execp_dwheel_command = 
execp_font_color = #000000 100
execp_padding = 0 0
execp_background_id = -1
execp_centered = 0
execp_icon_w = 0
execp_icon_h = 0
```
## Sample output:

```
25-09-18 10:10
Ping: 6.643 ms Download: 65.18 Mbit/s Upload: 67.10 Mbit/s
25-09-18 10:10
Ping: 7.21 ms Download: 75.33 Mbit/s Upload: 40.90 Mbit/s
25-09-18 10:11
Ping: 6.978 ms Download: 77.04 Mbit/s Upload: 61.81 Mbit/s
25-09-18 10:12
Ping: 6.572 ms Download: 75.04 Mbit/s Upload: 35.73 Mbit/s
25-09-18 10:13
Ping: 8.248 ms Download: 71.90 Mbit/s Upload: 45.71 Mbit/s
25-09-18 10:14
Ping: 6.704 ms Download: 68.97 Mbit/s Upload: 63.97 Mbit/s
25-09-18 10:15
Ping: 7.001 ms Download: 66.01 Mbit/s Upload: 40.28 Mbit/s
25-09-18 10:16
Ping: 6.585 ms Download: 75.53 Mbit/s Upload: 45.66 Mbit/s
25-09-18 10:16
Ping: 8.351 ms Download: 66.61 Mbit/s Upload: 54.26 Mbit/s
25-09-18 10:30
Ping: 7.344 ms Download: 68.45 Mbit/s Upload: 61.03 Mbit/s
25-09-18 11:01
Ping: 7.294 ms Download: 71.73 Mbit/s Upload: 60.54 Mbit/s
25-09-18 11:14
Ping: 6.62 ms Download: 71.29 Mbit/s Upload: 30.65 Mbit/s
```