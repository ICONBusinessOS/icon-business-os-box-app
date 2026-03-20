# ICON BusinessOS — Box Integration

> Operations intelligence for Box. Monitor document collaboration health, storage utilization, and security posture from within the ICON BusinessOS platform.

## Features

- **Document Operations Score**: storage utilization, collaboration health, sharing audit
- **Collaboration Intelligence**: co-edit frequency, comment velocity, task completion rate
- **Security Posture**: external sharing audit, link expiration compliance, download tracking
- **Storage Analytics**: growth trend, file type distribution, stale document detection

## Box API Endpoints Used

| Endpoint | Signal |
|----------|--------|
| `GET /2.0/users/me` | Account health, storage quota |
| `GET /2.0/folders/0` | Root folder structure |
| `GET /2.0/events` | Activity feed (uploads, downloads, shares) |
| `GET /2.0/collaborations` | Collaboration health |
| `GET /2.0/shared_links` | External sharing audit |

## Setup

1. Create app at https://developer.box.com/
2. Auth: OAuth 2.0 with User Authentication
3. Scopes: `root_readwrite`, `manage_managed_users`
4. Redirect URI: `https://os.theicon.ai/api/oauth/box/callback`
5. Connect via ICON BusinessOS dashboard

## Requirements
- Box Business plan or higher (for admin API access)
- OAuth 2.0 app approval from Box admin

## License
MIT
