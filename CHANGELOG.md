## New changes
* NFC: CharlieCard parser (by @zacharyweiss)
* SubGHz: Enabled tx-rx state on unused gpio pin by default (**external amp option was removed and is enabled by default now**)
* SubGHz: Status output !TX/RX on the GDO2 CC1101 pin (by @quen0n | PR #742)
* SubGHz: Reworked saved settings (by @xMasterX and @Willy-JL)
* Desktop: Fixes for animation unload (by @Willy-JL)
* Misc: Added `void` due to `-Wstrict-prototypes`
* Misc: Some code cleanup and proper log levels in nfc parsers
* Infrared: Allow external apps to use infrared settings (by @Willy-JL)
* JS & HAL: Various fixes and FURI_HAL_RANDOM_MAX define added (by @Willy-JL)
* JS: BadUSB layout support (by @Willy-JL)
* JS: Module `widget` and path globals (by @jamisonderek)
* Apps: NFC Magic - **Gen2 writing support** (by @Astrrra)
* Apps: MFKey - fixed crashes (by @noproto)
* Apps: **Check out Apps updates by following** [this link](https://github.com/xMasterX/all-the-plugins/commits/dev)
* OFW: Desktop: ensure that animation is unloaded before app start (fixes some out of memory crashes)
* OFW: Hide unlock with reader for MFU-C 
* OFW: fbt: fixed missing FBT_FAP_DEBUG_ELF_ROOT to dist env
* OFW: fbt: added -Wstrict-prototypes for main firmware
* OFW: Mifare Ultralight naming fix 
* OFW: IR: Remember OTG state
* OFW: Bad USB: fix crash when selecting a keyboard layout
* OFW: L1_Mods animation update : adding VGM visual 
* OFW: RFID Improvements 
* OFW: Fixed plugins and UI 
* OFW: NFC: Fix mf desfire detect
* OFW: infrared_transmit.h was missing `#pragma once`
* OFW: Show the wrong PIN Attempt count on the login screen
* OFW: SavedStruct: Introduce saved_struct_get_metadata
* OFW: JS CLI command
* OFW: Add ChromeOS Bad USB demo
* OFW: Configurable Infrared TX output (previous UL version is replaced with OFW version, new features added "AutoDetect" and saving settings)
* OFW: BadUSB: BLE, media keys, Fn/Globe key commands
* OFW: NFC: Slix privacy password reveal and Desfire detect fix
* OFW: github: additional pre-upload checks for doxygen workflow
* OFW: NFC UI fixes
* OFW: Gui: unicode support, new canvas API
* OFW: Api Symbols: replace asserts with checks 
<br><br>
#### Known NFC post-refactor regressions list: 
- Mifare Mini clones reading is broken (original mini working fine) (OFW)
- NFC CLI was removed with refactoring (OFW) (will be back soon)
- Current list of affected apps: https://github.com/xMasterX/all-the-plugins/tree/dev/apps_broken_by_last_refactors
- Also in app **Enhanced Sub-GHz Chat** - NFC part was temporarily removed to make app usable, NFC part of the app requires remaking it with new nfc stack

----

[-> How to install firmware](https://github.com/DarkFlippers/unleashed-firmware/blob/dev/documentation/HowToInstall.md)

[-> Download qFlipper (official link)](https://flipperzero.one/update)

## Please support development of the project
|Service|Remark|Link/Wallet|
|-|-|-|
|**Patreon**||https://patreon.com/mmxdev|
|**Boosty**|patreon alternative|https://boosty.to/mmxdev|
|cloudtips|only RU payments accepted|https://pay.cloudtips.ru/p/7b3e9d65|
|YooMoney|only RU payments accepted|https://yoomoney.ru/fundraise/XA49mgQLPA0.221209|
|USDT|(TRC20)|`TSXcitMSnWXUFqiUfEXrTVpVewXy2cYhrs`|
|ETH|(BSC/ERC20-Tokens)|`darkflippers.eth` (or `0xFebF1bBc8229418FF2408C07AF6Afa49152fEc6a`)|
|BTC||`bc1q0np836jk9jwr4dd7p6qv66d04vamtqkxrecck9`|
|SOL|(Solana/Tokens)|`DSgwouAEgu8iP5yr7EHHDqMNYWZxAqXWsTEeqCAXGLj8`|
|DOGE||`D6R6gYgBn5LwTNmPyvAQR6bZ9EtGgFCpvv`|
|LTC||`ltc1q3ex4ejkl0xpx3znwrmth4lyuadr5qgv8tmq8z9`|
|BCH||`qquxfyzntuqufy2dx0hrfr4sndp0tucvky4sw8qyu3`|
|XMR|(Monero)| `41xUz92suUu1u5Mu4qkrcs52gtfpu9rnZRdBpCJ244KRHf6xXSvVFevdf2cnjS7RAeYr5hn9MsEfxKoFDRSctFjG5fv1Mhn`|
|TON||`UQCOqcnYkvzOZUV_9bPE_8oTbOrOF03MnF-VcJyjisTZmsxa`|

#### Thanks to our sponsors who supported project in the past and special thanks to sponsors who supports us on regular basis:
ClaraCrazy, Pathfinder [Count Zero cDc], callmezimbra, Quen0n, MERRON, grvpvl (lvpvrg), art_col, ThurstonWaffles, Moneron, UterGrooll, LUCFER, Northpirate, zloepuzo, T.Rat, Alexey B., ionelife, ...
and all other great people who supported our project and me (xMasterX), thanks to you all!


## **Recommended update option - Web Updater**

### What `n`, `r`, `e`, ` `, `c` means? What I need to download if I don't want to use Web updater?
What build I should download and what this name means - `flipper-z-f7-update-(version)(n / r / e / c).tgz` ? <br>
`flipper-z` = for Flipper Zero device<br>
`f7` = Hardware version - same for all flipper zero devices<br>
`update` = Update package, contains updater, all assets (plugins, IR libs, etc.), and firmware itself<br>
`(version)` = Firmware version<br>
| Designation | 3 Custom Animation | [Base Apps](https://github.com/xMasterX/all-the-plugins#default-pack) | [Extra Apps](https://github.com/xMasterX/all-the-plugins#extra-pack) | ⚠️RGB mode* |
|-----|:---:|:---:|:---:|:---:|
| ` ` | ✅ | ✅ |  |  |
| `c` | ✅ |  |  |  |
| `n` |  | ✅ |  |  |
| `e` | ✅ | ✅ | ✅ |  |
| `r` | ✅ | ✅ | ✅ | ⚠️ |

⚠️This is [hardware mod](https://github.com/quen0n/flipperzero-firmware-rgb#readme), works only on modded flippers! do not install on non modded device!

Firmware Self-update package (update from microSD) - `flipper-z-f7-update-(version).tgz` for mobile app / qFlipper / web<br>
Archive of `scripts` folder (contains scripts for FW/plugins development) - `flipper-z-any-scripts-(version).tgz`<br>
SDK files for plugins development and uFBT - `flipper-z-f7-sdk-(version).zip`



