Steamcmd docker container
=====

Containerized steamcmd.sh

Setup
-----

```bash
docker pull blang/steamcmd
```
or build:
```bash
docker build -t blang/steamcmd .

```

Usage:
-----

Install/update and validate app 740 as your current user to `/home/user/gameserver`

```bash
docker run --rm -i --user="$(id -u):$(id -g)" \
 -v /home/user/gameserver:/data blang/steamcmd \
 +login anonymous \
 +force_install_dir /data \
 +app_update 740 validate \
 +quit
```

License
-----

See [LICENSE](LICENSE) file.