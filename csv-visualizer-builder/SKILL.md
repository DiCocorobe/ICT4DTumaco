---
name: csv-visualizer-builder
description: Design, build, and publish standalone web applications for CSV data visualization and previewing. Use when creating new CSV upload tools that must be published to GitHub Pages with separate URLs.
---

# CSV Visualizer Builder

This skill provides a standardized workflow for creating modern, card-based web applications that allow users to upload and visualize CSV datasets.

## Core Functionality

- **CSV Parsing**: Powered by [PapaParse](https://www.papaparse.com/) for high performance and header detection.
- **Modern UI**: Clean, responsive layout with a dedicated "Drop Zone" and interactive data table.
- **Preview Scaling**: Efficiently renders large datasets by truncating to the first 100 rows while providing total counts.

## Workflow

### 1. Initialize from Template
Use the boilerplate in `assets/template.html`. Clone this file to a new location in the repository.

```bash
cp csv-visualizer-builder/assets/template.html <new-filename>.html
```

### 2. Customize Metadata
Search and replace the placeholders in the new HTML file:
- `{{TITLE}}`: A descriptive name for the specific dataset tool.
- `{{DESCRIPTION}}`: Instructions or context for the data being analyzed.

### 3. Publishing Protocol
Follow the mandatory publishing process described in `references/publishing-workflow.md`:
- **Branch**: Always push to `main`.
- **URL**: Each app must have its own `.html` file (e.g., `survey-data.html`).
- **Linking**: Integrate the new tool into the `index.html` landing page.

## Command Reference

When adding the new tool to git, always use descriptive commit messages:
```bash
git add <filename>.html index.html
git commit -m "Publish new CSV visualizer: <Title>"
git push origin main
```
