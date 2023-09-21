---
title: Surface (Wayland)
excerpt: surface_wayland
---
A surface is a box of pixels that can be displayed on-screen. It's one of the primitives we build things like application windows out of.

## Requests

A request that surface sends of is "Damage", it is used to indicate if the surface needs to be redrawn.

```
0000000A    Object ID (10)
00180002    Message length (24) and request opcode (2)
00000000    X coordinate (int): 0
00000000    Y coordinate (int): 0
00000100    Width        (int): 256
00000100    Height       (int): 256
```

This is a snippet of a session — the surface was allocated earlier and assigned an ID of 10. When the server receives this message, it looks up the object with ID 10 and finds that it's a `wl_surface` instance. Knowing this, it looks up the signature for the request with opcode 2. It then knows to expect four integers as the arguments, and it can decode the message and dispatch it for processing internally.

## Events

The server can also send messages back to the client — events. One event that the server can send regarding a `wl_surface` is "enter", which it sends when that surface is being displayed on a specific output (the client might respond to this, for example, by adjusting its scale factor for a HiDPI display). Here's an example of such a message:

```
0000000A    Object ID (10)
000C0000    Message length (12) and event opcode (0)
00000005    Output (object ID): 5
```

This message references another object, by its ID: the `wl_output` object which the surface is being shown on. The client receives this and dances to a similar tune as the server did. It looks up object 10, associates it with the `wl_surface` interface, and looks up the signature of the event corresponding to opcode 0. It decodes the rest of the message accordingly, looking up the `wl_output` with ID 5 as well, then dispatches it for processing internally.

## Interfaces

A list of requests and events, and their respective opcodes and signatures.