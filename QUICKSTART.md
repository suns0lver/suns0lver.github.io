# Quick Start Guide

Get suns0lver.github.io live in under 30 minutes.

---

## TL;DR

1. Create GitHub org: `suns0lver`
2. Create repo: `suns0lver.github.io` (public)
3. Clone repo locally
4. Copy all files from this folder into your repo
5. Update crypto addresses in `index.html`
6. Push to GitHub
7. Enable GitHub Pages (Settings → Pages → main branch)
8. Site live at https://suns0lver.github.io

---

## Essential Files to Update BEFORE Launch

### 1. index.html
**Line ~850+** — Replace crypto address placeholders:
```html
<!-- Find these sections and replace -->
<div class="crypto-address">[BTC address will be inserted here]</div>
<div class="crypto-address">[ETH address will be inserted here]</div>
<div class="crypto-address">[USDC-ETH address will be inserted here]</div>
<div class="crypto-address">[XRP address will be inserted here]</div>
```

### 2. SECURITY.md
**Line ~22** — Add your security contact:
```markdown
- Email: [security contact will be added]
```

### 3. data/status.json
**Line 3** — Update timestamp:
```json
"last_updated": "2025-01-31T00:00:00Z"
```

---

## Post-Launch Updates (Do These As You Go)

### When First Contribution Received

**Update these files:**

1. `data/status.json`:
   - Increment `contributions.coin.total_count`
   - Update `contributions.coin.total_value_usd`

2. `data/contributions.json`:
   - Add entry to `contributions` array
   - Update summary counts

3. `data/wishlist.json`:
   - Update `funding.raised` for relevant item
   - Add contributor to `funding.contributors` (if permitted)

4. `index.html`:
   - Update progress bar percentage
   - Update progress text

### When First PR Merged

**Update these files:**

1. `data/status.json`:
   - Increment `contributions.code.merged_prs`

2. `data/contributions.json`:
   - Add entry with PR link and contributor

3. `data/pcd.json`:
   - Update PCD-002 status to "complete"
   - Fill in evidence checklist

---

## File Structure at a Glance

```
Essential:
├── index.html              ← Main landing page
├── README.md               ← GitHub landing
└── data/
    ├── status.json         ← Machine-readable state
    ├── wishlist.json       ← Tool wish lists
    ├── contributions.json  ← Contribution log
    └── pcd.json            ← Proof-of-concept tracking

Configuration:
├── SECURITY.md             ← Security policy
├── CODE_OF_CONDUCT.md      ← Minimal conduct guide
├── robots.txt              ← Crawler rules
└── _headers                ← Security headers

Documentation:
├── DEPLOYMENT.md           ← Full setup guide
└── QUICKSTART.md           ← This file
```

---

## Testing Before Launch

1. **Local preview:**
   ```bash
   python3 -m http.server 8000
   # Visit http://localhost:8000
   ```

2. **Check all links work**
3. **Verify crypto addresses are correct** (send a test transaction if possible)
4. **Test mobile responsiveness**
5. **Run security header check:** https://securityheaders.com

---

## First Day Checklist

After site goes live:

- [ ] Share link with close network for feedback
- [ ] Monitor GitHub Issues for questions
- [ ] Test contribution flow (crypto or Stripe)
- [ ] Document any bugs or issues
- [ ] Update status.json with accurate data
- [ ] Set up branch protection rules
- [ ] Enable GPG commit signing

---

## Need Help?

- **Full deployment guide:** See DEPLOYMENT.md
- **GitHub issues:** https://github.com/suns0lver/suns0lver.github.io/issues
- **GitHub Pages docs:** https://docs.github.com/en/pages

---

**Remember: This is infrastructure. It doesn't need to be perfect on day one. Ship it, iterate, improve.**

**♾️**
