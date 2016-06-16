# google-domains-synthetic-ip-change

A script for detecting a change in Google Domains Synthetic records.

## Configure

- Fill in appropriate information in the check-ip-change.json file
- Place the file in your `~/.config/` directory

## Uses

- cron job for updating IP addresses automatically.

## Future work

- Add the ability to add/remove/view configurations on the command line.

## Requirements

- Python3
- [python3-xdg](https://freedesktop.org/wiki/Software/pyxdg/)
- [python3-dnspython](http://www.dnspython.org/)
- [python3-jsonpickle](https://jsonpickle.github.io/)

### Ubuntu
```
sudo apt install python3-xdg python3-dnspython python3-jsonpickle
```
