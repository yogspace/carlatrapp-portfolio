# carlatrapp.de

Live: https://carlatrapp.de


## Deployment

Push auf `main` → GitHub Actions ([`.github/workflows/deploy.yml`](.github/workflows/deploy.yml)) lädt `public/` per rsync auf den Hetzner-Server nach `/opt/apps/sites/carlatrapp.de`. Ausgeliefert wird es dort von Caddy (Repo `proxy`, siehe Server-Handbuch) — ohne eigenen Container.

Secrets im Repo: `HETZNER_HOST` (IPv4), `HETZNER_USER`, `HETZNER_SSH_KEY` (wie in den anderen Repos).
