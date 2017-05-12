NUC stuff

### install process


- update BIOS; download .BIO-file from Intel and install it via usb.
- install wpa_supplicant; get the .deb-files in this repo and install via dpkg -i
- run lshw -C network to view the name of wifi-card
- edit /etc/network/interfaces and add name of card; something like auto wlps20, iface wlps20 manual and wpa_conf /etc/wpa_supplicant/wpa_supplicant.conf
- add file /etc/wpa_supplicant/wpa_supplicant.conf /w content like the one in this repo
- restart networking sudo service networking restart
- get ip; sudo dhclient wlps20
