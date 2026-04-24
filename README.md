# Josh Dev 🚀

A personal blog built with [Hugo](https://gohugo.io/) and deployed on GitHub Pages.

## About

This is my personal blog where I document my learning journey in software 
and technology. It was built as part of a university assignment to explore 
static site generators, version control, and web deployment.

## Built With

- **Hugo** - Static site generator
- **PaperMod** - Hugo theme
- **GitHub Pages** - Hosting and deployment
- **Markdown** - Content writing

## Project Structure
josh-dev/
├── content/
│   └── posts/          # Blog posts in Markdown
├── themes/
│   └── PaperMod/       # Site theme
├── static/             # Static assets
├── layouts/            # Custom layouts
└── hugo.toml           # Site configuration

## Running Locally

Make sure you have Hugo installed, then:

```bash
# Clone the repository
git clone https://github.com/yourusername/josh-dev.git

# Navigate into the project
cd josh-dev

# Start local development server
hugo server -D
```

Then open your browser at `http://localhost:1313/josh-dev/`

## Deployment

The site is built using Hugo and deployed to GitHub Pages.

```bash
# Build the site
hugo --minify

# The output is in the public/ folder
```

## Posts

- **Hello World** - Introduction to the blog
- **Assignment 1 Report** - System configuration and Python matrix multiplication

## Author

**Josh** - [GitHub](https://github.com/yourusername)

## License

This project is open source and available under the [MIT License](LICENSE).
