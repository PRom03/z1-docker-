![obraz](https://github.com/user-attachments/assets/50b01859-3e6c-4da1-be24-ae5befaba580)

C:\Users\romp1\z1-docker-master>docker-compose up
time="2025-05-26T20:54:21+02:00" level=warning msg="C:\\Users\\romp1\\z1-docker-master\\docker-compose.yaml: the attribute `version` is obsolete, it will be ignored, please remove it to avoid potential confusion"
[+] Running 3/3
 ✔ Network z1-docker-master_default       Created                                                                  0.1s
 ✔ Container z1-docker-master-backend-1   Created                                                                  0.3s
 ✔ Container z1-docker-master-frontend-1  Created                                                                  0.4s
Attaching to backend-1, frontend-1
frontend-1  | /docker-entrypoint.sh: /docker-entrypoint.d/ is not empty, will attempt to perform configuration
frontend-1  | /docker-entrypoint.sh: Looking for shell scripts in /docker-entrypoint.d/
frontend-1  | /docker-entrypoint.sh: Launching /docker-entrypoint.d/10-listen-on-ipv6-by-default.sh
frontend-1  | 10-listen-on-ipv6-by-default.sh: info: Getting the checksum of /etc/nginx/conf.d/default.conf
backend-1   | Aplikacja uruchomiona: 2025-05-26T18:54:24.388Z
frontend-1  | 10-listen-on-ipv6-by-default.sh: info: /etc/nginx/conf.d/default.conf differs from the packaged version
backend-1   | Autor: Przemysław Romaniak
frontend-1  | /docker-entrypoint.sh: Sourcing /docker-entrypoint.d/15-local-resolvers.envsh
backend-1   | Nasłuchiwanie na porcie: 3000
frontend-1  | /docker-entrypoint.sh: Launching /docker-entrypoint.d/20-envsubst-on-templates.sh
backend-1   | App running on port 3000
frontend-1  | /docker-entrypoint.sh: Launching /docker-entrypoint.d/30-tune-worker-processes.sh
frontend-1  | /docker-entrypoint.sh: Configuration complete; ready for start up
frontend-1  | 2025/05/26 18:54:24 [notice] 1#1: using the "epoll" event method
frontend-1  | 2025/05/26 18:54:24 [notice] 1#1: nginx/1.27.5
frontend-1  | 2025/05/26 18:54:24 [notice] 1#1: built by gcc 14.2.0 (Alpine 14.2.0)
frontend-1  | 2025/05/26 18:54:24 [notice] 1#1: OS: Linux 5.15.167.4-microsoft-standard-WSL2
frontend-1  | 2025/05/26 18:54:24 [notice] 1#1: getrlimit(RLIMIT_NOFILE): 1048576:1048576
frontend-1  | 2025/05/26 18:54:24 [notice] 1#1: start worker processes
frontend-1  | 2025/05/26 18:54:24 [notice] 1#1: start worker process 29
frontend-1  | 2025/05/26 18:54:24 [notice] 1#1: start worker process 30
frontend-1  | 2025/05/26 18:54:24 [notice] 1#1: start worker process 31
frontend-1  | 2025/05/26 18:54:24 [notice] 1#1: start worker process 32
frontend-1  | 2025/05/26 18:54:24 [notice] 1#1: start worker process 33
frontend-1  | 2025/05/26 18:54:24 [notice] 1#1: start worker process 34
frontend-1  | 2025/05/26 18:54:24 [notice] 1#1: start worker process 35
frontend-1  | 2025/05/26 18:54:24 [notice] 1#1: start worker process 36
frontend-1  | 2025/05/26 18:54:24 [notice] 1#1: start worker process 37
frontend-1  | 2025/05/26 18:54:24 [notice] 1#1: start worker process 38
frontend-1  | 2025/05/26 18:54:24 [notice] 1#1: start worker process 39
frontend-1  | 2025/05/26 18:54:24 [notice] 1#1: start worker process 40
frontend-1  | 172.20.0.1 - - [26/May/2025:18:54:42 +0000] "GET / HTTP/1.1" 200 3108 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:138.0) Gecko/20100101 Firefox/138.0" "-"
frontend-1  | 172.20.0.1 - - [26/May/2025:18:54:42 +0000] "GET /style.css HTTP/1.1" 200 563 "http://localhost:8080/" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:138.0) Gecko/20100101 Firefox/138.0" "-"
frontend-1  | 172.20.0.1 - - [26/May/2025:18:54:47 +0000] "GET /api/weather?city=Siedlce HTTP/1.1" 200 772 "http://localhost:8080/" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:138.0) Gecko/20100101 Firefox/138.0" "-"
