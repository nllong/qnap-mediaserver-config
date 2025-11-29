[longnas@longnas Container]$ cat start-docker-compose.sh
#!/bin/bash

# The source file is from /share/Container/start-docker-compose.sh

$(getcfg container-station Install_path -f /etc/config/qpkg.conf)/bin/docker-compose -f /share/Container/media_apps/docker-compose.yml up -d

$(getcfg container-station Install_path -f /etc/config/qpkg.conf)/bin/docker-compose -f /share/Container/notifyme/docker-compose.yml up --build -d
