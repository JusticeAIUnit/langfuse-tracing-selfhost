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
   ```bash
   # On macOS
   brew install quarto
   
   # Or download from https://quarto.org/docs/get-started/
   ```

2. **Preview the Website**
   ```bash
   quarto preview
   ```
   
   This will start a local server at `http://localhost:4000` with live reload.

3. **Build the Website**
   ```bash
   quarto render
   ```
   
   This creates the static site in the `docs/` directory.

## 🛠️ Development

### Adding Content

- **New pages**: Create `.qmd` files in the appropriate directory
- **Navigation**: Update `_quarto.yml` to add new pages to the navbar
- **Styling**: Modify `styles.css` for custom styling

### Structure

```
├── index.qmd              # Home page
├── explanation/           # Understanding-oriented content
│   └── overview.qmd       # What is LangFuse?
├── tutorials/             # Learning-oriented content
│   ├── quickstart.qmd     # Quick start guide
│   └── basic.qmd          # Core instrumentation and basic patterns
├── how-to/                # Problem-oriented content
│   ├── llm.qmd            # LLM applications with OpenAI, LangChain
│   ├── workflow.qmd       # Complex workflows and batch processing
│   ├── azure.qmd          # Azure deployment guide
│   ├── config.qmd         # Environment configuration
│   └── troubleshooting.qmd # Common issues and solutions
├── _quarto.yml            # Site configuration
├── styles.css             # Custom styles
└── .github/workflows/     # GitHub Actions for deployment
```

### Key Features

- **Theme Toggle**: Light/dark mode switching
- **Code Folding**: Expandable code blocks
- **Tabbed Content**: Multiple language examples
- **Mermaid Diagrams**: Architecture diagrams
- **Responsive Design**: Mobile-friendly layout

## 🔧 Configuration

The website is configured via `_quarto.yml` with:

- **Navigation**: Organized using the [Diátaxis](https://diataxis.fr/) framework (Understanding → Learning → Problem Solving)
- **Themes**: Flatly (light) and Darkly (dark) with toggle
- **Features**: Search, code tools, table of contents
- **Output**: GitHub Pages compatible

## 📝 Contributing

1. **Edit content**: Modify `.qmd` files using Markdown syntax
2. **Test locally**: Use `quarto preview` to see changes
3. **Commit changes**: Push to main branch for automatic deployment

### Writing Guidelines

- Use clear, descriptive headings
- Include practical code examples
- Add explanatory text for complex concepts
- Cross-reference related sections
- Test all code examples

## 🚀 Deployment

The website automatically deploys to GitHub Pages via GitHub Actions when:
- Changes are pushed to the main branch
- The workflow builds the site using Quarto
- The static files are deployed to the `gh-pages` branch

## 📞 Support

For questions or contributions:
- **GitHub Issues**: Report bugs or request features
- **Justice AI Team**: Internal support and guidance
- **LangFuse Community**: General questions about LangFuse

---

*This documentation is maintained by the Justice AI Unit to help teams implement observability and tracing in their AI applications.*
