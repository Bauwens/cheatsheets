cheatsheets
===========

## Services

| Action                                      |  Command                                         |
| :---                                        | :---                                             |
| List services                               | `systemctl list-units --type service`            |
| Query SERVICE status                        | `sudo systemctl status SERVICE.service`          |
| List failed services on boot                | `sudo systemctl --failed`                        |
| Start SERVICE                               | `sudo systemctl start SERVICE.service`           |
| Stop SERVICE                                | `sudo systemctl stop SERVICE.service`            |
| Restart SERVICE                             | `sudo systemctl restart SERVICE.service`         |
| *Kill* SERVICE (all processes) with SIGTERM | `sudo systemctl kill SERVICE.service`            |
| *Kill* SERVICE (all processes) with SIGKILL | `sudo systemctl kill -s SIGKILL SERVICE.service` |
| Start SERVICE on boot                       | `sudo systemctl enable SERVICE.service`          |
| Don't start SERVICE on boot                 | `sudo systemctl disable SERVICE.service`         |

## Red hat network config files

| Action                                      | Command                                          |
| :---                                        | :---                                             |
| network scripts                             | `/etc/sysconfig/network-scripts/ifcfg-eth0`      |
| gateway / hostname                          | `/etc/sysconfig/network`                         |
| DNS                                         | `/etc/resolv.conf       `                        |
| restart services                            | `/etc/init.d/network restart`                    |

## Network config commands

| Action                             | Command                                       |
| :---                               | :---                                          |
| List interfaces (and IP addresses) | `ip address`, `ip a`                          |
| Route table                        | `ip route`, `ip r`                            |
| DNS servers                        | `cat /etc/resolv.conf`                        |
| Set IP address of an interface*    | `ip address add 192.168.56.1/24 dev vboxnet0` |
| General info                       | `ifconfig`                                    |

## Firewall

| Action                           | Command                                                          |
| :---                             | :---                                                             |
| Firewall state                   | `firewall-cmd --state`                                           |
| Reload permanent rules           | `firewall-cmd --reload`                                          |
| Currently enabled features       | `firewall-cmd --list-all-zones`                                  |
| List supported zones             | `firewall-cmd --get-zones`                                       |
| List preconfigured services      | `firewall-cmd --get-services`                                    |
| Enabled features in current zone | `firewall-cmd --list-all`                                        |
| Enabled features in zone         | `firewall-cmd [--permanent] [--zone=ZONE] --list-all`            |
| Enable a service in zone         | `firewall-cmd [--permanent] [--zone=ZONE] --add-service=http`    |
| Remove service frome zone        | `firewall-cmd [--permanent] [--zone=ZONE] --remove-service=http` |
| Enable a port in zone            | `firewall-cmd [--permanent] [--zone=ZONE] --add-port=80/tcp`     |
| Remove a port from zone          | `firewall-cmd [--permanent] [--zone=ZONE] --remove-port=80/tcp`  |
| Turn panic mode on               | `firewall-cmd --panic-on`                                        |
| Turn panic mode off              | `firewall-cmd --panic-off`                                       |  
