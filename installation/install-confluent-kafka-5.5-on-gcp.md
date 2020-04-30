Install COnfluent Server 5.5
================================

#### Install Confluent Kafka using below commands:
```bash
wget -qO - https://packages.confluent.io/rpm/5.5/archive.key | sudo apt-key add -
sudo add-apt-repository "deb https://packages.confluent.io/deb/5.5 stable main"
sudo apt-get update
sudo apt-get install confluent-server
```


