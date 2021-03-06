# Cheatsheet for PHPStorm Ideolog Symfony logs format

## Requirements

 * PHPStorm
 * Installed and running **Ideolog** plugin
 
# Setting up
 1. Go to *Settings -> Editor -> Log highlighting (Ideolog)*.
 2. Add new *Log format* (plus sign on the right of the top list).
 3. Put a name *Symfony* or whatever suits You.
 4. Pick one of log formats that matches your case. There is no issue to add multiple log formats to the Ideolog, just repeat all steps with different log format.
   * If your log format is like this: `[2020-03-10 12:00:00] kernel.DEBUG:`, then in the field *Message pattern* put this regex: `^\[(\d{4}-\d{2}-\d{2}\s+\d{2}:\d{2}:\d{2})]\s+([^.]+)\.([^:]+):\s+(.*)$`.
   * If your log format is like this: `[2020-03-05T12:57:24.827849+00:00] console.DEBUG:`, then in the field *Message pattern* put this regex: `^\[\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{6}\+\d{2}:\d{2}\]\s+([^.]+)\.([^:]+):\s+(.*)$`.
 5. In the field *Message start pattern* put this regex: `^\[`.
 6. In the field *Time format* put this pattern: `yyyy-MM-dd HH:mm:ss`.
 7. In the field *Time capture group* set number **1**.
 8. In the field *Severity capture group* set number **3**.
 9. In the field *Category capture group* set number **2**.
 10. Push *OK* button. You're almost done!
 
# Tweaks
 
## Critical severity
To make *CRITICAL* severity to highlight do following steps:
 1. Go to *Settings -> Editor -> Log highlighting (Ideolog)*.
 2. Add new *Pattern* (plus sign on the right of the bottom-left list).
 3. Enter new pattern: `^\s*c(ritical)?\s*$`
 4. Select newly created pattern on the list and click *Edit* icon on the right.
 5. Check *Foreground*, click on the color field.
 6. In new dialog window, at the top right corner type red color in hex `#FF0000` and push *Enter* key.
 7. Click *OK* button, close settings and You're done!
