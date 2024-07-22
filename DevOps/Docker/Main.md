

Connect to a docker container interactively to explore

```
docker exec -it <container> sh
```

This will open a linux shell which can be used to interact with running container.
Finally leave the shell with exit


Delete an image

docker delete rmi -f <imgId>