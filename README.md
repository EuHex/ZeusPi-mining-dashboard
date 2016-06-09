# ZeusPi-mining-dashboard
Mining dashboard for RaspberryPi with bfgminer fork</a> for scrypt ZeusMiners.

<h2>How to use it?</h2>

First of all, you should download and install new clean version of Raspbian OS to SD card. All information and images can be found on <a href="https://www.raspberrypi.org/downloads/raspbian/">official site<a/>. After that, you should install <a href="https://github.com/Darkwinde/bfgminer">bfgminer scrypt fork by Darkwinde</a> and all required dependencies. This <a href="http://blog.rastating.com/mining-dogecoin-with-a-zeusminer-blizzard-and-a-raspberry-pi/">setup guide</a> might be very useful for beginners. You should install it to /home/pi/bfgminer. 

Then, copy this files to /home/pi/zeusPi/ directory of your RaspberryPi file system or clone it with git. Your're practically done. You can run dashboard server manually with <code>sudo node daemon.js</code> command in ZeusPi directory. Dashboard will be accessable from your browser, just enter your device IP. 

Test, look around, if everything works fine, you may wish ZeusPi daemon to start automatically on reboot. Use <code>crontab -e</code> command to edit cron tasks and add there <code>@reboot</code> command with path to node and daemon.js. Or you can edit /etc/rc.local file and add autorun command there. In any case, node should be started with superuser privileges, otherwise it would fail to work. 

In this dashboard you can find such useful functions as pool list editor, miner restart panel, mining stats, hardware settings and some other helpers. This is alpha version, you're welcome to experiment, modify, fork, send issues and pull requests.