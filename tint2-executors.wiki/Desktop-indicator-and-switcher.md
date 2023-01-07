## [desktop.py](https://github.com/nwg-piotr/tint2-executors/blob/master/desktop.py)

This Python script displays current desktop indicator. Assign scroll up/down command to `n` (next) / `p` (previous) argument to switch desktops.

![desktop icon](http://nwg.pl/wiki-tint2-executors/icon-desktop.png)

### Command:

```
python ~/tint2-executors/desktop.py [n] | [p] | [number]
```
`n` - next desktop

`p` - previous desktop

`number` - number of desktop to switch to

Called with no argument the script will just return the patch to appropriate icon to be displayed by the executor.

### Dependencies:

`python` (`python3`)

### Sample executor:

(switching desktops assigned to mouse scroll events)

```
#-------------------------------------
# Executor 2
execp = new
execp_command = python ~/tint2-executors/desktop.py
execp_interval = 1
execp_has_icon = 1
execp_cache_icon = 1
execp_continuous = 0
execp_markup = 1
execp_tooltip = Scroll ↓↑
execp_lclick_command = 
execp_rclick_command = 
execp_mclick_command = 
execp_uwheel_command = python ~/tint2-executors/desktop.py n
execp_dwheel_command = python ~/tint2-executors/desktop.py p
execp_font = Monospace 9
execp_font_color = #eeeeee 100
execp_padding = 5 0
execp_background_id = 6
execp_centered = 0
execp_icon_w = 16
execp_icon_h = 16
```