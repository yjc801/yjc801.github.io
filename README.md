# Junchao Yan's Personal Blog

A personal blog and portfolio website built with [Hugo](https://gohugo.io/) and hosted on GitHub Pages.

**Live Site:** [https://junchaoyan.com](https://junchaoyan.com)

## About

This is my personal blog where I share thoughts on random things. I'm a Software Engineer at Meta.

## Technologies

- **Static Site Generator:** Hugo
- **Theme:** [Beautiful Hugo](https://github.com/halogenica/beautifulhugo)
- **Hosting:** GitHub Pages
- **CI/CD:** GitHub Actions
- **Domain:** Custom domain via CNAME

## Features

- Responsive design
- Syntax highlighting for code blocks
- Reading time and word count
- Disqus comments support
- RSS feed
- Social sharing
- Related posts
- SEO optimized

## Local Development

### Prerequisites

- [Hugo](https://gohugo.io/installation/) (extended version recommended)
- Git

### Setup

1. Clone the repository with submodules:
```bash
git clone --recurse-submodules https://github.com/yjc801/yjc801.github.io.git
cd yjc801.github.io
```

2. If you already cloned without submodules, initialize them:
```bash
git submodule update --init --recursive
```

3. Start the Hugo development server:
```bash
hugo server -D
```

4. Visit `http://localhost:1313` in your browser

### Creating New Posts

Create a new blog post:
```bash
hugo new posts/my-post-title.md
```

Create a new page:
```bash
hugo new page/my-page.md
```

Edit the created markdown file in the `content/` directory.

### Building

Build the site for production:
```bash
hugo --minify
```

The built site will be in the `./public/` directory.

## Deployment

The site automatically deploys to GitHub Pages when changes are pushed to the `main` branch via GitHub Actions.

The workflow:
1. Triggers on push to `main`
2. Builds the site using Hugo
3. Deploys to GitHub Pages

See `.github/workflows/gh-pages.yml` for the deployment configuration.

## Configuration

Main configuration is in `config.toml`:
- Site metadata (title, description, URL)
- Theme settings
- Menu structure
- Author information
- Social media links
- Hugo parameters

## Project Structure

```
.
├── .github/
│   └── workflows/          # GitHub Actions workflows
├── archetypes/             # Content templates
├── content/                # Blog posts and pages
│   └── page/              # Static pages (About, etc.)
├── resources/              # Hugo cache and generated files
├── static/                 # Static files (CNAME, images, etc.)
├── themes/                 # Hugo themes (git submodule)
│   └── beautifulhugo/
├── config.toml            # Hugo configuration
└── README.md              # This file
```

## Custom Domain

The site uses a custom domain `junchaoyan.com` configured via the `static/CNAME` file.

## Theme

This site uses the [Beautiful Hugo](https://github.com/halogenica/beautifulhugo) theme, which is a responsive and clean theme adapted from Beautiful Jekyll.

The theme is included as a git submodule.

## Contact

- Twitter: [@junchao_yan](https://twitter.com/junchao_yan)
- LinkedIn: [junchao-yan](https://linkedin.com/in/junchao-yan)
- Instagram: [@yjc801](https://instagram.com/yjc801)

## License

Content is copyright © Junchao Yan. The Beautiful Hugo theme is licensed under the MIT License.
