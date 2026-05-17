# CICD — NestJS Boilerplate

NestJS loyihasi GitHub Actions CI/CD pipeline bilan.

## O'rnatish

```bash
npm install
```

## Ishga tushirish

```bash
# Development
npm run start:dev

# Production
npm run build
npm run start:prod
```

## GitHub Secrets

Settings → Secrets → Actions bo'limiga quyidagilarni qo'shing:

| Secret | Tavsif |
|---|---|
| `SERVER_HOST` | Serverning IP manzili |
| `SERVER_USER` | SSH foydalanuvchi nomi |
| `SERVER_SSH_KEY` | SSH private key |
| `SERVER_PORT` | SSH porti (odatda 22) |

## CI/CD Jarayon

`main` branchga push qilinganda:
1. Testlar ishga tushadi (lint + jest)
2. Loyiha build qilinadi
3. Serverga SSH orqali ko'chiriladi
4. pm2 orqali qayta ishga tushiriladi
