![Atlassian](https://www.appnovation.com/sites/default/files/2020-11/Atlassian%202-V2_0.png)
# Atlassian Software Docker Compose + Activate
***This project run & Activate (crack) Attlasian software as docker container, All programs can be run behind a reverse proxy***
***The database is deployed on a separate server, without docker***
```bash
nano /etc/postgresql/13/main/pg_hba.conf
```
![image](https://user-images.githubusercontent.com/86954730/219866097-90ac6871-104c-494e-9ac5-e338083c7daf.png)
```bash
sudo -i -u postgres
psql  --> CREATE USER jira WITH password '*'; --> CREATE DATABASE jiradb; --> GRANT ALL ON DATABASE jiradb TO jira; 
...
--> \q --> exit --> systemctl restart postgresql
```
## Run Application
### Jira
run [jira-compose.yml](/jira-compose.yml)

```bash
docker-compose -f jira-compose.yml up -d
```
> Use `http://<ip>:8080`

### Confluence

run [confluence-compose.yml](/confluence-compose.yml)

```bash
docker-compose -f confluence-compose.yml up -d
```
> Use `http://<ip>:8090`

### bitbucket

run [bitbucket-compose.yml](/bitbucket-compose.yml)

```bash
docker-compose -f bitbucket-compose.yml up -d
```
> Use `http://<ip>:8090`

### Bamboo

run [bamboo-compose.yml](/bamboo-compose.yml)

```bash
docker-compose -f bamboo-compose.yml up -d
```
> Use `http://<ip>:8085`

### Fisheye & Crucible

run [fisheye-compose.yml](/fisheye-compose.yml)

```bash
docker-compose -f fisheye-compose.yml up -d
```
> Use `http://<ip>:8088`

![image](https://user-images.githubusercontent.com/86954730/218108506-f5911ba4-b59a-4de4-aee4-d2d6a05fe8df.png)

*and restart:* 
```yml
docker restart fisheye
```
### Jira Server Manegment (Service Desk)

run [servicemanagement-compose.yml](/servicemanagement-compose.yml)

```bash
docker-compose -f servicemanagement-compose.yml up -d
```
> Use `http://<ip>:8088`


## Activate (Crack) 

Moved Here : [activateAtlassianSoftware.md](activateAtlassianSoftware.md)

##  Use Reverse Proxy

Moved Here : [Reverse-Proxy-for-Atlassian.md](Reverse-Proxy-for-Atlassian.md)
# P.S
[Jira Images](https://hub.docker.com/r/atlassian/jira-software)
