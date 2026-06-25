# psihic-sportiv.ro

Site de prezentare + blog pentru psiholog sportiv. Un singur fișier `index.html` (HTML/CSS/JS), fără build.

## Fișiere
- `index.html` — site-ul complet
- `logo.svg` — logo (creier + wordmark)
- `.nojekyll` — spune GitHub Pages să servească fișierele ca atare
- `CNAME` — (opțional) domeniul personalizat; vezi mai jos

---

## Varianta 1 — direct din browser (cel mai simplu)

1. Cont pe https://github.com (gratuit), apoi **New repository**.
2. Nume repo: `psihic-sportiv` · Public · **Create repository**.
3. **Add file → Upload files** → trage aici `index.html`, `logo.svg`, `.nojekyll` → **Commit changes**.
4. **Settings → Pages** → la *Source* alege **Deploy from a branch** → branch `main` → folder `/ (root)` → **Save**.
5. După ~1 minut, site-ul e live la:
   `https://NUMELE-TAU.github.io/psihic-sportiv/`

## Varianta 2 — din terminal (git)

```bash
cd folderul-cu-fisierele
git init
git add .
git commit -m "Initial: site psihic-sportiv"
git branch -M main
git remote add origin https://github.com/NUMELE-TAU/psihic-sportiv.git
git push -u origin main
```
Apoi activează Pages ca la pașii 4–5 de mai sus.

---

## Domeniu personalizat (psihic-sportiv.ro) — opțional

GitHub Pages poate servi pe domeniul tău .ro:

1. Creează un fișier `CNAME` (fără extensie) cu o singură linie:
   ```
   psihic-sportiv.ro
   ```
   și urcă-l în repo (sau pune-l în câmpul *Custom domain* din Settings → Pages).
2. La registrar / DNS (ex. gazduire.net), adaugă:
   - **A** `@` → `185.199.108.153`
   - **A** `@` → `185.199.109.153`
   - **A** `@` → `185.199.110.153`
   - **A** `@` → `185.199.111.153`
   - **CNAME** `www` → `NUMELE-TAU.github.io`
3. În Settings → Pages bifează **Enforce HTTPS** (după ce DNS-ul se propagă, ~1–24h).

> Notă: dacă pui domeniul personalizat acum, ai grijă să nu-l folosești în paralel pe gazduire.net pentru WordPress — alegi un singur loc unde „pointează" domeniul la un moment dat.
