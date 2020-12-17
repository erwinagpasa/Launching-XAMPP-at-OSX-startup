# Launching-XAMPP-at-OSX-startup

Fire up Terminal, and run the following command:

**BASH**

cd /Library/LaunchDaemons

sudo nano xampp.startapache.plist

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
 <dict>
  <key>Label</key>
    <string>org.xampp.server</string>
  <key>ProgramArguments</key>
    <array>
      <string>/Applications/XAMPP/xamppfiles/xampp</string>
      <string>startapache</string>
  </array>
  <key>RunAtLoad</key>
    <true/>
  <key>AbandonProcessGroup</key>
    <true/>
  </dict>
</plist>
```

Save the file and exit nano (control+o, return, control+x).

Now run the following terminal command:
