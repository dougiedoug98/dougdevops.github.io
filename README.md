# Doug DevOps Portfolio Website

Professional portfolio website for Douglas Collins - Systems & Cybersecurity Engineer

## 🌐 Live Site
**URL:** [https://dougdevops.com](https://dougdevops.com)

## 📋 Overview
This is a Jekyll-based static site hosted on GitHub Pages, featuring a distinctive terminal/cyberpunk aesthetic with green-on-black theming. The site showcases professional experience, projects, and technical expertise in DevOps, cybersecurity, and IT infrastructure.

## 🎨 Design Features
- **Terminal Aesthetic:** Retro green-on-black color scheme with neon glow effects
- **Responsive Design:** Mobile-first approach with breakpoints for tablets and desktop
- **Accessibility:** WCAG 2.1 compliant with ARIA labels, keyboard navigation, and screen reader support
- **Performance:** Optimized loading with lazy images, resource hints, and minimal dependencies
- **SEO Optimized:** Complete meta tags, Open Graph, structured data, and sitemap

## 🛠️ Technology Stack
- **Static Site Generator:** Jekyll
- **Hosting:** GitHub Pages
- **Styling:** Custom CSS with CSS variables
- **JavaScript:** Vanilla JS (no frameworks)
- **Version Control:** Git

## 📁 Site Structure
```
/
├── _layouts/
│   └── default.html          # Master layout template
├── assets/
│   ├── favicon.svg           # Site favicon
│   └── (other assets)
├── index.md                  # Home page
├── about.md                  # About/Skills page
├── projects.md               # Projects showcase
├── resume.md                 # Professional resume
├── contact.md                # Contact information
├── doom.md                   # Retro arcade (Space Invaders)
├── 404.md                    # Custom 404 error page
├── _config.yml               # Jekyll configuration
├── site.webmanifest          # PWA manifest
├── robots.txt                # Search engine directives
├── sitemap.xml               # XML sitemap
└── CNAME                     # Custom domain configuration
```

## 🚀 Key Improvements (Latest Update)

### SEO & Discoverability
✅ Comprehensive meta tags (title, description, keywords)
✅ Open Graph tags for social media sharing
✅ Twitter Card metadata
✅ Structured data (JSON-LD) for search engines
✅ XML sitemap for search engine crawling
✅ robots.txt for crawler directives
✅ Canonical URLs to prevent duplicate content

### Accessibility
✅ ARIA labels and roles throughout
✅ Semantic HTML5 elements (nav, main, footer, article)
✅ Skip-to-content link for keyboard navigation
✅ Focus states for all interactive elements
✅ Screen reader-only text for context
✅ Reduced motion support for accessibility
✅ High contrast mode support
✅ Keyboard navigation (Escape to dismiss intro)

### Performance
✅ CSS variables for consistent theming
✅ Lazy loading for images
✅ Resource hints (preconnect, dns-prefetch)
✅ Minimal external dependencies
✅ Optimized animations with will-change
✅ Responsive images with loading="lazy"

### UX Improvements
✅ Smooth page transitions with fade-in animations
✅ Active page indicator in navigation
✅ External link indicators (open in new tab)
✅ Improved mobile responsiveness
✅ Better touch targets for mobile
✅ Footer with copyright and tech stack info
✅ Print-friendly styles for resume page

### Content Enhancements
✅ New Contact page with professional networks
✅ Enhanced Projects page with detailed case studies
✅ Improved Resume page with better formatting
✅ Enhanced Home page with core competencies
✅ Better About page structure
✅ Custom 404 error page

### Code Quality
✅ Organized CSS with logical sections
✅ JavaScript error handling and safety checks
✅ Improved code comments and documentation
✅ Modular JavaScript functions
✅ Consistent naming conventions

## 🎯 Pages Overview

### Home (`/`)
Welcome page with introduction, core competencies grid, and call-to-action buttons.

### Projects (`/projects`)
Detailed showcase of 4 major projects with objectives, technologies, and impact metrics.

### Resume (`/resume`)
Professional resume with work experience, technical skills grid, education, and achievements.

### About (`/about`)
Comprehensive overview of professional expertise across 7 major categories with technology logos.

### Contact (`/contact`)
Contact information, professional networks, availability status, and location details.

### Retro Arcade (`/doom`)
Interactive Space Invaders game embedded in the site for a fun easter egg.

### 404 Error (`/404.html`)
Custom error page with helpful navigation links.

## 🎨 Color Scheme
- **Primary:** `#00ff00` (Neon Green)
- **Background:** `#000000` (Black)
- **Accent:** `rgba(0, 255, 0, 0.05)` (Subtle green tint)

## 📱 Responsive Breakpoints
- **Mobile:** `< 480px`
- **Tablet:** `480px - 768px`
- **Desktop:** `768px - 1024px`
- **Large Desktop:** `> 1024px`

## 🔧 Local Development

### Prerequisites
- Ruby 2.7+
- Jekyll 4.0+
- Bundler

### Setup
```bash
# Install dependencies
bundle install

# Run local server
bundle exec jekyll serve

# Build for production
bundle exec jekyll build
```

### Testing
```bash
# Serve locally at http://localhost:4000
bundle exec jekyll serve --livereload

# Test build
bundle exec jekyll build --verbose
```

## 📦 Deployment
Site is automatically deployed to GitHub Pages on push to the `main` branch.

### Deployment Checklist
- [ ] Update sitemap.xml with new pages
- [ ] Verify all links work
- [ ] Test responsive design
- [ ] Check accessibility with screen reader
- [ ] Validate HTML/CSS
- [ ] Test performance with Lighthouse

## 🔒 Security Considerations
- All external links use `rel="noopener noreferrer"`
- No inline JavaScript event handlers
- Content Security Policy headers (configured at GitHub Pages level)
- Session storage used safely with error handling

## 📈 Analytics & Monitoring
Currently no analytics installed. To add:
- Google Analytics 4
- Cloudflare Analytics
- GitHub Pages traffic insights

## 🐛 Known Issues
None currently. Report issues via GitHub Issues.

## 📝 TODO / Future Enhancements
- [ ] Add blog/articles section
- [ ] Create downloadable PDF resume
- [ ] Add more games to arcade
- [ ] Implement dark/light mode toggle (currently terminal theme only)
- [ ] Add testimonials section
- [ ] Create OG image generator for social sharing
- [ ] Add RSS feed for blog posts

## 🤝 Contributing
This is a personal portfolio site. However, suggestions and feedback are welcome!

## 📄 License
All rights reserved © 2026 Douglas Collins

## 📬 Contact
- **Website:** [dougdevops.com](https://dougdevops.com)
- **LinkedIn:** [douglas-collins-04a895215](https://www.linkedin.com/in/douglas-collins-04a895215/)
- **Email:** contact@dougdevops.com

---

**Built with ❤️ using Jekyll and hosted on GitHub Pages**
