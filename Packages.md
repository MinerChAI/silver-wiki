# `packages`
![](packages.png)

This module displays the number of packages with available updates.

The supported package managers are pacman, DNF, and APT.

## Daemon
This module requires the [packagesd](../tree/master/packagesd) daemon to be running.

### Installation
```sh
go get github.com/reujab/bronze/packagesd
sudo mv "$GOPATH/bin/packagesd" /usr/local/bin
sudo cp "$GOPATH/src/github.com/reujab/bronze/packagesd/packagesd.service" /etc/systemd/system
sudo systemctl enable packagesd
sudo systemctl start packagesd
systemctl status packagesd
```
