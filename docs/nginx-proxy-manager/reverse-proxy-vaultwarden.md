# Reverse Proxy Configuration - Vaultwarden

## Overview

This document outlines the configuration of Nginx Proxy Manager as a reverse proxy for the Vaultwarden password manager running in Docker on the Ubuntu Docker VM.

The purpose of this configuration is to:

- Route incoming HTTP/HTTPS requests to Vaultwarden
- Provide a central location for future SSL certificate management
- Prepare the homelab for hosting multiple self-hosted services under a single reverse proxy

---

## Environment

| Component | Value |
|-----------|-------|
| Hypervisor | Proxmox VE |
| VM | Ubuntu Server Docker Host |
| Service | Vaultwarden |
| Reverse Proxy | Nginx Proxy Manager |
| Container Platform | Docker Compose |

---

## Reverse Proxy Configuration

### Domain

```
vaultwarden.local
```

(***I may change this***)

### Forward Host

```
vaultwarden
```

### Forward Port

```
80
```

### Scheme

```
http
```

### SSL

Not configured yet.

---

## Screenshot

<img width="707" height="711" alt="Screenshot 2026-07-07 215835" src="https://github.com/user-attachments/assets/1fc973ef-5e1e-4485-8457-d0ce67ec10ae" />


---

## Verification

Verified the following:

- Reverse proxy created successfully
- Configuration saved without errors
- Nginx Proxy Manager resolves the Vaultwarden container
- Vaultwarden accessible through the configured proxy

---

## Notes

Current deployment is internal to the homelab.

Future enhancements include:

- Let's Encrypt certificates
- HTTPS enforcement
- HSTS
- External DNS integration
- Wildcard certificates
- Cloudflare Tunnel (planned)

---

## Lessons Learned

- Nginx Proxy Manager greatly simplifies reverse proxy management compared to manual Nginx configuration.
- Docker containers communicate using Docker networking rather than IP addresses.
- Forwarding traffic by container name makes configurations easier to maintain.

---

## References

- https://nginxproxymanager.com/
- https://github.com/dani-garcia/vaultwarden
