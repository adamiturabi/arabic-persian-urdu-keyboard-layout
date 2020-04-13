# arabic-persian-urdu-keyboard-layout
How to add a keyboard layout on Linux that supports Arabic, Persian, and Urdu.

## Description

Take a look at `src/my_ara` to check out the layout. 

+ `SHIFT` is the level-1 modifier

+ `AltGr` is the level-2 modifier (for adding dagger-alef, urdu/Persian characters, etc.)

+ `SHIFT+AltGr` is the level-3 modifier (for adding diacritical hamza, diacritical, maddah, etc.)

## Procedure

1. sudo edit /usr/share/X11/xkb/symbols/ara
   1. Copy-paste keyboard layout from `src/my_ara` to end of file.
2. sudo edit /usr/share/X11/xkb/symbols/nbsp
   1. Copy-paste "no-break-space" description from `src/my_nbsp` to end of file.
3. sudo edit /usr/share/X11/xkb/rules/evdev.xml
   1. Copy-paste the "variant" from `src/my_evdev.xml` and add as additional variant to "ara" layout after "azerty", "qwerty", "buckwalter", etc.
4. `CTRL-ALT-BACKSPACE` to restart X or log-out and log back in.
5. Find Keyboard layout settings in Desktop settings/configuration.
   1. Add "Arabic-Persian-Urdu (Custom)" from "Arabic" selection
6. Pick suitable key to switch layouts. I choose `CAPS LOCK`.

