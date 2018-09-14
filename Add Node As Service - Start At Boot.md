Create service file called "startnode.service" with nano editor
```
sudo nano /etc/systemd/system/startnode.service
```
Enter the following contents, replace USERNAME with username or path to the EveryCashD daemon
```
Description=start node

Wants=network.target
After=syslog.target network-online.target

[Service]
Type=simple
ExecStart=/home/USERNAME/everycash/build/src/EveryCashd
Restart=on-failure
RestartSec=10
KillMode=process

[Install]
WantedBy=multi-user.target
```
Setup as service and run! 
```
sudo systemctl daemon-reload
```
```
sudo systemctl enable startnode.service
```
```
sudo systemctl start startnode.service
```
```
sudo systemctl status startnode.service
```
