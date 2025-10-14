# Deployment Guide - Extended Features

This guide explains the enhanced GitHub Actions workflow that supports slides, resources, and papers.

## 📋 Overview

The repository now supports three types of content:

1. **📊 Slides** - Marp presentations (Markdown → HTML + PDF)
2. **🔗 Resources** - Additional materials (Markdown → HTML)
3. **📚 Papers** - Academic literature (PDF files)

All content is automatically built and deployed to GitHub Pages when pushed to the `main` branch.

---

## 🚀 Features

### Conditional Rendering
- Only sections with actual content appear on the index page
- Empty directories are gracefully ignored
- No manual configuration needed

### Automatic Processing
- **Slides:** Converted to HTML and PDF with custom theme
- **Resources:** Converted to styled HTML pages
- **Papers:** Copied directly with file size display

### Responsive Design
- Mobile-friendly layout
- Hover effects for better UX
- Color-coded buttons for different content types

---

## 📁 Directory Structure

```
rai-sai25/
├── slides/              # Marp presentation files
│   ├── *.md            # Markdown slides
│   └── images/         # Slide images
├── resources/          # Additional course materials (optional)
│   └── *.md           # Markdown resources
├── papers/             # Academic papers (optional)
│   └── *.pdf          # PDF documents
└── .github/workflows/
    └── deploy-slides.yml
```

---

## 📊 Adding Slides

### 1. Create Markdown File

Create a new `.md` file in the `slides/` directory:

```markdown
---
marp: true
theme: neutral
---

<!-- description: Brief description for the index page. -->

<!-- _class: title -->

# Your Presentation Title
## Subtitle

Your Name
Institution, Date

---

# Slide 2

Content here...
```

### 2. Add Description (Optional)

Include a description comment right after the frontmatter:

```markdown
<!-- description: Introduction to sustainable AI practices and green computing. -->
```

This description will appear on the index page.

### 3. Push to GitHub

```bash
git add slides/your-presentation.md
git commit -m "Add new presentation"
git push origin main
```

GitHub Actions will automatically:
- Convert to HTML and PDF
- Apply the neutral theme
- Add to the index page

---

## 🔗 Adding Resources

Resources are Markdown files that get converted to nicely styled HTML pages.

### 1. Create Resource File

Create a `.md` file in the `resources/` directory:

```markdown
<!-- description: Collection of useful tools for the course. -->

# Useful Tools

## Category 1

- [Tool Name](https://example.com) - Description
- [Another Tool](https://example.com) - Description

## Category 2

More content...
```

### 2. File Naming

Use descriptive, lowercase names with hyphens:
- ✅ `useful-tools.md`
- ✅ `external-links.md`
- ✅ `video-resources.md`
- ❌ `Resource 1.md`
- ❌ `TOOLS.MD`

### 3. Styling

Resources are automatically styled with:
- Clean typography (Open Sans)
- Responsive layout
- Proper link formatting
- Code syntax highlighting

### 4. Push to GitHub

```bash
git add resources/your-resource.md
git commit -m "Add resource: useful tools"
git push origin main
```

---

## 📚 Adding Papers

Papers are PDF files that are copied directly to the deployment.

### 1. Add PDF File

Place PDF files in the `papers/` directory:

```bash
papers/
├── walker-2024-ai-sustainability.pdf
├── demirel-2023-sustainable-engineering.pdf
└── strubell-2019-energy-costs-nlp.pdf
```

### 2. Naming Convention

Recommended format: `author-year-topic.pdf`

Examples:
- `walker-2024-ai-sustainability.pdf`
- `sharma-2024-green-computing.pdf`

### 3. File Size

- Keep PDFs under 10MB when possible
- For larger files, consider linking instead
- Check `.gitignore` settings for PDF tracking

### 4. Copyright

Only upload papers you have rights to share:
- Open access publications
- Your own authored papers
- Properly licensed materials (CC-BY, etc.)

### 5. Push to GitHub

```bash
git add papers/walker-2024-ai-sustainability.pdf
git commit -m "Add paper: AI for Sustainability"
git push origin main
```

The paper will appear on the index page with:
- Formatted title (from filename)
- File size
- Download button

---

## 🎨 Index Page Structure

The generated `index.html` includes:

### Header
```
📚 SAI25 Course Materials
Sustainability and AI for Green | Winter Semester 2025
```

### Sections (Conditional)

**📊 Course Slides** (if `slides/*.md` exist)
- View button (HTML)
- PDF button (if available)

**🔗 Resources** (if `resources/*.md` exist)
- View button (HTML)

**📚 Literature & Papers** (if `papers/*.pdf` exist)
- File size display
- Download button

### Footer
```
UAS IMC Krems | Winter Term 2025 | Roman Mesicek
```

---

## 🔧 GitHub Actions Workflow

### Workflow Steps

1. **Install Dependencies**
   - Marp CLI (for slides)
   - Pandoc (for resources)

2. **Build Slides**
   - Convert `.md` to HTML + PDF
   - Apply custom theme
   - Copy images

3. **Build Resources**
   - Convert `.md` to HTML
   - Apply custom styling
   - Generate CSS file

4. **Copy Papers**
   - Copy PDFs to `dist/`
   - Calculate file sizes

5. **Generate Index**
   - Check which directories have content
   - Create sections conditionally
   - Add all items with metadata

6. **Deploy to GitHub Pages**
   - Upload artifact
   - Deploy to Pages

### Triggers

Workflow runs on push to `main` when:
- `slides/**/*.md` changes
- `slides/images/**` changes
- `resources/**/*.md` changes
- `papers/**/*.pdf` changes

Manual trigger also available via GitHub Actions UI.

---

## 🎯 Best Practices

### For Slides

1. Always include frontmatter with `marp: true` and `theme: neutral`
2. Add descriptions for better index page UX
3. Test locally with Marp CLI before pushing
4. Optimize images (compress before adding)

### For Resources

1. Use semantic Markdown structure (H1, H2, etc.)
2. Add descriptions for context
3. Link to external resources instead of embedding large files
4. Keep content focused and organized

### For Papers

1. Use descriptive filenames
2. Check file sizes before committing
3. Respect copyright and licensing
4. Document paper metadata in README if needed

### General

1. Commit small, focused changes
2. Write clear commit messages
3. Test workflow with manual triggers
4. Monitor GitHub Actions for errors

---

## 🐛 Troubleshooting

### Slides not appearing

**Issue:** Slides don't show on index page

**Checklist:**
- [ ] File is in `slides/` directory (not subdirectory)
- [ ] File has `.md` extension
- [ ] Marp frontmatter is present
- [ ] GitHub Actions workflow succeeded

### Resources not building

**Issue:** Resources missing from index

**Checklist:**
- [ ] Files are in `resources/` directory
- [ ] Files have `.md` extension
- [ ] Pandoc installed in workflow (automatic)
- [ ] Check GitHub Actions logs for errors

### Papers not showing

**Issue:** Papers don't appear

**Checklist:**
- [ ] Files are in `papers/` directory
- [ ] Files have `.pdf` extension
- [ ] PDFs are valid (not corrupted)
- [ ] Files aren't too large (check GitHub limits)

### Workflow fails

**Issue:** GitHub Actions workflow errors

**Solutions:**
1. Check workflow logs in GitHub Actions tab
2. Verify file paths and names
3. Ensure no special characters in filenames
4. Test builds locally before pushing

### Theme not applying

**Issue:** Slides don't use neutral theme

**Solutions:**
1. Verify `slides/themes/neutral.css` exists
2. Check frontmatter: `theme: neutral`
3. Verify `.vscode/settings.json` points to `./slides/themes/neutral.css`
4. Review workflow logs for theme errors

---

## 📊 Monitoring Deployments

### View Workflow Status

1. Go to repository → **Actions** tab
2. Click on latest workflow run
3. Review each step's output
4. Check summary for counts

### Deployment Output

Successful deployment shows:
```
=== Index page generated ===
Summary:
  - Slides: 5
  - Resources: 2
  - Papers: 3
```

### Access Deployed Site

1. Go to repository **Settings** → **Pages**
2. Find your site URL
3. Bookmark for easy access
4. Share with students

---

## 🚀 Advanced Usage

### Custom CSS for Resources

The workflow generates `resources-style.css` automatically. To customize:

1. Modify the CSS in `.github/workflows/deploy-slides.yml`
2. Search for `cat > dist/resources-style.css`
3. Edit styles as needed

### Adding New Sections

To add more content types (e.g., videos, datasets):

1. Create new directory
2. Add build step in workflow
3. Add conditional section in index generation
4. Update triggers in workflow

### Local Preview

```bash
# Preview slides
marp --theme slides/themes/neutral.css slides/your-file.md -o preview.html

# Preview resources
pandoc resources/your-file.md -o preview.html --standalone --css=your-style.css

# Serve locally
python -m http.server 8000
# Visit http://localhost:8000
```

---

## 📝 Example Workflow

Complete example of adding new content:

```bash
# 1. Create new slide
echo "---
marp: true
theme: neutral
---

<!-- description: Week 3 lecture on green AI strategies. -->

# Green AI Strategies

Content here...
" > slides/week03-green-ai.md

# 2. Create resource
echo "<!-- description: List of recommended reading materials. -->

# Recommended Reading

- [Article 1](https://example.com)
- [Article 2](https://example.com)
" > resources/reading-list.md

# 3. Add paper (copy existing PDF)
cp ~/Downloads/paper.pdf papers/author-2024-topic.pdf

# 4. Commit and push
git add slides/ resources/ papers/
git commit -m "Add week 3 materials: slides, reading list, and paper"
git push origin main

# 5. Monitor deployment
# Check GitHub Actions tab

# 6. Verify on website
# Visit GitHub Pages URL
```

---

## 🎓 For Students

If you want to contribute resources or papers:

1. **Fork** the repository
2. **Add** your content in appropriate directory
3. **Follow** naming conventions
4. **Submit** pull request with description
5. **Wait** for instructor approval

See main README.md for detailed contribution guidelines.

---

## 📞 Support

- **Documentation:** See README.md and CLAUDE.md
- **Issues:** GitHub Issues tab
- **Contact:** Course instructor

---

**Last Updated:** October 3, 2025
**Version:** 2.0 (Extended with resources and papers support)
