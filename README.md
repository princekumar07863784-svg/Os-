# iOS 27 Launcher (Android)

An original, iOS 27 / iPhone 18 Pro-inspired Android launcher built with Jetpack Compose.
**100% offline - no ads, no trackers, no analytics, no INTERNET permission.**

## iOS 27 / iPhone 18 Pro features included
| Feature | File |
|---|---|
| Lock screen: big clock, date, Now Playing, swipe up to unlock | `LockScreen.kt` |
| Compact Dynamic Island (iPhone 18 Pro style): clock, battery + charging, live Now Playing; tap to expand, play/pause | `DynamicIsland.kt`, `Media.kt` |
| Liquid Glass clarity/tint slider, from Ultraclear to Tinted (Settings) | `SettingsScreen.kt` |
| Extra-large home widgets: Clock XL + Calendar with real upcoming events | `Widgets.kt` |
| Swipe-down Control Center: flashlight, Wi-Fi panel, Bluetooth panel, separate media & alarm volumes (iOS 27 separate alarm volume) | `ControlCenter.kt` |
| Swipe-away Now Playing mini player above the dock | `MainActivity.kt` |
| Swipe-right App Library with search | `MainActivity.kt` |
| Siri-style on-device assistant: open <app>, time, battery, torch, call - fully offline | `AssistantScreen.kt` |
| Camera app: live preview, zoom slider, photographic styles, simulated Pro aperture dial (f/1.4-f/16 like iPhone 18 Pro), saves to Pictures/iOSLauncher | `CameraScreen.kt` (CameraX) |
| iOS-style Phone: keypad + real Recents (missed calls in red) | `DialerScreen.kt` |
| iOS-style Photos: 3-column grid + full-screen viewer | `GalleryScreen.kt` |

## Gestures
- Swipe up on lock screen -> home
- Swipe right on home -> App Library
- Swipe down on home -> Control Center
- Drag mini player down -> dismiss Now Playing
- Back button -> return home from built-in apps

## Honest notes
- The assistant is a **local command parser**, not a cloud model - the app has no internet.
- The aperture dial is a visual simulation of the iPhone 18 Pro variable-aperture control.
- Now Playing needs Android "notification access" enabled once (shortcut in Settings).
- The Dynamic Island is an in-app overlay, not a system cutout.

## Permissions (runtime, each optional)
READ_CALL_LOG / CALL_PHONE / READ_PHONE_STATE - Phone
READ_MEDIA_IMAGES (or READ_EXTERNAL_STORAGE) - Photos
WRITE_EXTERNAL_STORAGE (Android 9-) - saving camera photos
CAMERA - camera preview & flashlight
READ_CALENDAR - calendar widget

## Build & run
1. Android Studio (Hedgehog+) -> open -> Gradle sync -> run on Android 8.0+.
2. Set as default launcher when prompted.
3. Enable notification access via the Settings shortcut for Now Playing.

## Ideas for next versions
- Third-party widgets via AppWidgetHost
- Photo albums by month, share/delete
- Icon packs / themes, app folders, notification badges
