# pi-blaster-git

Daemon for Raspberry Pi which provides an interface to drive multiple PWM via the GPIO pins.

## Installing

#### via [yaourt](https://github.com/archlinuxfr/yaourt)
```
yaourt -S pi-blaster-git
```


## [systemd](https://wiki.archlinux.org/index.php/Systemd) Service
#### Start on boot
```
sudo systemctl enable pi-blaster
```
#### Start
```
sudo systemctl start pi-blaster
```

