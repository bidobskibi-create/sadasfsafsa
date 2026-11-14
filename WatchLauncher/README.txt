WatchLauncher v5 - honeycomb launcher for a small round Android watch (Android 8.1, API 27)

LAUNCHER
  round icons on a hex grid with a fisheye lens, ambient glow, glossy icons, springy snap,
  pop-in intro, haptic ticks, swell-to-launch animation.
  Tap = launch. Back / Home = glide back to the centre.

LONG-PRESS MENU
  Long-press an app icon and a box pops up next to it with four options:
  - App info : Android's app info screen
  - Delete   : uninstall (system apps can't be removed, you get a message instead)
  - Hide     : removes it from the grid. Bring hidden apps back with
               Look & Feel > "Show N hidden apps"
  - Folder   : puts the app in a folder. The first time it makes "Folder 1"; after that you
               choose an existing folder or "+ New".
  Tap a folder to open it (use the Back icon, Back button or Home to leave).
  Long-press an app inside a folder for "Take out"; long-press a folder icon for Open / Ungroup.
  Tap outside the box (or press Back) to close it.

SETTINGS ("Look & Feel")
  Open it from the gear icon at the end of the grid, or long-press empty space.
  (It is also a normal app called "Launcher Settings" in other launchers.)
  - Theme:       Classic, Ocean, Sunset, Neon, Candy, Mono
  - Bounciness:  0 (no overshoot) ... 100 (very springy); release the slider to see a demo
  - Background:  Black, Midnight, Aurora, Graphite, Ember, Violet
  Changes save instantly and apply when you go back to the launcher (icons pop in again).
  "Reset to defaults" restores everything.

ADD YOUR OWN
  Styles.java: add a line to THEMES or BGS and it shows up in the settings automatically.
  Defaults at the top of HoneycombView.java: K (fisheye), FILL, SPACING, EDGE_DIM, GLOW_ALPHA.

BUILD
1. Android Studio: File > Open > this folder. Let Gradle sync (accept the plugin upgrade prompt if shown).
2. Build > Build APK(s). Output: app/build/outputs/apk/debug/app-debug.apk

INSTALL
  adb install -r app-debug.apk
(Updating over the old version keeps it as your default launcher.)

IF SOMETHING GOES WRONG
  adb uninstall com.example.watchlauncher
puts the stock launcher back.
