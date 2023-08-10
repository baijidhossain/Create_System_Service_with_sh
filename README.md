# Create_System_Service_with_sh

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

