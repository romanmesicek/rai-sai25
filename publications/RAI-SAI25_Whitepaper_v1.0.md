# ACADEMIC WHITEPAPER

## GitHub-Enabled Collaborative Learning in Sustainability and AI Education: A Case Study in Modern Pedagogical Infrastructure

**Roman Mesicek**
University of Applied Sciences IMC Krems, Austria
roman.mesicek@fh-krems.ac.at

**Winter Semester 2025**

---

### ABSTRACT

This whitepaper presents a novel pedagogical approach to teaching sustainability and artificial intelligence through GitHub-based collaborative learning infrastructure. The RAI-SAI25 course at UAS IMC Krems demonstrates how modern DevOps practices, automated deployment pipelines, and version-controlled content management can enhance master-level education in the intersection of AI and environmental sustainability. This paper outlines the technical implementation, pedagogical framework, and learning outcomes of a 5-ECTS course that combines theoretical instruction with practical, industry-standard collaborative tools. By leveraging GitHub Actions, Marp presentations, and automated continuous deployment, the course creates an open, transparent, and student-centered learning environment that mirrors real-world sustainable software development practices.

**Keywords:** Sustainability Education, AI for Green, GitHub-based Learning, Collaborative Pedagogy, DevOps in Education, Green Computing, Master Education, Open Educational Resources

---

## 1. INTRODUCTION

The intersection of artificial intelligence and environmental sustainability represents one of the most critical challenges of the 21st century. As AI systems consume increasing amounts of energy and computational resources, the need for sustainable AI practices has become paramount (Strubell et al., 2019). Simultaneously, AI offers unprecedented opportunities for addressing climate challenges through optimization, prediction, and intelligent resource management.

This whitepaper describes the RAI-SAI25 course ("Sustainability and AI for Green"), a master-level integrated course (ILV) at the University of Applied Sciences IMC Krems. The course uniquely combines substantive content on sustainable AI with an innovative pedagogical infrastructure based on GitHub, demonstrating how educational institutions can adopt industry-standard collaborative tools to enhance student learning, transparency, and engagement.

The course addresses three critical gaps in contemporary AI education:

1. **Content Gap:** Limited integration of sustainability principles within AI curricula
2. **Methodology Gap:** Insufficient exposure to collaborative, version-controlled workflows
3. **Practice Gap:** Disconnect between academic learning and industry-standard development practices

By addressing these gaps through a GitHub-centered approach, the course prepares students not only to understand sustainable AI conceptually but to practice it collaboratively using tools they will encounter in professional settings.

---

## 2. PEDAGOGICAL FRAMEWORK

### 2.1 Learning Outcomes and Competencies

The course is structured around three core learning outcomes aligned with the European Qualifications Framework (EQF Level 7 - Master's degree):

**LO1: Research and Critical Assessment**
Students develop the ability to search for, assess, prepare, and present information on sustainable practices as integral components of business and industrial processes, with specific focus on responsible AI systems that achieve both ecological and economic benefits.

**LO2: Tool Selection and Adoption**
Students acquire competency in selecting and adopting appropriate AI tools to enhance sustainability in various business operations, improving efficiency and profitability while minimizing environmental impact.

**LO3: Circular Economy Integration**
Students learn to explain and implement how integrating circular economy models into business strategies, supported by AI systems, can drive profitability and economic prosperity while benefiting the environment.

### 2.2 Content Architecture

The course covers nine key topic areas spanning 2 contact hours per week over 14 weeks (28 contact hours, 97 self-learning hours, total 125 hours):

1. Climate Crisis and Information Technology
2. AI's Carbon Footprint and Environmental Impact
3. Green AI Strategies and Sustainable Computing
4. AI for Environmental Solutions
5. Sustainable Software Development
6. Energy-Efficient Machine Learning
7. Life Cycle Assessment: Quantifying Environmental Impacts
8. Circular Economy: Transition for Future Sustainability
9. Sustainable Infrastructure Systems for AI

### 2.3 Learning Activities and Assessment

The course employs a multi-modal pedagogical approach:

- **Chalk Talks:** Foundation-building lectures introducing core concepts
- **Classroom Debates:** Critical engagement with responsible AI practices
- **Quizzes:** Formative assessment and knowledge reinforcement
- **Group Projects:** Collaborative problem-solving on real-world scenarios

Assessment is weighted as follows:
- Written Exam (60%): Theoretical understanding and concept integration
- Deliverable Submission (30%): Comprehensive project report demonstrating practical application
- Presentation (10%): Communication and justification of findings

---

## 3. TECHNICAL IMPLEMENTATION

### 3.1 Repository Architecture

The course infrastructure is built on a GitHub repository (`rai-sai25`) that serves as the single source of truth for all course materials. The repository structure follows software engineering best practices:

```
rai-sai25/
├── slides/                    # Marp presentations (Markdown → HTML/PDF)
├── resources/                 # Additional materials (Markdown → HTML)
├── papers/                    # Academic literature (PDF)
├── .github/workflows/         # CI/CD automation
├── themes/                    # Custom CSS styling
└── documentation/             # Course documentation
```

This architecture provides several pedagogical advantages:

1. **Transparency:** All content is version-controlled and publicly accessible
2. **Traceability:** Complete history of changes with attribution
3. **Collaboration:** Students can contribute via pull requests
4. **Reproducibility:** Automated builds ensure consistent output

### 3.2 Automated Deployment Pipeline

The course leverages GitHub Actions to implement a continuous deployment (CD) pipeline that automatically processes and publishes course materials. When content is committed to the main branch, the workflow:

1. **Builds Presentations:** Converts Markdown slides to HTML and PDF using Marp CLI with custom neutral theme
2. **Processes Resources:** Transforms supplementary Markdown materials into styled HTML pages using Pandoc
3. **Manages Papers:** Copies academic PDFs with metadata extraction and file size calculation
4. **Generates Index:** Creates a responsive, mobile-friendly landing page with conditional sections
5. **Deploys to GitHub Pages:** Publishes all materials to a publicly accessible website

This automation demonstrates several key concepts relevant to sustainable software engineering:

- **Efficiency:** Eliminates manual build processes
- **Consistency:** Ensures reproducible outputs
- **Resource Optimization:** Builds only when content changes
- **Accessibility:** Provides multiple formats (HTML, PDF) for diverse needs

### 3.3 Collaborative Features

The repository implements industry-standard collaborative workflows:

**Version Control:**
- Git-based tracking of all changes
- Semantic commit messages
- Branch-based development

**Student Contributions:**
- Fork-and-pull-request workflow
- Code review processes
- Contribution guidelines and templates

**Quality Assurance:**
- Automated build validation
- Link checking capabilities
- Consistent styling enforcement

These features mirror practices students will encounter in professional sustainable software development, creating authentic learning experiences.

---

## 4. INNOVATION AND IMPACT

### 4.1 Alignment with Sustainable Development Goals

The course directly addresses multiple United Nations Sustainable Development Goals (SDGs):

- **SDG 4 (Quality Education):** Open educational resources and modern pedagogical approaches
- **SDG 9 (Industry, Innovation, Infrastructure):** Sustainable infrastructure systems for AI
- **SDG 12 (Responsible Consumption):** Circular economy models and resource optimization
- **SDG 13 (Climate Action):** Green AI strategies and carbon footprint reduction

### 4.2 Pedagogical Innovation

The GitHub-based approach represents a paradigm shift in educational content delivery:

**Traditional Approach:**
- Static PDF documents
- Centralized content management
- One-way knowledge transfer
- Limited student agency

**GitHub-Enabled Approach:**
- Dynamic, version-controlled content
- Distributed collaboration
- Bi-directional knowledge exchange
- Student ownership and contribution

This shift empowers students as active participants in the learning ecosystem rather than passive consumers of information.

### 4.3 Transferability

The technical infrastructure is highly transferable to other educational contexts:

- **Discipline-agnostic:** Applicable to any field requiring collaborative content creation
- **Scalable:** Supports courses of varying sizes and complexities
- **Open-source:** All tools used are freely available and well-documented
- **Cost-effective:** Minimal infrastructure costs (GitHub offers free educational accounts)

Educational institutions can adapt this model for courses in computer science, engineering, environmental studies, business, and beyond.

---

## 5. THEORETICAL FOUNDATIONS

### 5.1 Constructivist Learning Theory

The course design is grounded in constructivist principles (Vygotsky, 1978), particularly the concept of learning through social interaction and collaborative knowledge construction. The GitHub platform serves as a digital zone of proximal development where students collaborate with peers and instructors to build understanding.

### 5.2 Communities of Practice

Following Wenger's (1998) communities of practice framework, the course creates a shared domain (sustainable AI), community (students, instructors, external contributors), and practice (GitHub-based collaboration). This mirrors professional communities in software engineering and sustainability fields.

### 5.3 Open Educational Resources Movement

The course aligns with the UNESCO (2019) Recommendation on Open Educational Resources by:

- Providing freely accessible, openly licensed materials
- Enabling adaptation and remixing through version control
- Supporting diverse learning needs through multiple formats
- Promoting inclusive and equitable education

---

## 6. CHALLENGES AND LESSONS LEARNED

### 6.1 Technical Barriers

**Challenge:** Students with limited Git/GitHub experience face initial learning curves.

**Solution:** Structured onboarding materials, paired with in-class GitHub tutorials, reduce friction. The investment in learning Git provides long-term benefits for student employability.

### 6.2 Content Management

**Challenge:** Maintaining consistency across multiple content types (slides, resources, papers).

**Solution:** Automated validation workflows and clear contribution guidelines ensure quality standards. Template files reduce variability.

### 6.3 Assessment Integrity

**Challenge:** Open repositories raise questions about academic integrity in assessments.

**Solution:** Assessment design focuses on synthesis, critical analysis, and original application rather than reproduction of repository content. Group projects emphasize unique problem-solving.

---

## 7. FUTURE DIRECTIONS

### 7.1 Enhanced Interactivity

Future iterations will explore:
- Integration of Jupyter Notebooks for executable code examples
- Interactive visualization tools for carbon footprint calculators
- Real-time collaborative editing environments

### 7.2 Community Expansion

Plans include:
- Cross-institutional collaboration with partner universities
- Industry partnerships for real-world case studies
- Alumni network for ongoing knowledge exchange

### 7.3 Research Opportunities

The infrastructure enables novel research on:
- Learning analytics from Git commit patterns
- Effectiveness of collaborative versus individual learning
- Impact of open educational practices on student outcomes

---

## 8. CONCLUSION

The RAI-SAI25 course demonstrates that GitHub-based collaborative infrastructure can significantly enhance master-level education in sustainability and AI. By combining substantive content on green AI with industry-standard collaborative tools, the course prepares students for the practical realities of sustainable software development while fostering transparency, engagement, and student agency.

The approach is transferable, scalable, and aligned with contemporary educational best practices. As universities increasingly recognize the importance of both sustainability education and modern technical skills, this model offers a blueprint for integrating these priorities into coherent, effective curricula.

Most importantly, the course practices what it preaches: it uses sustainable, efficient, and collaborative approaches to teach sustainable, efficient, and collaborative AI development. This alignment between content and methodology creates authentic, meaningful learning experiences that prepare students to address the critical environmental challenges facing our planet.

---

## REFERENCES

Strubell, E., Ganesh, A., & McCallum, A. (2019). Energy and policy considerations for deep learning in NLP. *Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics*, 3645-3650.

UNESCO. (2019). *Recommendation on Open Educational Resources (OER)*. Paris: UNESCO.

Vygotsky, L. S. (1978). *Mind in society: The development of higher psychological processes*. Cambridge, MA: Harvard University Press.

Walker, T., Wendt, S., Goubran, S., & Schwartz, T. (2024). *Artificial intelligence for sustainability*. Cham: Palgrave Macmillan. https://doi.org/10.1007/978-3-031-49979-1

Wenger, E. (1998). *Communities of practice: Learning, meaning, and identity*. Cambridge: Cambridge University Press.

---

## ABOUT THE AUTHOR

**Roman Mesicek** is a faculty member at the University of Applied Sciences IMC Krems, Austria, specializing in artificial intelligence, sustainability, and educational technology. His research focuses on the intersection of AI, environmental impact, and pedagogical innovation in higher education.

---

## REPOSITORY ACCESS

**Course Repository:** https://github.com/romanmesicek/rai-sai25
**Course Website:** https://romanmesicek.github.io/rai-sai25/
**License:** Creative Commons Attribution 4.0 International (CC BY 4.0)

---

**Citation:** Mesicek, R. (2025). GitHub-enabled collaborative learning in sustainability and AI education: A case study in modern pedagogical infrastructure. *UAS IMC Krems White Paper Series*, Winter Semester 2025.

---

**Document Version:** 1.0
**Publication Date:** October 19, 2025
**Word Count:** ~2,400 words

---
