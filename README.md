# batticonplus
Lightweight battery status icon for the system tray and notifier (based on cbatticon)

Originally based on code from xbattbar-acpi.

Note: The percentage for the battery's 'Maximum Capacity' in the systray icon\
tooltip is the comparison of its current maximum charge capacity and its design.\
On some systems the maximum and minimum charge can be limited by bios\
settings in which case e.g. the displayed maximum capacity can be 80% or lower.

`Make options:`\
`  WITH_GTK3=1 to build against gtk3, it is the default option`\
`  WITH_GTK3=0 to build against gtk2 (version 2.16)`

`  WITH_NOTIFY=1 to build with libnotify support, it is the default option`\
`  WITH_NOTIFY=0 to build without libnotify support`

`  WITH_APPINDICATOR=1 to build with ayatana-appindicator support`\
`  WITH_APPINDICATOR=0 to build without ayatana-appindicator support, it is the default option`

`Usage:`\
`  batticonplus [OPTION...] [BATTERY ID]`

`Help Options:`\
`  -h, --help                       Show help options`

`Application Options:`\
`  -v, --version                    Display the version`\
`  -d, --debug                      Display debug information`\
`  -u, --update-interval            Set update interval (in seconds)`\
`  -i, --icon-type                  Set icon type ('standard', 'notification' or 'symbolic')`\
`  -l, --low-level                  Set low battery level (in percent)`\
`  -r, --critical-level             Set critical battery level (in percent)`\
`  -o, --command-low-level          Command to execute when low battery level is reached`\
`  -c, --command-critical-level     Command to execute when critical battery level is reached`\
`  -x, --command-left-click         Command to execute when left clicking on tray icon`\
`  -n, --hide-notification          Hide the notification popups`\
`  -t, --list-icon-types            List available icon types`\
`  -p, --list-power-supplies        List available power supplies (battery and AC)`\
`  -s, --disable-startup-notify     Suppress the startup notification`\
`  -w  --charge-reached-notify      Warn when charging and level reached 80%`

`Default value for options:`\
`  update interval        : 5 seconds`\
`  icon type              : the first one that is available in this sequence:`\
`                           standard, notification or symbolic`\
`                           (check your setup with --list-icon-types)`\
`  low level              : 20 percent`\
`  critical level         : 5 percent`\
`  command low level      : none`\
`  command critical level : none`\
`  command left click     : none`\
`  battery id             : BAT0, if present`\
`                           (check available power sources with --list-power-supplies)`

`Tray icon click actions:`\
`  middle : Exit batticonplus`\
`  right  : Show batticonplus version`

`Examples:`\
`  batticonplus`\
`  batticonplus -t`\
`  batticonplus -p`\
`  batticonplus -u 20 -i notification -c "poweroff" -l 15 -r 3`\
`  batticonplus -u 20 -i notification -r 3 -c "poweroff" -l 15 -o "xbacklight = 5"`

Thanks to:
  - Bing Liu for adding icon theme and notification support
  - Zariep for adding Ayatana AppIndicator support
  - Drew Abbott for the option to disable charge notification on startup

--

 Carlo den Otter

