---
title: "Google Search Console: A 5‑Step Audit Guide for Beginners"
date: 2026-04-28
schema: Article
categories:
  - SEO
  - Technical SEO
tags:
  - Google Search Console
  - SEO Audit
  - Beginner Guide
excerpt: "Learn how to use Google Search Console to find indexing issues, track keywords, and measure SEO performance – step by step, with screenshots (simulated)."
---

Google Search Console (GSC) is the most powerful free SEO tool – yet many interns and small business owners only scratch the surface. This guide walks you through a 5‑step audit that you can complete in under 30 minutes.

---

## Step 1: Verify Your Site (Already Done)

If you see data in GSC, skip to Step 2. If not, add your site as a **URL‑prefix property** and verify via the HTML tag method (add the meta tag to `_includes/head-custom.html`). For GitHub Pages, this is usually automatic if you’ve already set up analytics.

---

## Step 2: Check the Performance Report (What People Search)

Go to **Performance → Search results**. Set the date range to the last 3 months. Look at:

- **Total clicks, impressions, average CTR, position.**  
  Low impressions? → Your content isn’t being discovered.  
  High impressions, low CTR? → Improve title/meta description.  
  High position (1‑5) but low clicks? → Maybe the query intent doesn’t match your page.

**Filter by “Pages”** to see which URLs drive traffic. Click on a URL, then switch to the **“Queries”** tab to see which search terms trigger it. That tells you exactly what keywords to optimise for.

**Action:** Export the top 10 queries and pages to a spreadsheet. Highlight opportunities: queries where your page ranks between 6‑15 – those are easiest to push into top 5.

---

## Step 3: Use the URL Inspection Tool (For Individual Pages)

Paste any URL from your site into the search bar at the top. You’ll see:

- **Indexing status:** “URL is on Google” (good) or “URL is not on Google” (request indexing).  
- **Coverage:** Any errors (e.g., “404”, “Soft 404”, “Redirect error”).  
- **Mobile usability:** If it says “Page not mobile friendly”, fix it immediately.  
- **AMP, structured data, and experience:** All in one place.

**Action:** Inspect your homepage and your 3 most important case studies. Request indexing for any that are not indexed.

---

## Step 4: Find and Fix Coverage Issues

Go to **Indexing → Pages**. This report shows all indexed and excluded pages.

- Click **“Excluded”** tab. Sort by reason.  
  Common harmless exclusions: “Page with redirect”, “Duplicate without user‑selected canonical”.  
  Dangerous exclusions: “Not found (404)”, “Soft 404”, “Blocked by robots.txt”.  
- Click on a dangerous error, then the **“Linked from”** tab to see which pages have the broken link. Fix those links.

**Action:** Fix all 404s. If you can’t fix a broken link, remove it. If a page is gone forever, set up a 301 redirect (on GitHub Pages via a `_redirects` file or simply by updating the link).

---

## Step 5: Submit Your Sitemap (If Not Already)

Go to **Indexing → Sitemaps**. If you don’t see a `sitemap.xml` listed, add it.

For a Jekyll site, your sitemap is usually at `https://yourdomain.com/sitemap.xml`. After submitting, check the status – it should say “Success”. If it says “Couldn’t fetch”, it’s often a temporary GitHub Pages issue; wait a few hours and retry.

**Action:** Submit sitemap and verify it’s processed.

---

## Bonus: Monitor Core Web Vitals

Go to **Experience → Core Web Vitals**. Google reports your site’s performance for mobile and desktop. If you have any “Poor” URLs, use PageSpeed Insights to diagnose and fix (compression, image optimisation, removing unused CSS).

---

## How Often to Run This Audit

- **Monthly:** Check Performance report for new keywords or sudden drops.  
- **Quarterly:** Full crawl coverage review.  
- **After publishing a new post:** Use URL Inspection to request indexing.

Search Console is not a set‑and‑forget tool. It’s your compass for SEO.

---

## Real Example from My Portfolio

When I first submitted my sitemap, I saw 3 pages marked “Crawled – currently not indexed”. I used URL Inspection for each, found they had thin content, added more text, and requested re‑indexing. Within two weeks, all were indexed.

Also, the Performance report showed that my cafe case study ranked for “cafe SEO Ahmedabad” (position 9) with decent impressions but low CTR. I rewrote the title and meta description using the patterns described in my other post. Two weeks later, CTR increased from 1.2% to 4.7%.

---

## Final Advice

You don’t need expensive SEO software. GSC + Google Analytics + PageSpeed Insights cover 90% of what an intern or small business needs. Master these tools, and you’ll impress any hiring manager.

*Have questions about your GSC data? Connect with me on [LinkedIn](https://www.linkedin.com/in/karan-dave-984a883a8).*

---

*This guide is based on my daily use of Google Search Console during my internship at Shaligram Infotech.*
