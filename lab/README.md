# Docker Compose SC4S (Docker Destop)

When you clone this repo and run docker-compose run it will create a sc4s container for you, it just that easy

https://splunk.github.io/splunk-connect-for-syslog/main/gettingstarted/docker-compose-MacOS/ -> this guide you /opt/sc4s/ but I don't want use that path on my Mac machine so I create ./opt/sc4s/ under this repo.

```bash
sudo docker volume create splunk-sc4s-var
```