podman run with -v : bound mount 
podman volumn

```
mkdir db_dir1
ls db_dir1
podman iamges
#docier.io/library/mysql

podman run -d --name mysql -v ~/db_dir1:/var/lib/mysql -e MQSQL_ROOT_PASSWORD=rpass -p 3306:3306 mysql

podman ps
#not running
podman logs mysql

podman run -d --name mysql -v ~/db_dir1:/var/lib/mysql:Z -e MQSQL_ROOT_PASSWORD=rpass -p 3306:3306 mysql
#TODO : Z vs z 


podman exec -it mysql bash
mysql -prpass
show databases

eixt
```

```
podman stop -a
podman rm mysql
podman volumn create db_volumne1
podman volumn list
podman volumn insepct db_volume1
podman run -d --name mysql -v db_volumn1:/var/lib/mysql -e MQSQL_ROOT_PASSWORD=rpass -p 3306:3306 mysql
podman ps

podman stop -a
podman rm
```
volumn created on container runtime
```
podman run -d --name mysql -v db_volumn2:/var/lib/mysql -e MQSQL_ROOT_PASSWORD=rpass -p 3306:3306 mysql


