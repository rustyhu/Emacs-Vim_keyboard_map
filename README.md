One kind of keyboard map
================

## Purpose 

When I started to learn and use Emacs and vim, I found the default keyboard map with default keybinds was painful for heavy typing. So I began to look for ideas about comfortable keymap, and remap something like this...

Simply, this keymap helps when you need to use left Ctrl and Esc very frequently, perhaps. 

## Main Idea

|Initial Key|Binded Key|
|-----------|----------|
|Caps Lock	|Esc	   |
|Esc        |Caps Lock |
|Alt_L		|Ctrl_L	   |
|Win_L		|Alt_L	   |
|Ctrl_L		|Win_L	   |


## Others
This Windows version configuration is tested by myself in MS Windows7.
And Linux version configuration is tested in Arch Linux with Xfce4 DE.
More tests are going to be done later.

Added 2016-11-10:
Linux version has been tested several times under Debian with Xfce4. .Xmodmap was effective but these remapped keys happened to be lost after using for a random period. It seemed that system frequently reseted the complete keymap to default.
According to some [info source](https://wiki.archlinux.org/index.php/Xmodmap):
>Note: xmodmap settings are reset by setxkbmap, which not only alters the alphanumeric keys to the values given in the map, but also resets all other keys to the startup default. So setting setxkbmap may be a better choice. 

Especially, Debian has a specific configure file __/etc/default/keyboard__ which could customize the keymap of console and Xorg both, relying on xkb rules. And it has config choices made inside already, which are named caps-swap-escape and l_ctrl-swap-l_win-swap-l_alt. It means some Debian users came up with the same idea as me and made the work done maybe long time ago...

In my computer, caps-swap-escape succedd but l_ctrl-swap-l_win-swap-l_alt failed until some specific system wide "apt upgrade". 
It worked well in my Debian 9, except for some software with GUI, for example Visual Studio Code.


## Acknowledgement

This map configuration in Windows is in regedit file format, which can be generated easily by a no-fee software KeybMap V1.7.3 refer to following URL:

http://www.mympc.org/down/1/2005-11-26_0111998067.html

Thanks to Silence, the author of KeybMap.
