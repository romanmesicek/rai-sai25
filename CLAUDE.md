# CLAUDE.md - Project Analysis & Documentation

## Project Overview

**Repository Name:** rai-sai25
**Course:** Sustainability and AI for Green (RAI-SAG25)
**Institution:** UAS IMC Krems
**Semester:** Winter Semester 2025
**Course Type:** Integrated Course (ILV)
**ECTS Credits:** 5
**Contact Hours:** 2 per week

### Purpose
This repository serves as the central hub for course materials, presentations, and student contributions for the Master's course "Sustainability and AI for Green." The course explores the intersection of artificial intelligence and environmental sustainability, examining how AI can contribute to green solutions while addressing its own environmental impact.

---

## Repository Structure

```
rai-sai25/
├── .github/
│   └── workflows/
│       └── deploy-slides.yml    # GitHub Actions workflow for automated deployment
├── slides/                     # Marp presentation slides
│   ├── *.md                   # Markdown slides
│   ├── images/                # Images for presentations
│   └── themes/                # Custom Marp themes
│       └── neutral.css        # Neutral presentation theme
├── resources/                  # Additional course materials
│   ├── useful-tools.md        # Tool collection
│   ├── external-links.md      # External resources
│   ├── references.md          # APA-style reference list
│   ├── contact-support.md     # Contact information
│   └── README.md              # Resource guidelines
├── papers/                     # Academic papers (NEW)
│   ├── *.pdf                  # Course reference papers
│   ├── .gitkeep               # Track empty directory
│   └── README.md              # Paper guidelines
├── .gitignore                 # Git ignore patterns
├── README.md                  # Main repository documentation
├── SAG_Syllabus.md           # Complete course syllabus
├── DEPLOYMENT_GUIDE.md        # Deployment documentation
└── CLAUDE.md                  # This file - AI assistant documentation
```

### Directory Purposes

#### `.github/workflows/`
Contains GitHub Actions automation workflows for CI/CD processes.

#### `slides/`
Marp-based presentation slides in Markdown format, with supporting images. All course parts (01-03) are now included.

#### `resources/` (NEW)
Additional course materials in Markdown format. Converted to styled HTML pages automatically.

#### `papers/` (NEW)
Academic papers and literature in PDF format. Directly downloadable from the website.

#### `themes/`
Custom CSS themes for Marp presentations to ensure consistent branding and visual style.

---

## Technology Stack

### Content Processing
- **Marp CLI** - Converts Markdown slides to HTML/PDF
- **Pandoc** - Converts resource Markdown to styled HTML
- **Poppler-utils** (pdfinfo) - Extracts PDF metadata

### Development Tools
- **VS Code** with Marp extension
- **Git** for version control
- **GitHub Pages** for hosting all materials

### Automation
- **GitHub Actions** for automated deployment of slides, resources, and papers
- **Custom workflow** for conditional rendering and multi-format support

---

## Key Features

### 1. Automated Slide Deployment

The repository uses GitHub Actions to automatically build and deploy presentations to GitHub Pages.

**Workflow File:** [.github/workflows/deploy-slides.yml](.github/workflows/deploy-slides.yml)

**Trigger Conditions:**
- Push to `main` branch with changes in `slides/**/*.md`
- Push to `main` branch with changes in `slides/images/**`
- Push to `main` branch with changes in `resources/**/*.md` (NEW)
- Push to `main` branch with changes in `papers/**/*.pdf` (NEW)
- Manual trigger via `workflow_dispatch`

**Build Process:**
1. **Install Dependencies**
   - Marp CLI (`@marp-team/marp-cli`)
   - Pandoc (for resources)
   - Poppler-utils (for PDF metadata)

2. **Build Slides**
   - Copy images from `slides/images/` to `dist/`
   - Copy themes to `dist/`
   - Convert all `.md` files in `slides/` to HTML + PDF
   - Apply custom `neutral.css` theme

3. **Build Resources** (NEW)
   - Convert `.md` files in `resources/` to styled HTML
   - Extract H1 as page title
   - Apply custom CSS styling
   - Skip README.md and .gitkeep files

4. **Copy Papers** (NEW)
   - Copy PDFs from `papers/` to `dist/papers/`
   - Extract metadata (title, if available)
   - Calculate file sizes
   - Sort alphabetically

5. **Generate Index**
   - Conditional sections (only show if content exists)
   - Extract descriptions from files
   - Create cards for each content type
   - Add footer with contact link (if available)

6. **Deploy to GitHub Pages**

**Theme Handling:**
- Uses `--theme slides/themes/neutral.css` to apply custom neutral theme
- Theme is applied to both HTML and PDF outputs
- Falls back to default Marp theme if `neutral.css` not found
- PDF generation continues even if it fails (non-blocking)

**Description Feature:**
- Index page displays descriptions for each presentation
- Descriptions extracted from HTML comments in slide files
- Format: `<!-- description: Your description here. -->`
- Falls back to "Course presentation slides" if no description found

**Ordering Feature:**
- Slides are displayed in custom order on the index page
- Order determined by `order: N` field in frontmatter
- Lower numbers appear first (e.g., order: 1, order: 2, etc.)
- Slides without an `order` field appear at the end (default: 999)
- Allows flexible ordering without file renaming

### 2. Custom Neutral Theme

**Theme File:** [slides/themes/neutral.css](slides/themes/neutral.css)

**Design Characteristics:**
- **Font:** Open Sans (300, 400, 600, 700 weights)
- **Color Scheme:** Black text on white background
- **Typography:** Large, light-weight headers (non-bold)
- **Layout:** Generous padding (60px), clear hierarchy
- **Special Slides:** Centered title slide layout

**Theme Elements:**
- H1: 48px (64px on title slides)
- H2: 40px (46px on title slides)
- H3: 36px
- Body: 28px, 1.4 line height
- Lists: 30px left padding, 8px item spacing

### 3. Resources Section

**Purpose:** Unified section for all course materials beyond slides - papers, tools, links, and references.

**Website Structure:**
The Resources section on the website contains four subsections:

1. **Downloads** - Academic papers and studies (PDFs from `papers/` directory)
2. **Literature** - Complete APA-style reference list (`references.md`)
3. **Useful Tools** - Collection of AI & sustainability tools (`useful-tools.md`)
4. **External Links** - External resources and datasets (`external-links.md`)

**Technical Features:**
- Markdown files converted to styled HTML via Pandoc
- H1 extracted as page title (browser tab shows proper title)
- Custom CSS with dark mode support
- Supports all Markdown features (code blocks, tables, images, etc.)
- PDF files directly downloadable with file size display
- Alphabetical sorting for downloads
- README.md and contact-support.md automatically excluded from listings

**References File (`references.md`):**
- Complete list of sources cited in course materials
- APA 7th edition formatting
- Single alphabetical list (no section headings)
- 100+ references from academic publications, standards, and reports
- Automatically converted to styled HTML
- Accessible from both Resources section and Literature subsection
- All slide presentations link to this reference list on their title slides

**Available Papers:**
- **Carroll-1991-The-Pyramid-of-Corporate-Social-Responsibility.pdf** - Foundational framework for CSR
- **Dyllick-Muff-2015-True-Business-Sustainability.pdf** - Business sustainability maturity model
- **fanning-raworth-2025-world-out-of-balance.pdf** - Doughnut economics analysis
- **Kramer-Porter-2006-Strategy-and-Society.pdf** - Strategic CSR and shared value
- **Laurel-etal-2024-Dimensions-of-the-Doughnut.pdf** - Recent doughnut economics research
- **Zadek-2004-The-Path-to-Corporate-Responsibility.pdf** - CSR evolution and pathways

### 4. Version Control Strategy

**Gitignore Configuration:**
- Excludes build outputs (HTML, PPTX, images from Marp)
- **Excludes PDFs by default** (Marp outputs)
- **EXCEPT allows** `papers/*.pdf` (exception with `!` prefix)
- Excludes distribution directories
- Excludes source materials (`00_material/`, `_extraction/`)
- Excludes Node.js dependencies
- Excludes OS and IDE files
- Excludes CLAUDE.md (AI assistant documentation)

**Critical Patterns:**
```gitignore
*.pdf           # Ignore all PDFs (Marp outputs)
!papers/*.pdf   # BUT allow PDFs in papers/ directory

# AI files
CLAUDE.md       # AI assistant documentation
```

This approach keeps the repository focused on published content while allowing course papers to be tracked.

---

## Course Content

### Learning Outcomes

Students completing this module will be able to:

1. **Research & Assessment**
   - Search for, assess, prepare, and present information on sustainable practices
   - Focus on responsible AI systems for ecological and economic benefits

2. **Tool Selection & Adoption**
   - Select and adopt appropriate AI tools to enhance sustainability
   - Improve efficiency and profitability in business operations

3. **Circular Economy Integration**
   - Explain how circular economy models drive profitability
   - Understand AI's role in environmental benefits and economic prosperity

### Key Topics

1. **Climate Crisis & Information Technology**
2. **AI's Carbon Footprint and Environmental Impact**
3. **Green AI Strategies and Sustainable Computing**
4. **AI for Environmental Solutions**
5. **Sustainable Software Development**
6. **Energy-Efficient Machine Learning**
7. **Life Cycle Assessment: Quantifying Environmental Impacts**
8. **Circular Economy: Transition for Future Sustainability**
9. **Sustainable Infrastructure Systems for AI**

### Learning Activities

- **Chalk talks:** Foundational concepts introduction
- **Classroom debates:** Critical thinking on responsible AI
- **Quizzes:** Knowledge reinforcement
- **Group project:** Real-world scenario collaboration

### Assessment Structure

| Component | Weight | Description |
|-----------|--------|-------------|
| Written Exam | 60% | Understanding of sustainable practices and AI integration |
| Submission (Deliverable) | 30% | Comprehensive project report on AI sustainability solutions |
| Presentation | 10% | Communication of findings and recommendations |

### Required Textbooks

1. **Thomas Walker, Stefan Wendt, et al.** - "Artificial Intelligence for Sustainability" (Palgrave Macmillan, 2024)
2. **Yasar Demirel, Marc A. Rosen** - "Sustainable Engineering" (CRC Press, 2023)
3. **Neha Sharma, et al.** - "Green Computing for Sustainable Smart Cities" (CRC Press, 2024)

---

## Student Contribution Guidelines

### Contribution Types

Students can contribute:
- **Research Summaries:** Analysis of recent Green AI papers
- **Case Studies:** Real-world sustainable AI implementations
- **Code Examples:** Energy-efficient algorithm implementations
- **Discussion Notes:** Insights from class discussions

### Contribution Workflow

1. **Fork** the repository
2. **Create** a feature branch
3. **Add** materials in appropriate directory
4. **Submit** a pull request with clear description
5. **Follow** naming conventions and file structure

### File Naming Convention

```
week01_climate_crisis_summary.md
student_initials_topic_date.md
green_ai_case_study_2025.md
```

Pattern: Use lowercase with underscores, descriptive names, include initials/dates

---

## Development Setup

### Prerequisites

1. **VS Code** with Marp extension installed
2. **Git** for version control
3. **Node.js** (for Marp CLI if building locally)

### Local Presentation Development

1. Open any `.md` file in `slides/` directory
2. Add the required frontmatter:
   ```yaml
   ---
   marp: true
   theme: neutral
   ---
   ```
3. (Optional) Add a description for the index page:
   ```markdown
   <!-- description: Brief description of your presentation. -->
   ```
4. Use VS Code Marp preview to view slides
5. Custom theme automatically loads from `slides/themes/neutral.css` when configured in `.vscode/settings.json` (VS Code only)

### Building Presentations Locally

```bash
# Install Marp CLI globally
npm install -g @marp-team/marp-cli

# Build single presentation to HTML with theme
marp --theme slides/themes/neutral.css slides/SAI_Introduction.md -o output.html

# Build single presentation to PDF with theme
marp --theme slides/themes/neutral.css --pdf slides/SAI_Introduction.md -o output.pdf --allow-local-files

# Build all presentations (HTML)
for file in slides/*.md; do
  marp --theme slides/themes/neutral.css "$file" -o "dist/$(basename "$file" .md).html"
done

# Build all presentations (HTML + PDF)
for file in slides/*.md; do
  name=$(basename "$file" .md)
  marp --theme slides/themes/neutral.css --html "$file" -o "dist/${name}.html" --allow-local-files
  marp --theme slides/themes/neutral.css --pdf "$file" -o "dist/${name}.pdf" --allow-local-files
done
```

**Important Notes:**
- Use `--theme slides/themes/neutral.css` (not `--theme-set`)
- `--html` flag enables HTML tags in markdown content
- `--pdf` flag generates PDF output
- `--allow-local-files` is required for PDF generation with local resources

### Deployment

Deployment is fully automated via GitHub Actions. Simply:
1. Commit changes to slide files
2. Push to `main` branch
3. GitHub Actions builds and deploys automatically
4. Access presentations at the GitHub Pages URL

---

## GitHub Actions Workflow Details

### Workflow: Deploy All Slides

**File:** [.github/workflows/deploy-slides.yml](.github/workflows/deploy-slides.yml:1)

#### Triggers
- **Push to main:** Changes in `slides/**/*.md` or `slides/images/**`
- **Manual:** `workflow_dispatch` for on-demand deployment

#### Permissions
- `contents: read` - Read repository content
- `pages: write` - Write to GitHub Pages
- `id-token: write` - Required for Pages deployment

#### Job: build-and-deploy

**Steps:**

1. **Checkout** ([line 21](.github/workflows/deploy-slides.yml#L21))
   - Uses `actions/checkout@v4`
   - Fetches repository content

2. **Install Marp** ([line 23-24](.github/workflows/deploy-slides.yml#L23))
   - Installs `@marp-team/marp-cli` globally via npm

3. **Build all slides** ([line 26-93](.github/workflows/deploy-slides.yml#L26))
   - Creates `dist/` directory
   - Verifies project structure with debug output
   - Copies `slides/images/` to `dist/images/` if exists
   - Copies `themes/` to `dist/themes/` for reference
   - Iterates through all `.md` files in `slides/`
   - For each file:
     - **HTML Build:** Uses `marp --theme slides/themes/neutral.css --html` with `--allow-local-files`
     - **PDF Build:** Uses `marp --theme slides/themes/neutral.css --pdf` with `--allow-local-files`
     - Falls back to default theme if `neutral.css` not found
     - PDF generation is non-blocking (continues on failure)
     - Detailed logging for each build step

4. **Generate index** ([line 95-258](.github/workflows/deploy-slides.yml#L95))
   - Creates `dist/index.html` with modern, responsive design
   - Extracts descriptions from each `.md` file using `grep`
   - Description format: `<!-- description: text -->`
   - Falls back to "Course presentation slides" if no description
   - Lists all presentations with:
     - Title (formatted from filename)
     - Description (extracted from source)
     - View button (HTML version, green)
     - PDF button (if available, red)
   - Includes course subtitle and footer

5. **Setup Pages** ([line 260-261](.github/workflows/deploy-slides.yml#L260))
   - Configures GitHub Pages deployment with `actions/configure-pages@v4`

6. **Upload artifact** ([line 263-266](.github/workflows/deploy-slides.yml#L263))
   - Uploads `dist/` directory as Pages artifact

7. **Deploy to Pages** ([line 268-269](.github/workflows/deploy-slides.yml#L268))
   - Deploys artifact to GitHub Pages using `actions/deploy-pages@v4`

#### Index Page Features

The generated index page includes:
- **Modern Design:**
  - Open Sans font (matching presentation theme)
  - Clean, professional layout on light gray background (#fafafa)
  - Maximum width: 1000px, centered

- **Header:**
  - Course title: "📚 SAI25 Course Presentations"
  - Subtitle: "Sustainability and AI for Green | Winter Semester 2025"

- **Presentation Cards:**
  - White cards with subtle shadow and hover effects
  - Each card contains:
    - Presentation title (capitalized, from filename)
    - Description text (from slide file)
    - View button (green, links to HTML)
    - PDF button (red, links to PDF if available)
  - Hover animation (lift effect)

- **Footer:**
  - Course information: "UAS IMC Krems | Winter Term 2025 | Roman Mesicek"

- **Responsive Design:**
  - Desktop: Side-by-side title and buttons
  - Mobile: Stacked layout with full-width buttons
  - Adapts to screen size with media queries

---

## Current Presentations

### SAI_Introduction.md

**Location:** [slides/SAI_Introduction.md](slides/SAI_Introduction.md)

**Description:** "Introduction to the course, exploring how AI intersects with environmental sustainability and green solutions."

**Content:**
- Title slide: "Sustainability and AI for Green"
- Subtitle: "Introduction"
- Instructor: Roman Mesicek
- Institution: UAS IMC Krems, Winter Term 2025
- Placeholder content ("Coming soon ... Yeah!")

**Build Outputs:**
- HTML: `SAI_Introduction.html`
- PDF: `SAI_Introduction.pdf`

---

### SAI_Part_01.md

**Location:** [slides/SAI_Part_01.md](slides/SAI_Part_01.md)

**Description:** "Global Sustainability Challenges"

**Topics Covered:**
- The state of our world - Anthropocene
- Planetary Boundaries framework
- Doughnut Economics (Social Foundations & Ecological Ceilings)
- History of sustainability and sustainable development
- Weak vs. Strong Sustainability
- Sustainable Development Goals (SDGs)
- Triple Bottom Line concept

**Key Features:**
- 28 slides with comprehensive coverage
- Multiple images (pt01_ prefixed, properly sized)
- Split-column layouts for concepts
- Citations and references in H6 format
- Embedded video links (TED Talks)
- Background images for visual impact

**Build Outputs:**
- HTML: `SAI_Part_01.html`
- PDF: `SAI_Part_01.pdf`

---

### SAI_Part_01_GroupExercise.md

**Location:** [slides/SAI_Part_01_GroupExercise.md](slides/SAI_Part_01_GroupExercise.md)

**Description:** "Session 1 Exercise - Taking Stock of Our Planet"

**Exercise Structure:**
- Task 1: Individual Perspective (15 min) - Select topic, form groups
- Task 2: Global Overview (45 min) - Research and create poster
- Poster Exhibition Round 1 (30 min) - View and discuss
- Task 3: Networking (15 min) - Add connections (green Post-its)
- Task 4: Regional Context (30 min) - Add regional data (blue Post-its)
- Poster Exhibition Round 2 (15 min) - Final viewing
- Total: 150 minutes (2.5 hours)

**Features:**
- Color-coding system (green/blue Post-its)
- Detailed task breakdowns
- Timeline summary table
- Tips for success
- Reflection questions

**Build Outputs:**
- HTML: `SAI_Part_01_GroupExercise.html`
- PDF: `SAI_Part_01_GroupExercise.pdf`

---

### SAI_Part_02.md

**Location:** [slides/SAI_Part_02.md](slides/SAI_Part_02.md)

**Description:** "Business Ethics, Corporate Social Responsibility, and Sustainability Management"

**Topics Covered:**
- Business Ethics fundamentals
- Morality, ethics, and ethical theory
- Regional differences in ethical approaches
- Corporate Social Responsibility (CSR)
- Triple Bottom Line (People, Planet, Profit)
- CSR Pyramid and maturity models
- Stakeholder Management and engagement
- Sustainability Management (Leadership, Marketplace, Workforce, Environment, Society)
- Non-Financial Reporting and standards (GRI, SASB, TCFD, ESRS)
- EU Green Deal and Sustainable Finance
- Corporate Due Diligence and accountability

**Key Features:**
- 85+ slides with comprehensive CSR coverage
- Multiple images (pt02_ prefixed, properly sized)
- Company examples (Lego/Shell, Erste Bank, Innocent, Unilever)
- Group work exercises integrated
- Stakeholder mapping frameworks
- Reporting standards overview
- Speaker notes preserved in comments

**Build Outputs:**
- HTML: `SAI_Part_02.html`
- PDF: `SAI_Part_02.pdf`

---

### SAI_Part_02_GroupExercise.md

**Location:** [slides/SAI_Part_02_GroupExercise.md](slides/SAI_Part_02_GroupExercise.md)

**Description:** "Group Work Exercises - Company Sustainability Analysis"

**Exercise Structure:**
- Exercise 1: Choose a company and understand its core business model (15 min)
- Exercise 2: Identify ethical values from sustainability reports (15 min)
- Exercise 3: Analyze motives for sustainability/CSR uptake (15 min)
- Exercise 4: CSR Maturity Assessment using Dyllick/Muff methodology (15 min)

**Features:**
- Company selection guidelines
- Padlet integration for collaboration
- Plenary discussion prompts
- Focus on multinational companies
- Practical sustainability analysis

**Build Outputs:**
- HTML: `SAI_Part_02_GroupExercise.html`
- PDF: `SAI_Part_02_GroupExercise.pdf`

---

### SAG_Part_03_Basics.md

**Location:** [slides/SAG_Part_03_Basics.md](slides/SAG_Part_03_Basics.md)

**Description:** "The AI/Sustainability Paradox - Environmental Impact and Green AI"

**Topics Covered:**
- The energy footprint of artificial intelligence
- Data center environmental impact
- Computing infrastructure and resource consumption
- E-waste and hardware lifecycle
- Green AI strategies and methodologies
- Energy-efficient machine learning
- Carbon-aware computing
- Sustainable AI development practices

**Key Features:**
- 75+ slides with comprehensive coverage
- Multiple images (pt03_ prefixed, properly sized)
- 24 consolidated citation lines with author-date format
- Detailed technical content on AI environmental impact
- Practical strategies for sustainable AI

**Build Outputs:**
- HTML: `SAG_Part_03_Basics.html`
- PDF: `SAG_Part_03_Basics.pdf`

---

### SAG_Part_03_Cases.md

**Location:** [slides/SAG_Part_03_Cases.md](slides/SAG_Part_03_Cases.md)

**Description:** "AI for Sustainability - Real-World Applications and Case Studies"

**Topics Covered:**
- Precision agriculture and smart farming
- Renewable energy optimization
- Smart grid and energy management
- Sustainable transportation and logistics
- Waste management and recycling
- Circular economy applications
- Climate modeling and prediction
- Conservation and biodiversity monitoring

**Key Features:**
- 60+ slides with real-world examples
- Multiple images (pt03_ prefixed, properly sized)
- 16 consolidated citation lines with author-date format
- Case studies from industry leaders
- Quantified environmental impact data

**Build Outputs:**
- HTML: `SAG_Part_03_Cases.html`
- PDF: `SAG_Part_03_Cases.pdf`

---

### SAG_Part_03_GroupExercise.md

**Location:** [slides/SAG_Part_03_GroupExercise.md](slides/SAG_Part_03_GroupExercise.md)

**Description:** "Group Work Exercise - Designing Sustainable AI Systems"

**Exercise Structure:**
- Setup (10 min) - Form groups and select scenario
- Design (30 min) - Design sustainable AI system
- Ethics (15 min) - Identify ethical considerations
- Present (15 min) - Present solutions to class
- Synthesis (15 min) - Reflect and connect learnings
- Total: 90 minutes (1.5 hours)

**Features:**
- Three scenario options (Smart City, Agricultural AI, E-Waste Management)
- Design thinking framework
- Ethical analysis prompts
- Presentation guidelines
- Reflection questions

**Build Outputs:**
- HTML: `SAG_Part_03_GroupExercise.html`
- PDF: `SAG_Part_03_GroupExercise.pdf`

---

## Citation Standardization System

### Overview

All course presentations now use a standardized citation format that separates in-slide citations from the complete reference list.

### Implementation

**Title Slide Reference:**
Every presentation includes a link to the master reference list on the title slide:
```markdown
###### Full reference list available at [GitHub](https://github.com/romanmesicek/rai-sai25/blob/main/resources/references.md)
```

**In-Slide Citations:**
Citations use compact author-date format with H6 heading:
```markdown
###### Sources: Author, Year
###### Sources: Author1, Year1; Author2, Year2; Author3, Year3
```

**Features:**
- Single space after `######`
- Semicolon-separated multiple sources
- Consistent author-date format
- Inline placement below relevant content
- No duplicate references

**Image Credits:**
Image credits are preserved separately from source citations:
```markdown
###### Image: Source description
###### Photo by Name (Unsplash)
```

### Master Reference List

**File:** [resources/references.md](resources/references.md)

**Statistics:**
- 100+ references in APA 7th edition format
- Alphabetically sorted
- Includes all sources from Parts 01, 02, and 03
- Automatically deployed as styled HTML page
- Accessible via Resources → Literature section

**Coverage:**
- Academic journal articles
- Technical reports
- Standards and frameworks
- Books and monographs
- Online resources and datasets

### Benefits

1. **Consistency:** Uniform citation style across all presentations
2. **Readability:** Compact citations don't clutter slides
3. **Maintainability:** Single source of truth for references
4. **Accessibility:** Web-accessible reference list with search functionality
5. **Academic Integrity:** Complete APA 7 citations for all sources

---

## Git History Summary

### Recent Commits

1. **a5b8c85** - Debug deployment
2. **cd3be08** - Title slide changed
3. **fd02c04** - Theme correction for deployment
4. **ac3d6d0** - Updated deployment instructions
5. **88aff63** - Changed title of pages website
6. **9e7f074** - Deployment for slides added
7. **5311cf4** - Updated repository description
8. **c8becb6** - Added comprehensive README.md
9. **e74b3cf** - First commit

### Development Timeline

The repository shows active development focused on:
- Setting up automated deployment infrastructure
- Refining presentation themes
- Documenting project structure
- Debugging deployment workflow
- Implementing description feature for index page
- Fixing theme application in GitHub Actions

### Latest Updates (October 2, 2025)

**Deployment Workflow Improvements:**
1. ✅ Fixed theme application - Changed from `--theme-set` to `--theme`
2. ✅ Added proper error handling and detailed logging
3. ✅ Verified slide detection and build process
4. ✅ Both HTML and PDF now build successfully with theme

**New Features:**
1. ✅ Description support - Index page now shows descriptions from slide files
2. ✅ Enhanced index page design - Modern, responsive cards with hover effects
3. ✅ Mobile-responsive layout - Adapts to different screen sizes
4. ✅ Course footer - Displays course information at bottom

**Documentation:**
1. ✅ Updated CLAUDE.md with latest workflow details
2. ✅ Added slide template and examples
3. ✅ Improved troubleshooting section
4. ✅ Corrected Marp CLI command syntax throughout

---

## Best Practices & Recommendations

### For Students

1. **Creating New Presentations**
   - Copy frontmatter from existing slides
   - Use `theme: neutral` for consistency
   - **Add a description comment** for the index page
   - Follow Markdown best practices
   - Test locally with Marp CLI before pushing

2. **Adding Images**
   - Place in `slides/images/` directory
   - Use relative paths: `![alt](images/filename.png)`
   - Optimize file sizes before committing

3. **Version Control**
   - Write clear commit messages
   - Create feature branches for new content
   - Submit PRs for review before merging

### For Instructors

1. **Content Management**
   - Keep source materials in `00_material/` (gitignored)
   - Convert to Markdown for version control
   - Use semantic versioning for major updates

2. **Theme Customization**
   - Modify `slides/themes/neutral.css` for branding changes
   - Test thoroughly across different slide types
   - Document theme changes in commit messages

3. **Deployment Management**
   - Monitor GitHub Actions runs
   - Check Pages deployment status
   - Review generated index page regularly

---

## Troubleshooting

### Common Issues

#### Presentations not building
- **Check:** Marp frontmatter is present
- **Check:** YAML syntax is valid
- **Check:** Theme file exists in `themes/`

#### Images not displaying
- **Check:** Images exist in `slides/images/`
- **Check:** Relative path is correct
- **Check:** Images copied to `dist/` during build

#### Theme not applying
- **Check:** Theme name matches CSS file (`theme: neutral`)
- **Check:** VS Code settings.json points to `./slides/themes/neutral.css` (for local preview)
- **Check:** GitHub workflow uses `--theme slides/themes/neutral.css` (not `--theme-set`)
- **Check:** File `slides/themes/neutral.css` exists and is valid CSS

#### Deployment failing
- **Check:** GitHub Actions logs for errors
- **Check:** Permissions are correctly set (pages: write, id-token: write)
- **Check:** Branch name is `main`
- **Check:** GitHub Pages is enabled in repository settings
- **Check:** Workflow has proper triggers configured

#### Descriptions not showing on index page
- **Check:** Description comment format: `<!-- description: text -->`
- **Check:** Comment is placed after frontmatter, before content
- **Check:** No extra spaces or special characters in comment
- **Check:** GitHub Actions successfully extracted description (check logs)

---

## Future Enhancements

### Potential Improvements

1. **Content Expansion**
   - Add more presentation slides
   - Create student contribution templates
   - Develop interactive exercises

2. **Theme Variants**
   - Dark mode theme
   - High-contrast accessibility theme
   - Print-optimized theme

3. **Automation**
   - Automated slide numbering
   - TOC generation
   - Cross-presentation navigation

4. **Quality Assurance**
   - Markdown linting
   - Link checking
   - Spell checking in CI/CD

5. **Student Features**
   - Contribution guidelines document
   - Issue templates for questions
   - Discussion board integration

---

## License & Attribution

**License:** Creative Commons Attribution 4.0 International License
**Course Instructor:** Roman Mesicek
**Institution:** UAS IMC Krems

All educational content is freely shared for academic purposes with proper attribution.

---

## Quick Reference

### Important Files
- [README.md](README.md) - Main documentation
- [SAI_Syllabus.md](SAI_Syllabus.md) - Complete syllabus
- [.github/workflows/deploy-slides.yml](.github/workflows/deploy-slides.yml) - Deployment workflow
- [slides/themes/neutral.css](slides/themes/neutral.css) - Presentation theme

### Key Commands
```bash
# Build HTML with theme
marp --theme slides/themes/neutral.css slides/filename.md -o output.html

# Build PDF with theme
marp --theme slides/themes/neutral.css --pdf slides/filename.md -o output.pdf --allow-local-files

# Watch mode (for live preview during development)
marp -w --theme slides/themes/neutral.css slides/filename.md

# Build all slides (HTML)
for file in slides/*.md; do
  marp --theme slides/themes/neutral.css "$file" -o "dist/$(basename "$file" .md).html"
done

# Build all slides (HTML + PDF)
for file in slides/*.md; do
  name=$(basename "$file" .md)
  marp --theme slides/themes/neutral.css --html "$file" -o "dist/${name}.html" --allow-local-files
  marp --theme slides/themes/neutral.css --pdf "$file" -o "dist/${name}.pdf" --allow-local-files
done
```

### Slide Template
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
UAS IMC Krems, Winter Term 2025

---

# Slide 2

Content here...
```

### Git Workflow
```bash
git checkout -b feature/new-presentation
# Make changes
git add .
git commit -m "Add new presentation on topic X"
git push origin feature/new-presentation
# Create pull request
```

---

## Recent Updates (October 3, 2025)

### Extended Deployment System

The repository now supports **three content types** with automated deployment:

1. **📊 Slides** (existing)
   - Marp Markdown → HTML + PDF
   - Custom neutral theme
   - Description extraction

2. **🔗 Resources** (NEW)
   - Markdown → styled HTML
   - H1 title extraction for page titles
   - Dark mode support
   - Full Markdown feature support

3. **📚 Papers** (NEW)
   - PDF downloads
   - Metadata extraction
   - File size display
   - Alphabetical sorting

### Key Improvements

**Conditional Rendering:**
- Each section only appears if content exists
- Empty directories gracefully ignored
- No manual configuration needed

**Smart Title Handling:**
- Resources: H1 extracted as browser title
- Papers: Title from PDF metadata or formatted filename
- Fallbacks for missing metadata

**Enhanced Footer:**
- Links to `contact-support.md` if available
- Clean, minimal design
- Automatic inclusion

**Fixed .gitignore:**
- `*.pdf` blocks Marp outputs
- `!papers/*.pdf` allows course papers
- Critical for paper tracking

### Documentation

- **README.md** - Updated with new structure and quick start
- **DEPLOYMENT_GUIDE.md** - Comprehensive deployment documentation
- **CLAUDE.md** - This file, updated with all changes
- **papers/README.md** - Guidelines for adding papers
- **resources/README.md** - Guidelines for adding resources

---

## Contact & Support

For questions, issues, or contributions:
- Create an issue in the repository
- Submit a pull request
- Contact course instructor: Roman Mesicek
- See: `resources/contact-support.md` (once deployed)

---

---

## Recent Updates (November 20, 2025)

### Website Restructuring
- **Split Course Slides:** Separated into two subsections
  - Course Lecture Presentations (main lectures)
  - Course Exercise Guides (GroupExercise files)
- **Unified Resources Section:** Consolidated all materials under Resources with four subsections
  - Downloads (Papers and Studies) → now links to dedicated sub-page
  - Literature (APA Reference List)
  - Useful Tools
  - External Links
- **Removed:** Separate "Literature & Papers" top-level section

### New Features
- **Downloads Page:** Created `resources/downloads.md` as dedicated page for paper downloads
  - Organized by category (Business Ethics/CSR, Sustainability)
  - Direct download links to PDFs
  - Cross-references to Literature section
- **References Page:** Added `resources/references.md` with complete APA 7th edition reference list
- **23 Citations:** All sources from course slides compiled and formatted alphabetically
- **Smart Subsections:** Each subsection only appears if content exists

### Exercise Updates
- **Part 03 Group Exercise:** Extended timeline from 60 to 90 minutes
  - Setup: 5→10 min
  - Design: 20→30 min
  - Ethics: 10→15 min
  - Present: 10→15 min
  - Synthesis: 10→15 min

### Repository Maintenance
- **Gitignore:** Added `_extraction/` directory to exclusions
- **Documentation:** Updated CLAUDE.md to reflect new structure

---

*Last Updated: November 20, 2025*
*Generated and maintained with Claude AI Assistant*
