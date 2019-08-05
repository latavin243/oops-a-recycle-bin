Remove useless docker image with name `none`

```bash
docker ps -a | grep 'Exited' | awk '{print $1}' | xargs docker stop
docker ps -a | grep 'Exited' | awk '{print $1}' | xargs docker rm
docker images | awk '$1 == "<none>" {print $3}' | xargs docker rmi
```
