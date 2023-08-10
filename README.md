# Create Systemd  Service with sh

## Create a new service file (/etc/systemd/system/service_name.service) using a text editor
#### [Unit]
#### Description=Send Pending Pessage
#### After=network.target
#### StartLimitIntervalSec=0

#### [Service]
#### Type=simple
#### WorkingDirectory=/var/www/adminPanel/sh_services
#### ExecStart=/var/www/adminPanel/sh_services/sendPendingMsg.sh
#### Restart=always
#### RestartSec=3

#### [Install]
#### WantedBy=multi-user.target

## Create a new sh_file (/var/www/adminPanel/sh_services/sendPendingMsg.sh) using a text editor

#### #!/bin/bash

#### cd /var/www/adminPanel/sh_services

#### php send_pending_msg.php


# Sudo Command
## Service Enable And Start
sudo systemctl enable service_name.service
sudo systemctl start service_name.service


## Service Status check
#### sudo systemctl status counter.service
####  sudo systemctl status counter.timer
####  sudo systemctl daemon-reload
####  sudo systemctl restart counter.timer
####  sudo systemctl restart counter.service
####  sudo systemctl status counter.timer
####  sudo systemctl status counter.service
####  sudo journalctl -u counter

