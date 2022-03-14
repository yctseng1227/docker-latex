# Some Complier with VSCode

## LaTeX
- support CJK8
- support SSH
- can directly pull from [dockerhub](https://hub.docker.com/repository/docker/arikoi/vscode_latex)
- [sample docker-compose.yml](https://github.com/arikoi0703/docker/blob/master/vscode/docker-compose.yml)
- default user: root:latex
    - **You must change your password using `passwd` command**
- VSCode will auto install while first connect, there is no any VSCode-server installed during build

### Usage
```
$ docker-compose up -d
$ docker exec -it [container_id] bash
$ passwd # change password
```
