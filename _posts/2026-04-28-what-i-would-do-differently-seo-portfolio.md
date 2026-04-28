---
title: "What I Would Do Differently If I Started My SEO Portfolio from Scratch"
date: 2026-04-28
schema: Article
categories:
  - Career
  - SEO
tags:
  - Portfolio
  - Lessons Learned
  - SEO Strategy
  - BBA
excerpt: "A candid look back at building my portfolio – mistakes I made, things I’d change, and advice for other students starting their own."
---

Building this portfolio has been one of the most valuable learning experiences of my BBA journey. I went from zero knowledge of GitHub and Jekyll to a fully functional, SEO‑optimised site with case studies, research articles, and a custom domain (still on the list). But looking back, there are several things I would do differently.

This post is not a “look how perfect I am” piece. It’s an honest reflection to help other students avoid the same pitfalls.

---

## 1. Publish Earlier, Even If Imperfect

**What I did:** Spent weeks tweaking colours, layouts, and fonts before publishing the first post.

**What I’d do instead:** Publish a minimum viable post (e.g., “Hello World – I’m learning SEO”) on day one. A live site with one paragraph is infinitely better than a perfect site that lives only on your hard drive.

**Why:** Google needs time to crawl and index. The clock starts when you publish, not when you’re happy with the design.

---

## 2. Focus on Content, Not Theme Tinkering

**What I did:** Endlessly customised the Minimal Mistakes theme – sticky headers, back‑to‑top buttons, category filters, search overlays (some of which I eventually removed).

**What I’d do instead:** Leave the theme 90% default. Write the case studies first. After you have 3–4 solid posts, then add polish. Recruiters care about your insights, not your border radius.

**Why:** Time spent on CSS is time not spent on keyword research or client outreach.

---

## 3. Use a Simpler Blogging Workflow from Day One

**What I did:** Wrote posts directly in GitHub’s web editor, often fighting with YAML errors and indentation. I also experimented with various search implementations that never worked perfectly.

**What I’d do instead:** Start with a local Jekyll installation and a text editor (VS Code). Draft posts in Markdown, preview locally, and only push when ready. For search, I’d skip custom code and rely on Google’s site search or a simple `/search.json` fallback.

**Why:** A local workflow catches errors before they break your live site, and it’s much faster for writing.

---

## 4. Optimise Titles and Meta Descriptions from the Start

**What I did:** Wrote functional but boring titles like “Ahmedabad Cafe SEO Audit”. Only later learned to add numbers, power words, and a clear benefit.

**What I’d do instead:** Apply the formula “`[Number] + [Adjective] + [Topic] + [Result]`” to every post from day one. Example: “Ahmedabad Cafe SEO Audit” → “How I Boosted a Cafe’s Traffic by 150% (A Complete Case Study)”.

**Why:** Titles and meta descriptions affect click‑through rates immediately. Changing them later means recrawling and losing early momentum.

---

## 5. Start Internal Linking Immediately

**What I did:** Published several posts in isolation before linking them together. The Market Research Hub came late.

**What I’d do instead:** Build a simple “Hub” page after the first two posts. Add a “Related posts” section at the bottom of each article (Minimal Mistakes supports it with `related: true` in `_config.yml`).

**Why:** Internal links pass authority and help Google understand topic clusters. They’re free SEO juice.

---

## 6. Not Over‑Engineer Contact Forms

**What I did:** Spent hours integrating Formspree, setting up redirects, and creating a thank‑you page. It works, but it was overkill.

**What I’d do instead:** Just put my email address and a LinkedIn link on the Contact page. For a portfolio site that gets fewer than 100 visitors a month, a simple `mailto:` is enough.

**Why:** Simpler is more reliable. You can always add a form later if traffic grows.

---

## 7. Set Up Google Analytics and Search Console Immediately

**What I did:** Added GSC after several weeks, and GA4 even later. Missed early traffic data.

**What I’d do instead:** On day one, add the GA4 tag and verify site ownership in GSC. Then, spend 15 minutes to understand the key reports (Performance, Coverage, Sitemaps).

**Why:** You can’t improve what you don’t measure. Early data helps you spot what works.

---

## 8. Plan a Content Calendar, Not Just Random Topics

**What I did:** Wrote posts whenever inspiration struck. Ended up with an unbalanced mix – many SEO case studies, fewer market research pieces.

**What I’d do instead:** Decide on 5–7 core topic clusters (e.g., local SEO, consumer psychology, BBA career advice). Aim for at least one post per cluster before expanding.

**Why:** A portfolio with depth in a few areas is more impressive than shallow breadth.

---

## 9. Not Fear the YAML

**What I did:** Avoided front matter customisation because I was afraid of breaking the build. Consequently, I missed opportunities like adding `schema: Article`, custom excerpts, and `last_modified_at`.

**What I’d do instead:** Read the Minimal Mistakes documentation and experiment on a local branch. YAML errors are fixable; missing structured data is a lost ranking opportunity.

**Why:** Schema markup directly improves how your site appears in search results.

---

## 10. Ask for Feedback Sooner

**What I did:** Kept the portfolio private until it was 90% complete.

**What I’d do instead:** Share the link after the first 2–3 posts – with peers, on LinkedIn, with my internship mentor. Their feedback would have saved me weeks of wasted effort.

**Why:** Early feedback validates direction or corrects course when it’s cheap to change.

---

## What I Got Right (So I’m Not Only Criticising Myself)

- **Choosing a static site generator** – Jekyll + GitHub Pages is free, fast, and teaches real‑world tooling (Git, Markdown, CI/CD).
- **Writing original research** – The EV adoption and consumer psychology posts are unique to my experience and cannot be copied.
- **Keeping it live** – Despite the mistakes, the portfolio is live and improving.

---

## Advice for Other BBA Students

You don’t need a perfect portfolio. You need a **real** portfolio. Start with a single post – 500 words on a topic you understand. Publish it. Then repeat. Iteration beats perfection.

And remember: the goal of a portfolio isn’t to impress recruiters with technical wizardry. It’s to prove that you can take an idea, execute it, and deliver results. Everything else is noise.

---

*Have you started your portfolio? Questions or want feedback? Connect with me on [LinkedIn](https://www.linkedin.com/in/karan-dave-984a883a8).*

---

*This post is based on my personal experience building `karandave211.github.io`. Your mileage may vary – but the principles are universal.*
