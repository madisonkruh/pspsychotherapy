# P.S. Psychotherapy

Website for P.S. Psychotherapy — Jordyn Brownstein-Howard, RP(Q).

## Structure

- `index.html` — page content
- `styles.css` — styling
- `script.js` — mobile nav + footer year
- `CNAME` — tells GitHub Pages to serve this repo at pspsychotherapy.com

## TODO before launch

- [ ] Buy the domain `pspsychotherapy.com` (see below)
- [ ] Swap the placeholder JaneApp link (`https://pspsychotherapy.janeapp.com`) for the real booking URL in `index.html` (appears 3 times)
- [ ] Swap the placeholder email (`hello@pspsychotherapy.com`) for a real inbox
- [ ] Add a real headshot photo, replacing `.photo-placeholder` in `index.html`/`styles.css`
- [ ] Double check credentials/bio text against current registration status

## Buying the domain

1. Go to a registrar (Namecheap, Google Domains successor Squarespace Domains, or Cloudflare Registrar — Cloudflare sells at cost, no markup).
2. Search `pspsychotherapy.com`, purchase.
3. In the registrar's DNS settings, add these records (GitHub Pages requires all four A records for the apex domain, plus a CNAME for `www`):

   | Type  | Host | Value |
   |-------|------|-------|
   | A     | @    | 185.199.108.153 |
   | A     | @    | 185.199.109.153 |
   | A     | @    | 185.199.110.153 |
   | A     | @    | 185.199.111.153 |
   | CNAME | www  | madisonkruh.github.io |

4. In the GitHub repo → Settings → Pages, set the custom domain to `pspsychotherapy.com` and enable "Enforce HTTPS" once it's available (can take a few hours after DNS propagates).

## Local preview

Open `index.html` directly in a browser, or run a local server:

```
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.
