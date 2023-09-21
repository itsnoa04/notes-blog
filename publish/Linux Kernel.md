---
title: What is Linux Kernel
excerpt: linux_kernel
---
- the system [[Kernel]] for the [[linux]] operating system
- Only component allowed to talk to hardware
- Provides an abstraction layer over hardware so it can be safely accessed by [[Userspace]] - where display compositors like the [[The Wayland Compositor]] runs.
- For graphics this abstraction layer is called the [[DRM]] or [[DRM |Direct Rendering Manager]]
	- ![[DRM]]
- has a [[KMS]] or [[KMS |Kernel Mode Setting]] 
	- ![[KMS]]