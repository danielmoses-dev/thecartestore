# 🛍️ The Carté Store – AI-Powered Trend Blog Automation

https://thecartestore.42web.io/

An elegant, fully automated content system that transforms trending Amazon products into visually stunning, editorial-quality blog posts. This automation blends AI writing, intelligent web scraping, and aesthetic media generation — all orchestrated in a stable, self-hosted n8n environment.

---

## 🚀 Overview

The Carté Store automation performs the following:

- Randomly selects a trending Amazon product from a curated Google Sheet
- Scrapes product title, description, image, reviews, and price using Puppeteer and a scraping API
- Sends data to **Gemini 1.5 Flash** with a structured prompt to generate:
  - A short blog title
  - A poetic introductory blurb
  - A compact excerpt for SEO
  - A detailed outline of subheadings and content structure
- Generates full narrative content and dynamic HTML sections for each subheading using Gemini and prompt engineering
- Extracts **semantic image prompts** based on content tone and fetches visuals from the **Pexels API**
- Injects contextually matching images into each blog section
- Formats the complete post with SEO, tags, categories, and HTML blocks
- Publishes directly to WordPress via the REST API
- Runs on a scheduled basis from a self-hosted **AWS EC2** instance

---

## 🧠 Tech Stack

- **n8n** – Workflow automation engine
- **Gemini 1.5 Flash** – AI content generation (custom prompts for tone and structure)
- **Puppeteer & ScraperAPI** – Product detail scraping
- **Pexels API** – Visual enrichment
- **Google Sheets** – Input control for product links
- **AWS EC2 (Ubuntu)** – Hosting the n8n instance
- **WordPress REST API** – Automated publishing
- **InfinityFree** – Free hosting of WordPress.org

---

## 🔧 Workflow Summary

> Screenshots of workflows are included separately for visual reference. The code and node structure are not publicly shared to protect proprietary automation logic.

- The workflow starts with a **scheduled or manual trigger**
- A **Google Sheet** is used as the dynamic input source for product URLs
- The product page is scraped for essential details like image, rating, and description
- A highly structured **Gemini prompt** generates the blog outline
- Another loop sends subheadings + structure instructions to Gemini to create section content
- A second prompt extracts visual context to query **Pexels**
- Relevant aesthetic images are injected into the post
- All blocks are formatted and sent to WordPress as a **ready-to-publish blog post**

---

## 🖼️ Visuals & Examples

### 🔧 Workflow Overview

This is the complete visual structure of the n8n automation powering The Carté Store.  
It includes scraping, AI rewriting, image fetching, content formatting, and WordPress publishing:

![Workflow Visual](https://github.com/danielmoses-dev/thecartestore/blob/main/Workflow%20Visual.png)

---

### 📝 Example Blog Outputs

Below are two real examples of blog posts auto-generated and published by the system:

**Example 1**  
![Blog Example 1](https://github.com/danielmoses-dev/thecartestore/blob/main/Blog%20Example%201.png)

**Example 2**  
![Blog Example 2](https://github.com/danielmoses-dev/thecartestore/blob/main/Blog%20Example%202.png)

---

### 📚 Blog Archive View

This is how the published posts appear on the main blog archive page, styled for a premium, elegant brand:

![Blog Archive](https://github.com/danielmoses-dev/thecartestore/blob/main/Blog%20Archive%20Page.png)

---

## ✨ Highlights

- Built to support future affiliate monetization with an SEO-aware structure
- Uses LLM prompt engineering for **tone control**, **content modularity**, and **consistency**
- Generates a **complete blog post**, not just raw text
- Produces **brand-aligned visuals** that elevate content quality
- Self-hosted for full control, cost-efficiency, and long-term deployment

---

## 🔒 Intellectual Property Notice

To protect the automation’s logic, structure, and potential for monetization, actual node code or JSON workflows are not shared publicly. This repository includes only high-level documentation and visuals.

---

## 👤 Author

_**Daniel Moses**_  
Automation & AI Content Engineering Enthusiast  
[LinkedIn](https://linkedin.com/in/danielmoses15) | [GitHub](https://github.com/danielmoses-dev)

---
