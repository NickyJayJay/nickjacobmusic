# nickjacobmusic.com

Single-page static hub for Nick Jacob — dual-audience: sync licensing (music supervisors) + direct fan listening/sales.

**Zero build step.** Plain HTML/CSS in `index.html`. Nothing to compile, no dependencies, no `npm install`. Edit the file, push, done.

## Files

| File | Purpose |
|------|---------|
| `index.html` | The entire site (inline CSS). |
| `favicon.svg` | Guitar-pick favicon in brand colors. |
| `_headers` | Cloudflare Pages caching/security headers. |

## Deploy — Cloudflare Pages

1. Push this repo to GitHub/GitLab.
2. Cloudflare dashboard → **Workers & Pages** → **Create** → **Pages** → **Connect to Git** → pick this repo.
3. Build settings:
   - **Framework preset:** `None`
   - **Build command:** *(leave empty)*
   - **Build output directory:** `/`
4. Save & Deploy.

### Custom domain

Pages → your project → **Custom domains** → **Set up a domain** → `nickjacobmusic.com` (and `www`).
Since the domain is already on Cloudflare, the CNAME/apex records are added automatically. Add `www` as a redirect to the apex if you want a canonical host.

## Design tokens (palette)

Defined as CSS variables at the top of `index.html`:

- Parchment bg `#f6f1e7` · espresso ink `#241d17` · muted `#6f6153`
- **"Old Blue" denim** `#2f4a5e` (nods to the Strat) · **rust/amber accent** `#c25a2b`
- SoundCloud player accent themed to rust: `color=%23c25a2b` in the iframe `src`.

## TODO before launch

- [ ] Optional: add a real social share image (`og:image` meta is present but no image is set).

## Phase 2 (deferred)

- Bandcamp link (none yet) — add a fourth `.stream-card`.
- Mailing-list signup — drop in an embed once a service is chosen (Buttondown / Mailchimp / etc.).
