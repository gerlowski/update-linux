<div align="center">

# <img src="http://icons.iconarchive.com/icons/alecive/flatwoken/512/Apps-Terminal-Pc-104-icon.png"  height="50px" width="50px">update-linux<img src="http://icons.iconarchive.com/icons/alecive/flatwoken/512/Apps-Terminal-Pc-104-icon.png"  height="50px" width="50px" >
### (Bash Script Update Linux)
#### An easier way to update the linux distribution

</div>

# Notes
This gets you the latest bleeding edge kernel/firmware. There is always the possibility of regressions.

# Installing
```
sudo curl -L --output /usr/bin/update-linux https://raw.githubusercontent.com/gerlowski/update-linux/master/update-linux && sudo chmod +x /usr/bin/update-linux
```
# Usage
```
update-linux
```

You can check log output by typing:
```
cat /var/log/update-linux/update.log
```

# To-do list
- [x] **Check internet connection**
- [x] **Create log file**
- [ ] **Automatic script update at runtime**

# Contributing

Please fork this repository and contribute back using
[pull requests](https://github.com/Gerlowski/update-linux/pulls).

Any contributions, large or small, major features, bug fixes, are welcomed and appreciated
but will be thoroughly reviewed.

# Troubleshooting
There are two possible problems related to SSL certificates that may prevent this tool from working.
- The time may be set incorrectly on your linux, which you can fix by setting the time using NTP.
```
sudo apt-get install ntpdate
sudo ntpdate -u ntp.ubuntu.com
```

- The other possible issue is that you might not have the ```ca-certificates``` package installed, and so GitHub's SSL certificate isn't trusted. If you are on Debian, you can resolve this by typing:
```
sudo apt-get install ca-certificates
```

# License
Copyright (c) 2019 Bartosz Gerłowski

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
