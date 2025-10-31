# MARP Style Guide for SAG25 Course Presentations

This document describes the formatting conventions and style patterns used in SAG25 course presentations based on the `SAG_Part_01.md` template. Use this guide when creating new MARP presentations for this course.

---

## 1. Frontmatter Configuration

Every presentation file must start with the following YAML frontmatter:

```yaml
---
marp: true
theme: neutral
size: 16:9
order: 1
---
```

**Required Elements:**
- `marp: true` - Enables Marp processing
- `theme: neutral` - Uses the custom neutral theme (defined in [slides/themes/neutral.css](slides/themes/neutral.css))
- `size: 16:9` - Sets aspect ratio to widescreen 16:9
- `order: N` - Numeric value that controls display order on the index page (lower numbers appear first)

**Description Comment (Required for Index Page):**
Immediately after frontmatter, add a description comment:

```markdown
<!-- description: Brief description for the index page. -->
```

Example:
```markdown
---
marp: true
theme: neutral
size: 16:9
order: 2
---

<!-- description: Global Sustainability Challenges -->
```

**Note:** The `order` field determines the presentation's position on the index page. Use sequential numbers (1, 2, 3...) or leave gaps (10, 20, 30...) for easy insertion of new slides later. Presentations without an `order` field will appear at the end.

---

## 2. Title Slide Format

The first content slide should be the title slide with the `title` class:

```markdown
<!-- _class: title -->


# Main Title
## Subtitle or Session Number

IMC University of Applied Sciences Krems, Austria
Roman Mesicek


---
```

**Key Conventions:**
- Use `<!-- _class: title -->` directive to apply title slide styling
- Two blank lines after the class directive
- Main title uses single `#` (H1)
- Subtitle uses double `##` (H2)
- Institution and instructor name on separate lines (no markdown formatting)
- Two blank lines before the slide separator `---`

**Example:**
```markdown
<!-- _class: title -->


# Global Sustainability Challenges
## SAG Part 1

IMC University of Applied Sciences Krems, Austria
Roman Mesicek


---
```

---

## 3. Regular Slide Format

### Basic Content Slide

```markdown
# Slide Title

Content goes here with clear paragraph spacing.


---
```

**Conventions:**
- One H1 heading per slide (using single `#`)
- Two blank lines before slide separator `---`
- Clear paragraph breaks between content blocks

### Slide with Subtitle/Description

```markdown
# Main Heading

Descriptive text or subtitle.


---
```

**Example:**
```markdown
# The state of our World

Combining ecological and social challenges in one overview.


---
```

---

## 4. Special Slide Classes

### Groupwork Slides

For interactive/groupwork slides, use the `groupwork` class:

```markdown
<!-- _class: groupwork -->

# Activity Title

## **Goal**: Clear objective statement.

Additional instructions or details.

---
```

**Example:**
```markdown
<!-- _class: groupwork -->

# State of the World - Challenges

## **Goal**: Create a comprehensive picture of the socio-ecological challenges facing our society.

Structuring based on a selection of thematic areas from the Doughnut Economics concept: **Ecological Ceilings** and **Social Foundations**.

---
```

**Conventions:**
- Use `**Goal**:` for activity objectives
- Bold the "Goal" label
- Clear, actionable instructions

---

## 5. Image Handling

### Standard Images (Centered/Sized)

```markdown
![width:700px center](images/filename.png)
```

**Size Options:**
- `width:XXXpx` - Set specific width
- `height:XXXpx` - Set specific height
- `center` - Center alignment

**Examples:**
```markdown
![height:380px](images/pt01_PB-over-time-v3_2_1920x627.png)
![width:650px center](images/pt01_slide25_img1_726x451.png)
```

### Background Images

For images as slide backgrounds:

```markdown
![bg](images/filename.jpg)
```

**Background Options:**
- `![bg]` - Full background
- `![bg left]` or `![bg right]` - Split layout
- `![bg left:XX%]` or `![bg right:XX%]` - Custom split ratio
- `![bg fit]` or `![bg contain]` - Fit image without cropping
- `![bg XX%]` - Scale background to percentage

**Examples:**
```markdown
![bg left 90%](images/pt01_slide13_img1_680x680.png)
![bg right:74% 105%](images/pt01_slide06_img1_1040x776.png)
![bg right:30% contain](images/pt01_slide20_img1_704x396.png)
```

### Multiple Background Images

Stack multiple `![bg]` directives for layered backgrounds:

```markdown
![bg](images/image1.jpg)
![bg](images/image2.jpg)
![bg](images/image3.jpg)
![bg](images/image4.jpg)
```

**Example from Slide 5:**
```markdown
![width:700px center](images/pt01_slide05_img3_1206x240.png)
![bg](images/pt01_slide05_img1_692x745.jpg)
![bg](images/pt01_slide05_img2_558x694.jpg)
![bg](images/pt01_slide05_img4_400x300.jpg)
![bg](images/pt01_slide05_img5_800x533.jpg)
```

### Combined Content and Background

```markdown
# Slide Title

Content here.

![bg right:50% contain](images/background.png)
```

---

## 6. Citations and References

### Academic Citations (Footnote Style)

Use H6 (six `#` symbols) for citations at the bottom of slides:

```markdown
###### Author, A., & Author, B. (Year). Title. Journal/Publisher.
```

**Examples:**
```markdown
###### Steffen, W., Crutzen, P. J., & McNeill, J. R. (2016). The Anthropocene: Are humans now overwhelming the great forces of nature?. In The New World History (pp. 440-459). University of California Press.

###### Raworth, K. (2018). Doughnut economics: Seven ways to think like a 21st century economist. Chelsea Green Publishing.
```

### Image Credits

For image source attribution:

```markdown
###### Source: Author/Organization
```

**Example:**
```markdown
###### Source: Jarker/Lokrantz/Azote
```

### Long Attribution Text

For detailed credits or descriptions:

```markdown
###### The evolution of the planetary boundaries framework. (Credit: Azote for Stockholm Resilience Centre, Stockholm University. Based on Sakschewski and Caesar et al. 2025, Richardson et al. 2023, Steffen et al. 2015, and Rockström et al. 2009).
```

---

## 7. Hyperlinks

### External Links (Videos, Websites)

Format links with descriptive text in brackets:

```markdown
[Description (Source/Type, Year)](https://url)
```

**Examples:**
```markdown
An [Introduction by Johan Rockström (TED Talk, 2010)](https://www.youtube.com/watch?v=RgqtrlixYR4) on the state of the world.

An interesting take on the connections between the issues by [Hans Rosling (TED Talk, 2010)](https://www.youtube.com/watch?v=fTznEIZRkLg) .
```

**Convention:** Include context in link text (speaker, type, year)

---

## 8. Custom Styling (Scoped CSS)

For complex layouts, use scoped CSS within slides:

```markdown
<style scoped>
.cols {
  display: grid;
  grid-template-columns: 50% 50%;
  gap: 2rem;
  padding-right: 1rem;
}
</style>

<div class="cols">

Content in first column.

Content in second column.

</div>
```

**Two-Column Layout Example:**

```markdown
<style scoped>
.cols {
  display: grid;
  grid-template-columns: 50% 50%;
  gap: 2rem;
  padding-right: 1rem;
}
</style>

<div class="cols">

**Weak sustainability** is an idea within environmental economics which states that human capital can substitute natural capital.

**Strong sustainability** as used in ecological economics assumes that human capital and natural capital are complementary, but not interchangeable.

</div>
```

**Conventions:**
- Use `.cols` class name for multi-column layouts
- `gap: 2rem;` for consistent spacing
- `padding-right: 1rem;` to prevent edge overflow
- Leave blank lines between div tags and content for proper markdown parsing

---

## 9. Text Formatting

### Bold Text

Use `**double asterisks**` for emphasis:

```markdown
**The social foundation** – below which lies critical human deprivation

**The ecological ceiling** – beyond which lies critical planetary degradation
```

### Italic Text

Use `*single asterisks*` or `_underscores_` for italics:

```markdown
*"We are searching for a model output..."*
```

### Bold in Headings

For emphasis within headings or goal statements:

```markdown
## **Goal**: Clear objective statement.
```

### Quoted Text

Use standard markdown blockquotes for quoted passages:

```markdown
"Sustainable development is a development that meets the needs of the present without compromising the ability of future generations to meet their own needs".
```

---

## 10. Comments and Notes

### Slide Comments

Use HTML comments for notes not displayed in presentation:

```markdown
<!-- Notes:
Additional information or speaker notes here.
-->
```

**Example:**
```markdown
<!-- Notes:
An Article from 2015 "Only eight countries meet two key conditions for sustainable development as United Nations adopts Sustainable Development Goals":

Algeria, Colombia, Cuba, Ecuador, Georgia, Jamaica, Jordan and Sri Lanka are the only countries...
-->
```

### Commented-Out Slides

To temporarily disable a slide, use comment tags:

```markdown
<!-- Notes:
# State of the world  - Connections

## Question

For the challenges identified – how do they relate to each other?

-->
```

---

## 11. Image Naming Convention

### File Naming Pattern

Images follow a structured naming convention:

```
pt{XX}_slide{YY}_img{Z}_{width}x{height}.{ext}
```

**Components:**
- `pt{XX}` - Part number (e.g., `pt01` for Part 1)
- `slide{YY}` - Slide number (e.g., `slide05` for slide 5)
- `img{Z}` - Image number on that slide (e.g., `img1`, `img2`)
- `{width}x{height}` - Original dimensions in pixels
- `{ext}` - File extension (png, jpg, etc.)

**Examples:**
```
pt01_slide05_img1_692x745.jpg
pt01_slide05_img2_558x694.jpg
pt01_slide05_img3_1206x240.png
pt01_slide18_img1_200x250.png
pt01_PB-over-time-v3_2_1920x627.png  (special naming for diagrams)
pt01_1_Planetary-Boundaries_website_img_1_708x452.png
```

### Image Location

All images must be in:
```
slides/images/
```

Reference images with relative path:
```markdown
![alt](images/filename.png)
```

---

## 12. Content Structure Patterns

### Section Introduction Slide

```markdown
# Section Title

Brief description or subtitle.


---
```

**Example:**
```markdown
# Sustainability and Sustainable Development

History and Definitions.


---
```

### Concept Explanation Slide

```markdown
# Concept Title

Explanatory paragraph with clear, concise definition or description.

Optional additional details or context.


---
```

### Visual-Heavy Slide

```markdown
# Title

Brief descriptive text.

![sizing](images/filename.png)

###### Citation or source.

---
```

**Example:**
```markdown
# Pathways of the earth system

![Pathways](images/pt01_1_Planetary-Boundaries_website_img_1_708x452.png)

###### Steffen, W., Rockström, J., Richardson, K., Lenton, T. M., Folke, C., Liverman, D., ... & Schellnhuber, H. J. (2018). Trajectories of the Earth System in the Anthropocene. Proceedings of the National Academy of Sciences, 115(33), 8252-8259.


---
```

### Split Content-Image Slide

```markdown
# Title

Text content on left side.

![bg right:XX% contain](images/filename.png)

###### Optional citation.

---
```

### Historical/Biography Slide

```markdown
# Title

Date/Year, **Person Name** "Quote or key contribution."

Descriptive paragraph.

![bg right:33%](images/portrait.png)
![bg](images/document.png)


---
```

**Example:**
```markdown
# Sylvicultura oeconomica

1713, **Hans Carl von Carlowitz** "Sylvicultura oeconomica" or the "economic news and instructions for the natural growing of wild trees (...) requires the careful management of sustainable forestry resources."

His book Sylvicultura oeconomica, oder **haußwirthliche Nachricht und Naturmäßige Anweisung zur wilden Baum-Zucht** (1713) was the first comprehensive treatise about forestry. He is considered to be the father of sustainable yield forestry.

![bg right:33%](images/pt01_slide18_img1_200x250.png)
![bg](images/pt01_slide18_img2_498x810.png)


---
```

---

## 13. Typography Conventions

### Headings Hierarchy

- **H1 (`#`)**: Slide titles (one per slide)
- **H2 (`##`)**: Subtitles, activity goals
- **H3-H5 (`###`-`#####`)**: Rarely used; avoid if possible
- **H6 (`######`)**: Citations and attributions only

### Line Spacing

- Two blank lines before `---` slide separator
- One blank line between content blocks
- No blank lines within paragraphs (use line breaks for continuation)

### Punctuation

- Use en-dash `–` for ranges and separators in definitions
- Use em-dash `—` sparingly
- Period at end of sentences, even in bullet points (when used)

---

## 14. Best Practices

### DO:
✅ Start every file with proper frontmatter and description comment
✅ Use `<!-- _class: title -->` for the first slide
✅ Apply consistent image sizing and positioning
✅ Include proper citations using H6
✅ Use two blank lines before slide separators
✅ Keep slide titles clear and concise (single H1)
✅ Use background images for visual impact
✅ Add speaker notes in comments when needed

### DON'T:
❌ Use multiple H1 headings on one slide
❌ Forget the description comment after frontmatter
❌ Skip blank lines before `---`
❌ Use absolute paths for images (use `images/` relative path)
❌ Mix different citation styles
❌ Overcrowd slides with too much text
❌ Use inconsistent spacing patterns

---

## 15. Complete Slide Templates

### Template 1: Basic Content Slide

```markdown
# Slide Title

Clear, concise content explaining the topic.

Additional paragraph if needed.


---
```

### Template 2: Image + Citation Slide

```markdown
# Slide Title

![width:700px center](images/diagram.png)

###### Author, A., & Author, B. (Year). Title. Journal/Publisher.


---
```

### Template 3: Split Layout Slide

```markdown
# Title

Content on the main area (left side by default).

![bg right:50% contain](images/visual.png)

###### Optional citation.

---
```

### Template 4: Two-Column Text Slide

```markdown
# Title

<style scoped>
.cols {
  display: grid;
  grid-template-columns: 50% 50%;
  gap: 2rem;
  padding-right: 1rem;
}
</style>

<div class="cols">

Left column content here.

Right column content here.

</div>


---
```

### Template 5: Activity/Groupwork Slide

```markdown
<!-- _class: groupwork -->

# Activity Name

## **Goal**: Clear objective for the activity.

Detailed instructions or context.

---
```

### Template 6: Quote/Definition Slide

```markdown
# Concept Title

"Key quote or definition goes here."

Additional context or explanation.

![bg right:30% contain](images/related-image.png)

###### Source attribution.


---
```

---

## 16. Quality Checklist

Before finalizing a presentation, verify:

- [ ] Frontmatter includes `marp: true`, `theme: neutral`, `size: 16:9`
- [ ] Description comment added after frontmatter
- [ ] Title slide uses `<!-- _class: title -->` and proper format
- [ ] All slides have clear H1 titles
- [ ] Images use relative paths (`images/filename`)
- [ ] Citations use H6 format (`######`)
- [ ] Two blank lines before each `---`
- [ ] Consistent spacing throughout
- [ ] All external links include context (speaker, type, year)
- [ ] Special classes (`groupwork`, `title`) properly applied
- [ ] No broken image links
- [ ] Speaker notes in comments where appropriate
- [ ] File builds successfully with Marp CLI

---

## 17. Building the Presentation

### Local Build Commands

**HTML only:**
```bash
marp --theme slides/themes/neutral.css --html slides/filename.md -o output.html --allow-local-files
```

**PDF only:**
```bash
marp --theme slides/themes/neutral.css --pdf slides/filename.md -o output.pdf --allow-local-files
```

**Both formats:**
```bash
marp --theme slides/themes/neutral.css --html slides/filename.md -o output.html --allow-local-files
marp --theme slides/themes/neutral.css --pdf slides/filename.md -o output.pdf --allow-local-files
```

### Automated Deployment

When you push to the `main` branch, GitHub Actions automatically:
1. Builds all `.md` files in `slides/` to HTML and PDF
2. Applies the neutral theme
3. Copies images to `dist/`
4. Generates index page with descriptions
5. Deploys to GitHub Pages

---

## 18. Additional Resources

- **Marp Documentation**: https://marpit.marp.app/
- **Marp CLI Guide**: https://github.com/marp-team/marp-cli
- **Theme File**: [slides/themes/neutral.css](slides/themes/neutral.css)
- **Project README**: [README.md](README.md)
- **Deployment Guide**: [DEPLOYMENT_GUIDE.md](DEPLOYMENT_GUIDE.md)
- **Project Documentation**: [CLAUDE.md](CLAUDE.md)

---

## Quick Reference Card

```markdown
---
marp: true
theme: neutral
size: 16:9
---

<!-- description: Brief description for index. -->

<!-- _class: title -->


# Main Title
## Subtitle

IMC University of Applied Sciences Krems, Austria
Roman Mesicek


---

# Regular Slide

Content here.


---

# Slide with Image

![width:700px center](images/diagram.png)

###### Citation here.


---

# Split Layout

Content on left.

![bg right:50% contain](images/visual.png)

---

<!-- _class: groupwork -->

# Activity Title

## **Goal**: Objective statement.

Instructions here.

---
```

---

*Last Updated: October 29, 2025*
*Based on: SAI_Part_01.md and SAI_Part_02.md template analysis*
*Generated for Claude Desktop and other AI assistants*
