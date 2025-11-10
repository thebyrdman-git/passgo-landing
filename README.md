# PassGo Landing Page

**Coming Soon** page for passgo.app

Hosted on GitHub Pages.

## DNS Configuration (Cloudflare)

### For passgo.app (apex domain):

Add **4 A records** pointing to GitHub Pages:

| Type | Name | Content | Proxy Status | TTL |
|------|------|---------|--------------|-----|
| `A` | `@` | `185.199.108.153` | DNS only (grey cloud) | Auto |
| `A` | `@` | `185.199.109.153` | DNS only (grey cloud) | Auto |
| `A` | `@` | `185.199.110.153` | DNS only (grey cloud) | Auto |
| `A` | `@` | `185.199.111.153` | DNS only (grey cloud) | Auto |

### For www.passgo.app (optional):

| Type | Name | Content | Proxy Status | TTL |
|------|------|---------|--------------|-----|
| `CNAME` | `www` | `ansaico.github.io` | DNS only (grey cloud) | Auto |

## GitHub Pages Setup

1. Create repository: `passgo-landing` (or similar)
2. Push this code to `main` branch
3. Go to Settings → Pages
4. Set source to `main` branch
5. Add custom domain: `passgo.app`
6. Wait for DNS check to pass
7. Enable HTTPS (automatic after DNS propagates)

## Files

- `index.html` - Main landing page
- `CNAME` - Custom domain file (required for GitHub Pages)
- `README.md` - This file

## Local Development

```bash
# Serve locally
python3 -m http.server 8000

# Visit: http://localhost:8000
```

## Deployment

```bash
git add .
git commit -m "Update landing page"
git push origin main
```

GitHub Pages will automatically deploy within 1-2 minutes.

