# Help Desk Ticketing Lab (GLPI)

An IT service desk running in Docker with ticket categories, priorities, SLAs and a knowledge base, worked through 10 realistic tickets from logging to resolution.

## Start

```bash
docker compose up -d
```

Open http://localhost:8080. If the image asks for the database during setup, use host `db`,
user `glpi` and the password from `docker-compose.yml`. Change the default admin passwords
right after the first login. (Check the image's page on Docker Hub if the setup steps differ.)

## Configure

1. **Categories:** Hardware, Software, Network, Accounts & Access, Email, Printers.
2. **Priorities and SLAs:**

| Priority | Example | First response | Resolution |
| --- | --- | --- | --- |
| P1 Critical | Whole office has no internet | 15 min | 4 h |
| P2 High | Manager cannot access email | 30 min | 8 h |
| P3 Medium | Printer not working for one user | 4 h | 2 days |
| P4 Low | Request for new software | 1 day | 5 days |

3. **Tickets:** create the 10 sample tickets in `sample-tickets.md`, work each one
   (assign, add notes, change status, solve with a clear solution note).
4. **Knowledge base:** publish the articles in `kb/` in GLPI.
5. **Report:** export the ticket list and SLA status, and take screenshots.
