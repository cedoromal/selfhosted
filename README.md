# Requirements
Add a `.env` file with the following fields in the same dir as `compose.yaml`:
```.env
# Base domain for services
BASE_DOMAIN=""

# (Optional) Defaults to "latest"
TRAEFIK_TAG=""
# (Optional) Defaults to "latest"
DOCKER_SOCKET_PROXY_TAG=""
# (Optional) Defaults to "latest"
HOMEPAGE_TAG=""
# (Optional) Defaults to "latest"
REDBOT_TAG=""

# Email for ACME
CF_DNS_CHALLENGE_ACME_EMAIL=""
# Cloudflare API Token with DNS:Edit Permission
CF_DNS_API_TOKEN=""
# Cloudflare API Token with Zone:Read Permission
CF_ZONE_API_TOKEN=""

# Discord bot token (get from https://discord.com/developers)
REDBOT_DISCORD_TOKEN=""
# RedBot prefix
REDBOT_PREFIX=""
# (Optional) Defaults to "Etc/UTC"
REDBOT_TIMEZONE=""
# (Optional) User PUID from host (get from `id $user` command) - defaults to 1000
REDBOT_PUID=""
```

# Usage
Run the following command on the dir where `compose.yaml` is located:
```bash
docker compose pull
docker compose up -d --remove-orphans
```
