<div align="center">
    <h1><code>minimal-wm-config</code></h1>

**[Preview] | [Basic Keybinds] | [Docs] | [Install] | [Contribute]**
</div>

[Preview]: https://github.com/mubin-thinks/minimal-wm-config/blob/master/showcases.md
[Basic Keybinds]: https://github.com/mubin-thinks/minimal-wm-config/?tab=readme-ov-file#basic-keybinds
[Docs]: https://github.com/mubin-thinks/minimal-wm-config/wiki
[Install]: https://github.com/mubin-thinks/minimal-wm-config?tab=readme-ov-file#install-automated
[Contribute]: https://github.com/mubin-thinks/minimal-wm-config?tab=readme-ov-file#contributing

## About
minimal-wm-config is a configuration for window managers in Linux. It contains
configurations for terminal, app launcher, window manager etc. minimal-wm-config is used
to configure a window-manager quickly rather than writing configurations from scratch and
can be used as base for other configurations.

minimal-wm-config is very simply written for clarity and to avoid complexity. The goal
is to write as little configuration as possible to make window managers exquisite.

## Basic Keybinds
The `super` key is the Windows key on traditional keyboards. And the Command Key on Mac
keyboards.

| Keybind | Action | Description |
| --- | --- | --- |
| `super+enter` | Open terminal | Opens the Alacritty Terminal. |
| `super+q` | Close a program | Terminates the focused window and program if the program does not run in background. |
| `super+d` | Open Launcher | Opens the Tofi Application Launcher. |
| `super+s` | Take Screenshot | Take screenshot of a selected portion with `grim` and `slurp` programs. |
| `super+<h,j,k,l or arrow keys>` |  Focus window in tiling mode | Focus window in given direction. |
| `super+shift+<h,j,k,l or arrow keys>` | Swap with window | Swap with a tiling window within a tiling window in given direction. |
| `super+space` | Swap focus with tiling and floating windows | Change focus from a tiling window to a floating window(if any) and vise-versa. |
| `super+f` | Fullscreen current window | Fullscreen the currently focused window. |
| `super+shift+f` | Turn window mode to floating | Turn the focused window's mode to tiling to floating or vise-versa. |
| `super+<mouse left click + move mouse>` | Move tiling or floating window position | In floating mode, change the window's position. In tiling mode swap with other window. |
| `super+<mouse right click + move mouse>` | Resize tiling or floating window | In floating mode, change the window's size. In tiling mode resize focused and other adjacent windows accordingly. |
| `super+m` | Exit Window Manager | Terminate window manager. The computer goes to login display manager or TTY terminal. |

There are more keybinds then listed here. If you are interested on those, then take a
look at files ending with `_keybinds` in the `~/.config/sway` directory.

## Install (Automated)
### Dependencies
```bash
# ARCH LINUX
$ yay -Sy sway swaybg swaylock swayidle alacritty fish waybar eza grim slurp tofi

# VOID LINUX
$ sudo xbps-install -S sway swaybg swaylock swayidle alacritty fish-shell Waybar eza grim slurp tofi

# DEBIAN LINUX (tofi needs to be built from source)
$ sudo apt update
$ sudo apt install sway swaybg swaylock swayidle alacritty fish waybar eza grim slurp
```

### Installing the font
The configuration uses the [Iosevka](https://github.com/be5invis/Iosevka) font. You can
download it from [here](https://github.com/be5invis/Iosevka/releases/latest). After
you have downloaded and unzipped the file, run the following command to install it:
```bash
$ mv *.ttf /usr/share/fonts/TTF
```

### Installation
> [!WARNING]
> This method will automatically delete your old configurations. If you care about them,
> make sure to back them up before running the script.

This installation process is automated with `install.fish`. Make sure you have `fish`
shell installed. If so, `cd` into the project. Now, you shall list the themes available
to minimal-wm-config. You can do so with this command:
```fish
$ ./install.fish -h
```

Then, add the theme's name you like to the following command:
``` fish
$ ./install.fish -t <theme-name>
```

## Contributing
If you encounter any bug or want to suggest change/improvement, create an issue.


If you wish to contribute/create Pull Requests, feel free to do so. I will review them
and make proper changes(typos, code-style etc.) before merging with upstream.


Currently minimal-wm-config supports few themes and it should be increased. If you are
not sure where to contribute to, you can focus in this section.
