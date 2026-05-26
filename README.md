# ZMK CONFIG
---

This is my firmware configuration for [ZMK](https://zmk.dev/docs/).

## My journey

My layout started in a Ferris Sweep so I only had two availabe thumb keys. Initially used Colemak with a layout based on [Seniply](https://stevep99.github.io/seniply/), but have since transitioned to QWERTY. 

Now I'm using a Corne. Having three thumb keys opens the possibility to have mouse movements and other features I want to try.
One problem I have with my keymap is that using the space/shift on both hands takes too much real state in the thumb cluster. To solve the issue I've started experimenting with only moving the SHFT key into home-row mods.
If I see that I can get used to home-row mods, I'll start transitioning my layout to something resembling [Mirioku](https://github.com/manna-harbour/miryoku). 

> Update 3 Jan 2026

I've been using my corne keyboards for the last six months. The shift in the home row feels odd (maybe due to bad config?). 
I've decided to switch from *Colemak* back to *qwerty*. It will be a pain but I think it will be worth it in the long run.

## Hardware setup

This config targets a **5-column Corne** with a dongle setup:

- **Seeed Studio XIAO BLE** — acts as the USB dongle (central). Plugs into the computer via USB and relays keystrokes from the halves over BLE.
- **Left nice!nano** — left keyboard half (BLE peripheral).
- **Right nice!nano** — right keyboard half (BLE peripheral).

### Flashing after firmware changes

Whenever the split topology changes (or after any significant firmware update), BLE bond data must be cleared or the halves and dongle will fail to connect and no keypresses will register.

**Always follow this order:**

1. Flash `settings_reset` to the XIAO BLE, then each nice!nano.
2. Re-flash the actual firmware: dongle first, then left half, then right half.
3. Power on the XIAO (via USB) first, wait a few seconds, then power on each half.

The halves auto-pair with the dongle over BLE. The computer recognises the XIAO as a USB HID keyboard.

## Distinctive features

I did so many modifications to the layout that it no longer resembles the original one. Here a none exhaustive list of modifications:

- Moved the arrow positioning to emulate vim
- Tried to group most of the symbols and numbers under the symbol layout.
    - For breakets, curly braces and parenthesis I use tap dance to complete the closing pair. This is not cumbersome since most IDEs autocomplete the closing pair.
- SPACE/SHIFT on every thumb (currently transitioning out of it).


