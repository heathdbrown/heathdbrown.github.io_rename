
# Infrastructure API used by Tumblr
- http://tumblr.github.io/collins/

## Issues with Quickstart:

When attempting to run the quickstart on Fedora 22:

```
docker run -p 9000:9000 tumblr/collins
```

Received the following error:
```
Post http:///var/run/docker.sock/v1.19/containers/create: dial unix /var/run/docker.sock: no such file or directory. Are you trying to connect to a TLS-enabled daemon without TLS?
```
Found the docker.service was not enabled via systemd.

```
[root@objtest ~]# chkconfig

Note: This output shows SysV services only and does not include native
      systemd services. SysV configuration data might be overridden by native
      systemd configuration.

      If you want to list systemd services use 'systemctl list-unit-files'.
      To see services enabled on particular target use
      'systemctl list-dependencies [target]'.

netconsole     	0:off	1:off	2:off	3:off	4:off	5:off	6:off
network        	0:off	1:off	2:on	3:on	4:on	5:on	6:off
xe-linux-distribution	0:off	1:off	2:on	3:on	4:on	5:on	6:off
```

Then reviewed systemd

```
[root@objtest ~]# systemctl list-unit-files | grep docker
docker-storage-setup.service              disabled
docker.service                            disabled
```

Busted when attempting to start docker.service, turns out I have no clue what I am doing wit systemd and Fedora knows it.

```
[root@objtest ~]# service docker.service start
Redirecting to /bin/systemctl start  docker.service.service
Failed to start docker.service.service: Unit docker.service.service failed to load: No such file or directory.
```

Reviewed the documentation, you need to run with the correct name for the service. https://docs.docker.com/installation/fedora/

```
[root@objtest ~]# service docker start
Redirecting to /bin/systemctl start  docker.service
```

## Screenshot

![](/img/collins-search.png)
