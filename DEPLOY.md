# Deploy to GitHub Pages

## Steps

1. Create a GitHub repo (e.g. `tonpilote-landing`)

2. Push the landing-page files:
   ```bash
   cd landing-page
   git init
   git add .
   git commit -m "Landing page for Forum IA 2026"
   git branch -M main
   git remote add origin git@github.com:YOUR_USERNAME/tonpilote-landing.git
   git push -u origin main
   ```

3. Enable GitHub Pages:
   - Go to repo Settings → Pages
   - Source: Deploy from a branch
   - Branch: main, folder: / (root)
   - Save

4. Configure custom domain on GitHub:
   - In the same Pages settings, enter: `tonpilote.fr`
   - Check "Enforce HTTPS"

5. Configure DNS on IONOS:
   - Go to IONOS → Domains → tonpilote.fr → DNS settings
   - Add these records:

   | Type | Name | Value |
   |---|---|---|
   | A | @ | 185.199.108.153 |
   | A | @ | 185.199.109.153 |
   | A | @ | 185.199.110.153 |
   | A | @ | 185.199.111.153 |
   | CNAME | www | YOUR_USERNAME.github.io |

6. Wait 10-30 minutes for DNS propagation

7. Test: https://tonpilote.fr

## TODO before going live

- [ ] Replace email placeholder in index.html
- [ ] Replace phone number placeholder in index.html
- [ ] Update CNAME file if domain name changes
- [ ] Test on mobile
