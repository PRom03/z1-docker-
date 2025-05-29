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

-----------------------------------------------------------

![obraz](https://github.com/user-attachments/assets/bf1fe670-b623-4885-899d-7e6fdecdb1e7)


node:18-alpine jako obraz bazowy:

C:\Users\romp1\z1-docker-master>docker pull ghcr.io/prom03/z1-docker-backend:sha-baa7d33
sha-baa7d33: Pulling from prom03/z1-docker-backend
2a3ed1d9be05: Pull complete
1a8529962aaf: Pull complete
10511f014887: Pull complete
Digest: sha256:077ea7efb2cc67c5efd3336e0af5877827e7ea68e43e9d37248dbd7f44383a57
Status: Downloaded newer image for ghcr.io/prom03/z1-docker-backend:sha-baa7d33
ghcr.io/prom03/z1-docker-backend:sha-baa7d33

C:\Users\romp1\z1-docker-master>docker scout cves ghcr.io/prom03/z1-docker-backend:sha-baa7d33
    i New version 1.18.1 available (installed version is 1.17.0) at https://github.com/docker/scout-cli
    v Image stored for indexing
    v Indexed 292 packages
    x Detected 1 vulnerable package with 1 vulnerability


## Overview

                    │                 Analyzed Image
────────────────────┼─────────────────────────────────────────────────
  Target            │  ghcr.io/prom03/z1-docker-backend:sha-baa7d33
    digest          │  077ea7efb2cc
    platform        │ linux/amd64
    vulnerabilities │    0C     1H     0M     0L
    size            │ 48 MB
    packages        │ 292


## Packages and Vulnerabilities

   0C     1H     0M     0L  cross-spawn 7.0.3
pkg:npm/cross-spawn@7.0.3

    x HIGH CVE-2024-21538 [Inefficient Regular Expression Complexity]
      https://scout.docker.com/v/CVE-2024-21538
      Affected range : >=7.0.0
                     : <7.0.5
      Fixed version  : 7.0.5
      CVSS Score     : 7.7
      CVSS Vector    : CVSS:4.0/AV:N/AC:L/AT:N/PR:N/UI:N/VC:N/VI:N/VA:H/SC:N/SI:N/SA:N/E:P



1 vulnerability found in 1 package
  CRITICAL  0
  HIGH      1
  MEDIUM    0
  LOW       0


What's next:
    View base image update recommendations → docker scout recommendations ghcr.io/prom03/z1-docker-backend:sha-baa7d33

node:24-alpine jako obraz bazowy:

C:\Users\romp1\z1-docker-master>gh workflow run
? Select a workflow Z2 (z2-workflow.yml)
✓ Created workflow_dispatch event for z2-workflow.yml at main

To see runs for this workflow, try: gh run list --workflow=z2-workflow.yml

C:\Users\romp1\z1-docker-master>gh run watch
? Select a workflow run * Z2, Z2 [main] 18s ago
✓ main Z2 · 15272556071
Triggered via workflow_dispatch about 2 minutes ago

JOBS
✓ Build and push to ghcr.io in 1m52s (ID 42951323545)
  ✓ Set up job
  ✓ Checkout
  ✓ QEMU setup
  ✓ Docker Buildx setup
  ✓ Extract Docker metadata
  ✓ Sign in - ghcr.io
  ✓ Log in to DockerHub
  ✓ Build for a vulnerability check
  ✓ Run Trivy
  ✓ Build and push to GHCR
  ✓ Post Build and push to GHCR
  ✓ Post Run Trivy
  ✓ Post Build for a vulnerability check
  ✓ Post Log in to DockerHub
  ✓ Post Sign in - ghcr.io
  ✓ Post Docker Buildx setup
  ✓ Post QEMU setup
  ✓ Post Checkout
  ✓ Complete job

✓ Run Z2 (15272556071) completed with 'success'

C:\Users\romp1\z1-docker-master>docker pull ghcr.io/prom03/z1-docker-backend:sha-2fb8c4a
sha-2fb8c4a: Pulling from prom03/z1-docker-backend
39a55249cba7: Pull complete
51b1596d83e2: Pull complete
fdd2886d98a0: Pull complete
918b215413e3: Pull complete
67cdafb02007: Pull complete
c618aeaf9f0a: Pull complete
Digest: sha256:77a163ecc88afd6098ccb6e49f6127770ab1210021e853128264a4acf90ec780
Status: Downloaded newer image for ghcr.io/prom03/z1-docker-backend:sha-2fb8c4a
ghcr.io/prom03/z1-docker-backend:sha-2fb8c4a

C:\Users\romp1\z1-docker-master>docker scout cves ghcr.io/prom03/z1-docker-backend:sha-2fb8c4a
    i New version 1.18.1 available (installed version is 1.17.0) at https://github.com/docker/scout-cli
    v Image stored for indexing
    v Indexed 291 packages
    v No vulnerable package detected


## Overview

                    │                 Analyzed Image
────────────────────┼─────────────────────────────────────────────────
  Target            │  ghcr.io/prom03/z1-docker-backend:sha-2fb8c4a
    digest          │  77a163ecc88a
    platform        │ linux/amd64
    vulnerabilities │    0C     0H     0M     0L
    size            │ 61 MB
    packages        │ 291


## Packages and Vulnerabilities

  No vulnerable packages detected


C:\Users\romp1\z1-docker-master>gh workflow run
? Select a workflow Z2 (z2-workflow.yml)
✓ Created workflow_dispatch event for z2-workflow.yml at main

To see runs for this workflow, try: gh run list --workflow=z2-workflow.yml

C:\Users\romp1\z1-docker-master>gh run watch
? Select a workflow run * Z2, Z2 [main] 3s ago
✓ main Z2 · 15279945961
Triggered via workflow_dispatch about 1 minute ago

JOBS
✓ Build and push to ghcr.io in 51s (ID 42976100728)
  ✓ Set up job
  ✓ Checkout
  ✓ QEMU setup
  ✓ Docker Buildx setup
  ✓ Extract Docker metadata
  ✓ Sign in - ghcr.io
  ✓ Log in to DockerHub
  ✓ Build for a vulnerability check
  ✓ Run Trivy
  ✓ Build and push to GHCR
  ✓ Post Build and push to GHCR
  ✓ Post Run Trivy
  ✓ Post Build for a vulnerability check
  ✓ Post Log in to DockerHub
  ✓ Post Sign in - ghcr.io
  ✓ Post Docker Buildx setup
  ✓ Post QEMU setup
  ✓ Post Checkout
  ✓ Complete job

✓ Run Z2 (15279945961) completed with 'success'

C:\Users\romp1\z1-docker-master>docker pull ghcr.io/prom03/z1-docker-backend:sha-3eea431
sha-3eea431: Pulling from prom03/z1-docker-backend
3fc295d0e4bb: Pull complete
5a5134deb427: Pull complete
7928a0bb65fb: Pull complete
Digest: sha256:f807546a437a09252ad21832aeb6ab1ebad52b5d13a57650c55a6e2b5f834fdf
Status: Downloaded newer image for ghcr.io/prom03/z1-docker-backend:sha-3eea431
ghcr.io/prom03/z1-docker-backend:sha-3eea431

C:\Users\romp1\z1-docker-master>docker-compose up
time="2025-05-27T18:03:01+02:00" level=warning msg="C:\\Users\\romp1\\z1-docker-master\\docker-compose.yaml: the attribute `version` is obsolete, it will be ignored, please remove it to avoid potential confusion"
[+] Running 2/2
 ✔ Container z1-docker-master-backend-1   Created                                                                  0.0s
 ✔ Container z1-docker-master-frontend-1  Created                                                                  0.0s
Attaching to backend-1, frontend-1
frontend-1  | /docker-entrypoint.sh: /docker-entrypoint.d/ is not empty, will attempt to perform configuration
frontend-1  | /docker-entrypoint.sh: Looking for shell scripts in /docker-entrypoint.d/
frontend-1  | /docker-entrypoint.sh: Launching /docker-entrypoint.d/10-listen-on-ipv6-by-default.sh
frontend-1  | 10-listen-on-ipv6-by-default.sh: info: Getting the checksum of /etc/nginx/conf.d/default.conf
backend-1   | Aplikacja uruchomiona: 2025-05-27T16:03:03.584Z
frontend-1  | 10-listen-on-ipv6-by-default.sh: info: /etc/nginx/conf.d/default.conf differs from the packaged version
backend-1   | Autor: Przemysław Romaniak
frontend-1  | /docker-entrypoint.sh: Sourcing /docker-entrypoint.d/15-local-resolvers.envsh
backend-1   | Nasłuchiwanie na porcie: 3000
frontend-1  | /docker-entrypoint.sh: Launching /docker-entrypoint.d/20-envsubst-on-templates.sh
backend-1   | App running on port 3000
frontend-1  | /docker-entrypoint.sh: Launching /docker-entrypoint.d/30-tune-worker-processes.sh
frontend-1  | /docker-entrypoint.sh: Configuration complete; ready for start up
frontend-1  | 2025/05/27 16:03:03 [notice] 1#1: using the "epoll" event method
frontend-1  | 2025/05/27 16:03:03 [notice] 1#1: nginx/1.27.5
frontend-1  | 2025/05/27 16:03:03 [notice] 1#1: built by gcc 14.2.0 (Alpine 14.2.0)
frontend-1  | 2025/05/27 16:03:03 [notice] 1#1: OS: Linux 5.15.167.4-microsoft-standard-WSL2
frontend-1  | 2025/05/27 16:03:03 [notice] 1#1: getrlimit(RLIMIT_NOFILE): 1048576:1048576
frontend-1  | 2025/05/27 16:03:03 [notice] 1#1: start worker processes
frontend-1  | 2025/05/27 16:03:03 [notice] 1#1: start worker process 29
frontend-1  | 2025/05/27 16:03:03 [notice] 1#1: start worker process 30
frontend-1  | 2025/05/27 16:03:03 [notice] 1#1: start worker process 31
frontend-1  | 2025/05/27 16:03:03 [notice] 1#1: start worker process 32
frontend-1  | 2025/05/27 16:03:03 [notice] 1#1: start worker process 33
frontend-1  | 2025/05/27 16:03:03 [notice] 1#1: start worker process 34
frontend-1  | 2025/05/27 16:03:03 [notice] 1#1: start worker process 35
frontend-1  | 2025/05/27 16:03:03 [notice] 1#1: start worker process 36
frontend-1  | 2025/05/27 16:03:03 [notice] 1#1: start worker process 37
frontend-1  | 2025/05/27 16:03:03 [notice] 1#1: start worker process 38
frontend-1  | 2025/05/27 16:03:03 [notice] 1#1: start worker process 39
frontend-1  | 2025/05/27 16:03:03 [notice] 1#1: start worker process 40
frontend-1  | 172.20.0.1 - - [27/May/2025:16:03:38 +0000] "GET / HTTP/1.1" 200 3108 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:138.0) Gecko/20100101 Firefox/138.0" "-"
frontend-1  | 172.20.0.1 - - [27/May/2025:16:03:38 +0000] "GET /style.css HTTP/1.1" 200 563 "http://localhost:8080/" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:138.0) Gecko/20100101 Firefox/138.0" "-"
frontend-1  | 172.20.0.1 - - [27/May/2025:16:03:41 +0000] "GET /api/weather?city=Siedlce HTTP/1.1" 200 747 "http://localhost:8080/" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:138.0) Gecko/20100101 Firefox/138.0" "-"
