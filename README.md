# Background
I wanted to use the USB over IP functionality to improve my old printer which has no WiFi support (and unfortunately no linux drivers for ARM chips). Everything works great and I can use the printer even with multiple devices. 
The only downside is having to detach the USB device after every usage so other computers can attach it.

# Auto-detach
This fork will auto-detach (unbind and rebind the port) when a new client wants to connect while another client is still connected. Even though the other client loses its connection, this is totally acceptable for me because at 
least I don't have to go to another computer anymore to "attach" my printer.\
For the printer scenario this means everytime I want to print something, I force-attach my printer (detaching other clients) and after that just leaving it attached because other computers can force-detach mine when they wanna print something.

# Reference
The original code is available here:
https://github.com/torvalds/linux/tree/master/tools/usb/usbip
