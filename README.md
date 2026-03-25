<!-- BlackRoad SEO Enhanced -->

# curb

> Part of **[BlackRoad OS](https://blackroad.io)** — Sovereign Computing for Everyone

[![BlackRoad OS](https://img.shields.io/badge/BlackRoad-OS-ff1d6c?style=for-the-badge)](https://blackroad.io)
[![BlackRoad-OS-Inc](https://img.shields.io/badge/Org-BlackRoad-OS-Inc-2979ff?style=for-the-badge)](https://github.com/BlackRoad-OS-Inc)

**curb** is part of the **BlackRoad OS** ecosystem — a sovereign, distributed operating system built on edge computing, local AI, and mesh networking by **BlackRoad OS, Inc.**

### BlackRoad Ecosystem
| Org | Focus |
|---|---|
| [BlackRoad OS](https://github.com/BlackRoad-OS) | Core platform |
| [BlackRoad OS, Inc.](https://github.com/BlackRoad-OS-Inc) | Corporate |
| [BlackRoad AI](https://github.com/BlackRoad-AI) | AI/ML |
| [BlackRoad Hardware](https://github.com/BlackRoad-Hardware) | Edge hardware |
| [BlackRoad Security](https://github.com/BlackRoad-Security) | Cybersecurity |
| [BlackRoad Quantum](https://github.com/BlackRoad-Quantum) | Quantum computing |
| [BlackRoad Agents](https://github.com/BlackRoad-Agents) | AI agents |
| [BlackRoad Network](https://github.com/BlackRoad-Network) | Mesh networking |

**Website**: [blackroad.io](https://blackroad.io) | **Chat**: [chat.blackroad.io](https://chat.blackroad.io) | **Search**: [search.blackroad.io](https://search.blackroad.io)

---


> Curb — Sovereign object storage. BlackRoad fork of MinIO. S3-compatible CDN on Pi hardware.

Part of the [BlackRoad OS](https://blackroad.io) ecosystem — [BlackRoad-OS-Inc](https://github.com/BlackRoad-OS-Inc)

---

# Curb — BlackRoad Road Fleet

> **Sovereign object storage.** Fork of [MinIO](https://github.com/minio/minio).

---

**Curb** is BlackRoad's sovereign fork of MinIO — S3-compatible object storage running on Pi hardware. CDN, backups, assets, and media — all self-hosted.

## What's Different

- **Pi-optimized** — tuned for ARM64, 8GB RAM, SD/USB storage
- **Fleet CDN** — serves images.blackroad.io, cdn.blackroad.io
- **4 buckets** — blackroad-assets, blackroad-backups, blackroad-media, blackroad-uploads
- **R2 replacement** — migrating from Cloudflare R2 to self-hosted Curb

## Deployment

```bash
# On Cecilia (primary storage node)
minio server /data --address :9000 --console-address :9001
```

## Current Storage

| Bucket | Size | Contents |
|--------|------|----------|
| blackroad-assets | 120MB | Pixel art, logos, brand kit |
| blackroad-backups | 2GB+ | Pi fleet backups |
| blackroad-media | 500MB | Videos, audio, images |
| blackroad-uploads | 100MB | User uploads |

## Fleet Access

- **S3 API**: `http://cecilia:9000`
- **Console**: `http://cecilia:9001`
- **CDN**: `https://images.blackroad.io` → Gematria → WireGuard → Cecilia

## Upstream

Forked from [minio/minio](https://github.com/minio/minio) (AGPL v3 upstream).
All BlackRoad modifications are proprietary.

---

**BlackRoad OS, Inc.** — Pave Tomorrow.

*Proprietary. All rights reserved.*
