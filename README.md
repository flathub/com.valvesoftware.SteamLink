Steam Link client for desktop Linux
===================================

This repository contains metadata to build a standalone Steam Link client
for desktop Linux. It connects to the full Steam application running
on Windows or Linux on the same LAN, sends input events (controller,
keyboard, mouse) to Steam and games running under it, and receives video
frames from Steam and games.

Support
-------
Official support for the Steam Link client is on Steam's community forums at
https://steamcommunity.com/app/353380/discussions/10/.
Please use this forum for any feature requests or issues with the Steam Link client.

The issue tracker in this repository is limited to issues with the Flatpak
packaging of the client and integration with Flathub's runtime.

Known issues
------------

The [steam-devices udev rules](https://github.com/ValveSoftware/steam-devices/)
will be required for full functionality of some USB HID and Bluetooth HID
game controllers. These cannot be shipped as part of a Flatpak app, and
need to be installed on the host system.

If the full Steam client that is being remote-controlled is also
running on Linux, for best results it should be running under X11
(Xorg). "Rootless" Xwayland displays in a Wayland session, such as
GNOME in Wayland mode, will only partially work. However, running this
Steam Link client in Xwayland shouldn't be a problem.
