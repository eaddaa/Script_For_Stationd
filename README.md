# Script_For_Stationd

```
sudo nano /root/restart_stationd.sh
```
```
#!/bin/bash
echo "$(date): Restarting stationd" >> /var/log/restart_stationd.log
sudo systemctl restart stationd
```
```
sudo chmod +x /root/restart_stationd.sh
```
```
sudo /root/restart_stationd.sh
```
```
sudo crontab -e
```
```
*/20 * * * * /root/restart_stationd.sh >> /var/log/restart_stationd.log 2>&1
```
```
sudo systemctl start cron
```
```
sudo systemctl status cron
```
```
sudo journalctl -u cron
```
```
sudo tail -f /var/log/restart_stationd.log
```

```
cat /var/log/restart_stationd.log
```
```
sudo systemctl status stationd
```
