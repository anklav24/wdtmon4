```bash
./show_tty_for_lsusb.sh  # get watchdog serial port
./wdtmon4 /dev/ttyACM0 -w  # run service
```

# For persistent installation
Add to cron
```bash
# add wdtmon4 to /root dir on the server
vim /etc/systemd/system/wdtmon4.service  # get from ./services/wdtmon4.service
systemctl daemon-reload
systemctl enable
systemctl start wdtmon4.service

# go to http://localhost:8000
http://proxmox-srv.local.:8000  # Real world example
```