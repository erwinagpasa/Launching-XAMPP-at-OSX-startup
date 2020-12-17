# Launching-XAMPP-at-OSX-startup

Fire up Terminal, and run the following command:

**BASH**

cd /Library/LaunchDaemons

```
sudo nano xampp.startapache.plist
```

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

```
sudo nano apachefriends.xampp.mysql.start.plist
```

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
  <dict>
    <key>EnableTransactions</key>
    <true/>

    <key>Label</key>
    <string>apachefriends.xampp.mysql.start</string>

    <key>ProgramArguments</key>
    <array>
      <string>/Applications/XAMPP/xamppfiles/xampp</string>
      <string>startmysql</string>
    </array>

    <key>RunAtLoad</key>
    <true/>

    <key>WorkingDirectory</key>
    <string>/Applications/XAMPP/xamppfiles</string>

    <key>KeepAlive</key>
    <false/>

    <key>AbandonProcessGroup</key>
    <true/>
  </dict>
</plist>
```


When you restart your computer the XAMPP Apache and MySQL services should start automatically. You can check this by launching XAMPP Control and checking that Apache and MySQL have green lights displayed next to them.
