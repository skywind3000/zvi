# Z-VI

Smallest Vi-clone text editor for Windows (62KB) that runs in terminal and SSH sessions.

## Features

- Smallest full function vi-clone text editor, **only 62KB**.
- Portable, distrubted as a single executable file.
- Offers a wide range of vi functions: search (`/` and `?`), undo (`u`), repeat (`.`), and marks (`m{letter}`).
- Named register for yank/paste: `"a3yy` and `"ap`.
- Supports multiple files with commands like `:next`, `:prev`, and `:rewind`.
- Some colon mode commands with `:` (available options can be listed with `:set`).
- Adapt to window re-sizes.
- Can be used in ssh sessions and none-GUI environments (eg. server container).
- Even runs on Windows XP and Windows 7.
- Supports `%USERPROFILE%\.exrc` configuration.
- Ideal for occasional or emergency use.
- Ideal for keeping it in your rescue USB-stick.


## Download

- Executable file can be found in the [release](https://github.com/skywind3000/zvi/releases) page.

## Screenshots

Runs remotely over an SSH session on a Windows 10 server (using PuTTY):

![](https://skywind3000.github.io/images/p/zvi/zvi_ssh.png)

Runs natively on Windows 7:

![](https://skywind3000.github.io/images/p/zvi/zvi_win7.png)

Runs natively on Windows XP:

![](https://skywind3000.github.io/images/p/zvi/zvi_xp.png)


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
mv busybox.exe zvi.exe
```

## Credit

- https://github.com/rmyorston/busybox-w32


