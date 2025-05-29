node:18-alpine jako obraz bazowy:

C:\Users\romp1\z1-docker-master>docker pull ghcr.io/prom03/z1-docker-backend:sha-baa7d33 sha-baa7d33: Pulling from prom03/z1-docker-backend 2a3ed1d9be05: Pull complete 1a8529962aaf: Pull complete 10511f014887: Pull complete Digest: sha256:077ea7efb2cc67c5efd3336e0af5877827e7ea68e43e9d37248dbd7f44383a57 Status: Downloaded newer image for ghcr.io/prom03/z1-docker-backend:sha-baa7d33 ghcr.io/prom03/z1-docker-backend:sha-baa7d33

C:\Users\romp1\z1-docker-master>docker scout cves ghcr.io/prom03/z1-docker-backend:sha-baa7d33 i New version 1.18.1 available (installed version is 1.17.0) at https://github.com/docker/scout-cli v Image stored for indexing v Indexed 292 packages x Detected 1 vulnerable package with 1 vulnerability
Overview

                │                 Analyzed Image

────────────────────┼───────────────────────────────────────────────── Target │ ghcr.io/prom03/z1-docker-backend:sha-baa7d33 digest │ 077ea7efb2cc platform │ linux/amd64 vulnerabilities │ 0C 1H 0M 0L size │ 48 MB packages │ 292
Packages and Vulnerabilities

0C 1H 0M 0L cross-spawn 7.0.3 pkg:npm/cross-spawn@7.0.3

x HIGH CVE-2024-21538 [Inefficient Regular Expression Complexity]
  https://scout.docker.com/v/CVE-2024-21538
  Affected range : >=7.0.0
                 : <7.0.5
  Fixed version  : 7.0.5
  CVSS Score     : 7.7
  CVSS Vector    : CVSS:4.0/AV:N/AC:L/AT:N/PR:N/UI:N/VC:N/VI:N/VA:H/SC:N/SI:N/SA:N/E:P

1 vulnerability found in 1 package CRITICAL 0 HIGH 1 MEDIUM 0 LOW 0

What's next: View base image update recommendations → docker scout recommendations ghcr.io/prom03/z1-docker-backend:sha-baa7d33

node:24-alpine jako obraz bazowy:

C:\Users\romp1\z1-docker-master>gh workflow run ? Select a workflow Z2 (z2-workflow.yml) ✓ Created workflow_dispatch event for z2-workflow.yml at main

To see runs for this workflow, try: gh run list --workflow=z2-workflow.yml

C:\Users\romp1\z1-docker-master>gh run watch ? Select a workflow run * Z2, Z2 [main] 18s ago ✓ main Z2 · 15272556071 Triggered via workflow_dispatch about 2 minutes ago

JOBS ✓ Build and push to ghcr.io in 1m52s (ID 42951323545) ✓ Set up job ✓ Checkout ✓ QEMU setup ✓ Docker Buildx setup ✓ Extract Docker metadata ✓ Sign in - ghcr.io ✓ Log in to DockerHub ✓ Build for a vulnerability check ✓ Run Trivy ✓ Build and push to GHCR ✓ Post Build and push to GHCR ✓ Post Run Trivy ✓ Post Build for a vulnerability check ✓ Post Log in to DockerHub ✓ Post Sign in - ghcr.io ✓ Post Docker Buildx setup ✓ Post QEMU setup ✓ Post Checkout ✓ Complete job

✓ Run Z2 (15272556071) completed with 'success'

C:\Users\romp1\z1-docker-master>docker pull ghcr.io/prom03/z1-docker-backend:sha-72b3a36 sha-72b3a36: Pulling from prom03/z1-docker-backend 217ed91e0428: Pull complete 01a6be3bbbd2: Pull complete d18a884e67e0: Pull complete Digest: sha256:fb48eaa8d5ff3b4adb2da7e524c97aec74275107d54787e2e98a08cb351f1162 Status: Downloaded newer image for ghcr.io/prom03/z1-docker-backend:sha-72b3a36 ghcr.io/prom03/z1-docker-backend:sha-72b3a36

C:\Users\romp1\z1-docker-master>docker scout cves ghcr.io/prom03/z1-docker-backend:sha-72b3a36 i New version 1.18.1 available (installed version is 1.17.0) at https://github.com/docker/scout-cli v Image stored for indexing v Indexed 291 packages v No vulnerable package detected
Overview

                │                 Analyzed Image

────────────────────┼───────────────────────────────────────────────── Target │ ghcr.io/prom03/z1-docker-backend:sha-72b3a36 digest │ fb48eaa8d5ff platform │ linux/amd64 vulnerabilities │ 0C 0H 0M 0L size │ 61 MB packages │ 291
Packages and Vulnerabilities

No vulnerable packages detected

C:\Users\romp1\z1-docker-master>docker-compose up
time="2025-05-29T14:05:20+02:00" level=warning msg="C:\\Users\\romp1\\z1-docker-master\\docker-compose.yaml: the attribute `version` is obsolete, it will be ignored, please remove it to avoid potential confusion"
[+] Running 2/2
 ✔ Container z1-docker-master-backend-1   Created                                                                  0.0s
 ✔ Container z1-docker-master-frontend-1  Created                                                                  0.0s
Attaching to backend-1, frontend-1
frontend-1  | /docker-entrypoint.sh: /docker-entrypoint.d/ is not empty, will attempt to perform configuration
frontend-1  | /docker-entrypoint.sh: Looking for shell scripts in /docker-entrypoint.d/
frontend-1  | /docker-entrypoint.sh: Launching /docker-entrypoint.d/10-listen-on-ipv6-by-default.sh
frontend-1  | 10-listen-on-ipv6-by-default.sh: info: Getting the checksum of /etc/nginx/conf.d/default.conf
frontend-1  | 10-listen-on-ipv6-by-default.sh: info: /etc/nginx/conf.d/default.conf differs from the packaged version
frontend-1  | /docker-entrypoint.sh: Sourcing /docker-entrypoint.d/15-local-resolvers.envsh
frontend-1  | /docker-entrypoint.sh: Launching /docker-entrypoint.d/20-envsubst-on-templates.sh
frontend-1  | /docker-entrypoint.sh: Launching /docker-entrypoint.d/30-tune-worker-processes.sh
frontend-1  | /docker-entrypoint.sh: Configuration complete; ready for start up
frontend-1  | 2025/05/29 12:05:22 [notice] 1#1: using the "epoll" event method
frontend-1  | 2025/05/29 12:05:22 [notice] 1#1: nginx/1.27.5
frontend-1  | 2025/05/29 12:05:22 [notice] 1#1: built by gcc 14.2.0 (Alpine 14.2.0)
frontend-1  | 2025/05/29 12:05:22 [notice] 1#1: OS: Linux 5.15.167.4-microsoft-standard-WSL2
frontend-1  | 2025/05/29 12:05:22 [notice] 1#1: getrlimit(RLIMIT_NOFILE): 1048576:1048576
frontend-1  | 2025/05/29 12:05:22 [notice] 1#1: start worker processes
backend-1   | Aplikacja uruchomiona: 2025-05-29T12:05:22.864Z
frontend-1  | 2025/05/29 12:05:22 [notice] 1#1: start worker process 29
backend-1   | Autor: Przemysław Romaniak
frontend-1  | 2025/05/29 12:05:22 [notice] 1#1: start worker process 30
backend-1   | Nasłuchiwanie na porcie: 3000
frontend-1  | 2025/05/29 12:05:22 [notice] 1#1: start worker process 31
backend-1   | App running on port 3000
frontend-1  | 2025/05/29 12:05:22 [notice] 1#1: start worker process 32
frontend-1  | 2025/05/29 12:05:22 [notice] 1#1: start worker process 33
frontend-1  | 2025/05/29 12:05:22 [notice] 1#1: start worker process 34
frontend-1  | 2025/05/29 12:05:22 [notice] 1#1: start worker process 35
frontend-1  | 2025/05/29 12:05:22 [notice] 1#1: start worker process 36
frontend-1  | 2025/05/29 12:05:22 [notice] 1#1: start worker process 37
frontend-1  | 2025/05/29 12:05:22 [notice] 1#1: start worker process 38
frontend-1  | 2025/05/29 12:05:22 [notice] 1#1: start worker process 39
frontend-1  | 2025/05/29 12:05:22 [notice] 1#1: start worker process 40
frontend-1  | 172.20.0.1 - - [29/May/2025:12:05:37 +0000] "GET / HTTP/1.1" 304 0 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:138.0) Gecko/20100101 Firefox/138.0" "-"
frontend-1  | 172.20.0.1 - - [29/May/2025:12:05:37 +0000] "GET /style.css HTTP/1.1" 304 0 "http://localhost:8080/" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:138.0) Gecko/20100101 Firefox/138.0" "-"
frontend-1  | 172.20.0.1 - - [29/May/2025:12:05:40 +0000] "GET /api/weather?city=Siedlce HTTP/1.1" 200 769 "http://localhost:8080/" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:138.0) Gecko/20100101 Firefox/138.0" "-"

![obraz](https://github.com/user-attachments/assets/936ef25c-770c-44c4-9f66-67d0d4b3f6b8)

