# ACADEMIC WHITEPAPER

## Preparing GitHub-Based Infrastructure for Teaching Sustainability and Business Responsibility in AI Education: A Pre-Implementation Design Document

**Roman Mesicek**  
University of Applied Sciences IMC Krems, Austria  
roman.mesicek@fh-krems.ac.at

**Winter Semester 2025**

---

### ABSTRACT

This whitepaper documents the design and preparation of GitHub-based collaborative infrastructure for teaching sustainability challenges and business responsibility within a master-level AI course at the University of Applied Sciences IMC Krems. The RAI-SAG25 course infrastructure, prepared for deployment in the upcoming semester, integrates version control and automated content delivery systems into the first half of a 5-ECTS course focusing on environmental impacts, business ethics, and corporate responsibility in AI development. This pre-implementation report describes the technical architecture, pedagogical rationale, and anticipated challenges of employing software development workflows in teaching sustainability and business responsibility concepts. The infrastructure is designed to model sustainable practices while delivering content on responsible AI deployment in business contexts.

**Keywords:** Sustainability education, Business responsibility, AI ethics, GitHub, Educational infrastructure, Green computing, Pre-implementation design, Open educational resources

---

## 1. INTRODUCTION

The preparation of educational infrastructure for teaching sustainability and business responsibility in AI contexts requires careful consideration of both content delivery mechanisms and the implicit messages conveyed through chosen technologies. As organizations increasingly grapple with the environmental and ethical implications of AI deployment, educational programs must prepare students to navigate these challenges from business and sustainability perspectives (Schwartz et al., 2020).

This whitepaper describes the preparation of infrastructure for the RAI-SAG25 course ("Sustainability and AI for Green") at the University of Applied Sciences IMC Krems, scheduled to begin in one month. Specifically, this document focuses on the first half of the course, which addresses sustainability challenges and business responsibility in AI contexts. The infrastructure employs GitHub as a central platform for content delivery and anticipated student interaction, though actual deployment and student engagement remain future considerations.

The infrastructure design addresses three preparatory objectives:

1. **Content organization:** Structuring materials on sustainability challenges and business responsibility in AI
2. **Delivery mechanism:** Establishing automated systems for content distribution and updates
3. **Pedagogical alignment:** Ensuring infrastructure choices reflect sustainable and responsible practices

This document serves as a design record and implementation guide for educators considering similar approaches, while acknowledging that empirical validation awaits actual course delivery.

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

The first half of the course addresses:

**Lecture 1: Environmental Context**
- Climate crisis and information technology interconnections
- Carbon footprint of AI systems from business perspectives
- Corporate environmental responsibility in AI deployment

**Lecture 2: Business Models and Sustainability**
- Sustainable business models in AI contexts
- Cost-benefit analyses including environmental externalities
- Stakeholder management in responsible AI initiatives

**Lecture 3: Regulatory and Ethical Frameworks**
- EU AI Act implications for business
- Corporate governance for responsible AI
- ESG reporting and AI transparency requirements

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

## 8. FUTURE IMPLEMENTATION PLANS

### 8.1 Pre-Launch Preparation (Current Phase)

**Completed:**
- Repository structure established
- Core content for weeks 1-3 prepared
- Automation workflows configured
- Initial case studies selected

**Remaining (Next Month):**
- Complete content for weeks 4-7
- Develop assessment rubrics
- Create onboarding materials for GitHub
- Test automation systems

### 8.2 Launch Phase (Course Start)

**Week 1 Priorities:**
- Student orientation to GitHub interface
- Establishment of discussion norms
- Initial feedback collection on accessibility
- Adjustment based on actual enrollment and backgrounds

### 8.3 Iterative Refinement

The infrastructure anticipates continuous improvement through:
- Weekly feedback collection via GitHub Issues
- Mid-term assessment of technical barriers
- End-of-term comprehensive evaluation
- Documentation of lessons learned for future iterations

---

## 9. LIMITATIONS AND CONSIDERATIONS

### 9.1 Design Limitations

This pre-implementation design acknowledges:

**Untested assumptions:** Student engagement patterns remain theoretical until actual deployment

**Context specificity:** Design reflects specific institutional context and may require adaptation elsewhere

**Technical prerequisites:** Infrastructure assumes basic digital literacy and internet access

**Content scope:** Focus on business responsibility represents partial course coverage

### 9.2 Evaluation Needs

Post-implementation evaluation should address:
- Effectiveness of GitHub for business-focused content
- Student perception of infrastructure-message alignment
- Technical barrier impact on learning outcomes
- Comparative analysis with traditional delivery methods

---

## 10. CONCLUSION

The preparation of GitHub-based infrastructure for teaching sustainability and business responsibility in AI contexts represents an attempt to align delivery mechanisms with pedagogical objectives. By modeling transparency, efficiency, and accountability through the chosen platform, the infrastructure aims to reinforce concepts central to responsible business practices in AI deployment.

This pre-implementation documentation provides a snapshot of design decisions and anticipated challenges before actual student engagement. The focus on business responsibility and sustainability challenges in the first half of the course necessitates careful balance between technical infrastructure and business-oriented content. 

As educational institutions increasingly recognize the importance of preparing students for responsible AI deployment in corporate contexts, approaches that demonstrate sustainable and transparent practices through their infrastructure warrant exploration. This design document offers one approach for consideration, with full recognition that effectiveness claims await empirical validation through actual implementation.

---

## REFERENCES

Dillenbourg, P. (1999). *Collaborative learning: Cognitive and computational approaches*. Oxford: Elsevier Science.

Lago, P., Koçak, S. A., Crnkovic, I., & Penzenstadler, B. (2015). Framing sustainability as a property of software quality. *Communications of the ACM*, 58(10), 70-78.

McLuhan, M. (1964). *Understanding media: The extensions of man*. New York: McGraw-Hill.

Patterson, D., Gonzalez, J., Le, Q., Liang, C., Munguia, L. M., Rothchild, D., ... & Dean, J. (2021). Carbon emissions and large neural network training. *arXiv preprint arXiv:2104.10350*.

Schwartz, R., Dodge, J., Smith, N. A., & Etzioni, O. (2020). Green AI. *Communications of the ACM*, 63(12), 54-63.

Strubell, E., Ganesh, A., & McCallum, A. (2019). Energy and policy considerations for deep learning in NLP. *Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics*, 3645-3650.

UNESCO. (2019). *Recommendation on Open Educational Resources (OER)*. Paris: UNESCO.

Verdecchia, R., Procaccianti, G., Malavolta, I., Lago, P., & Koedijk, J. (2017). Estimating energy impact of software releases and deployment strategies: The KPMG case study. *2017 ACM/IEEE International Symposium on Empirical Software Engineering and Measurement*, 257-266.

Walker, T., Wendt, S., Goubran, S., & Schwartz, T. (2023). *Artificial intelligence for sustainability*. Cham: Palgrave Macmillan. https://doi.org/10.1007/978-3-031-49979-1

Wenger, E. (1998). *Communities of practice: Learning, meaning, and identity*. Cambridge: Cambridge University Press.

---

## APPENDIX: REPOSITORY ACCESS

**Course Repository:** https://github.com/romanmesicek/rai-sai25  
**Course Website:** https://romanmesicek.github.io/rai-sai25/  
**License:** Creative Commons Attribution 4.0 International (CC BY 4.0)  
**Status:** Pre-implementation (Course will take place in November 2025)

---

**Document Version:** 3.0  
**Revision Date:** October 19, 2025  
**Word Count:** ~2,400 words

---
