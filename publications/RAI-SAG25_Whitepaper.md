# ACADEMIC WHITEPAPER

## GitHub-Based Infrastructure for Teaching Sustainability and Business Responsibility in AI Education: Design, Implementation, and Pilot Findings

**Roman Mesicek**
University of Applied Sciences IMC Krems, Austria
roman.mesicek@fh-krems.ac.at

**Winter Semester 2025**

---

### ABSTRACT

This whitepaper documents the design, implementation, and pilot evaluation of GitHub-based collaborative infrastructure for teaching sustainability challenges and business responsibility within a master-level AI course at the University of Applied Sciences IMC Krems. The RAI-SAG25 course ("Sustainability and AI for Green"), delivered in Winter Semester 2025, integrated version control and automated content delivery systems into the first half of a 5-ECTS course focusing on environmental impacts, business ethics, and corporate responsibility in AI development. Building on initial design documentation, this paper now incorporates empirical findings from post-course evaluation (n=4), including evidence of awareness improvement among participants, moderate confidence gains in applying sustainability frameworks, and a notable finding that the GitHub infrastructure choice was perceived as pedagogically neutral by all respondents. The paper presents both the technical architecture and pedagogical rationale while critically examining assumptions about infrastructure-as-pedagogy in light of actual student feedback.

**Keywords:** Sustainability education, Business responsibility, AI ethics, GitHub, Educational infrastructure, Green computing, Pilot evaluation, Open educational resources

---

## 1. INTRODUCTION

The preparation of educational infrastructure for teaching sustainability and business responsibility in AI contexts requires careful consideration of both content delivery mechanisms and the implicit messages conveyed through chosen technologies. As organizations increasingly grapple with the environmental and ethical implications of AI deployment, educational programs must prepare students to navigate these challenges from business and sustainability perspectives (Schwartz et al., 2020).

This whitepaper documents the RAI-SAG25 course ("Sustainability and AI for Green") at the University of Applied Sciences IMC Krems, delivered in Winter Semester 2025. Specifically, this document focuses on the first half of the course, which addressed sustainability challenges and business responsibility in AI contexts. The infrastructure employed GitHub as a central platform for content delivery, with post-course evaluation providing initial empirical insights into this approach.

The infrastructure addressed three objectives:

1. **Content organization:** Structuring materials on sustainability challenges and business responsibility in AI
2. **Delivery mechanism:** Establishing automated systems for content distribution and updates
3. **Pedagogical alignment:** Ensuring infrastructure choices reflect sustainable and responsible practices

This document serves as both a design record and an initial evaluation report for educators considering similar approaches. While the pilot sample size (n=4) limits generalizability, the findings offer preliminary evidence regarding both content effectiveness and infrastructure perception.

---

## 2. THEORETICAL FRAMEWORK

### 2.1 Sustainability and Business Responsibility in AI Education

The integration of sustainability concepts with business responsibility in AI education responds to increasing corporate attention to environmental, social, and governance (ESG) criteria. Organizations require professionals who understand both the technical capabilities of AI and its broader implications for sustainable business practices (Lago et al., 2015). This necessitates educational approaches that connect environmental considerations with business decision-making frameworks.

### 2.2 Infrastructure as Pedagogy

The choice of educational infrastructure carries pedagogical implications. By selecting GitHub—a platform designed for collaborative, transparent development—the course infrastructure embodies principles of openness and accountability relevant to responsible business practices. This alignment between medium and message follows McLuhan's (1964) observation that the medium itself communicates beyond its content, though the effectiveness of this implicit teaching awaits empirical investigation.

### 2.3 Open Educational Resources in Business Education

The adoption of open educational resources (OER) in business and sustainability education aligns with UNESCO (2019) recommendations while modeling transparency principles essential to responsible business practices. Public repositories demonstrate accountability and enable stakeholder scrutiny—concepts central to corporate sustainability reporting and responsible AI governance.

---

## 3. COURSE CONTEXT AND SCOPE

### 3.1 Program Positioning

The infrastructure serves the first half of the RAI-SAG25 course within the Master's program "Engineering Responsible AI Systems" at IMC Krems. This portion focuses on foundational concepts before transitioning to technical implementation in the course's second half (taught by another instructor).

### 3.2 Content Focus: Sustainability and Business Responsibility

The first half of the course addressed three interconnected sessions:

**Session 1: Planetary Boundaries & Social Foundation**
- The Anthropocene and state of our world
- Planetary Boundaries framework (Rockström et al., 2009)
- Doughnut Economics model integrating ecological ceilings and social foundations (Raworth, 2017)
- History and evolution of sustainability concepts
- Weak vs. Strong Sustainability distinctions
- Sustainable Development Goals (SDGs) and Triple Bottom Line

**Session 2: Business Ethics & Responsibility**
- Foundations of business ethics and ethical theory
- Corporate Social Responsibility (CSR) frameworks and evolution
- CSR Pyramid and maturity models (Carroll, 1991; Dyllick & Muff, 2015)
- Stakeholder management and engagement strategies
- Non-financial reporting standards (GRI, SASB, TCFD, ESRS)
- EU Green Deal and corporate due diligence requirements

**Session 3: Artificial Intelligence for Green**
- Environmental impact and carbon footprint of AI systems
- Data center resource consumption and e-waste considerations
- Green AI strategies and energy-efficient machine learning
- AI applications for sustainability (precision agriculture, smart grids, circular economy)
- Carbon-aware computing and sustainable AI development practices

### 3.3 Learning Objectives for Business Responsibility Component

The infrastructure supports three learning objectives specific to the business responsibility focus:

**LO1:** Analyze sustainability challenges facing organizations deploying AI systems, considering stakeholder impacts and environmental costs

**LO2:** Evaluate business cases for sustainable AI practices, including risk assessment and opportunity identification

**LO3:** Design governance frameworks for responsible AI implementation in corporate contexts

---

## 4. INFRASTRUCTURE DESIGN

### 4.1 Repository Structure

The prepared repository organizes content to reflect the sustainability-focused curriculum:

```
rai-sai25/
├── slides/                   # Marp presentation slides
│   ├── *.md                 # Markdown-based presentations
│   ├── images/              # Images for presentations
│   └── themes/              # Custom Marp themes
│       └── neutral.css      # Neutral presentation theme
├── resources/               # Additional course materials
│   ├── useful-tools.md
│   ├── external-links.md
│   └── contact-support.md
├── papers/                  # Academic papers (PDFs)
│   └── *.pdf               # Course reference papers
├── publications/            # Academic publications about the course
│   └── *.md                # Whitepapers and documentation
├── .github/workflows/       # GitHub Actions automation
│   └── deploy-slides.yml   # Automated deployment workflow
├── README.md               # Repository documentation
├── SAI_Syllabus.md        # Complete course syllabus
└── DEPLOYMENT_GUIDE.md    # Deployment documentation
```

This structure anticipates iterative refinement based on student needs once the course begins.

### 4.2 Content Preparation

Materials prepared for the repository include:

**Lecture Slides:** Markdown-based presentations focusing on business implications of sustainability challenges, convertible to multiple formats for accessibility

**Case Studies:** Real-world examples of organizations addressing AI sustainability, prepared with discussion prompts and analysis frameworks

**Assessment Templates:** Structured formats for sustainability impact assessments, stakeholder analyses, and governance framework development

**Reading Lists:** Curated academic and industry publications on sustainable business practices in AI, with proper licensing verification

### 4.3 Automation Setup

The infrastructure includes automated workflows to:

- Convert Markdown content to presentation formats (HTML, PDF)
- Generate navigable index pages for content discovery
- Validate links and references to prevent broken resources
- Deploy updates to GitHub Pages for web access

These automations reduce maintenance overhead while demonstrating efficient resource utilization—a principle relevant to sustainable business operations.

---

## 5. PEDAGOGICAL DESIGN CONSIDERATIONS

### 5.1 Anticipated Student Profile

The infrastructure design assumes master's students with:
- Bachelor's degrees in computer science, engineering, or business
- Basic familiarity with sustainability concepts
- Limited experience with version control systems
- Interest in responsible AI from business perspectives

### 5.2 Scaffolding Approach

Recognizing varied technical backgrounds, the infrastructure includes:

**Progressive Engagement Levels:**
1. **Passive consumption:** Reading materials via web interface
2. **Active discussion:** Using GitHub Issues for case study debates
3. **Collaborative contribution:** Suggesting improvements via pull requests

Students can engage at comfortable levels while observing more advanced interactions.

### 5.3 Business Responsibility Modeling

The infrastructure itself demonstrates responsible business practices:

- **Transparency:** All materials publicly accessible
- **Accountability:** Change history tracked and attributed
- **Efficiency:** Automated processes minimize resource waste
- **Stakeholder engagement:** Open to external contributions and review

These implicit demonstrations complement explicit instruction on corporate responsibility.

---

## 6. ANTICIPATED CHALLENGES

### 6.1 Technical Barriers

Expected challenges include:

**Student-facing:**
- Unfamiliarity with Git/GitHub among business-oriented students
- Learning curve for Markdown syntax
- Navigation of repository structure

**Instructor-facing:**
- Maintaining content organization as materials accumulate
- Managing potential contributions while ensuring quality
- Balancing openness with assessment integrity

### 6.2 Content Considerations

The business responsibility focus raises specific concerns:

- Rapid evolution of regulations (e.g., EU AI Act updates)
- Sensitivity of corporate case studies
- Balancing theoretical frameworks with practical applications
- Connecting technical sustainability metrics to business decision-making

### 6.3 Assessment Design

The open nature of materials necessitates assessment approaches that:
- Emphasize application over recall
- Require original analysis of new cases
- Focus on stakeholder-specific recommendations
- Evaluate critical thinking about trade-offs

Detailed assessment rubrics are under development for deployment when the course begins.

---

## 7. RELATIONSHIP TO BROADER CURRICULUM

### 7.1 Integration with Technical Components

While this infrastructure serves the business-focused first half, it provides foundation for the technical second half by:
- Establishing sustainability priorities that inform technical choices
- Creating business context for green AI implementation
- Developing governance frameworks that guide technical development

### 7.2 Program-Level Alignment

The infrastructure supports program objectives for "Engineering Responsible AI Systems" by:
- Modeling responsible development practices
- Connecting business and technical perspectives
- Demonstrating transparency and accountability
- Preparing students for interdisciplinary collaboration

---

## 8. IMPLEMENTATION REPORT

### 8.1 Course Delivery (November–December 2025)

The course was delivered across three sessions in Winter Semester 2025, with the following implementation details:

**Infrastructure Deployment:**
- Repository structure finalized and publicly accessible
- Automated deployment via GitHub Actions operational throughout
- All lecture slides, resources, and papers available via GitHub Pages
- Content delivered in HTML and PDF formats with consistent theming

**Session Delivery:**
- Session 1: Planetary Boundaries & Social Foundation (including group exercise with poster creation)
- Session 2: Business Ethics & Responsibility (including company sustainability analysis)
- Session 3: Artificial Intelligence for Green (including sustainable AI system design exercise)

**Collaborative Activities:**
- Poster-based group exercises requiring synthesis across sustainability domains
- Company case study analyses using Dyllick/Muff CSR maturity framework
- Scenario-based AI system design incorporating ethical considerations

### 8.2 Post-Course Evaluation

A voluntary post-course questionnaire was administered via Microsoft Forms, collecting responses between 5–12 December 2025 (n=4).

**Respondent Demographics:**
- Professional backgrounds: 2 IT/Technical, 1 Other, 1 unspecified
- Current role involves AI: 1 Yes, 3 No/unspecified
- Sustainability in job description: 0 Yes, 3 No, 1 Partial

### 8.3 Iterative Refinement Outcomes

Based on implementation experience and feedback, the following refinements are documented for future iterations:

**Content Refinements:**
- Explicit "big picture" framing needed before collaborative poster exercises
- Session 3 content depth showed heterogeneous responses (1 Too Advanced, 2 Just Right, 1 Too Basic), suggesting need for differentiated scaffolding
- Doughnut Economics framework identified as particularly memorable and applicable

**Delivery Refinements:**
- Consider MS Teams integration for materials access (noted preference for institutional platform consistency)
- Maintain mixed format approach (lectures, case studies, discussions) based on preference data

---

## 9. PILOT FINDINGS

### 9.1 Quantitative Results

The post-course questionnaire yielded the following quantitative findings across the three sessions:

**Session Clarity Ratings (1-5 scale):**

| Session | Clarity | Relevance |
|---------|---------|-----------|
| Session 1: Planetary Boundaries | 4.75 | 4.50 |
| Session 2: Business Ethics | 4.25 | 4.25 |
| Session 3: AI for Green | 4.75 | 4.50 |

**Content Depth Assessment:**
- Session 1: 4/4 rated "Just Right"
- Session 2: 4/4 rated "Just Right"
- Session 3: 1 "Too Advanced," 2 "Just Right," 1 "Too Basic"

**Session Logic and Flow:** All 4 respondents (100%) perceived clear progression between sessions.

**Awareness Change (AI environmental/societal impact):**

| Level | Before Course | After Course |
|-------|---------------|--------------|
| Slightly aware | 2 | 0 |
| Moderately aware | 2 | 2 |
| Very aware | 0 | 2 |

**Confidence Levels (1-5 scale):**

| Competency | Mean Score |
|------------|------------|
| Explain planetary boundaries in AI context | 3.50 |
| Apply ethical frameworks to AI projects | 3.75 |
| Identify green AI opportunities | 3.75 |

**Practical Application Likelihood:** 3 respondents indicated "Likely" or "Very likely" to apply concepts within 6 months; 1 indicated "Neutral."

**Format Preferences:** 2 preferred mixed approach, 1 preferred case study analysis, 1 preferred interactive discussions. No respondents preferred lecture-only format.

### 9.2 GitHub Infrastructure Assessment

A central design hypothesis was that GitHub-based infrastructure would carry implicit pedagogical value by modeling transparency, version control, and open practices. This assumption requires significant qualification based on pilot findings.

**Infrastructure Effect on Learning:** All 4 respondents (100%) reported "No effect" when asked how GitHub-based delivery affected their learning.

**Possible Explanations:**
1. **Content consumption mode:** Students may have accessed materials primarily via the web interface (GitHub Pages), experiencing it as a standard website rather than a collaborative development platform
2. **Limited Git familiarity:** The sample included predominantly non-technical or AI-adjacent roles; implicit infrastructure messaging may require baseline familiarity to perceive
3. **Transparency as baseline expectation:** For digitally native master's students, openly accessible course materials may be expected rather than pedagogically notable

**Platform Preference Feedback:** One respondent noted: "MS Teams would have been easier because most lecturers use teams (only for simplicity, not because I am a fan of Teams)." This suggests that institutional platform consistency may outweigh theoretical benefits of specialized infrastructure for some learners.

**Implications for Infrastructure-as-Pedagogy:** The null finding does not invalidate the infrastructure choice but suggests that implicit pedagogical messaging through platform selection may be less effective than explicit instruction. Future iterations might benefit from direct discussion of why GitHub was chosen and how version control relates to transparency and accountability in AI governance.

### 9.3 Qualitative Findings

**Most Valuable Learning:**
One respondent provided detailed feedback: "Taking into account the whole picture of sustainability, also the social aspect. In practice, sustainability is often mistaken with only 'CO2' emissions. The course was very helpful to get the whole picture of sustainability on a high level. This is a good starting point for taking a deep dive in any of the topics."

**Key Takeaway:**
"Sustainability is much more than minimizing CO2 emissions"

**Concepts to Apply First:** Respondents identified "AI For Green" and "Donut Diagram" (Doughnut Economics) as concepts they would apply first.

**Improvement Suggestions:**
"A bit more clarification before the task where the Flipchart was drawn. Our group focused too much on a Sub-topic which didn't help for the Big Picture."

This feedback directly informs scaffolding recommendations: collaborative exercises require explicit framing of expected scope and integration objectives.

### 9.4 Learning Outcomes Evidence

Mapping findings to the stated learning objectives:

**LO1 (Analyze sustainability challenges):** Supported by awareness improvement (shift from "Slightly aware" to "Moderately/Very aware") and qualitative feedback indicating expanded understanding of sustainability scope beyond carbon emissions.

**LO2 (Evaluate business cases):** Moderately supported by confidence ratings (3.75/5 for ethical frameworks application). Room for improvement through more applied case work.

**LO3 (Design governance frameworks):** Limited direct evidence. Confidence in identifying green AI opportunities (3.75/5) provides partial indication, but governance-specific assessment would strengthen future evaluation.

---

## 10. LIMITATIONS AND CONSIDERATIONS

### 10.1 Sample Size Limitations

The pilot evaluation is based on n=4 responses, which severely limits generalizability. Findings should be interpreted as formative rather than summative, providing directional insights for future iterations rather than definitive conclusions about pedagogical effectiveness.

**Specific limitations:**
- Response rate unknown (total enrollment not specified in available data)
- Self-selection bias likely (respondents may represent more engaged students)
- Small sample prevents meaningful subgroup analysis
- Statistical significance testing inappropriate at this sample size

### 10.2 Design Limitations

**Context specificity:** Design reflects specific institutional context and may require adaptation elsewhere

**Technical prerequisites:** Infrastructure assumes basic digital literacy and internet access

**Content scope:** Focus on business responsibility represents partial course coverage

### 10.3 Evaluation Design Limitations

**Single-point measurement:** Pre/post awareness change relies on retrospective self-assessment rather than true pre-test

**Missing long-term follow-up:** 6-month application intentions cannot be validated without longitudinal data collection

**Limited demographic coverage:** Small sample prevents analysis of how professional background affects learning outcomes

---

## 11. CONCLUSION

The implementation of GitHub-based infrastructure for teaching sustainability and business responsibility in AI contexts yielded mixed evidence regarding its pedagogical value. While content delivery functioned as designed and session clarity ratings were high (4.25-4.75/5), the central hypothesis that infrastructure choice would carry implicit pedagogical weight was not supported by pilot data—all respondents reported the GitHub platform had no effect on their learning.

Content effectiveness showed more promising indicators. Participants demonstrated measurable awareness improvement regarding AI's environmental and societal impacts, with the proportion reporting "Very aware" increasing from 0% to 50%. The Doughnut Economics framework (Raworth, 2017) emerged as particularly memorable and applicable, with participants explicitly citing it as a concept they intended to apply professionally. Qualitative feedback indicated successful broadening of sustainability conceptualization beyond carbon-centric views.

The focus on business responsibility and sustainability challenges in the first half of the course achieved its objective of establishing foundations for technical implementation in subsequent sessions. However, Session 3 content depth ratings varied more than Sessions 1-2, suggesting heterogeneous prior knowledge that future iterations should address through differentiated materials or adaptive scaffolding.

For educators considering similar approaches, these pilot findings suggest: (1) infrastructure choices may need explicit pedagogical framing to achieve intended messaging effects; (2) mixed-format delivery combining lectures, case studies, and interactive discussions aligns with student preferences; (3) collaborative exercises benefit from explicit scope-setting to prevent sub-topic focus; and (4) frameworks providing holistic sustainability perspectives (e.g., Doughnut Economics) may be particularly effective for learners without extensive sustainability backgrounds.

Further research with larger samples is needed to validate these preliminary findings and to examine whether explicit infrastructure pedagogy (discussing why GitHub was chosen) would yield different perceptions than the implicit approach evaluated here.

---

## REFERENCES

Carroll, A. B. (1991). The pyramid of corporate social responsibility: Toward the moral management of organizational stakeholders. *Business Horizons*, 34(4), 39-48.

Dillenbourg, P. (1999). *Collaborative learning: Cognitive and computational approaches*. Oxford: Elsevier Science.

Dyllick, T., & Muff, K. (2015). Clarifying the meaning of sustainable business: Introducing a typology from business-as-usual to true business sustainability. *Organization & Environment*, 29(2), 156-174.

Lago, P., Koçak, S. A., Crnkovic, I., & Penzenstadler, B. (2015). Framing sustainability as a property of software quality. *Communications of the ACM*, 58(10), 70-78.

McLuhan, M. (1964). *Understanding media: The extensions of man*. New York: McGraw-Hill.

Patterson, D., Gonzalez, J., Le, Q., Liang, C., Munguia, L. M., Rothchild, D., ... & Dean, J. (2021). Carbon emissions and large neural network training. *arXiv preprint arXiv:2104.10350*.

Raworth, K. (2017). *Doughnut economics: Seven ways to think like a 21st-century economist*. London: Random House Business Books.

Rockström, J., Steffen, W., Noone, K., Persson, Å., Chapin, F. S., Lambin, E. F., ... & Foley, J. A. (2009). A safe operating space for humanity. *Nature*, 461(7263), 472-475.

Schwartz, R., Dodge, J., Smith, N. A., & Etzioni, O. (2020). Green AI. *Communications of the ACM*, 63(12), 54-63.

Strubell, E., Ganesh, A., & McCallum, A. (2019). Energy and policy considerations for deep learning in NLP. *Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics*, 3645-3650.

UNESCO. (2019). *Recommendation on Open Educational Resources (OER)*. Paris: UNESCO.

Verdecchia, R., Procaccianti, G., Malavolta, I., Lago, P., & Koedijk, J. (2017). Estimating energy impact of software releases and deployment strategies: The KPMG case study. *2017 ACM/IEEE International Symposium on Empirical Software Engineering and Measurement*, 257-266.

Walker, T., Wendt, S., Goubran, S., & Schwartz, T. (2023). *Artificial intelligence for sustainability*. Cham: Palgrave Macmillan. https://doi.org/10.1007/978-3-031-49979-1

Wenger, E. (1998). *Communities of practice: Learning, meaning, and identity*. Cambridge: Cambridge University Press.

---

## APPENDIX A: REPOSITORY ACCESS

**Course Repository:** https://github.com/romanmesicek/rai-sai25
**Course Website:** https://romanmesicek.github.io/rai-sai25/
**License:** Creative Commons Attribution 4.0 International (CC BY 4.0)
**Status:** Post-implementation (Course delivered Winter Semester 2025)

---

## APPENDIX B: EVALUATION DATA

The post-course questionnaire data (n=4) collected between 5–12 December 2025 is available in the repository at:
`development/Post-Course Questionnaire_ RAI-SAG25 Sustainability and AI for Green_Submissions_2026-01-08.csv`

**Data Collection Method:** Microsoft Forms voluntary questionnaire
**Response Period:** 5–12 December 2025
**Instrument:** Custom post-course evaluation covering session quality, learning outcomes, and infrastructure perception

---

**Document Version:** 4.0
**Revision Date:** January 8, 2026
**Word Count:** ~4,200 words

---
