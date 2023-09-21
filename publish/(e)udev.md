---
title: udev
excerpt: eudev
---
- udev is a daemon system
- Deals with the appearance of new devices from the [[Kernel]]
- configures permissions for the resulting device nodes in `/dev`
- notifying the various applications running about these changes
- used by the [[Userspace]].
- [[The Wayland Compositor]] uses udev to enumerate input devices and [[GPU]]s , and to receive notifications when new ones appear or old ones are unplugged.