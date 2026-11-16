# GR4Y-dev AirPodsDesktop fork

Based on AirPodsWindows commit `b7dd2cbf9811c68af4207d1d68b7088d62529c12`, preserving
its history and the original SpriteOvO/AirPodsDesktop history. Original copyrights
and GPL-3.0-or-later licensing are retained. The executable retains the inherited
name `AirPodsWindows.exe`.

## Listening modes

For Pro 3, right-click the tray icon and open Noise Control for Off, Noise
Cancellation, Transparency, and Adaptive. Adaptive is hidden on unsupported older
models. Controls require a connected AAP channel; a battery advertisement alone
does not enable them. The checkmark reflects the last mode reported by the earbuds,
not merely a successful write. Opening the menu refreshes it; an open submenu
refreshes every 500 ms. Device loss clears the selection. Failed writes show a
notification.

## Driver and verification

The inherited transport uses the third-party MagicAAP driver, which is not bundled
or installed by this repository. Review its current official documentation:
https://magicpods.app/magicaap/. Windows/firmware compatibility on this PC has not
been verified. No Windows security settings have been changed.

No Visual Studio C++/Qt build environment was detected locally. GitHub's Windows
workflow builds RelWithDebInfo and runs the tests, including the menu regression
test. A passing build does not establish hardware compatibility.

Before releasing, test with real Pro 3 hardware:

1. Without the driver, battery display works but mode actions remain disabled.
2. With the driver connected, switch all available modes and verify audible
   behavior and the device-reported checkmark.
3. Change modes on the stem; reopen the menu and verify the selection updates.
4. Disconnect/reconnect and put both earbuds in the case; verify no stale selection
   or hang remains.
5. If Off is disabled in Apple-device settings, verify the app does not claim Off
   was applied merely because a write succeeded.

Updater defaults target GR4Y-dev/AirPodsDesktop. CI supplies its repository owner
and name dynamically. Pushing a development branch is not a validated release.
