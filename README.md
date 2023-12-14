# Z-VI

Smallest Vi-clone Text Editor for Windows (62KB).

## Features

- Portable, distrubted as a single executable.
- Smallest full function vi-clone, **only 62KB**.
- Offers a wide range of vi functions: search (`/` and `?`), undo (`u`), repeat (`.`), and marks (`m{letter}`).
- Named register for yank/paste: `"a3yy` and `"ap`.
- Supports multiple files with commands such as `:next`, `:prev`, and `:rewind`.
- Some colon mode commands with `:` (can be listed with `:set`).
- Adapt to window re-sizes.
- Can be used in ssh sessions and none-GUI environments (eg. server container).
- Even runs on Windows XP and Windows 7.
- Ideal for occasional or emergency use.


## Download

- See the release page.


## Source

Busybox includes a well-implemented and maintained `vi` applet, which has been contributed to for more than 10 years by the busybox contributors

The code is from [busybox-w32](https://github.com/rmyorston/busybox-w32) project, I just tailor it into a single applet.

## Build

Download and install MSYS2, start `MinGW32` program:

```
git clone --depth 1 https://github.com/rmyorston/busybox-w32.git
git clone https://github.com/skywind3000/zvi.git
cd busybox-w32
make mingw32_defconfig    # 32 bits will run on more platforms
```

then just:

```
copy ../zvi/.config .     # use the predefined configuration
make
ren busybox.exe zvi.exe
```

## Credit

- https://github.com/rmyorston/busybox-w32


