# siteSurvey

M5Atom Behavior
Startup (boot):
LED blinks blue
Turns solid blue when:
WiFi connected
External IP received
GPS fix + HDOP < 2.5
Logging (normal operation):
Sends GPS positions at 1Hz over UDP (keep blue LED)
Button press:
LED blinks green
Sends siteSurvey:newfile
Waits for backend ACK:
If received in ≤ 3 seconds → solid green
If not received → solid red
After failure (red), revert to ready state (blue)
