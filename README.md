# Requirements
Add a `.env` file with the following fields in the same dir as `compose.yaml`:
```.env
# Base domain for services
BASE_DOMAIN=""

# (Optional) Defaults to "latest"
TRAEFIK_VERSION=""
# (Optional) Defaults to "latest"
HOMEPAGE_VERSION=""

# Email for ACME
CF_DNS_CHALLENGE_ACME_EMAIL=""
# Cloudflare API Token with DNS:Edit Permission
CF_DNS_API_TOKEN=""
# Cloudflare API Token with Zone:Read Permission
CF_ZONE_API_TOKEN=""
```

# Usage
Run the following command on the dir where `compose.yaml` is located:
```bash
docker compose pull
docker compose up -d --remove-orphans
```
