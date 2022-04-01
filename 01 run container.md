```
podman sesarch nginx | grep -i official
podman pull docker.io......

podman images
podmain inspect <iamge_name> | grep less

podman run -d --name nginx-1 -p 8080:80 <image_name>

podman ps

curl localhost:8080

podman exit -it ngnix-1 bash

//inside container

```

log
```
podman logs nigix-1
```
event
```
podman events --since 1h
```
systemd
```
mkdir -p ~/.config/systemd/user
cd .config /systemd/user
podman generate systemd --files --new --name nainx-1
```

```
podman stop nginx-1
podman ps 
<empty>
```

```
systemctl --user daemon-reload
systemctl --user enable --now container0nginx-1
systemctl --user status container-nginx-1


loginctl show-user cloud_user | grep -i linger
loginctl enablle-linger
<reboot>

systemctl --user status container-nginx-1

curl localhost:8080
podman ps
```
```


