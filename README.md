# Local Development

## Prerequisites

- [Hugo](https://gohugo.io/installation/) (extended version recommended)
- Git

## Setup

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

## Creating New Posts

Create a new blog post:
```bash
hugo new posts/my-post-title.md
```

Create a new page:
```bash
hugo new page/my-page.md
```

Edit the created markdown file in the `content/` directory.

## Building

Build the site for production:
```bash
hugo --minify
```

The built site will be in the `./public/` directory.
