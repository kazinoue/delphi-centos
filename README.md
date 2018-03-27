# Summary

It is image for RAD Studio Delphi Linux development.
It is for my private use.

# Detail

It is for RAD Studio 10.2 Tokyo Linux development.

It includes following packagers.

- development
- xterm
- httpd

But PAServer has not included. so you have to install PAServer by yourself.

# How to use it.

## Launch container

```
docker run -it -p 64211:64211 kazinoue/delphi-centos
```

## Copy PAServer

For first, you can find container id or container name as following.

```
$ docker ps
CONTAINER ID        IMAGE                    COMMAND             CREATED             STATUS              PORTS                      NAMES
8fc609336bd8        kazinoue/delphi-centos   "/bin/bash"         12 seconds ago      Up 12 seconds       0.0.0.0:64211->64211/tcp   sad_engelbart
```

And then you can copy LinuxPAServer19.0.tar.gz into container.

```
$ docker cp LinuxPAServer19.0.tar.gz sad_engelbart:/
$ docker cp LinuxPAServer19.0.tar.gz 8fc609336bd8:/
```
