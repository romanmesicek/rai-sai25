# ACADEMIC WHITEPAPER

## GitHub as Pedagogical Infrastructure for Sustainability and AI Education: Implementation and Preliminary Observations from the RAI-SAI25 Course

**Roman Mesicek**
University of Applied Sciences IMC Krems, Austria
roman.mesicek@imc.ac.at

**Winter Semester 2025**

---

### ABSTRACT

This whitepaper documents the implementation of GitHub-based collaborative infrastructure in the course "Sustainability and AI for Green" (RAI-SAI25), part of the Master of Science in Engineering program "Engineering Responsible AI Systems" at the University of Applied Sciences IMC Krems. The course (5 ECTS, 28 contact hours) employs version control, automated deployment, and collaborative workflows as integral components of the pedagogical approach. The paper describes the technical architecture, pedagogical rationale, and initial observations from deploying industry-standard development practices in an educational context focused on sustainable AI. While empirical evaluation remains ongoing, this implementation report provides a foundation for discussing the integration of software development workflows into sustainability-focused AI education.

**Keywords:** Sustainability education, AI education, GitHub, Version control, Collaborative learning, Educational technology, Green computing, Open educational resources

---

## 1. INTRODUCTION

The environmental impact of artificial intelligence systems presents educational challenges that require both theoretical understanding and practical engagement with sustainable development practices. As computational demands of AI systems continue to grow, with training large language models producing carbon emissions equivalent to multiple transatlantic flights (Strubell et al., 2019), educational programs must address both the environmental implications of AI and the methodologies for developing more sustainable systems.

This whitepaper describes the implementation of the RAI-SAI25 course ("Sustainability and AI for Green") at the University of Applied Sciences IMC Krems, Austria. The course integrates GitHub-based collaborative infrastructure into a curriculum focused on sustainable AI practices. Rather than treating version control and collaborative development as supplementary skills, the course positions these tools as central to understanding and practicing sustainable software development.

The implementation addresses three pedagogical objectives:

1. **Content objective:** Developing understanding of sustainability principles within AI development and deployment
2. **Process objective:** Acquiring competency in collaborative, version-controlled workflows standard in industry
3. **Integration objective:** Connecting sustainable development principles with practical software engineering practices

This paper provides a descriptive account of the course structure, technical implementation, and pedagogical considerations, offering a foundation for future empirical investigation and adaptation by other institutions.

---

## 2. THEORETICAL BACKGROUND

### 2.1 Version Control in Educational Contexts

The integration of version control systems in education has been explored across computer science curricula, though primarily in programming courses. Zagalsky et al. (2015) identified GitHub's emergence as a collaborative platform in education, noting its potential for transparency and peer learning. However, application in interdisciplinary contexts combining sustainability and AI remains underexplored.

Version control offers several pedagogical affordances relevant to sustainability education:
- **Transparency:** All changes are tracked and attributed
- **Iteration:** Content evolves through documented modifications
- **Collaboration:** Multiple contributors can work simultaneously
- **Reproducibility:** Previous states can be recovered and examined

### 2.2 Sustainability in AI Education

The intersection of sustainability and AI education requires addressing both the environmental costs of AI systems and their potential for environmental benefit. Current approaches typically separate these concerns into distinct courses on green computing or AI applications. The integration attempted in RAI-SAI25 follows recommendations from Lago et al. (2019) for embedding sustainability throughout technical curricula rather than treating it as an isolated topic.

### 2.3 Collaborative Learning Frameworks

The course design draws on established collaborative learning principles (Dillenbourg, 1999), particularly the notion that knowledge construction occurs through interaction with tools and peers. GitHub provides a digital environment where these interactions are documented and structured through pull requests, issues, and collaborative editing—mechanisms that mirror professional software development practices while supporting pedagogical goals.

---

## 3. COURSE STRUCTURE AND CONTENT

### 3.1 Program Context

The RAI-SAI25 course operates within the Master of Science in Engineering program "Engineering Responsible AI Systems" at IMC Krems. The program targets graduates of computer science and engineering bachelor programs, preparing them for roles requiring expertise in ethical, sustainable AI development.

### 3.2 Learning Outcomes

The course defines three primary learning outcomes aligned with the European Qualifications Framework Level 7:

**LO1:** Search for, assess, prepare, and present information on sustainable practices as components of business and industrial processes, focusing on AI systems that balance ecological and economic considerations

**LO2:** Select and apply appropriate AI tools to enhance sustainability in business operations while considering efficiency and environmental impact

**LO3:** Analyze how circular economy models, supported by AI systems, can be integrated into business strategies

### 3.3 Content Organization

The curriculum spans nine thematic areas across 14 weeks:

1. Climate crisis and information technology interconnections
2. Carbon footprint measurement and analysis for AI systems
3. Green AI strategies and implementation approaches
4. AI applications for environmental monitoring and optimization
5. Sustainable software development methodologies
6. Energy-efficient machine learning techniques
7. Life cycle assessment for AI systems
8. Circular economy principles in technology sectors
9. Infrastructure planning for sustainable AI deployment

### 3.4 Assessment Structure

Assessment combines multiple modalities:
- **Written examination (60%):** Tests conceptual understanding
- **Project deliverable (30%):** Requires practical application
- **Presentation (10%):** Evaluates communication skills

This distribution balances theoretical knowledge with practical application, though the effectiveness of this weighting requires empirical validation through student performance analysis.

---

## 4. TECHNICAL IMPLEMENTATION

### 4.1 Repository Architecture

The course materials reside in a public GitHub repository structured as follows:

```
rai-sai25/
├── slides/           # Markdown-based presentations
├── resources/        # Supplementary materials
├── papers/          # Academic literature (with proper licensing)
├── .github/
│   └── workflows/   # Automation scripts
├── themes/          # Visual styling
└── docs/            # Generated website
```

This structure separates source content from generated artifacts, following software engineering conventions while maintaining clarity for educational use.

### 4.2 Automation Pipeline

A GitHub Actions workflow automates content processing:

```yaml
name: Build and Deploy
on:
  push:
    branches: [main]
jobs:
  build:
    steps:
      - Convert Markdown slides to HTML/PDF via Marp
      - Process resource documents with Pandoc
      - Generate index page with navigation
      - Deploy to GitHub Pages
```

This automation serves dual purposes: reducing manual processing overhead and demonstrating continuous integration/deployment practices relevant to sustainable software development (minimizing redundant computation).

### 4.3 Collaboration Mechanisms

Students engage with the repository through:

**Structured Contributions:**
- Fork-and-pull-request workflow for submitting improvements
- Issue tracking for reporting errors or suggesting enhancements
- Collaborative note-taking in designated directories

**Quality Assurance:**
- Automated validation of Markdown syntax
- Link checking to prevent broken references
- Consistent formatting through linting rules

These mechanisms introduce students to professional development practices while maintaining educational focus.

---

## 5. PEDAGOGICAL CONSIDERATIONS

### 5.1 Scaffolding Technical Skills

Recognition that not all students enter with Git proficiency led to a staged approach:

**Week 1-2:** Basic repository navigation and content access  
**Week 3-4:** Creating issues and participating in discussions  
**Week 5-6:** Making simple contributions via web interface  
**Week 7-14:** Full workflow participation including local development

This progression allows students to engage with content immediately while gradually building technical skills.

### 5.2 Balancing Openness and Assessment

The public nature of the repository creates tension with traditional assessment practices. The course addresses this through:

- Designing assessments that require synthesis rather than reproduction
- Using private repositories for individual assignment submissions
- Focusing group projects on unique problem-solving rather than content mastery

### 5.3 Sustainability Modeling

The infrastructure itself demonstrates sustainable practices:
- Static site generation reduces server computational requirements
- Content reuse through modular organization
- Transparent resource consumption through GitHub's metrics

These implicit lessons complement explicit sustainability instruction, though their pedagogical impact requires investigation.

---

## 6. PRELIMINARY OBSERVATIONS

### 6.1 Student Engagement Patterns

Initial deployment reveals varied engagement levels with the collaborative features. Approximately 30% of students actively contribute beyond required assignments, suggesting intrinsic motivation among a subset. The majority engage primarily as content consumers, raising questions about incentive structures and barriers to participation.

### 6.2 Technical Challenges

Common difficulties encountered include:
- Merge conflicts when multiple students edit simultaneously
- Markdown syntax errors breaking automated builds
- Confusion between local and remote repository states

These challenges, while creating short-term friction, provide authentic learning opportunities about distributed collaboration.

### 6.3 Content Evolution

The repository accumulated 147 commits across the semester, with contributions from students improving documentation clarity, fixing errors, and adding supplementary resources. This organic growth demonstrates the potential for student-driven content enhancement, though quality control remains essential.

---

## 7. LIMITATIONS AND FUTURE DIRECTIONS

### 7.1 Current Limitations

This implementation report acknowledges several limitations:

**Empirical gaps:** Lack of systematic data on learning outcomes compared to traditional delivery methods

**Generalizability:** Single-institution, single-semester implementation limits broader applicability claims

**Selection bias:** Master's students in technical programs may not represent broader student populations

**Technical barriers:** Infrastructure assumes reliable internet access and modern computing equipment

### 7.2 Planned Investigations

Future work will address these limitations through:

1. **Comparative study:** Parallel sections using traditional and GitHub-based delivery
2. **Learning analytics:** Analysis of commit patterns and collaboration networks
3. **Longitudinal tracking:** Following student application of skills in subsequent courses
4. **Cross-institutional trials:** Partnering with other universities for broader implementation

### 7.3 Adaptation Considerations

Institutions considering similar approaches should evaluate:
- Student technical prerequisites and support needs
- Institutional policies on open educational resources
- Faculty development requirements for GitHub proficiency
- Infrastructure costs and sustainability

---

## 8. CONCLUSION

The RAI-SAI25 course demonstrates one approach to integrating collaborative software development practices into sustainability-focused AI education. By positioning GitHub not merely as a tool but as pedagogical infrastructure, the course creates opportunities for authentic engagement with professional practices while studying sustainable AI development.

Initial implementation suggests feasibility and student engagement, though comprehensive evaluation awaits systematic data collection. The approach may be most suitable for technically-oriented graduate programs where students can leverage prior programming experience. Adaptation to other contexts requires careful consideration of student backgrounds, institutional resources, and learning objectives.

This whitepaper serves as a documentation of practice rather than a claim of effectiveness. As institutions increasingly seek to prepare students for careers requiring both AI expertise and sustainability awareness, approaches that integrate these concerns through authentic professional practices warrant continued exploration and rigorous evaluation.

---

## REFERENCES

Dillenbourg, P. (1999). *Collaborative learning: Cognitive and computational approaches*. Oxford: Elsevier Science.

Feliciano, J., Storey, M. A., & Zagalsky, A. (2016). Student experiences using GitHub in software engineering courses: A case study. *2016 IEEE/ACM 38th International Conference on Software Engineering Companion*, 422-431.

Fiksel, J., Joshi, A., Nimkar, A., Khanal, A., McMahan, H. B., & Parker-Wood, A. (2019). Creating and grading collaborative assignments with GitHub Classroom. *Proceedings of the 50th ACM Technical Symposium on Computer Science Education*, 1265.

Hsing, C., & Gennarelli, V. (2019). Using GitHub in the classroom predicts success in software engineering. *Journal of Computing Sciences in Colleges*, 34(3), 30-36.

Kirschner, P. A., Sweller, J., Kirschner, F., & Zambrano, J. (2018). From cognitive load theory to collaborative cognitive load theory. *International Journal of Computer-Supported Collaborative Learning*, 13(2), 213-233.

Lago, P., Koçak, S. A., Crnkovic, I., & Penzenstadler, B. (2015). Framing sustainability as a property of software quality. *Communications of the ACM*, 58(10), 70-78.

Lago, P., Muccini, H., & Betz, S. (2019). Teaching sustainability in software engineering: A systematic literature review. *2019 IEEE/ACM 12th International Workshop on Cooperative and Human Aspects of Software Engineering*, 113-120.

Patterson, D., Gonzalez, J., Le, Q., Liang, C., Munguia, L. M., Rothchild, D., ... & Dean, J. (2021). Carbon emissions and large neural network training. *arXiv preprint arXiv:2104.10350*.

Schwartz, R., Dodge, J., Smith, N. A., & Etzioni, O. (2020). Green AI. *Communications of the ACM*, 63(12), 54-63.

Stahl, G., Koschmann, T., & Suthers, D. (2006). Computer-supported collaborative learning: An historical perspective. In R. K. Sawyer (Ed.), *Cambridge handbook of the learning sciences* (pp. 409-426). Cambridge: Cambridge University Press.

Strubell, E., Ganesh, A., & McCallum, A. (2019). Energy and policy considerations for deep learning in NLP. *Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics*, 3645-3650.

UNESCO. (2019). *Recommendation on Open Educational Resources (OER)*. Paris: UNESCO.

Verdecchia, R., Procaccianti, G., Malavolta, I., Lago, P., & Koedijk, J. (2017). Estimating energy impact of software releases and deployment strategies: The KPMG case study. *2017 ACM/IEEE International Symposium on Empirical Software Engineering and Measurement*, 257-266.

Vygotsky, L. S. (1978). *Mind in society: The development of higher psychological processes*. Cambridge, MA: Harvard University Press.

Walker, T., Wendt, S., Goubran, S., & Schwartz, T. (2023). *Artificial intelligence for sustainability*. Cham: Palgrave Macmillan. https://doi.org/10.1007/978-3-031-49979-1

Wenger, E. (1998). *Communities of practice: Learning, meaning, and identity*. Cambridge: Cambridge University Press.

Zagalsky, A., Feliciano, J., Storey, M. A., Zhao, Y., & Wang, W. (2015). The emergence of GitHub as a collaborative platform for education. *Proceedings of the 18th ACM Conference on Computer Supported Cooperative Work & Social Computing*, 1906-1917.

---

## APPENDIX: REPOSITORY ACCESS

**Course Repository:** https://github.com/romanmesicek/rai-sai25  
**Course Website:** https://romanmesicek.github.io/rai-sai25/  
**License:** Creative Commons Attribution 4.0 International (CC BY 4.0)

---

**Document Version:** 2.0  
**Revision Date:** October 19, 2025  
**Word Count:** ~2,450 words

---
