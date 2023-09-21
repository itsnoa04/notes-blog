---
title: What is libinput
excerpt: libinput
---
- similar to [[libdrm]]
- abstracts the [[DRM]] subsystem
- provides the [[Userspace]] end of [[evdev]].
- responsible for receiving input events from the [[Kernel]] from various input devices -> decoding them into a usable format -> passing them on to the [[The Wayland Compositor]].