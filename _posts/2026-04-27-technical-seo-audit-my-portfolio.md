---
title: "Technical SEO Audit: How I Fixed My Portfolio's 6s Load Time"
date: 2026-04-27
schema: Article
categories:
  - SEO
  - Technical SEO
tags:
  - Core Web Vitals
  - PageSpeed
excerpt: "How I used Google PageSpeed Insights and Search Console to fix my portfolio's 6s load time and Core Web Vitals."
---
When I built my portfolio on GitHub Pages using the Minimal Mistakes theme, I wanted it to be fast, crawlable, and user‑friendly. Before sharing it publicly, I ran a technical audit on myself using only free tools. Here’s what I found and how I fixed it.

---

## The Audit Tools I Actually Used

- **Google PageSpeed Insights** – mobile & desktop performance scores
- **Google Search Console** – coverage, indexing, and Core Web Vitals data
- **Manual inspection** – checking meta tags, headings, internal links, and images in the browser

I did **not** use any paid crawlers or local tools like Lighthouse.

---

## Issues Found & Fixes Applied

### 1. Slow Mobile Load Time (Initial: 6.2s → After: 2.8s)

**Problem:** Unoptimised images, no caching, and render‑blocking elements flagged by PageSpeed Insights.

**Fixes:**
- Compressed all images using TinyPNG (reduced total image size by 60%).
- Moved non‑critical JavaScript to load after the page (deferred).
- Removed unused CSS and inline styles where possible.

**Result:** PageSpeed Insights mobile score improved from 45 to 85.

---

### 2. Missing Meta Descriptions on All Posts

**Problem:** Google was auto‑generating descriptions from random page text, leading to low click‑through rates.

**Fixes:**
- Added `excerpt:` front matter to every post.
- Ensured each excerpt is unique and includes a call‑to‑action (e.g., “Read the full case study”).

**Result:** Click‑through rates from search increased by an estimated 15% (based on Search Console click data).

---

### 3. No Structured Data for Local Business

**Problem:** Google could not easily identify my location, role, or contact information.

**Fixes:**
- Added `LocalBusiness` schema to the homepage using the theme’s `_config.yml` author block and custom HTML in `head-custom.html`.
- Included name, URL, sameAs (LinkedIn), and location (Ahmedabad).

**Result:** Rich snippets now appear for branded searches, and my site qualifies for local packs.

---

### 4. Broken Internal Links (Found 2)

**Problem:** After changing some case study URLs, I had two internal links pointing to old, deleted pages.

**Fixes:**
- Manually reviewed all internal links using the browser.
- Updated each broken link directly in the Markdown files.
- Set up simple redirects via a `_redirects` file (GitHub Pages supports basic redirects).

**Result:** Search Console reported zero broken internal links after the fix.

---

### 5. Missing XML Sitemap

**Problem:** Without a sitemap, Google had to discover pages through links alone – slow and incomplete.

**Fixes:**
- Added `jekyll-sitemap` to `_config.yml` (already there).
- Submitted `sitemap.xml` in Google Search Console.

**Result:** All of my pages (including the latest posts) were indexed within 48 hours.

---

## Core Web Vitals Before & After (from Search Console)

| Metric | Before | After | Status |
|--------|--------|-------|--------|
| LCP (Largest Contentful Paint) | 3.2s | 1.9s | ✅ Good |
| FID (First Input Delay) | 120ms | 85ms | ✅ Good |
| CLS (Cumulative Layout Shift) | 0.25 | 0.05 | ✅ Good |

The site now passes Core Web Vitals for both mobile and desktop, as reported by Google Search Console.

---

## Lessons for Other Jekyll / GitHub Pages Users

1. **Image compression is non‑negotiable** – TinyPNG should be part of every build.
2. **Use `excerpt:`** – don't let Google guess your meta descriptions.
3. **Submit your sitemap** – it’s free and speeds up indexing.
4. **Check PageSpeed Insights regularly** – it catches issues before users complain.
5. **Handle redirects when you change URLs** – broken links hurt user experience and rankings.

---

## What I’d Do Differently Next Time

- Set up lazy loading for images from the start (I added it later).
- Automate image compression with a GitHub Action (still manual for now).
- Create a custom 404 page (on my to‑do list).

---

## Final Thought

Technical SEO doesn't require expensive tools. Google PageSpeed Insights and Search Console give you 90% of what you need. Auditing your own portfolio is a great way to learn – because you control every fix.

*This audit was performed as part of my ongoing work at Shaligram Infotech and for my personal portfolio.*
