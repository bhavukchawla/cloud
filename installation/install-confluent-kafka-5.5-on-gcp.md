Install Confluent Server 5.5
================================

#### Install Confluent Kafka using below commands:
```bash
wget -qO - https://packages.confluent.io/rpm/5.5/archive.key | sudo apt-key add -
sudo add-apt-repository "deb https://packages.confluent.io/deb/5.5 stable main"
sudo apt-get update
sudo apt-get install confluent-server
```

#### Give 777 permission to /var/lib/zookeeper
```bash
sudo chmod -R 777 /var/lib/zookeeper
```

#### Start the Zookeeper Services:
```bash
sudo systemctl start confluent-zookeeper
```
**Note:** If you are facing issue while starting zookeeper
Open myid file and specify ``0`` in it 
```bash
sudo vi /var/lib/zookeeper/myid
```
 
### Restart the Zookeeper Services: 
```bash
sudo systemctl restart confluent-zookeeper
```

### Check the status of Zookeeper Services: 
```bash
sudo systemctl status confluent-zookeeper
```

#### Start Confluent server
```bash
sudo systemctl start confluent-server.service
```


