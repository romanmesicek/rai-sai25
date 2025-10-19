# Sustainability and AI for Green (RAI-SAI25)

**Master Course Repository | Winter Semester 2025**

This repository contains course materials, presentations, and student contributions for the Master's course "Sustainability and AI for Green" (RAI-SAI25).

## 📋 Course Overview

This course explores the intersection of artificial intelligence and environmental sustainability, examining how AI can contribute to green solutions while addressing its own environmental impact.

### Key Topics
- Climate Crisis & Information Technology
- AI's Carbon Footprint and Environmental Impact
- Green AI Strategies and Sustainable Computing
- AI for Environmental Solutions
- Sustainable Software Development
- Energy-Efficient Machine Learning

## 🌐 Course Website

All materials are automatically deployed to GitHub Pages:
- **📊 Slides** - HTML and PDF presentations
- **🔗 Resources** - Additional materials and links
- **📚 Papers** - Downloadable academic literature

**Visit: [https://romanmesicek.github.io/rai-sai25/](https://romanmesicek.github.io/rai-sai25/)**

## 📁 Repository Structure

```
rai-sai25/
├── slides/                  # Marp presentation slides
│   ├── *.md                # Markdown slides
│   ├── images/             # Slide images
│   └── themes/             # Marp presentation themes
│       └── neutral.css     # Custom neutral theme
├── resources/              # Additional course materials (Markdown)
│   ├── useful-tools.md
│   ├── external-links.md
│   └── contact-support.md
├── papers/                 # Academic papers (PDFs)
│   └── *.pdf              # Course reference papers
├── .github/workflows/      # GitHub Actions
│   └── deploy-slides.yml  # Automated deployment
├── README.md              # This file
├── SAI_Syllabus.md        # Complete course syllabus
└── DEPLOYMENT_GUIDE.md    # Deployment documentation
```

## 🚀 Quick Start

### Adding Slides
1. Create `.md` file in `slides/`
2. Add Marp frontmatter:
```markdown
---
marp: true
theme: neutral
---

<!-- description: Brief description for index page. -->

# Your Title
```
3. Commit and push - automatically deployed!

### Adding Resources
1. Create `.md` file in `resources/`
2. Add H1 heading and description
3. Push - converts to styled HTML automatically

### Adding Papers
1. Copy PDF to `papers/` directory
2. Use format: `author-year-topic.pdf`
3. Push - appears on website with download button

See [DEPLOYMENT_GUIDE.md](DEPLOYMENT_GUIDE.md) for details.

## 🛠️ Technology Stack

- **Marp** - Markdown presentations
- **Pandoc** - Resource conversion
- **GitHub Actions** - Automated deployment
- **GitHub Pages** - Website hosting

## 👥 Student Contributions

Students are encouraged to contribute to this repository through:

- **Research Summaries**: Analysis of recent papers on Green AI
- **Case Studies**: Real-world examples of sustainable AI implementations
- **Discussion Notes**: Insights from class discussions and debates

## 🤝 Contributing

We welcome contributions from students, researchers, and practitioners interested in sustainable AI. Please read our contribution guidelines above and feel free to:

- Report issues or suggest improvements
- Share relevant resources and papers
- Propose new topics or case studies
- Contribute code examples and implementations

## 📄 License

This educational content is shared under [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

---

*Last updated: October 2025*