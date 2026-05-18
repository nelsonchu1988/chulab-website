# Chu Lab Website

Live at: https://nelsonchu1988.github.io/chulab-website (after setup below)
Custom domain: https://chulab.org (after DNS setup)

## Setup — 5 steps

### 1. Add your headshot
Save your photo as: `assets/images/nelson-chu.jpg`
(The site already references this path.)

### 2. Verify your email
In `index.html`, search for `nelson.chu@gu.se` and replace with your actual GU email address.

### 3. Push to GitHub
```bash
git init
git add .
git commit -m "Initial Chu Lab website"
git remote add origin https://github.com/nelsonchu1988/chulab-website.git
git push -u origin main
```

### 4. Enable GitHub Pages
- Go to your GitHub repo → Settings → Pages
- Source: Deploy from branch → `main` / `(root)`
- Click Save
- Site will be live at `https://nelsonchu1988.github.io/chulab-website` within ~1 minute

### 5. Add custom domain (optional, ~$12/year)
- Buy `chulab.org` at Namecheap or Porkbun
- In GitHub Pages settings, add custom domain: `chulab.org`
- In Namecheap DNS, add:
  - 4× A records pointing to GitHub IPs: 185.199.108.153 / .109.153 / .110.153 / .111.153
  - 1× CNAME: `www` → `nelsonchu1988.github.io`

## Updating content

Everything is in `index.html`. Sections are clearly labelled with comments:
- Publications: find `<!-- STM 2026 -->` etc.
- Videos: find `<!-- Add more videos here -->`
- Team members: find `<!-- ===== TEAM =====`

After editing, just `git add . && git commit -m "update" && git push` — GitHub Pages auto-deploys.
