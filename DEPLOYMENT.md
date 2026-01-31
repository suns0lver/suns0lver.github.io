# Deployment Guide

Step-by-step instructions for getting suns0lver.github.io live.

---

## Phase 1: GitHub Setup (10 minutes)

### 1. Create GitHub Organization

1. Go to https://github.com/organizations/plan
2. Choose "Create a free organization"
3. Name: `suns0lver`
4. Contact email: [your email]
5. Organization type: "My personal account"
6. Complete setup

### 2. Create Repository

1. In the `suns0lver` organization, click "New repository"
2. Repository name: **`suns0lver.github.io`** (exact name required)
3. Description: "Build systems that endure — long-horizon regenerative infrastructure"
4. Public repository
5. **Do NOT initialize with README** (we'll push our own)
6. Click "Create repository"

### 3. Configure Repository Settings

1. Go to Settings → General
2. **Features:**
   - ✅ Enable Issues
   - ✅ Enable Discussions (optional but recommended)
   - ✅ Enable Wikis (optional)
3. **Pull Requests:**
   - ✅ Allow merge commits
   - ✅ Allow squash merging
   - ✅ Automatically delete head branches
4. **Security:**
   - Go to Settings → Security → Code security and analysis
   - ✅ Enable Dependency graph
   - ✅ Enable Dependabot alerts

### 4. Enable GitHub Pages

1. Go to Settings → Pages
2. **Source:** Deploy from a branch
3. **Branch:** `main` (or `master`)
4. **Folder:** `/ (root)`
5. Click Save
6. Site will be live at `https://suns0lver.github.io` in ~1 minute

---

## Phase 2: Local Setup (5 minutes)

### 1. Clone the Repository

```bash
git clone https://github.com/suns0lver/suns0lver.github.io.git
cd suns0lver.github.io
```

### 2. Copy All Files

Copy everything from the suns0lver-repo folder into your cloned repository.

### 3. Initial Commit

```bash
git add .
git commit -m "Initial commit: suns0lver portal v0.1.0"
git push origin main
```

### 4. Verify Deployment

- Wait ~1-2 minutes
- Visit https://suns0lver.github.io
- Site should be live

---

## Phase 3: Cloudflare Setup (15 minutes) [OPTIONAL]

### Why Add Cloudflare?

- Free SSL/TLS
- DDoS protection
- Global CDN
- Web Application Firewall (WAF)
- Analytics without tracking cookies

### 1. Buy Domain (Optional)

If you want a custom domain:
1. Go to Porkbun, Namecheap, or Google Domains
2. Search for `suns0lver.org` (or `.com`, `.io`)
3. Purchase (~$8-15/year)

**Skip this if staying on suns0lver.github.io**

### 2. Add Site to Cloudflare

1. Go to https://dash.cloudflare.com
2. Click "Add site"
3. Enter: `suns0lver.org` (if you bought a domain)
4. Choose "Free" plan
5. Cloudflare will scan DNS records
6. Click "Continue"

### 3. Update Nameservers

1. Cloudflare will give you 2 nameservers (e.g., `ns1.cloudflare.com`)
2. Go to your domain registrar (Porkbun/Namecheap)
3. Update nameservers to Cloudflare's
4. Wait 5-60 minutes for propagation

### 4. Configure DNS

In Cloudflare DNS settings:

```
Type    Name    Content                      Proxy status
----    ----    -------                      ------------
CNAME   @       suns0lver.github.io          Proxied (orange)
CNAME   www     suns0lver.github.io          Proxied (orange)
```

### 5. Enable Security Features

**SSL/TLS:**
- Go to SSL/TLS → Overview
- Set to "Full (strict)"

**Security:**
- Go to Security → Settings
- ✅ Enable "Bot Fight Mode"
- ✅ Enable "Challenge Passage" (1 hour)
- Set Security Level to "Medium"

**Firewall:**
- Go to Security → WAF
- ✅ Enable "OWASP Core Ruleset"

**Speed:**
- Go to Speed → Optimization
- ✅ Enable Auto Minify (JavaScript, CSS, HTML)
- ✅ Enable Brotli compression

### 6. Update GitHub Pages

1. Go to GitHub → Settings → Pages
2. Custom domain: `suns0lver.org`
3. ✅ Enforce HTTPS
4. Save

---

## Phase 4: Final Configuration (10 minutes)

### 1. Update Placeholder Content

Edit these files and add real data:

**index.html:**
- Crypto addresses (search for `[BTC address will be inserted here]`)
- Stripe payment link (search for `href="#"` in "Contribute with Card" button)

**data/status.json:**
- Update `last_updated` timestamp
- Update contribution counts as they happen

**SECURITY.md:**
- Add security contact email

### 2. Test All Links

Visit your site and click every link. Make sure:
- Internal links work
- External links open
- Forms/buttons have proper destinations

### 3. Set Up Git Signing (Security Best Practice)

```bash
# Generate GPG key
gpg --full-generate-key

# List keys
gpg --list-secret-keys --keyid-format=long

# Export public key
gpg --armor --export YOUR_KEY_ID

# Add to GitHub
# Go to Settings → SSH and GPG keys → New GPG key
# Paste your public key

# Configure git to sign commits
git config --global user.signingkey YOUR_KEY_ID
git config --global commit.gpgsign true
```

### 4. Enable Branch Protection

1. Go to Settings → Branches
2. Add rule for `main` branch
3. ✅ Require pull request reviews before merging
4. ✅ Require status checks to pass
5. ✅ Require signed commits (if GPG set up)
6. Save changes

---

## Phase 5: Announce (When Ready)

### Pre-Launch Checklist

- [ ] All crypto addresses updated
- [ ] Payment link working
- [ ] All internal links work
- [ ] Mobile responsive test passed
- [ ] Security headers verified (check with securityheaders.com)
- [ ] GPG signing enabled
- [ ] Branch protection active

### Launch Announcement

Share on:
- GitHub Discussions (create "Announcements" category)
- HN (Show HN: Building non-extractive regenerative infrastructure)
- Relevant subreddits (with permission)
- Personal networks

---

## Maintenance

### Updating Content

```bash
# Make changes locally
git add .
git commit -S -m "Update: [description]"
git push origin main

# GitHub Pages auto-deploys in ~1 minute
```

### Updating status.json

When contributions happen:
1. Edit `/data/status.json`
2. Update counts, dates, progress
3. Commit and push
4. JavaScript on index.html will read new data

### Adding New Wish List Items

1. Create new file in `/wishlist/item-name.html`
2. Add entry to `/data/wishlist.json`
3. Link from `/wishlist/index.html`

---

## Troubleshooting

**Site not loading:**
- Check GitHub Pages settings (Settings → Pages)
- Verify branch is set to `main`
- Check GitHub Actions for build errors

**Custom domain not working:**
- Verify DNS propagation (use dnschecker.org)
- Check Cloudflare DNS settings
- Ensure GitHub Pages has custom domain set
- Wait up to 24 hours for full propagation

**SSL errors:**
- In Cloudflare: SSL/TLS → "Full (strict)"
- In GitHub Pages: ✅ Enforce HTTPS

**Need help?**
- Open an issue: https://github.com/suns0lver/suns0lver.github.io/issues
- Check GitHub Pages docs: https://docs.github.com/en/pages

---

**You're building infrastructure that will outlast platforms. Take your time. Do it right.**

**♾️**
