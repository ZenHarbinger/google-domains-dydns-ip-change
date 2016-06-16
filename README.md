# check-ip-change

A script for detecting a change in Google Domains dynamic DNS records.

## Configure

- Fill in appropriate information in the check-ip-change.json file
- Place the file in your `~/.config/` directory

## Uses

- cron job for updating IP addresses automatically.

## Usage

Add Configured Dynamic DNS Record.

```
$ check-ip-change --add
Domain: sub.domain.com
User: [Google Provided]
Password: [Google Provided]
E-Mail: [Google E-Mail address]
```

List Configured Dynamic DNS Records. This will list out an index value and name. This index or name value can be used when removing a configured record.

```
$ check-ip-change --list
[ 1 ] sub.domain.com
--------------------------
username: [Google Provided]
password: [Google Provided]
email: [Google E-Mail address]
```

Remove Configured Dynamic DNS Record.

```
$ check-ip-change --remove
Domain to Remove (Index or Name): 1
or
Domain to Remove (Index or Name): sub.domain.com
```

Configurations are stored in `~/.config/check-ip-change.json` nothing is saved remotely

## Future work

- Add the ability to add/remove/view configurations on the command line.

## Requirements

- Python3
- [python3-xdg](https://freedesktop.org/wiki/Software/pyxdg/)
- [python3-dnspython](http://www.dnspython.org/)
- [python3-jsonpickle](https://jsonpickle.github.io/)

### Ubuntu Server

```
sudo apt install python3-xdg python3-dnspython python3-jsonpickle
```

### Ubuntu Desktop

```
sudo apt install python3-dnspython python3-jsonpickle
```

python3-xdg is already available in the Desktop.

### Fedora Server

```
sudo dnf install python3-pyxdg python3-dns python3-jsonpickle
```

### Fedora Desktop

```
sudo dnf install python3-dns python3-jsonpickle
```

python3-pyxdg is already available in the Desktop.
