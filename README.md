# Tim Huynh — Portfolio

Personal portfolio website. Built with vanilla HTML, CSS, and JavaScript. No frameworks, no build step — just open `index.html`.

## Live Demo

Hosted at: [thuynhportfolio.dev](https://thuynhportfolio.dev)

## Features

- Dark minimal design with scroll-triggered animations
- Fully responsive (mobile + desktop)
- Interactive Fitness AI Agent demo (powered by self-hosted llama3.1:8b via Ollama)
- Sections: Hero, About, Experience, Projects, Skills, Contact

## Setup

### 1. Clone the repo

```bash
git clone https://github.com/timhuynh94/timhuynh94.github.io
cd timhuynh94.github.io
```

### 2. Configure the AI demo

The Fitness Intelligence Agent demo calls a self-hosted backend at `api.thuynhportfolio.dev`, which proxies requests to a local Ollama instance running `llama3.1:8b`. The backend authenticates requests via a portfolio token in the `X-Portfolio-Token` header.

If you fork this and want the demo to work in your own deployment, you'll need to:
- Run your own Ollama instance with a compatible model
- Stand up a backend API that accepts `{ message, history }` and returns `{ data: { reply } }`
- Update `CHAT_ENDPOINT` and `PORTFOLIO_TOKEN` in `index.html` to point to your backend

### 3. Customize content

All portfolio content (name, experience, projects, skills, etc.) lives in `data.json`. Edit that file — no code changes needed.

### 4. Deploy to GitHub Pages

```bash
# In your repo settings:
# Settings → Pages → Source: Deploy from branch → main → / (root)
```

Your site will be live at `https://<your-username>.github.io` within a few minutes.

### 5. Custom domain (optional)

Add a `CNAME` file to the repo root with your domain:

```
yourdomain.com
```

Then update your DNS provider to point to GitHub Pages (see [GitHub docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)).

## Project Structure

```
/
├── index.html      # Everything — HTML, CSS, JS in one file
├── data.json       # All portfolio content (edit this to update the site)
└── README.md
```

## Tech

- HTML / CSS / JavaScript (no frameworks)
- [Syne](https://fonts.google.com/specimen/Syne) + [DM Mono](https://fonts.google.com/specimen/DM+Mono) via Google Fonts
- [Ollama](https://ollama.com) + llama3.1:8b for the self-hosted AI demo
