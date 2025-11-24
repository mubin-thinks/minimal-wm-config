# Configuration
This page will guide the newcomers on how to configure basic elements of status-line,
window manager, terminal etc.


By default, minimal-wm-config may not fit your needs and thus needs to be configured. The
configuration files are located at `$HOME/.config` after install. Below we will discuss
how to configure the basic elements.


## Table of Contents
- [How to customize](https://github.com/mubin-thinks/minimal-wm-config/wiki#how-to-customize)
- [Changing the wallpaper](https://github.com/mubin-thinks/minimal-wm-config/wiki#changing-the-wallpaper)
- [Setting cursor acceleration](https://github.com/mubin-thinks/minimal-wm-config/wiki#setting-cursor-acceleration)
- [Changing overall font and font-size](https://github.com/mubin-thinks/minimal-wm-config/wiki#changing-overall-font-and-font-size)
- [Editing wallpaper to match theme](https://github.com/mubin-thinks/minimal-wm-config/wiki#editing-wallpaper-to-match-theme)
- [Configuring Firefox to match theme](https://github.com/mubin-thinks/minimal-wm-config/wiki#configuring-firefox-to-match-theme)
- [Changing gaps between windows and status-line](https://github.com/mubin-thinks/minimal-wm-config/wiki#changing-gaps-between-windows-and-status-line)


## How to customize
Before we begin customize to fit our needs, we need to understand how configuration of
programs work in Linux.

Linux uses "configuration files" to configure software. The software itself looks at
the config files and changes the settings accordingly. There's a common location where
softwares in Linux usually look at to find them. In Linux the directory is at
`$HOME/.config`. Here the `$HOME` is a environment variable that points to /home/<user> or
the directory that is usually selected as default directory for terminals on startup.
`$HOME` is sometimes also referred to as `~`(tilde character).

Before we edit any config files. We must make sure we have a text editor. You can choose
your favourite text editor for this. Most popular text-editor of today are: Neovim, Emacs,
Nano, VScode and Sublime Text. But you can choose what-ever text editor your prefer.

## Changing the wallpaper
The wallpaper configuration falls on window-managers. So we have to tell/configure
window manager to use our wallpaper. minimal-wm-config currently configured for SwayWM.
So we will look at how to change wallpaper in Sway.

First, we have to open the `~/.config/sway/io` file with a text editor. In the file, you
will find a line like this:
```
output * bg #RRGGBB solid_color
```
Here, #RRGGBB can be any hex value indicating a color. To tell Sway to use a wallpaper,
the line will look like this:
```
output * bg <path/to/wallpaper> fill
```
Here, `fill` is used to tell how the wallpaper will be drawn. Instead of `fill` you can
use `fit`, `center` or `tile`. To find more configuration options for displays, see
manual of `sway-output` by running `man 5 sway-output` in your terminal.

## Setting cursor acceleration
Changing or disabling cursor acceleration is a part of the window-manager. And therefore,
we need to open `~/.config/sway/io` file with a text editor. Then you can add the
following:
```
input type:<"pointer" or "touchpad">
{
    accel_profile <"adaptive" or "flat">
    pointer_accel <-1 to 1>
}
```
Here flat accel_profile indicates that there will be no acceleration for the cursor. The
value of `pointer_accel` can be from -1 to 1. Any value outside of this range will raise
error messages.

Here is an example:
```
input type:pointer
{
    accel_profile flat
    pointer_accel -0.6
}
```

## Changing overall font and font-size
_todo_


## Editing wallpaper to match theme
_todo_


## Configuring Firefox to match theme
To add a custom theme to match Firefox with system's theme, we use an add-on called
[Firefox Color](https://addons.mozilla.org/en-US/firefox/addon/firefox-color/). After
you've installed the add-on, we can add a custom theme.

Open the extension and move to the "Custom Colors" Tab. From there, we will apply colors
for specific themes. The colors of the elements are given below:
### Charcoal Monochrome Dark
```
Toolbar Color = #1b140a
Background Color = #120e08
Search Bar Color = #2a2012
Tab Highlight Color = #8c734e
Popup Text = #d1b994
Toolbar Icons and Text = #d1b994
Background Tab Text Color = #b3976d
Search Text = #d1b994
Popup Background = #120e08
```

### Charcoal Monochrome Light
```
Toolbar Color = #bcab85
Background Color = #c9ba96
Search Bar Color = #9f8f69
Tab Highlight Color = #2e2412
Popup Text = #150f05
Toolbar Icons and Text = #150f05
Background Tab Text Color = #4a3c25
Search Text = #150f05
Popup Background = #bcab85
```

After you've set all the options, you can then save the theme from the top-right
"save" button. The saved themes will be located at "Saved themes" tab.

## Changing gaps between windows and status-line
_todo_
