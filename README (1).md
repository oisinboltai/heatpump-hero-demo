# heatpump-hero-demo

A static landing page for a heat pump company, with a hero image that can be updated dynamically via an n8n workflow.

## Structure

```
├── index.html         # Main landing page
├── style.css          # All styles
└── images/
    └── hero.jpg       # Hero image — replaced by n8n workflow
```

## How it works

1. A user submits an image via an n8n form
2. n8n pushes the new image to `images/hero.jpg` in this repo via the GitHub API
3. Vercel detects the commit and auto-redeploys
4. The live site shows the new hero image within ~30 seconds

## Setup

- Connect this repo to Vercel (static site, zero config needed)
- Deploy the n8n workflow (see workflow JSON in repo or n8n docs)
