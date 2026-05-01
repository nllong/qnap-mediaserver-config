This repo contains the docker-compose config for my media server. The containers are run on a QNAP server. Make sure to confgiure docker compose on the QNAP and add in the start-docker-compose.sh file below and add it to the "start up".

```bash
[longnas@longnas Container]$ cat start-docker-compose.sh
#!/bin/bash

# The source file is from /share/Container/start-docker-compose.sh

$(getcfg container-station Install_path -f /etc/config/qpkg.conf)/bin/docker-compose -f /share/Container/media_apps/docker-compose.yml up -d

$(getcfg container-station Install_path -f /etc/config/qpkg.conf)/bin/docker-compose -f /share/Container/notifyme/docker-compose.yml up --build -d
```
