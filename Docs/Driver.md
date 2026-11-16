# MagicAAP driver

Noise-control commands require a compatible Apple Accessory Protocol transport.
This fork inherits the MagicAAP integration from AirPodsWindows; it does not bundle
or install the driver. Battery advertisements do not establish a control connection.

Consult the [official driver documentation](https://magicpods.app/magicaap/) for
current compatibility and installation requirements. Driver signing requirements
vary by Windows version. We have not verified this driver on the user's PC and do
not provide a one-click installer or instructions to disable Windows protections.

Settings distinguishes an absent driver, an installed but disconnected driver,
and an active control connection. Pair the AirPods through Windows Bluetooth,
select them in the app, and inspect that status if Noise Control remains disabled.
See [the hardware checklist](Fork.md).

Credits: [MagicPods](https://magicpods.app/),
[AirPodsWindows](https://github.com/YimingZhanshen/AirPodsWindows), and
[AirPodsDesktop](https://github.com/SpriteOvO/AirPodsDesktop).
