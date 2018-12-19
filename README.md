# HarmonyApi
Python class for the Logitech Harmony remote. Using WebSockets instead of disabled API. (TESTING)

Based on the information found on:
https://github.com/jlynch630/Harmony.NET and https://github.com/chadcb/harmonyhub

Usage examples:
harmony = harmonysock('192.168.19.223') #connects and gets initial info
allactivitiedata = harmony.listactivities()
alldevicedata = harmony.listdevices()
print('TV =', harmony.getactivitybyname('TV Kijken'))
current = harmony.getstate() # get all current state info
print('now on =', harmony.currentactivity()) #prints the current activity
harmony.sendkey('31764193','PowerToggle') #press PowerToggle button for device whith ID ...
harmony.startactivity('Smart-tv kijken') # start an activity by name/label
harmony.startactivity('28513235') # start an activity by id (automaticaly detected if the string contains only a number)
