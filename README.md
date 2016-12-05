#Fresh install
1. sudo apt-get install make gcc git software-properties-common curl vim
2. git clone https://bitbucket.org/sanrath/mediatek_mt7610u_sta_driver_linux-64bit 
3. cd mediatek_mt_7610u_sta_driver_linux-64bit
4. make
5. ifconfig
6. ifconfig -a #should show the USB wireless interface
7. sudo ip link set <interface> up
8. ifconfig #should now show the interface
9. Edit /etc/network/interfaces and add the below

auto <interface>
iface <interface> inet dhcp
netmask 255.255.255.0
gateway 192.168.1.1
wpa-ssid <Wifi name>
wpa-psk <Wifi password>
dns-nameservers 8.8.8.8 4.4.4.4

10. sudo ifdown <interface> && sudo ifup <interface> #Restart the interface for the settings to take place
11. git clone https://github.com/creationix/nvm
cd nvm
./install.sh
logout
nvm install <node-version>
nvm alias default v4.2.1
npm install -g npm
12. git clone https://sahilnarain@github.com/sahilnarain/vim-setup
cd vim-setup
./setup.sh
14. Install gnome desktop
sudo apt-get install gdm ubuntu-gnome-desktop --no-install-recommends
15. Install communication clients - Thunderbird (Email), Pidgin (IRC) and LiFeRea (RSS)
sudo apt-get install thunderbird pidgin liferea
16. Enable desktop shortcuts via dconf-editor
org > gnome > desktop > background --> Enable desktop icons
<Optional> - Make <application>.desktop and write the config. Mark the shortcut as executable
17. Launch the tweak tool and enable minimize and maximize window buttons.
18. Install maximus - it gets rid of weird titlebars. 
sudo apt-get install maximus
Log out log in again.
