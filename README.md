# Atlassian Software Docker Compose + Activate
This project run & Activate (crack) Attlasian software as docker container, All programs can be run behind a reverse proxy


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

and restart: docker restart fisheye

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
