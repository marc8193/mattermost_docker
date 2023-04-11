# Mattermost Docker Guide
## Install
### 1. Clone repository and enter dirctory
```
git clone https://github.com/marc8193/mattermost_docker.git
cd mattermost_docker
```
### 2. Create your .env file by copying and adjusting the env.example file.
## !! You must edit the DOMAIN value in the .env file !!
```
cp env.example .env
```
### 3. Create the required directories and set their permissions.
```yml
mkdir -p ./volumes/app/mattermost/{config,data,logs,plugins,client/plugins,bleve-indexes}
sudo chown -R 2000:2000 ./volumes/app/mattermost
```
### 4. Deploy Mattermost with docker compose
```
sudo docker compose up -d
```
