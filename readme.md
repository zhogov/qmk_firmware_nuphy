# zhogov's custom fork

This is my custom fork of the non-merged QMK firmware for Nuphy Air75 v2.
`qmk/qmk_firmware` ← `nuphy-src/qmk_firmware` ← `zhogov/qmk_firmware_nuphy`

**Changes** to the Nuphy version:
- Windows layer is enabled when NumLock is on
- Windows mapping:
  - `LEFT_CMD`    to `LEFT_CTRL`
  - `RIGHT_CMD`   to `RIGHT_WIN`
  - `LEFT_OPTION` to `LEFT_ALT`
  - `FN + CAPS_LOCK` to `NUM_LOCK`
- Common mapping:
  - `FN + B` to `BAT_NUM` – shows battery as LEDs on numbers
  - Macros on `FN + CAT` button. `macro.h` must contain macros like:
```
char _MACRO_STRING[ ] = "\x12\x34\x12\x34\x12\x34\x12\x34\x12\x34";
```

Pulling latest Nuphy changes:
```
git remote add nuphy-src git@github.com:nuphy-src/qmk_firmware.git
git pull --rebase nuphy-src nuphy-keyboards
git push --force
```

**Compiling**: generates nuphy_air75_v2_ansi_via.bin
```
util/docker_build.sh nuphy/air75_v2/ansi:via 
```

**Flash** using QMK Toolbox app:
- Start QMK Toolbox
- Either:
  - Move switch from OFF to WIRED while holding ESC
  - Connect keyboard while holding ESC
- Select firmware file
- Flash

# Quantum Mechanical Keyboard Firmware

[![Current Version](https://img.shields.io/github/tag/qmk/qmk_firmware.svg)](https://github.com/qmk/qmk_firmware/tags)
[![Discord](https://img.shields.io/discord/440868230475677696.svg)](https://discord.gg/Uq7gcHh)
[![Docs Status](https://img.shields.io/badge/docs-ready-orange.svg)](https://docs.qmk.fm)
[![GitHub contributors](https://img.shields.io/github/contributors/qmk/qmk_firmware.svg)](https://github.com/qmk/qmk_firmware/pulse/monthly)
[![GitHub forks](https://img.shields.io/github/forks/qmk/qmk_firmware.svg?style=social&label=Fork)](https://github.com/qmk/qmk_firmware/)

This is a keyboard firmware based on the [tmk\_keyboard firmware](https://github.com/tmk/tmk_keyboard) with some useful features for Atmel AVR and ARM controllers, and more specifically, the [OLKB product line](https://olkb.com), the [ErgoDox EZ](https://ergodox-ez.com) keyboard, and the Clueboard product line.

## Documentation

* [See the official documentation on docs.qmk.fm](https://docs.qmk.fm)

The docs are powered by [Docsify](https://docsify.js.org/) and hosted on [GitHub](/docs/). They are also viewable offline; see [Previewing the Documentation](https://docs.qmk.fm/#/contributing?id=previewing-the-documentation) for more details.

You can request changes by making a fork and opening a [pull request](https://github.com/qmk/qmk_firmware/pulls), or by clicking the "Edit this page" link at the bottom of any page.

## Supported Keyboards

* [Planck](/keyboards/planck/)
* [Preonic](/keyboards/preonic/)
* [ErgoDox EZ](/keyboards/ergodox_ez/)
* [Clueboard](/keyboards/clueboard/)
* [Cluepad](/keyboards/clueboard/17/)
* [Atreus](/keyboards/atreus/)

The project also includes community support for [lots of other keyboards](/keyboards/).

## Maintainers

QMK is developed and maintained by Jack Humbert of OLKB with contributions from the community, and of course, [Hasu](https://github.com/tmk). The OLKB product firmwares are maintained by [Jack Humbert](https://github.com/jackhumbert), the Ergodox EZ by [ZSA Technology Labs](https://github.com/zsa), the Clueboard by [Zach White](https://github.com/skullydazed), and the Atreus by [Phil Hagelberg](https://github.com/technomancy).

## Official Website

[qmk.fm](https://qmk.fm) is the official website of QMK, where you can find links to this page, the documentation, and the keyboards supported by QMK.
