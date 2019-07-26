# 3DS.py

[![Build Status](https://travis-ci.org/vbe0201/3DS.py.svg?branch=master)](https://travis-ci.org/vbe0201/3DS.py)

3DS.py is a WIP port of the [Python 3.6.9 interpreter][cpython] to the Nintendo 3DS.
It allows you to run your Python scripts directly on the 3DS by having the interpreter
embedded into a homebrew application that launches a `main.py` script from the same
directory.

![3DS.py in action](./.github/showcase.jpg)

## Installation & Usage

Just grab one of the releases [over here][releases] and unzip it. Copy the entire `3DS.py`
folder to the `3ds` directory of your SD card and navigate into it. You should
see a `3DS.py.3dsx` application.

The same directory also contains the entire Python standard library and a `main.py` file.
To run your own projects, copy all source files into the `3DS.py` directory and "start"
your application from within the `main.py` file as this is the entry point to any Python
homebrew.

## Compiling

If you want to compile from source, it is required to set up a
[devkitARM development environment][devkitarm] first. Next, you need to
install the zlib portlib by running `(dkp-)pacman -S 3ds-zlib`. Otherwise
you will get linker errors for the zlib module. Then `cd` into the 3DS.py
directory and run `make` to build the binaries and a statically linked Python
library with the corresponding header files for building Python C modules.

If you're on macOS, make sure to have gnu-sed installed. `brew install gnu-sed`

## Homebrew that uses 3DS.py

A list of cool homebrew projects that make use of 3DS.py.
Want yours to be listed here? PR them.

## Development & Support

Need help? Or want to have an active voice in development of and around this project?
Then join our [Discord guild][discord] which focusses on homebrew development for the
Nintendo 3DS in Python.

This way, things can be discussed more directly and you'll likely get answfers to your
questions faster than through GitHub issues.

## Special thanks

In no particular order, I want to credit these amazing people for
their contributions.

* [3DBrew][3dbrew] for their extensive documentation and research pertaining
to the 3DS.

* [devkitPro][devkitpro] for their devkitARM toolchain.

* [smea][smealum] for the [ctrulib][ctrulib] project.

* [David Buchanan][david buchanan] for troubleshooting assistance.

* [Fenrir][fenrirwolf] for his support and the [ctru-rs][ctru-rs] project
that helped me out with the condition variables implementation.

* [Richard Caseres][richardbmx] for the awesome app icon he designed.

[cpython]: https://github.com/python/cpython/tree/3.6
[releases]: https://github.com/vbe0201/3DS.py/releases
[devkitarm]: https://www.3dbrew.org/wiki/Setting_up_Development_Environment
[discord]: https://discord.gg/PSjzVp8
[3dbrew]: https://www.3dbrew.org
[devkitpro]: https://devkitpro.org
[smealum]: https://github.com/smealum
[ctrulib]: https://github.com/smealum/ctrulib
[david buchanan]: https://github.com/DavidBuchanan314
[fenrirwolf]: https://github.com/FenrirWolf
[ctru-rs]: https://github.com/rust3ds/ctru-rs
[richardbmx]: https://github.com/richardbmx
