---
title: Flashcard Firmwares
---

TWiLight Menu++ is an all-in-one customizable menu for a variety different applications. We'll be setting it up to launch homebrew that cannot directly be launched via your kernel and for emulator usage.
 - For the iPlayer, Games'N'Music and other flashcarts only able to launch homebrew, you can also use the pre-installed B4DS to launch retail ROMs.

## Installation
### Section I -- SD Card Setup

1. Download the latest version of [TWiLight Menu++](https://github.com/DS-Homebrew/TWiLightMenu/releases/latest)
2. Extract the `_nds` folder to the root of your flashcart's microSD card.
  - **Not** the one located in `Flashcard users`
3. Delete `_nds\TWiLightMenu\widescreen`. Cheat codes from `.bin` files aren't applied on B4DS.

### Section II -- Flashcart Specific setups
#### R4iDSN/R4 Ultra/R4i Gold RTS & SuperCard DSTWO

These flashcarts are able to boot Nintendo DS ROMs using their flashcart kernel as opposed to the rather low compatibility of B4DS.

1. Delete `GBARunner2_arm7dldi_3ds.nds`, `GBARunner2_arm7dldi_dsi.nds`, `nds-bootstrap-nightly.nds` & `nds-bootstrap-release.nds` from the `_nds` folder.
2. If there is no `BOOT.NDS` found on the flashcart's microSD card's root, copy it from `Flashcard users`.
3. Extract the `_nds` folder from `Flashcard users` to the root of your flashcart's microSD card.
  - If asked, merge the directories.
4. Download the pack for your flashcard:

- [R4iDSN/R4 Ultra/R4i Gold RTS](https://www.dropbox.com/s/j8nquh073k9y0h7/DS%20Game%20Forwarder%20pack%20%28R4iDSN%2C%20R4i%20Gold%20RTS%29.7z?dl=1)
- [SuperCard DSTWO](https://www.dropbox.com/s/pyyg0vq8b0nmhqd/DS%20Game%20Forwarder%20pack%20%28SC%20DSTWO%29.7z?dl=1)

5. Extract the contents of `For Slot-1 microSD` to the root of the flashcart's microSD card.
6. If you'd like to automatically launch into TWiLight Menu++ when you launch your Slot-1 Flashcart, extract the contents of `Flashcard users/Autoboot/(your card)` to the root of your flashcart's microSD card.
7. Go to the TWiLight Menu++ settings application and set "Use nds-bootstrap" to "No".

#### CycloDS iEvolution

This flashcart is able to use the Nintendo DSi version of nds-bootstrap as opposed to B4DS. This has access to the features that B4DS doesn't, such as soft-reset not shutting down the console, cheats & full access to the 16 MB of RAM.

- Extract `BOOT_cyclodsi.nds`, rename it to `BOOT.NDS` and place it at the root of your SD card.

#### Other flashcarts

1. Delete `GBARunner2_arm7dldi_3ds.nds`, `GBARunner2_arm7dldi_dsi.nds`, `nds-bootstrap-nightly.nds` & `nds-bootstrap-release.nds` from the `_nds` folder.
2. If there is no `BOOT.NDS` found on the flashcart's microSD card's root, copy it from `Flashcard users`.
3. Extract the `_nds` folder from `Flashcard users` to the root of your flashcart's microSD card.
  - If asked, merge the directories.

### Section III - Configuration

Most of this boils down to personal preference, so change the configuration per your likings.
The way to access the TWiLight Menu++ settings varies between your configuration.

- DS Classic Menu: Hit the button on the very bottom
- Nintendo DSi/SEGA Saturn/Homebrew Launcher themes using SELECT Menu: Hit SELECT, then launch the Settings Applet (use the D-PAD to highlight options)
- Nintendo DSi/SEGA Saturn/Homebrew Launcher themes not using SELECT Menu: Hitting SELECT will bring you to the DS Classic Menu
- Nintendo 3DS theme: Use the touch screen to touch the wrench
- R4 Original theme: Hit START (if you're in the file browser), then hit SELECT
- Acekard theme: Go out of the file browser (hit B a bunch), then scroll to find and launch the Settings Applet

From there, you will get a few options of things you could do.

#### GUI Settings
- **DS Classic Menu on startup** - This option will enable the DS Classic Menu to appear on startup (explanation below).
- **DSi/Saturn: SELECT** - This option changes the functionality of what hitting the SELECT button does in the Nintendo DSi, SEGA Saturn and Homebrew Launcher themes.
  - DS Classic Menu: This menu is similar to the user interface of the original Nintendo DS. While not full-scale for a theme, it's made for quick and easy access. Has shortcuts to Pictochat and Nintendo DS Download Play. It will take longer than using the SELECT Menu, since it is an entirely separate application.
  - SELECT Menu: This menu is embedded in the theme, so it will load much quicker. The downside is that there is no shortcut to Pictochat and DS Download Play.
- **Themes** - There are 6 different themes included with TWiLight Menu++. You can also hit A for sub themes, taken from your SD card. 
  - Nintendo DSi: Made to mimick the Nintendo DSi System Menu. Uses a pagination system, where there is a new page every 20 files. You can use the bottom scrollbar to navigate quickly through the current page, or hit the triggers to go back a page or forward a page.
    - You can set `.png` images to display on the top screen. If you have multiple images, it will select which to use at random. Just make sure to use tinypng to reduce the file size and have the image size be no bigger than 208x156.
  - Nintendo 3DS: Made to mimick the Nintendo 3DS Home Menu. Uses the same pagination system as DSi theme, but without the bottom bar.
  - SEGA Saturn: Only allows for one entry at a time. Particularly space like. Does not have any sub-theme support. 
  - Homebrew Launcher: Mimicks the 3DS Homebrew Launcher & Wii Homebrew Channel. Implements the bubble effect on the bottom screen.
  - R4 Original: Mimicks the original UI of the original R4 Firmware. Subthemes must use either `A1 R5 G5 B5` or `X1 R5 G5 B5` BMP images.
  - Acekard: Ported the UI from Wood RPG. Subthemes are cross-compatible with the original Wood RPG or Wood R4.
- **DSi/3DS Music** - Changes the music played for the Nintendo DSi, Nintendo 3DS & Homebrew Launcher themes. Options should be self-explanatory.
- **Update Recently Played list** - Updates a list used for the "Last Played" sort option. Disable this, if launching a game or app causes a Guru Meditation Error.
- **Sort Method** - Changes the order that the applications are viewed in, for the Nintendo DSi, Nintendo 3DS, SEGA Saturn and Homebrew Launcher themes.
- **Directories/Folders** - Toggles showing folders in the UI.
- **Show hidden files** - Toggles showing hidden files in the UI.
 - Files are hidden via FAT attributes (Windows/MacOS) or if they have a period in front of it (Unix).
 - Regardless of the toggle above, the `_nds` folder will never be shown.
- **Show box art** - Show's the box art of the item highlighted on the top screen.
 - This only works on the Nintendo DSi, Nintendo 3DS & SEGA Saturn themes.
 - Place the PNG images in `/_nds/TWiLightMenu/boxart`
 - The images can be titled either the game's title ID (ex. `ASME.png`, DS Games only) or the filename (ex. `SM64DS.nds.png`).
 - You can use [TWiLight Menu++ Boxart Downloader](https://github.com/KirovAir/TwilightBoxart) to download the images for you.
 - If you'd like to make your own, follow these file sizes:

```
NDS/DSi: 128x115
GBA/FDS/GBC/GB: 115x115
NES/GEN/MD/SFC/MS/GG: 84x115
SNES: 158x115
```

- **Animate DSi icons** - Animates the Nintendo DSi icons in the UI.
- **Clock System** - Switch between the 12 hour (AM/PM) system and the 24 hour system in the Acekard theme
- **Scroll speed** - Sets the scroll speed of the Acekard theme.

#### Emulation/HB settings

This page is for the individual loaders that TWiLight Menu++ uses.

- **NDS ROMs** - This is launched using nds-bootstrap/B4DS or your flashcart kernel. Not recommended to use B4DS unless absolutely necessary.
- **Video Files** - These are `.rvid` and `.mp4` videos, using RocketVideoPlayer and MPEG4Player. We recommend converting your videos to Moonshell, instead.
- **Atari 2600 ROMs** - These are launched using StellaDS.
- **NES/FDS ROMs** - These are launched using nesDS
- **GameBoy (Color) ROMs** - These are launched using GameYob.
- **Sega Master System/Game Gear ROMs** - These are launched using S8DS.
- **Sega Mega Drive/Genesis ROMs** - You have two options: PicoDriveTWL & jEnesisDS. We recommend using jEnesisDS
  - PicoDriveTWL: No audio, choppy framerate, but has a higher filesize limit if you use a DS Memory Pak. Otherwise, if you **don't** have a Memory Pak, it has a 2.5 MB filesize limit.
  - jEnesisDS: Audio, smooth framerate but has a 3 MB filesize limit that is not extendable with a DS Memory Pak.
- **Super NES/FDS ROMs** - These ROMs are launched using SNEmulDS.

#### GBARunner2 Settings

GBARunner2 is a Gameboy Advance hypervisor for the Nintendo DS. It allows you to run Gameboy Advance ROMs from your DS Flashcart, without the need of a GBA Flashcart.

{% capture notice-1 %}
In order to use GBARunner2, you will need to have a Gameboy Advance BIOS file titled `bios.bin`. While you can place it on the root or the `/gba` folder, we recommend placing it in `/_gba`, next to where the configuration file is stored.

In order to verify that you have a valid BIOS, we have added a few hashes you can compare your file towards. You only need to check one of these hashes, but MD5 is the most common and can be done [through a website too](http://onlinemd5.com/).

**CRC32**: `81977335`
**MD5**: `a860e8c0b6d573d191e4ec7db1b1e4f6`
**SHA1**: `300c20df6731a33952ded8c436f7f186d25d3492`
**SHA256**: `fd2547724b505f487e6dcb29ec2ecff3af35a841a77ab2e85fd87350abd36570`

There are three ways you can dump a BIOS:

- [A homebrew'd non-family edition Wii/GameCube with a link cable](https://github.com/FIX94/gba-link-cable-dumper)
- [GBA/DS (Phat + Lite) with a GBA Flashcard](https://glazedbelmont.github.io/gbabiosdump/#gameboy-advance-sp-micro-ds-ds-lite)
- [CFW'd 3DS using most Virtual Console Titles](https://glazedbelmont.github.io/gbabiosdump/#virtual-console-title-from-a-3ds) (can't be GBA or non-nintendo).
{% endcapture %}

<div class="notice">{{ notice-1 | markdownify }}</div>

- **(Slot-1 SD:) DLDI access** - Set which ARM processor should handle DLDI. Recommended one is ARM9 but use ARM7 if your flashcart is incompatible
- **Screen Display** - Pick which screen to display the gameboy advance application in.
- **Center and Mask** - Centers the game with a border, at the cost of a frame delay.
- **Simulate GBA colors** - Stimulates GBA colors by darkening the screen