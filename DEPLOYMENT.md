# Deployment Checklist & Instructions

## 🚀 Quick Deploy Guide

This site is configured for **GitHub Pages** with a custom domain. Follow these steps to deploy the improved site.

---

## ✅ Pre-Deployment Checklist

### 1. Content Verification
- [ ] Review all page content for accuracy
- [ ] Verify email addresses and contact information
- [ ] Check LinkedIn URL is correct
- [ ] Update any placeholder text
- [ ] Ensure dates are current

### 2. Asset Preparation
- [ ] Create PNG favicon images (see `ASSETS_NEEDED.md`)
- [ ] Upload favicons to `/assets/` directory
- [ ] Create Open Graph image for social sharing
- [ ] Optimize all images with TinyPNG or similar

### 3. Configuration Check
- [ ] Verify `_config.yml` has correct site URL
- [ ] Check `CNAME` file has correct domain
- [ ] Review `sitemap.xml` for all pages
- [ ] Verify `robots.txt` allows crawling

### 4. Testing
- [ ] Test all internal links
- [ ] Test all external links
- [ ] Verify navigation works on all pages
- [ ] Test mobile responsiveness
- [ ] Check intro screen dismissal works
- [ ] Test Space Invaders game loads
- [ ] Verify contact buttons work
- [ ] Test 404 page appears correctly

### 5. Code Quality
- [ ] No console errors in browser
- [ ] No 404s in network tab
- [ ] All images load correctly
- [ ] CSS renders properly
- [ ] JavaScript functions work

---

## 📋 Deployment Methods

### Method 1: Git Push (Recommended)

```bash
# Navigate to your repository
cd "c:/Users/mrmca/OneDrive/Documents/Dougs Website/dougdevops_portfolio_site (1)"

# Check status
git status

# Add all changes
git add .

# Commit with descriptive message
git commit -m "Major site improvements: SEO, accessibility, new pages, enhanced design"

# Push to GitHub
git push origin main
```

**Result:** GitHub Pages will automatically build and deploy your site in 1-2 minutes.

---

### Method 2: Manual Upload

If not using Git:

1. Zip the entire project directory
2. Upload to GitHub repository
3. Ensure GitHub Pages is enabled in repository settings
4. Wait for automatic build

---

### Method 3: Local Build + Deploy

```bash
# Install Jekyll (if not installed)
gem install bundler jekyll

# Navigate to project
cd "c:/Users/mrmca/OneDrive/Documents/Dougs Website/dougdevops_portfolio_site (1)"

# Build site
bundle exec jekyll build

# Output will be in _site/ directory
# Upload _site/ contents to any static hosting
```

---

## 🔧 GitHub Pages Configuration

### Repository Settings

1. Go to GitHub repository settings
2. Navigate to **Pages** section
3. Verify settings:
   - Source: `Deploy from branch`
   - Branch: `main` (or `master`)
   - Folder: `/ (root)`
   - Custom domain: `dougdevops.com`
   - Enforce HTTPS: ✅ Enabled

### DNS Configuration

Ensure your domain DNS is configured:

**A Records** (point to GitHub Pages):
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**CNAME Record** (if using www):
```
www.dougdevops.com → YOUR_USERNAME.github.io
```

---

## 🧪 Post-Deployment Testing

### Immediate Tests (within 5 minutes)

1. **Visit the live site:** `https://dougdevops.com`
2. **Test all pages:**
   - [ ] Home page loads
   - [ ] Projects page displays correctly
   - [ ] Resume page shows all content
   - [ ] About page renders
   - [ ] Contact page is accessible
   - [ ] Arcade (doom) page works
   - [ ] 404 page appears for invalid URLs

3. **Test navigation:**
   - [ ] All nav links work
   - [ ] Active page is highlighted
   - [ ] Footer links function

4. **Test responsive design:**
   - [ ] Open on mobile device
   - [ ] Test tablet view
   - [ ] Test desktop view
   - [ ] Verify touch targets work

### SEO Tests (within 1 hour)

1. **Meta Tags:**
   - [ ] View page source, check `<head>` section
   - [ ] Verify title tags on each page
   - [ ] Confirm meta descriptions are present
   - [ ] Check Open Graph tags exist

2. **Social Sharing Test:**
   - [ ] Share on LinkedIn - check preview
   - [ ] Share on Facebook - check preview
   - [ ] Share on Twitter - check preview

3. **Search Engine Tools:**
   - [ ] Submit to [Google Search Console](https://search.google.com/search-console)
   - [ ] Submit sitemap: `https://dougdevops.com/sitemap.xml`
   - [ ] Request indexing for main pages

### Performance Tests

1. **Google PageSpeed Insights:**
   - Visit: https://pagespeed.web.dev/
   - Test: `https://dougdevops.com`
   - Target: 90+ score on mobile and desktop

2. **GTmetrix:**
   - Visit: https://gtmetrix.com/
   - Analyze site performance
   - Review recommendations

3. **Lighthouse (Chrome DevTools):**
   ```
   1. Open site in Chrome
   2. Open DevTools (F12)
   3. Go to Lighthouse tab
   4. Run audit (Mobile & Desktop)
   ```

   **Target Scores:**
   - Performance: 90+
   - Accessibility: 95+
   - Best Practices: 90+
   - SEO: 95+

### Accessibility Tests

1. **Keyboard Navigation:**
   - [ ] Tab through all links
   - [ ] Test Skip to Content link
   - [ ] Use arrow keys, Enter, Space
   - [ ] Press Escape on intro screen

2. **Screen Reader Test:**
   - Windows: NVDA (free)
   - Mac: VoiceOver (built-in)
   - Test: Navigate through home page

3. **WAVE Tool:**
   - Visit: https://wave.webaim.org/
   - Analyze: `https://dougdevops.com`
   - Fix any errors reported

---

## 🐛 Troubleshooting

### Site Not Updating?

**Problem:** Changes don't appear on live site

**Solutions:**
1. Check GitHub Actions tab for build status
2. Clear browser cache (Ctrl+Shift+Delete)
3. Wait 2-5 minutes for CDN propagation
4. Force refresh (Ctrl+F5)
5. Check DNS propagation: https://www.whatsmydns.net/

### 404 Errors?

**Problem:** Pages show 404 error

**Solutions:**
1. Verify file extensions (.md files)
2. Check permalink in front matter
3. Ensure `_config.yml` is correct
4. Rebuild site locally to check for errors

### Images Not Loading?

**Problem:** Favicon or images don't display

**Solutions:**
1. Verify images exist in `/assets/` folder
2. Check file paths are correct (case-sensitive!)
3. Ensure images are pushed to GitHub
4. Check browser console for 404 errors

### CSS Not Applied?

**Problem:** Site looks unstyled

**Solutions:**
1. Verify `default.html` layout is being used
2. Check all pages have `layout: default` in front matter
3. Clear browser cache
4. Check browser console for errors

---

## 🔄 Update Workflow

### For Content Updates

```bash
# 1. Edit markdown files
# 2. Test locally (optional)
bundle exec jekyll serve

# 3. Commit and push
git add .
git commit -m "Update: [description]"
git push origin main
```

### For Adding New Pages

```bash
# 1. Create new .md file
# 2. Add front matter with layout: default
# 3. Add to navigation in _layouts/default.html
# 4. Add to sitemap.xml
# 5. Test locally
# 6. Commit and push
```

### For Design Changes

```bash
# 1. Edit _layouts/default.html
# 2. Test thoroughly locally
# 3. Backup previous version
# 4. Commit and push with detailed message
```

---

## 📊 Monitoring & Analytics

### Set Up Google Analytics (Optional)

1. Create GA4 property
2. Get tracking ID
3. Add to `_layouts/default.html` before `</head>`:
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

### Monitor Search Console

1. Verify site ownership
2. Submit sitemap
3. Monitor:
   - Indexing status
   - Search queries
   - Page performance
   - Mobile usability

---

## 🎯 Success Metrics

### Week 1:
- [ ] Site is live and accessible
- [ ] All pages load correctly
- [ ] No console errors
- [ ] Mobile responsive

### Week 2:
- [ ] Submitted to search engines
- [ ] Social sharing works
- [ ] Lighthouse score 90+
- [ ] Accessibility verified

### Month 1:
- [ ] Appearing in Google search
- [ ] LinkedIn shares look good
- [ ] Traffic analytics set up
- [ ] All features working

---

## 📞 Support Resources

### Jekyll Documentation
- Official Docs: https://jekyllrb.com/docs/
- GitHub Pages: https://docs.github.com/en/pages

### Testing Tools
- PageSpeed: https://pagespeed.web.dev/
- WAVE: https://wave.webaim.org/
- HTML Validator: https://validator.w3.org/

### Community
- Jekyll Forum: https://talk.jekyllrb.com/
- Stack Overflow: [jekyll] tag
- GitHub Issues: In your repository

---

## ✅ Final Checklist

Before announcing your site:

- [ ] All pages reviewed and accurate
- [ ] Contact information correct
- [ ] Images optimized and uploaded
- [ ] Mobile tested on real device
- [ ] Shared on LinkedIn/Twitter to test previews
- [ ] Google Search Console submitted
- [ ] Performance tested (90+ score)
- [ ] Accessibility tested (WAVE clean)
- [ ] Cross-browser tested (Chrome, Firefox, Safari)
- [ ] SSL certificate active (https://)

---

## 🎉 Go Live!

Once all checks pass:

1. Announce on LinkedIn
2. Update resume with website link
3. Add to email signature
4. Share with network
5. Monitor analytics

**Congratulations! Your professional portfolio is live! 🚀**

---

**Need Help?**
- Check `README.md` for technical details
- Review `IMPROVEMENTS_SUMMARY.md` for features
- See `ASSETS_NEEDED.md` for image requirements

**Last Updated:** January 2, 2026
