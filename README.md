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
