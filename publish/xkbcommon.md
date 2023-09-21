---
title: xkbcommon
excerpt: what is xkbcommon
tags:
---
- XKB, short for X Keyboard
- original keyboard handling subsystem of the [[Xorg]] server.
- converts keyboard input from [[libinput]] ( with the help of [[The Wayland Compositor]] ) in the form of scancodes (which are different for different keyboards ) to a more meaningful and generic key "symbols"
- for example, converting `65` to `XKB_KEY_Space`. It also contains a state machine which knows that pressing "1" while shift is held emits "!".