# Networks

## Random commands
### Reactivate network card
```
sudo ifconfig wlan0 down
sudo ifconfig wlan0 up
```
sudo ifconfig eth0 down
sudo ifconfig eth0 up
### Dhcp server
```
sudo service isc-dhcp-server restart | stop | start | status
sudo service isc-dhcp-server status
```

## Change RPi ssid
```
sudo vi /etc/hostapd/hostapd.conf
// Find ssid=
sudo ifconfig wlan0 down
sudo ifconfig wlan0 up
sudo service hostapd restart
```