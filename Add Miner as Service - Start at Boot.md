NODE MUST BE RUNNING FOR MINER TO WORK
--------------------------------------
Create service file called "startminer.service" with nano editor
```
sudo nano /etc/systemd/system/startminer.service
```
Enter the following contents, replace USERNAME with username or path to the miner daemon
```
Description=start miner

Wants=network.target
After=syslog.target network-online.target

[Service]
Type=simple
ExecStart=/home/USERNAME/everycash/build/src/miner --threads 1 --address YOURWALLET ADDRESS SEE EXAMPLE BELOW
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
sudo systemctl enable startminer.service
```
```
sudo systemctl start startminer.service
```
```
sudo systemctl status startminer.service
```


Example Wallet Address
everNwTYgwiKcb9Rg8dSV4TYC5Y2xmu1yfcalsdkfj0089asdlkfj3kivuee6oyBuoZgjEHLLKP1EUUHEbc5KkE5qg9099dfadf9
