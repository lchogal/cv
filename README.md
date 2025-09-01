# Leslie Hodges Gallagher CV

Professional CV built with Quarto markdown, generating both interactive HTML and print-ready PDF versions, optimized for GitHub Pages deployment.

## Files

- `HodgesGallagher_CV_20250713.qmd` - Main CV source file
- `styles.css` - Custom styling for professional appearance  
- `_quarto.yml` - Quarto configuration (GitHub Pages optimized)
- Generated files appear in root directory after rendering

## GitHub Pages Setup

This project is specifically configured to work with GitHub Pages, which requires a particular structure due to limitations with publishing HTML files rendered from QMD files.

### Key Configuration

The project uses these critical settings in `_quarto.yml`:
```yaml
project:
  type: website
  output-dir: .  # Output to root directory for GitHub Pages
  resources:
    - "*.pdf"    # Include PDF files as resources

website:
  title: "Leslie Hodges Gallagher CV"
  navbar:
    left:
      - href: index.html
        text: Home

format-links: [pdf]  # Enable PDF download link
```

### Why This Structure?

1. **Output Directory**: Set to `.` (root) instead of `output/` or `docs/` because GitHub Pages has issues with HTML files generated from QMD files in subdirectories
2. **Website Type**: Uses `website` project type rather than `document` for better GitHub Pages integration  
3. **PDF Resources**: Explicitly includes PDF files as resources to ensure they're accessible via absolute GitHub URLs
4. **Navbar Configuration**: Simple navigation structure that works reliably with GitHub Pages

## Rendering

### Local Development
```bash
quarto render HodgesGallagher_CV_20250713.qmd
```

### For GitHub Pages Deployment
1. Render the project: `quarto render`
2. Commit all generated files in root directory
3. Push to GitHub
4. Enable GitHub Pages from repository settings (source: root directory)

## Generated Files

After rendering, these files appear in the root directory:
- `index.html` - Main CV webpage
- `HodgesGallagher_CV_20250713.pdf` - PDF version
- Supporting files for GitHub Pages deployment

## Features

- **Responsive Design**: Optimized for both web and print
- **Interactive Elements**: Collapsible sections for publications and patents  
- **Professional Styling**: Blue headers, dark grey separators, clean typography
- **Clickable Links**: Company, ORCID, and patent portfolio links (HTML only)
- **Print Optimization**: Clean formatting without interactive elements for PDF
- **GitHub Pages Compatible**: All files output to root directory for reliable deployment

## Troubleshooting GitHub Pages

If GitHub Pages isn't working:

1. **Check output directory**: Ensure `_quarto.yml` has `output-dir: .`
2. **Verify file paths**: All resource paths must be relative to root
3. **PDF links**: Use absolute GitHub URLs for PDF downloads: 
   `https://raw.githubusercontent.com/[username]/[repo]/main/[filename].pdf`
4. **Repository settings**: Enable Pages from root directory, not `/docs`

## Updating

1. Edit the `.qmd` file
2. Run `quarto render` to generate new outputs in root directory
3. Commit all generated files (including HTML, PDF, and support files)
4. Push to GitHub - Pages will update automatically

## Contact

Leslie Hodges Gallagher, Ph.D.  
Email: hodges.gallagher@gmail.com  
