# Requirements
Add a `.env` file with the following fields in the same dir as `compose.yaml`:
```.env
# Base domain for services
BASE_DOMAIN=""

# (Optional) Defaults to "latest"
TRAEFIK_VERSION=""
# (Optional) Defaults to "latest"
HOMEPAGE_VERSION=""
# (Optional) Defaults to "latest"
CODER_VERSION=""

# Email for ACME
CF_DNS_CHALLENGE_ACME_EMAIL=""
# Cloudflare API Token with DNS:Edit Permission
CF_DNS_API_TOKEN=""
# Cloudflare API Token with Zone:Read Permission
CF_ZONE_API_TOKEN=""

# (Optional) PUID of user on host (check using `id $user` command) defaults to 1000
CODE_SERVER_PUID=""
# (Optional) PGID of user on host (check using `id $user` command) defaults to 1000
CODE_SERVER_PGID=""
# (Optional) Defaults to "Etc/UTC"
CODE_SERVER_TIMEZONE=""
# Web GUI password
CODE_SERVER_PASSWORD=""
# Password for sudo access
CODE_SERVER_SUDO_PASSWORD=""
```

# Usage
Run the following command on the dir where `compose.yaml` is located:
```bash
docker compose pull
docker compose up -d
```
