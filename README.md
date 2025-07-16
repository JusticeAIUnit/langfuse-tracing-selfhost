# LangFuse Tracing at Justice AI

Access the site live on [GitHub Pages](https://justiceaiunit.github.io/langfuse-tracing-selfhost/)

Documentation website for using and deploying self-hosted LangFuse to trace applications and workflows.

## 🚀 Quick Start

This is a [Quarto](https://quarto.org/) website that provides comprehensive documentation for:
- **Getting Started** - Understanding LangFuse and quick setup
- **Python Examples** - Practical implementation patterns with step-by-step instrumentation
- **Self-Hosted Deployment** - Azure deployment guides and configuration

## 📖 Using This Documentation

### Online Access

The documentation is automatically deployed to GitHub Pages when changes are pushed to the main branch.

### Local Development

To run the website locally:

1. **Install Quarto**
   
   **Important**: Use the same version as the GitHub Actions workflow to ensure consistent rendering:
   
   ```bash
   # Install specific version (1.7.32) to match CI
   # On macOS with Homebrew
   brew install quarto@1.7.32
   
   # Or download version 1.7.32 specifically from:
   # https://github.com/quarto-dev/quarto-cli/releases/tag/v1.7.32
   
   # Verify correct version
   quarto --version  # Should show 1.7.32
   ```

2. **Preview the Website**
   ```bash
   quarto preview
   ```
   
   This will start a local server at `http://localhost:4000` with live reload.

3. **Build and Test Locally**
   ```bash
   quarto render
   ```
   
   This creates the static site in the `docs/` directory.

::: {.callout-warning}
**Always test locally before pushing to main!** Pushes to the main branch automatically trigger the GitHub Actions workflow that renders and deploys the site to GitHub Pages. Make sure your changes render correctly locally using `quarto preview` and `quarto render` before committing.
:::

## 🛠️ Development

### Adding Content

- **New pages**: Create `.qmd` files in the appropriate directory
- **Navigation**: Update `_quarto.yml` to add new pages to the navbar
- **Styling**: Modify `styles.css` for custom styling

### Structure

```
├── index.qmd              # Home page
├── explanation/           # Understanding-oriented content
├── tutorials/             # Learning-oriented content
├── how-to/                # Problem-oriented content
├── _quarto.yml            # Site configuration
├── styles.css             # Custom styles
└── .github/workflows/     # GitHub Actions for deployment
```

## 📝 Contributing

1. **Edit content**: Modify `.qmd` files using Markdown syntax
2. **Test locally**: Use `quarto preview` to see changes
3. **Commit changes**: Open a PR, merge to main will trigger deployment to GitHub Pages.

### Writing Guidelines

- Use clear, descriptive headings
- Include practical code examples
- Add explanatory text for complex concepts
- Cross-reference related sections
- Test all code examples

## 🚀 Deployment

The website automatically deploys to GitHub Pages via GitHub Actions:

- **Trigger**: Any push to the `main` branch automatically starts the deployment process
- **Build Process**: The workflow uses Quarto 1.7.32 to render the site  
- **Deployment**: Static files are deployed to the `gh-pages` branch and served via GitHub Pages
- **Live Site**: Changes are visible at https://justiceaiunit.github.io/langfuse-tracing-selfhost/ within a few minutes

**⚠️ Important**: Since deployment is automatic, always ensure your changes work correctly locally before pushing to main. Use `quarto preview` and `quarto render` to test your changes.

### Manual Deployment

If you need to manually trigger deployment:
1. Navigate to the [Actions tab](https://github.com/JusticeAIUnit/langfuse-tracing-selfhost/actions) in GitHub
2. Select the "Deploy Quarto Website" workflow
3. Click "Run workflow" on the main branch

---

*This documentation is maintained by the Justice AI Unit to help teams implement observability and tracing in their AI applications.*
