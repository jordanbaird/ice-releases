# Ice 0.11.11

## Bug Fixes
* Fixed an issue where Ice would crash on launch for some users.
* Fixed a bug preventing the menu bar search panel from appearing in full screen.

# Ice 0.11.10

## What's New
* Menu bar search updates.
* Added the ability to set different menu bar appearances for light and dark mode.

## Bug Fixes
* Fixed a rare case of menu bar items failing to move.

## Other Changes
* Improved menu bar item caching.
* Lots of under-the-hood changes and improvements.

# Ice 0.11.9

## What's New
* Added a setting to show all sections when dragging items.

## Bug Fixes
* Fixed some minor behavior glitches with Smart rehide on Sequoia.
* Application menus now correctly hide when showing the always-hidden section.
* Fixed a bug where Ice's app icon would remain in the Dock and app switcher after unhiding application menus.
* The update interface should no longer appear behind other apps when checking for updates from Ice's menu.

## Other Changes
* Reworked menu bar item retrieval and caching for better reliability.

# Ice 0.11.8.1

This is a hot fix release that reverts menu bar shape rendering on screens without a notch.

# Ice 0.11.8

## What's New
* Minor interface changes.
* Adjusted rendering of menu bar shapes.
* Ice now dynamically adjusts its sidebar item sizes to better respect system settings.

## Bug Fixes
* Fixed rare cases of unexpected mouse movement when rehiding temporarily shown items.
* Fixed an issue where long application menus would interfere with temporarily showing items.

# Ice 0.11.7

## What's New
* System notifications for updates.

## Bug Fixes
* Fixed issues with granting permissions.
* Fixed an issue where the app would fail to initialize after launching.
* Fixed an issue preventing the settings window from opening after launching at login.

## Other Changes
* Visual adjustments and performance improvements.

# Ice 0.11.6

## What's New
* Added a hotkey to enable/disable the Ice Bar.
* When Command+dragging items in the menu bar, all sections are now shown when the Ice Bar is enabled.

## Bug Fixes
* Fixed an issue with menu bar item image caching.

## Other Changes
* Various minor code improvements.

# Ice 0.11.5

## Bug Fixes
* Fixed an issue where items couldn't be dragged to empty menu bar sections.

# Ice 0.11.4

## What's New
* The "Default" Ice Bar location has been renamed to "Dynamic".
* Lots of under the hood improvements.

## Bug Fixes
* Fixed an issue where the app would fail to properly launch.

# Ice 0.11.3

## What's New
* The "always hidden" section is now disabled by default for new users.

## Bug Fixes
* Fixed screen capture permissions issue on macOS 15 Sequoia.
* Fixed an issue where the Ice Bar wasn't being sized properly.
* Menu bar search panel now always appears on the correct screen, regardless of the method used to show it.

## Other Changes
* Code cleanup.

# Ice 0.11.2

## What's New
* Bug fixes and UI adjustments.
* Ice's menu bar items now treat Control+clicks as right clicks.

# Ice 0.11.1

## What's New
* Minor UI fixes.

# Ice 0.11.0

## What's New
* Brand new UI implementation.
* Search menu bar items using a custom hotkey.
* Adjust the spacing between menu bar items.
* Customize the time it takes to rehide temporarily shown menu bar items.

## Bug Fixes
* When temporarily showing menu bar items, Ice no longer moves them if they are already shown.
* Fixed a timeout that can occur when moving menu bar items while running certain apps that modify system events.
* Improved compatibility with macOS 15.

## Known Issues
* Applying menu bar item spacing can occasionally fail. This can be resolved by logging out.
* Ice's menu bar item does not respect spacing changes. This can be resolved by restarting Ice.

# Ice 0.10.5

## What's New
* Accessibility support for Ice Bar.
* Partial accessibility support for menu bar item layout (work in progress).
* Various UI updates.

## Bug Fixes
* Fixed the occurrence of false positives in menu bar item responsiveness check.
* Temporarily shown menu bar items are now remembered if their app is restarted.
* Fixed potential undefined behavior when toggling between sections in Ice Bar.
* Fixed an issue that could cause the hidden section to toggle when clicking the Apple menu.

## Other Changes
* Restored the ability to choose the location of the Ice Bar.

# Ice 0.10.4

## What's New
* Added the ability to set a custom delay for the "show on hover" feature.
* Improved the wording of settings and descriptions throughout the app.

## Bug Fixes
* Fixed a regression that caused application menus to sometimes fail to hide.
* Fixed vertical offset of menu bar items in settings when showing scroll bars.
* The notch is now taken into account when temporarily showing menu bar items.
* Ice now ignores interactions with the notch. This improves compatibility with apps that utilize notch space.
* Improved menu bar appearance reliability for apps that dynamically update their application menus.

## Other Changes
* To keep the available options simple, the ability to set the location of the Ice Bar has been removed.

# Ice 0.10.3

## What's New
* Items shown by the Ice Bar are no longer immediately rehidden when the Ice Bar is opened again. This allows multiple items to be shown at once.
* Ice's menu bar items now use a variable length instead of fixed.
* Simplified options in settings for a more streamlined experience.

## Bug Fixes
* More robust rehiding for items shown by Ice Bar.
* Improved consistency of the "Focused app" rehide strategy when clicking on inactive displays.
* Work around clipped menu items when using the "Split" appearance on multi-display setups.
* Extended delay in event tap callback to help prevent occasional item movement timeouts.

# Ice 0.10.2

## What's New
* Improved the logic for retrieving menu bar items.
* Menu bar item images no longer update if the app isn't focused, leading to increased efficiency and the purple screen capture icon appearing less often.

## Bug Fixes
* Fixed a crash that would occur when the Ice Bar was longer than the width of the screen.
* Fixed a visual glitch where menu bar items wouldn't initially show in the "Menu Bar Items" settings.
* Fixed faulty menu bar item image caching.
* Fixed a bug that caused the visible section's arranging interface to disappear in "Menu Bar Items" settings when the Ice icon was disabled.
* Adjusted the menu bar split appearance shape to have even padding on both sides when using the inset appearance on screens with a notch.

# Ice 0.10.1

This is a hot fix release for a bug that was introduced in 0.10.0 that could prevent one or more sections from hiding.

# Ice 0.10.0

## What's New
* Menu bar items can now be shown in a secondary bar below the menu bar! (look for "Use Ice Bar" in the "General" settings pane).
* Added ability to move menu bar items individually in a new "Menu Bar Items" settings pane.
* Menu bar appearance can now be inset on screens with a notch.
* Ice now ensures that the always-hidden section stays to the left of the hidden section.
* Added the ability to disable the always-hidden section.
* Ice now launches in the background by default.
* Ice now uses the GPL-3.0 license.

## Bug Fixes
* The menu bar appearance overlay should now work with fullscreen in apps that don't use the default macOS fullscreen interface, such as VLC and Keynote.
* Reliably check for default macOS fullscreen spaces.
* Fixed mouse location checks in fullscreen and when using multiple displays.
* The menu bar appearance now renders at the correct size across multiple displays with different sized menu bars (i.e. when one display has a notch and the other does not).
* Fixed screen flicker when playing DRM media.
* Improved reliability of application menu hiding.
* Fixed excessive CPU usage by menu bar overlay panel when switching apps.

# Ice 0.9.0

## What's New
* Slight UI redesign.

## Bug Fixes
* Fixed menu bar items not hiding on secondary screens when the "show section dividers" feature is disabled.
* Fixed menu bar appearance not applying across multiple displays.
* Menu bar appearance now updates more reliably when the focused application changes.
* Fixed mouse cursor detection not working across multiple displays. Features like "show on hover" and "show on click" should now behave correctly on external displays.
* Fixed an occasional bug where hotkeys weren't deleting.

## Other Changes
* Optimizations.
* Menu bar appearance only updates the components that need it.
* Slight menu bar appearance design refresh.
* You can now change the opacity of the menu bar border.

# Ice 0.8.0

## What's New
* Hotkeys have been reimplemented to support new actions.
* UI improvements.
* Performance optimizations.

## Bug Fixes
* Fixed some rare issues with custom menu bar appearances.

> [!NOTE]
> This version introduces changes that are incompatible with previous versions. If you wish to downgrade to a previous version, some of your settings will be lost.

# Ice 0.7.1

## What's New
* Minor efficiency improvements.
* UI tweaks.
* Code cleanup.
* Internal reorganization.

## Bug Fixes
* Fixed a bug that prevented Ice from seeing all menu bar items. This was affecting the "hide application menus" feature and the "menu bar appearance" features.

# Ice 0.7.0

## What's New
* The "always hidden" section is now always enabled.
* The divider icons between sections can now be hidden.
* The Ice icon can now be hidden. To show Ice's settings, right-click on an empty space in the menu bar.
* Scroll or two finger swipe in the menu bar to toggle hidden items.
* Perform a secondary action by clicking one of Ice's menu bar items with a modifier key.

> [!NOTE]
> Currently, only one action is available, which toggles the "always hidden" section. More actions are on the way!

## Bug Fixes
* Fixed occasional visual glitching when adjusting the menu bar appearance.
* Ice now hides application menus more reliably when showing menu bar items.

# Ice 0.6.3

## What's New
* Minor user experience improvements.

## Bug Fixes
* Fixed menu bar appearance not updating in certain cases.

# Ice 0.6.2

## What's New
* When show-on-click is enabled, you can now click inside an empty area of the menu bar while the "Hidden" section is visible to show the "Always hidden" section as well.

## Bug Fixes
* Fixed a visual glitch that would appear when using the split menu bar while the "Always hidden" section was disabled.
* Fixed a bug that was causing the app to quit immediately after launch on some machines.
* The "HideApplicationMenus" setting is now properly retained after quitting the app.

# Ice 0.6.1

## Bug Fixes
* DRM media no longer flickers when Ice is open.
* Fixed a visual glitch that caused split menu bar shapes to sometimes disappear.

## Other Changes
* Minor UI tweaks.

# Ice 0.6.0

## New Features
* Support for Homebrew.
* Auto-rehide now has 3 different modes:
  * Smart – rehides items using a smart algorithm.
  * Timed – rehides items after a fixed amount of time.
  * Focused app – rehides items when the focused app changes.
* Click an empty space in the menu bar to show hidden items.
* Hide the left application menus when showing hidden items.
* Command-dragging in the menu bar now shows all sections.

# Ice 0.5.0

## New Features
* You can now right-click an empty space in the menu bar to edit its appearance.

## Bug Fixes
* Menu bar appearance customizations should now appear across multiple screens.
* Auto show/hide now only applies when the mouse is on the focused screen.

# Ice 0.4.3

This release fixes some bugs with custom menu bar appearances.

# Ice 0.4.2

This release fixes a few minor bugs.

# Ice 0.4.1

This release includes various improvements and minor bug fixes.

# Ice 0.4.0

This release adds the ability to automatically rehide menu bar items with a click outside the menu bar.

There are also a number of bug fixes and performance improvements.

# Ice 0.3.1

This release includes lots of minor fixes to improve the overall user experience.

# Ice 0.3.0

This release adds the ability to automatically check for updates directly within the app. Recommended for all users.

# Ice 0.2.7

This is a minor release. Next release will include some big improvements!

# Ice 0.2.6

This release includes minor improvements and code cleanup.

# Ice 0.2.5

This release includes minor UI updates.

# Ice 0.2.4

This release includes bug fixes and performance improvements.

# Ice 0.2.3

This release improves the permissions interface for a better onboarding experience.

# Ice 0.2.2

This release fixes an issue that causes excessive memory usage when the screen is locked or the screen saver is active.

# Ice 0.2.1

Fixed a small visual bug.

# Ice 0.2.0

This release adds the ability to customize the shape of your menu bar. Choose between full-length or split, with options for rounded or squared ends.

# Ice 0.0.3

This release includes minor UI improvements and bug fixes.

# Ice 0.0.2

This release adds the ability to show hidden items when the mouse is inside the menu bar.

> [!Note]
> As part of the implementation of this feature, Ice uses the Accessibility API, and can no longer be sandboxed. From a practical standpoint, all this means is that Ice can no longer be distributed on the official Apple App Store (it wasn't anyway).

# Ice 0.0.1

Initial release of Ice.
