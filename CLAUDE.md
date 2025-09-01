# Claude Code Instructions for Leslie's CV Project

## Working Directory
**ALWAYS use absolute path:** `/Users/lchg5/Documents/Science 2025/Bios CVs etc./HodgesGallagher_CV_2025_quarto/`

**IMPORTANT:** This project has directory reset issues. Always verify with `pwd` and use absolute paths in commands.

## Critical Rules for This Project

### NEVER Modify These Settings
- `_quarto.yml` → `output-dir: .` (MUST remain root directory)
- `_quarto.yml` → `project: type: website` (required for GitHub Pages)

### Always Use These Command Patterns
```bash
# Navigation
cd "/Users/lchg5/Documents/Science 2025/Bios CVs etc./HodgesGallagher_CV_2025_quarto" && command

# Git operations
git -C "/Users/lchg5/Documents/Science 2025/Bios CVs etc./HodgesGallagher_CV_2025_quarto" status

# Rendering
cd "/Users/lchg5/Documents/Science 2025/Bios CVs etc./HodgesGallagher_CV_2025_quarto" && quarto render
```

## Key Files
- **Main source:** `HodgesGallagher_CV_20250713.qmd`
- **Config:** `_quarto.yml` (DO NOT change output-dir)
- **Styling:** `styles.css`

## Common Workflows

### CV Updates
1. `cd "/full/path" && quarto render HodgesGallagher_CV_20250713.qmd`
2. Verify files appear in root (not subdirectories)
3. Commit ALL generated files: HTML, PDF, site_libs/

### Git Operations
- Always use absolute path in git commands
- Commit generated files (index.html, *.pdf, site_libs/) after rendering

## Project-Specific Behavior Rules

### For GitHub Pages Compatibility
- Output MUST go to root directory (not docs/ or output/)
- PDF links in production use absolute GitHub URLs
- All generated files must be committed to repo

### Error Prevention
- If GitHub Pages fails → check `_quarto.yml` output-dir is `.`
- If PDF 404s → use `https://raw.githubusercontent.com/[user]/[repo]/main/[file].pdf`
- If directory issues → always start commands with `cd "/full/path" &&`

## Quick Reference Commands
```bash
# Check location
cd "/Users/lchg5/Documents/Science 2025/Bios CVs etc./HodgesGallagher_CV_2025_quarto" && pwd

# Render project
cd "/Users/lchg5/Documents/Science 2025/Bios CVs etc./HodgesGallagher_CV_2025_quarto" && quarto render

# Git status
cd "/Users/lchg5/Documents/Science 2025/Bios CVs etc./HodgesGallagher_CV_2025_quarto" && git status

# List generated files
cd "/Users/lchg5/Documents/Science 2025/Bios CVs etc./HodgesGallagher_CV_2025_quarto" && ls -la *.html *.pdf site_libs/
```