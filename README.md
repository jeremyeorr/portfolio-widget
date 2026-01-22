# Portfolio Widget

A self-updating portfolio page that automatically displays your GitHub projects. Designed to be embedded via iframe on platforms that don't support JavaScript (like SimpleSite).

## Features

- **Auto-updates** — Automatically fetches and displays your GitHub projects via the GitHub API
- **Two sections** — Separates live web apps (GitHub Pages) from other repositories
- **Sorted by recent activity** — Most recently updated projects appear first
- **Live previews** — Shows embedded previews of your GitHub Pages sites
- **Language badges** — Displays the primary language for each repository
- **Zero maintenance** — Add a new repo or enable Pages, and it appears automatically

## Live Demo

[https://jeremyeorr.github.io/portfolio-widget/](https://jeremyeorr.github.io/portfolio-widget/)

## Embedding

Add this iframe to your website:

```html
<iframe 
  src="https://jeremyeorr.github.io/portfolio-widget/" 
  width="100%" 
  height="800" 
  style="border: none;">
</iframe>
```

## Configuration

Edit the configuration section in `index.html`:

```javascript
var GITHUB_USERNAME = 'jeremyeorr';        // Your GitHub username
var SHOW_PREVIEWS = true;                   // Show/hide iframe previews
var EXCLUDE_REPOS = ['jeremyeorr', 'portfolio-widget']; // Repos to hide
```

## How It Works

1. Fetches your public repositories from the GitHub API
2. Filters out excluded repos and forks
3. Separates repos into two categories:
   - **Live Web Apps**: Repos with GitHub Pages enabled (`has_pages: true`)
   - **Public Repositories**: All other repos
4. Renders each section sorted by `updated_at` (most recent first)

## License

MIT
