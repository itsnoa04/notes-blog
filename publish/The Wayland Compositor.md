---
title: The Wayland Compositor
excerpt: 
tags:
---
- dispatches events to the appropriate wayland client
- process of bringing together application windows ( [[The Wayland Client]] ) for display on an [[output]] is called [[compositing]]. 
- uses both [[GBM]] and [[OpenGL]] via [[Mesa]]
- Requires special permission to use the [[evdev]] files, forcing [[The Wayland Client |wayland clients]] to go through the compositor to receive input events. hence preventing key logging.