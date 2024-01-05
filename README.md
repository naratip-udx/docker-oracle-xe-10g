# docker-oracle-xe-10g

Oracle Express Edition Universal 10g Release 2 (10.2.0.1) 32-bit on Debian.

Based on
[jaanonim/docker-oracle-xe-10g](https://github.com/jaanonim/docker-oracle-xe-10g).

### Installation

```docker
docker pull naratipud/oracle-xe-10g
```

Run with 1521 and 8080 ports opened:

```docker
docker run -d -p 49161:1521 -p 49162:8080 --mount source=oracle10g_vol,target=/usr/lib/oracle naratipud/oracle-xe-10g
```

Connect database with following setting:

```text
hostname: localhost
port: 49161
sid: xe
username: system
password: oracle
```

Login to web administrator on a browser:

```text
http://localhost:49162/apex
```
