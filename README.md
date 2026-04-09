# Tim Huynh — Portfolio

Personal portfolio website. Built with vanilla HTML, CSS, and JavaScript. No frameworks, no build step — just open `index.html`.

## Live Demo

Hosted via GitHub Pages: [timhuynh94.github.io](https://timhuynh94.github.io)

## Features

- Dark minimal design with scroll-triggered animations
- Fully responsive (mobile + desktop)
- Interactive Fitness AI Agent demo (powered by Claude API)
- Sections: Hero, About, Experience, Projects, Skills, Contact

## Setup

### 1. Clone the repo

```bash
git clone https://github.com/timhuynh94/timhuynh94.github.io
cd timhuynh94.github.io
```

### 2. Configure the AI demo

The Fitness Intelligence Agent demo calls the Anthropic API. To enable it locally, the API key is handled by the hosting environment — no key is embedded in the source.

If you fork this and want the demo to work in your own deployment, you'll need to proxy API calls through a serverless function (Vercel, Netlify Functions, Cloudflare Workers) that injects your key server-side.

> **Note:** Never hardcode an API key directly in client-side HTML — it will be publicly visible in the source.

### 3. Deploy to GitHub Pages

```bash
# In your repo settings:
# Settings → Pages → Source: Deploy from branch → main → / (root)
```

Your site will be live at `https://<your-username>.github.io` within a few minutes.

### 4. Custom domain (optional)

Add a `CNAME` file to the repo root with your domain:

```
yourdomain.com
```

Then update your DNS provider to point to GitHub Pages (see [GitHub docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)).

## Project Structure

```
/
├── index.html      # Everything — HTML, CSS, JS in one file
├── CNAME           # Custom domain (add if needed)
└── README.md
```

## Tech

- HTML / CSS / JavaScript (no frameworks)
- [Syne](https://fonts.google.com/specimen/Syne) + [DM Mono](https://fonts.google.com/specimen/DM+Mono) via Google Fonts
- [Anthropic Claude API](https://docs.anthropic.com) for the AI demo
