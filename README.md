# Bhuvexa Consultancy — Website

Single-page site for Bhuvexa Consultancy (Kolhapur, Maharashtra). Static HTML, no build step required.

- `index.html` — the full site
- `CNAME` — tells GitHub Pages to serve this repo at **bhuvexa.com** (leave this file as-is)

## 1. Create the GitHub repo

1. Go to https://github.com/new
2. Repository name: `bhuvexa` (or whatever you prefer)
3. Keep it **Public** (required for free GitHub Pages)
4. Don't initialize with a README/gitignore — this folder already has one
5. Click **Create repository**

## 2. Push this folder

Open a terminal in this folder and run:

```bash
git init
git add .
git commit -m "Initial Bhuvexa website"
git branch -M main
git remote add origin https://github.com/<your-username>/bhuvexa.git
git push -u origin main
```

Replace `<your-username>` with your GitHub username.

## 3. Turn on GitHub Pages

1. In the repo, go to **Settings → Pages**
2. Under **Build and deployment → Source**, choose **Deploy from a branch**
3. Branch: `main`, folder: `/ (root)` → **Save**
4. Under **Custom domain**, enter `bhuvexa.com` and save (this reads the `CNAME` file already in the repo)
5. Check **Enforce HTTPS** once it becomes available (can take a few minutes after DNS is verified)

## 4. Point your domain at GitHub Pages

At your domain registrar (wherever you bought bhuvexa.com), set these DNS records:

**Apex domain (`bhuvexa.com`)** — four A records, all pointing to GitHub's Pages IPs:

```
A    @    185.199.108.153
A    @    185.199.109.153
A    @    185.199.110.153
A    @    185.199.111.153
```

**`www.bhuvexa.com`** (optional but recommended, so both work) — one CNAME record:

```
CNAME    www    <your-username>.github.io
```

DNS changes can take anywhere from a few minutes to ~24 hours to propagate. Once it resolves, GitHub will auto-issue an SSL certificate and the site will be live at `https://bhuvexa.com`.

## Making future edits

Edit `index.html`, then:

```bash
git add .
git commit -m "Update site"
git push
```

GitHub Pages redeploys automatically within a minute or two of every push.
