# Docker Compose Guide

1. **What does the `services:` block do?**
   - It defines each container/service that will run — in this case, the database (`db`) and the web application (`app`).

2. **How does the `app` container know where to find the database?**
   - Through the environment variable `MYSQL_HOST=db`. Docker has its own internal DNS system, so the service name `db` resolves automatically to the database container.

3. **Difference between `docker compose up` and `docker compose up -d`**
   - `docker compose up` — runs in the foreground; logs appear in the terminal and you cannot use it until stopped.
   - `docker compose up -d` — runs in detached/background mode; the terminal is immediately available for other commands.

4. **Difference between `docker compose stop` and `docker compose down`**
   - `docker compose stop` — only stops the containers; they are not deleted.
   - `docker compose down` — stops AND removes containers, networks, and other resources created by Compose.
