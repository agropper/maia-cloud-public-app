# maia-cloud-public-app

Public demo app for MAIA (Medical AI Assistant) - `public.agropper.xyz`

## Purpose

Simplified public-facing app for demoing MAIA features without authentication. Supports deep links for viewing shared chats.

## Features

- **Demo chat**: Pre-seeded demo knowledge base and agent
- **Deep link viewer**: View shared chats via deeplink URLs
- **No authentication**: Public access only, no passkeys
- **Clean architecture**: < 5,000 lines total, minimal backend

## Configuration

`.env`:
```
DOMAIN=public.agropper.xyz
CLOUDANT_URL=https://...
DIGITALOCEAN_TOKEN=...
SPACES_KEY=...
RESEND_KEY=...
# NO PASSKEY CONFIG
```

## Architecture

- **Frontend**: Vue 3 + Quasar + Vite
- **Backend**: Express.js minimal API server
- **Libraries**: Uses `lib-maia-do-client`, `lib-maia-cloudant` (no passkey)
- **Storage**: DigitalOcean Spaces (read-only)
- **Database**: Cloudant (for shared chat logs, deeplink data)

## Development

### Setup
```bash
npm install
npm link ../lib-maia-do-client
npm link ../lib-maia-cloudant
npm run dev
```

### Build
```bash
npm run build
npm start
```

## Status

🚧 In Progress - Initial structure only

