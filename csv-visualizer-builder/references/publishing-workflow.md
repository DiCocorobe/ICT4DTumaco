# Publishing Workflow for CSV Visualizers

This guide outlines the mandatory steps for publishing new CSV visualization apps to GitHub Pages within this repository.

## 1. File Naming & Scope
- Always create a **new** HTML file for each specific app (e.g., `sales-preview.html`, `census-tool.html`).
- DO NOT overwrite `index.html`, `map.html`, or `resilience.html` unless explicitly asked to update those specific modules.
- Ensure the filename is URL-friendly (lowercase, hyphens instead of spaces).

## 2. Integration with Landing Page
- After creating the new file, you MUST add a link or card to `index.html` (the landing page) so users can find the new tool.
- Add the tool to the "Analytical Toolset" grid in `index.html`.

## 3. Git Operations (Main Branch)
The user requires publishing on the `main` branch. Follow this sequence:

```bash
# 1. Stage the new file and the updated landing page
git add <new-filename>.html index.html

# 2. Commit with a descriptive message
git commit -m "Add new CSV visualization tool: <Name>"

# 3. Push to the main branch
git push origin main
```

## 4. Verification
- Verify the URL structure: `https://<username>.github.io/<repo-name>/<new-filename>.html`
- Confirm GitHub Pages is set to deploy from the `main` branch in repository settings.
