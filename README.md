# Luke's build of dwm

## FAQ

> What are the bindings?

This is suckless, mmmbud, the source code is the documentation! Check out [config.h](config.h).

Okay, okay, actually I keep a readme in `larbs.mom` for my whole system, including the binds here.
Press `super+F1` to view it in dwm (zathura is required for that binding).
I haven't kept `man dwm`/`dwm.1` updated though. PRs welcome on that, lol.

## Patches and features

- [Clickable statusbar](https://dwm.suckless.org/patches/statuscmd/) with my build of [dwmblocks](https://github.com/lukesmithxyz/dwmblocks).
- Reads [xresources](https://dwm.suckless.org/patches/xresources/) colors/variables (i.e. works with `pywal`, etc.).
- scratchpad: Accessible with mod+shift+enter.
- New layouts: bstack, fibonacci, deck, centered master and more. All bound to keys `super+(shift+)t/y/u/i`.
- True fullscreen (`super+f`) and prevents focus shifting.
- Windows can be made sticky (`super+s`).
- [stacker](https://dwm.suckless.org/patches/stacker/): Move windows up the stack manually (`super-K/J`).
- [shiftview](https://dwm.suckless.org/patches/nextprev/): Cycle through tags (`super+g/;`).
- [vanitygaps](https://dwm.suckless.org/patches/vanitygaps/): Gaps allowed across all layouts.
- [swallow patch](https://dwm.suckless.org/patches/swallow/): if a program run from a terminal would make it inoperable, it temporarily takes its place to save space.

## Installation on Arch Linux based distributions

### Download the source code

```bash
git clone https://github.com/LukeSmithxyz/dwm.git
cd dwm
```

### Configure

To use a custom `config.h`, place it in the package directory.

### Compile and install

To compile dwm you need to install the `base-devel` package group if you haven't done it previously.

If you have `paru` installed:

```bash
paru -Ui
```

Otherwise:

```bash
makepkg -cirs
```

## Installation for newbs

```bash
git clone https://github.com/LukeSmithxyz/dwm.git
cd dwm
sudo make install
```

## Please install `libxft-bgra`!

This build of dwm does not block color emoji in the status/info bar, so you must install [libxft-bgra](https://aur.archlinux.org/packages/libxft-bgra/) from the AUR, which fixes a libxft color emoji rendering problem, otherwise dwm will crash upon trying to render one. Hopefully this fix will be in all libxft soon enough.
