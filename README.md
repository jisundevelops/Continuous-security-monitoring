# Continuous Security Monitoring

A self-hosted external attack surface scanner. Give it a domain and it
checks DNS, email security, TLS, security headers, open ports, exposed
cloud assets, leaked secrets and known CVEs, then tracks the findings over
time with scheduled re-scans and alerts.

Built by Maruf Ahmed Jisun, Rabbe Hasan and Rakesh Bala Arnob.

## Features

- Passive and active scan modes (active scans need domain authorization)
- Scheduled monitoring and Slack/Teams alerts
- Findings register with status, assignee and notes
- Exposure score per scan
- CSV export

## Run with Docker

    docker compose -f docker-compose.singleimage.yml up -d --build

Open http://localhost:8000. First login is admin / admin; you will be
asked to change the password.

Before running, set SECRET_KEY, DB_PASSWORD and ALLOWED_HOSTS in
docker-compose.singleimage.yml. Serve it behind HTTPS if you expose it
beyond localhost.

## Responsible use

Only scan domains you own or have written permission to test.
