# SCOPE: A Decision Framework for Evaluating the Sustainability and Ethics of AI Adoption

**Roman Mesicek**

Sustainability Skills Academy, Austria

**March 2026**

---

## Abstract

Evaluation tools for AI rarely address both ethical and environmental dimensions. This paper introduces SCOPE, a decision framework for assessing AI projects across five integrated dimensions: **S**ufficiency (Is AI necessary?), **C**arbon (What is the full environmental footprint?), **O**utcomes (Who benefits and who bears costs?), **P**ower (Who controls the system?), and **E**ndurance (Is the solution sustainable long-term?). A review of existing frameworks, spanning regulatory instruments, international standards, corporate tools, and academic proposals, reveals a structural divide: most address either ethics or environmental sustainability, but rarely both. The question of whether an AI system should be built at all (sufficiency) remains the most neglected dimension across the field. SCOPE integrates sustainability science and AI ethics into a single instrument, positions sufficiency as the foundational question, and requires explicit net impact assessment. The framework is designed for decision-makers evaluating AI adoption in organizational contexts, applicable before implementation decisions are made. This paper presents the framework's theoretical foundations, details each dimension with reference to current literature, compares SCOPE with existing frameworks, and discusses implications for research and practice.

**Keywords:** Responsible AI, sustainability assessment, AI ethics, sufficiency, environmental footprint, decision framework, Doughnut Economics, EU AI Act, Green AI

---

## 1. Introduction

Organizations are adopting AI faster than they can assess what it costs them. The costs are substantial and unevenly distributed: environmental damage, social disruption, structural dependency. Current governance instruments address them only partially. Training a single large language model such as GPT-3 emits approximately 552 tonnes of CO₂ equivalent (Patterson et al., 2021), while daily inference operations consume vastly more energy than the training phase itself, with inference accounting for 60–90% of total AI-related energy in production environments (Verdecchia et al., 2023). Water consumption presents a parallel concern: training GPT-3 in Microsoft's U.S. data centers directly evaporated approximately 700,000 liters of freshwater (Li et al., 2023). The International Energy Agency (IEA, 2025) projects that global data center electricity consumption will double to approximately 945 TWh by 2030, with AI as the primary growth driver.

The benefits, meanwhile, accrue unevenly. The World Economic Forum (2025) projects a net gain of 78 million jobs globally by 2030, but the aggregate figure obscures sharp asymmetries: women face nearly three times the automation risk of men in high-income countries (Gmyrek et al., 2025), 2.2 billion people remain offline and excluded from AI's benefits entirely (International Telecommunication Union [ITU], 2025), and an estimated 78% of global e-waste from AI hardware production flows to the Global South (United Nations Conference on Trade and Development [UNCTAD], 2024). Market power concentrates among a small number of companies, creating dependency structures that current governance frameworks address only partially (Roberts et al., 2021).

A growing number of frameworks, standards, and tools have emerged in response. The EU AI Act (European Parliament, 2024) establishes the world's first comprehensive binding AI regulation. The OECD AI Principles (2024), UNESCO Recommendation on the Ethics of AI (2021), IEEE 7000 series (2021), ISO/IEC 42001 (2023), and NIST AI Risk Management Framework (2023) provide institutional guidance. Corporate tools from Microsoft, Google, IBM, and others offer practical assessment capabilities. Academic proposals including SustAIn/SCAIS (Rohde et al., 2024), Green AI (Schwartz et al., 2020), and the AI ESG Protocol (Saetra, 2023) push toward integrated evaluation.

Yet a systematic analysis reveals three gaps. First, most frameworks address either ethical/governance concerns or environmental sustainability—not both in an integrated manner. Second, the question of whether an AI system should be deployed at all (what sustainability science terms "sufficiency") is virtually absent from all existing frameworks. Third, the vast majority of frameworks evaluate AI systems during or after development; pre-decision assessment tools that could prevent unnecessary or harmful deployments before resources are committed remain rare.

This paper introduces the SCOPE framework to address these gaps. SCOPE is a structured pre-decision reflection tool that integrates five dimensions—Sufficiency, Carbon, Outcomes, Power, and Endurance—into a unified evaluation instrument for responsible AI deployment. It is a focusing tool, not a blocking mechanism: a systematic way to ensure that the right questions are asked before an organization commits to AI.

The paper proceeds as follows: Section 2 reviews existing frameworks and identifies the gaps SCOPE addresses. Section 3 presents the framework. Section 4 compares SCOPE with existing instruments. Section 5 walks through a hypothetical application. Section 6 discusses implications, limitations, and future research.

---

## 2. Literature Review

### 2.1 The Ethics–Sustainability Divide

The number of frameworks for evaluating the ethics and sustainability of AI has grown rapidly since 2019, yet a structural divide persists. On one side, regulatory and governance frameworks—the EU AI Act (European Parliament, 2024), NIST AI RMF (2023), ISO/IEC 42001 (2023)—excel at risk classification, transparency requirements, and accountability structures but contain limited provisions for environmental sustainability. The EU AI Act, the most comprehensive binding AI regulation globally, does not include environmental impact as a core regulatory dimension.

On the other side, sustainability-focused proposals—Green AI (Schwartz et al., 2020), the foundational work of Strubell et al. (2019) on energy consumption in NLP, and lifecycle analysis approaches (Kaack et al., 2022)—concentrate on computational efficiency and carbon accounting without engaging with broader social or governance concerns.

Corporate tools reinforce this divide. Microsoft's Responsible AI Impact Assessment (2022), Google's Model Cards (Mitchell et al., 2019), and IBM's AI Fairness 360 (2018) offer practical tools for fairness, explainability, and accountability but do not address environmental sustainability at all. An analysis of 32,000 Hugging Face model cards found that environmental metrics are entirely absent, while safety evaluation (~65%) and bias/fairness (~60%) sections are often superficially completed (Hugging Face, n.d.).

Two academic proposals stand out for attempting integration. The SustAIn/SCAIS framework (Rohde et al., 2024) offers the most comprehensive multi-dimensional assessment, comprising 19 sustainability criteria across social, ecological, economic, and governance dimensions with 67 measurable indicators. The AI ESG Protocol (Saetra, 2023) bridges AI assessment with established corporate sustainability reporting practices and the Sustainable Development Goals. Both attempt integration, yet neither places sufficiency—the question of whether AI should be deployed at all—as a central evaluation dimension.

### 2.2 The Sufficiency Blind Spot

The concept of sufficiency—asking "how much is enough?" rather than "how can we do more with less?"—has a long tradition in sustainability science (Sachs, 1993; Princen, 2005; Linz, 2012) but remains remarkably absent from AI discourse. Sustainability theory identifies three complementary strategies: efficiency (same output, fewer resources), consistency (closing material loops), and sufficiency (reducing absolute demand by questioning whether a product or service is needed at all). While AI research has extensively pursued efficiency—through model compression, pruning, quantization, and architectural innovations—sufficiency receives virtually no systematic attention.

This omission matters because efficiency gains in AI consistently fail to reduce absolute resource consumption. Google reports a sixfold improvement in computing power per unit of electricity, yet total greenhouse gas emissions increased 13% year-over-year (Google, 2024). This pattern exemplifies the Jevons paradox—technological efficiency improvements that paradoxically increase total consumption—now well-documented for digital technologies (Santarius et al., 2022; Luccioni et al., 2025). Santarius et al. (2022) formalize this observation in the concept of "digital sufficiency," proposing four interconnected dimensions: hardware sufficiency, software sufficiency, user sufficiency, and economic sufficiency.

The Shift Project's work on "digital sobriety" provides a practical complement, arguing that digital technologies should be deployed with restraint and intentionality rather than as default solutions (The Shift Project, 2019). Morozov's (2013) critique of "solutionism," the tendency to frame all problems as having technological solutions, applies directly to organizations adopting AI without rigorous necessity assessment.

Berry and Stockman (2024) revive Schumacher's (1973) "appropriate technology" concept for the generative AI era, arguing that the question of technological appropriateness must precede questions of implementation. They note that in many contexts, simpler approaches, whether rule-based systems, statistical models, or manual processes, achieve comparable outcomes at substantially lower cost and risk.

### 2.3 Environmental Footprint: Beyond Carbon

Most research on AI's environmental footprint has focused on greenhouse gas emissions from training, but the full picture is broader. Strubell et al. (2019) first drew widespread attention to the energy costs of training large NLP models. Patterson et al. (2021) quantified GPT-3 training at approximately 552 tCO₂e, while Luccioni et al. (2023) conducted the first full lifecycle assessment of a large language model (BLOOM), yielding approximately 50.5 tCO₂e when including hardware manufacturing.

Water consumption is another concern that has received growing attention. Li et al. (2023) estimate that GPT-3 training directly evaporated approximately 700,000 liters of freshwater, with global AI-driven water withdrawal projected to reach 4.2–6.6 billion cubic meters annually by 2027. Hardware lifecycle impacts—embodied carbon in AI chips, rare earth mineral extraction, and e-waste—remain less well quantified but carry substantial environmental and social costs, particularly in resource-extraction regions of the Global South.

Kaack et al. (2022) propose a three-category framework for understanding AI's climate effects: (A) compute-related emissions from hardware and energy use, (B) immediate application impacts, and (C) system-level impacts including societal and rebound effects. This distinction matters because AI's potential to reduce emissions in application domains (energy optimization, logistics, materials science) must be weighed against its own growing footprint. Most frameworks do not require this net impact calculation.

### 2.4 Distributional Impacts and the Doughnut Lens

The distribution of AI's costs and benefits follows patterns of existing inequality. Gray and Suri (2019) document the invisible labor force of "ghost workers" who perform data labeling, content moderation, and other tasks essential to AI systems, often under precarious conditions in the Global South. Birhane (2020) and Mohamed et al. (2020) frame AI development as a form of digital colonialism, where resource extraction (data, minerals, labor) flows from developing countries to technology companies concentrated in a handful of wealthy nations.

Algorithmic bias compounds these distributional effects. Buolamwini and Gebru (2018) demonstrated systematic accuracy disparities in commercial facial recognition systems across gender and skin-type categories. Obermeyer et al. (2019) found that a widely used healthcare algorithm systematically under-referred Black patients for additional care. These are not isolated incidents but structural features of AI systems trained on historically biased data and deployed without adequate impact assessment.

Kate Raworth's Doughnut Economics model (2017), now empirically updated as a live monitoring system with 35 indicators in *Nature* (Fanning & Raworth, 2025), provides a useful lens for evaluating whether AI deployment stays within the "safe and just space" between social foundations (below which people suffer deprivation) and ecological ceilings (above which environmental systems degrade). Formal academic application of the Doughnut to AI assessment is still rare, but it provides a principled basis for asking whether a given AI deployment supports or undermines both dimensions simultaneously.

### 2.5 Governance, Power, and Long-Term Viability

The EU AI Act (European Parliament, 2024) is the first binding AI regulation of its kind, establishing a four-tier risk classification system with corresponding obligations. However, fundamental power asymmetries between AI developers and affected populations remain largely unaddressed by regulation alone. Market concentration among a small number of companies creates vendor lock-in risks, switching costs, and governance dependencies (Roberts et al., 2021). Meaningful opt-out from AI-mediated services is becoming structurally impractical as AI is embedded in essential services.

Long-term viability introduces additional concerns. AI systems are subject to compounding lock-in effects—technical, organizational, and environmental—that accumulate over time (Arthur, 1989). Model degradation through concept drift, hardware obsolescence cycles of 2–3 years, and the "hidden technical debt" in ML systems (Sculley et al., 2015) challenge assumptions of durability. Richardson et al. (2023) confirm that six of nine planetary boundaries are now transgressed, raising the question of whether growing AI infrastructure is compatible with a trajectory toward a 1.5°C world.

---

## 3. The SCOPE Framework

### 3.1 Design Principles

SCOPE was developed at the University of Applied Sciences IMC Krems within the Master's program "Engineering Responsible AI Systems" as part of the course "Sustainability and AI for Green" (Mesicek, 2025). Its design reflects four principles:

1. **Integration over compartmentalization.** SCOPE combines environmental sustainability and social/ethical dimensions in a single instrument, addressing the divide identified in the literature review.

2. **Sufficiency as the entry point.** By opening with the question "Is AI necessary here?", SCOPE breaks with the implicit assumption, shared by virtually all existing frameworks, that AI adoption is a default rather than a choice requiring justification.

3. **Pre-decision orientation.** SCOPE is designed for use before implementation decisions are made, when it is still feasible and cost-effective to choose alternatives. This aligns with the precautionary principle and the technology assessment tradition.

4. **Focusing, not blocking.** SCOPE does not aim to prevent AI deployment. It aims to ensure that when AI is deployed, the decision is informed, the costs are transparent, and the benefits are genuine.

### 3.2 The Five Dimensions

#### S — Sufficiency: Is AI Necessary Here?

The first dimension asks whether AI is the appropriate response to the problem at hand. This requires distinguishing between efficiency ("How can we do it better with AI?") and sufficiency ("Is AI needed at all?").

Key assessment questions include: What problem is being solved? What non-AI alternatives exist? Could non-AI solutions achieve 80% of the benefit at 20% of the cost? What unique AI advantage justifies its use, and are those advantages genuine (speed, scale, pattern recognition) rather than superficial (trend-following, marketing)?

The inclusion of sufficiency as a first-order question is SCOPE's most distinctive contribution. It draws on the digital sufficiency framework (Santarius et al., 2022), the appropriate technology tradition (Schumacher, 1973; Berry & Stockman, 2024), and evidence that rebound effects consistently undermine efficiency-only approaches to resource consumption.

#### C — Carbon: What Is the Full Environmental Footprint?

The second dimension requires a full lifecycle assessment of the AI system's environmental impact, extending beyond carbon to include water, hardware, and infrastructure.

Assessment covers four phases: training (compute time, energy, CO₂), inference (ongoing operations, API calls), hardware (embodied carbon, rare earth minerals, e-waste), and infrastructure (data centers, cooling, water). SCOPE requires a **net impact calculation**: the environmental costs of the AI system weighed against demonstrable savings it enables. This distinguishes SCOPE from frameworks that measure only consumption or only potential benefits.

Reference values from current literature provide calibration: GPT-3 training at ~552 tCO₂e (Patterson et al., 2021), a single ChatGPT query at ~0.3–0.4 Wh (Epoch AI, 2025), data center water consumption of ~500 ml per 20–50 question dialogue (Li et al., 2023), and projected AI share of 2–4% of world electricity by 2030 (IEA, 2025).

#### O — Outcomes: Who Benefits and Who Bears Costs?

The third dimension assesses the distributional impact of AI deployment through the lens of Doughnut Economics (Raworth, 2017): Does deployment support the social foundation (meeting basic human needs) without exceeding the ecological ceiling (staying within planetary boundaries)?

Assessment requires identifying direct and indirect beneficiaries, cost-bearers (financial costs, data extraction, job displacement), risk-bearers (who is affected by AI errors), and whether vulnerable groups are disproportionately impacted. The framework draws attention to asymmetries documented in the literature: technology companies versus displaced workers, skilled versus unskilled labor, Global North versus Global South, and the connected versus the 2.2 billion people still offline.

#### P — Power: Who Controls the System?

The fourth dimension examines governance and power structures across six sub-dimensions: data ownership (who owns, uses, sells, deletes the data?), algorithm control (who understands how decisions are made?), dependencies (vendor lock-in risks and contingency planning), opt-out (can affected parties withdraw?), accountability (who is responsible when AI fails?), and human override (can decisions be appealed and manual intervention ensured?).

This dimension is informed by the EU AI Act's transparency and human oversight requirements (European Parliament, 2024), the four types of "responsibility gaps" identified by Santoni de Sio and Mecacci (2021), and growing evidence that meaningful human oversight faces practical challenges including automation bias and scalability constraints.

#### E — Endurance: Is the Solution Sustainable Long-Term?

The fifth dimension assesses long-term viability across five sub-dimensions: technology (provider stability, update paths, compatibility), data (quality and availability over time), regulation (AI Act, CSRD, Taxonomy compliance), knowledge (resilience to personnel changes), and hardware (upgrade paths, obsolescence, spare parts).

SCOPE incorporates a "2050 test": Will this solution still make sense in 2050? This test examines lock-in effects (are we creating irreversible path dependencies?), planetary boundaries (does this fit in a 1.5°C world?), and societal change (do our assumptions remain valid?). The dimension draws on technology lock-in theory (Arthur, 1989), the planetary boundaries framework (Richardson et al., 2023), and the technical debt literature (Sculley et al., 2015).

### 3.3 Decision Outcomes

After assessing each dimension, the overall evaluation leads to one of four recommendations:

**Implement.** No dimension raises fundamental concerns. The AI adoption can proceed as proposed, with standard monitoring.

**Modify.** One or more dimensions raise concerns that are addressable through redesign, additional safeguards, or contractual provisions. The project can proceed once the identified issues are resolved.

**Reject.** Multiple dimensions reveal fundamental problems — for example, no genuine need for AI (Sufficiency), unacceptable environmental costs without offsetting benefits (Carbon), or irresolvable governance risks (Power). The project should not proceed in its current form.

**Defer.** Too many uncertainties remain to make a responsible decision. The assessment identifies what additional information is needed before re-evaluation.

### 3.4 Application Process

SCOPE is designed for use by project teams, management, or governance boards evaluating a proposed AI deployment. The process involves:

1. Answering the structured questions for each dimension
2. Assessing each dimension with documented rationale
3. Producing one of the four decision outcomes (Implement, Modify, Reject, Defer) with explicit risk documentation
4. Identifying the single biggest risk, its mitigation strategy, and a "blindspot warning" (a risk decision-makers likely underestimate)

The framework is intentionally lightweight, a single structured assessment rather than a multi-month audit, to encourage adoption and repeated use throughout the AI project lifecycle.

---

## 4. Comparative Analysis

### 4.1 Positioning Among Existing Frameworks

Table 1 maps existing frameworks against SCOPE's five dimensions to show where current instruments concentrate their coverage and where gaps remain.

**Table 1.** Coverage of SCOPE dimensions in existing frameworks

| Framework | Sufficiency | Carbon | Outcomes | Power | Endurance |
|---|---|---|---|---|---|
| EU AI Act (2024) | -- | Low | High | High | Mod |
| OECD AI Principles (2024) | Mod | Mod | Mod | Mod | Mod |
| UNESCO Recommendation (2021) | Mod | High | High | Mod | Mod |
| ISO/IEC 42001 (2023) | Low | Low | Mod | High | High |
| NIST AI RMF (2023) | Low | Low | Mod | High | Mod |
| Microsoft RAI (2022) | -- | -- | High | Mod | Mod |
| IBM AI Fairness 360 (2018) | -- | -- | High | Low | Low |
| SustAIn/SCAIS (Rohde et al., 2024) | Mod | High | High | High | Mod |
| Green AI (Schwartz et al., 2020) | High | High | Low | Low | Low |
| AI ESG Protocol (Saetra, 2023) | Mod | High | Mod | High | Mod |

*Note.* High = core dimension; Mod = addressed but not central; Low = mentioned peripherally; -- = not addressed.

### 4.2 Distinctive Contributions

SCOPE makes four contributions relative to existing frameworks:

**1. Sufficiency as a first-order question.** No other reviewed framework systematically requires an assessment of whether AI deployment is necessary. The closest parallels—the Green AI emphasis on reporting computational costs (Schwartz et al., 2020) and Strubell et al.'s (2019) call for cost-aware research practices—frame sufficiency as a research norm rather than a governance question. SCOPE elevates it to the primary evaluation dimension.

**2. Integrated ethics and sustainability.** While most frameworks cluster on either the ethics/governance side or the environmental side, SCOPE's five dimensions span both domains. The Carbon and Endurance dimensions address environmental sustainability; Outcomes and Power address social ethics and governance; Sufficiency bridges both by questioning whether the environmental and social costs of deployment are justified by genuine benefits.

**3. Pre-decision timing.** The EU AI Act evaluates systems during development and post-market. The NIST AI RMF and ISO/IEC 42001 structure ongoing risk management. SustAIn/SCAIS assesses existing systems. SCOPE is explicitly designed for use *before* the decision to build or deploy, when alternatives are still viable and sunk costs have not yet created path dependencies.

**4. Net impact requirement.** The Carbon dimension's explicit requirement for a net impact calculation—environmental costs weighed against demonstrable savings—goes beyond most frameworks, which measure either inputs (energy consumed) or outputs (emissions reduced) but not both. This aligns with Kaack et al.'s (2022) three-category framework for understanding AI's climate effects.

### 4.3 Complementarity With Existing Instruments

SCOPE complements rather than replaces existing frameworks. It functions as a pre-decision gate: does a proposed AI adoption warrant more detailed assessment?

- A project that passes SCOPE's assessment could proceed to **EU AI Act** compliance evaluation for legal requirements
- **SustAIn/SCAIS** could provide detailed sustainability metrics during development
- **ISO/IEC 42001** could structure the ongoing management system
- **Corporate tools** (Microsoft RAI, IBM AIF360) could support technical implementation

The intended use is sequential: SCOPE comes first, as the initial check that determines whether an AI project should move forward at all. If it does, the more specialized frameworks take over for regulatory compliance, technical implementation, and ongoing management. SCOPE does not duplicate their work — it decides whether that work is warranted.

---

## 5. Illustrative Application

To demonstrate SCOPE's practical application, consider a hypothetical scenario: a mid-sized European logistics company evaluating whether to deploy an AI-powered route optimization system for its fleet of 200 delivery vehicles.

**S — Sufficiency:** The company currently uses a commercial fleet management system with rule-based route planning. Analysis reveals that existing software achieves approximately 85% of theoretical optimal routing. The proposed AI system promises 92–95% optimization. Key question: Does a 7–10 percentage point improvement justify the cost, complexity, and environmental footprint of an AI system? The improvement is real but modest, and the existing system covers most of the benefit. This dimension raises concerns but does not block the project.

**C — Carbon:** The AI system would run on a cloud provider's infrastructure (estimated inference costs: ~2,000 kWh/year). However, projected fuel savings from improved routing are estimated at 45,000 liters of diesel annually (~118 tCO₂e saved vs. ~0.8 tCO₂e from compute). Net impact is clearly positive. No concerns.

**O — Outcomes:** Benefits accrue primarily to the company (cost savings) and customers (faster delivery). No significant negative distributional effects identified — existing drivers retain their roles but follow AI-suggested routes. Minor concern: drivers lose route autonomy. No vulnerable groups disproportionately affected. No concerns.

**P — Power:** The system would be provided by a major cloud vendor, creating dependency. Data (delivery addresses, timing, driver behavior) would be stored on the vendor's infrastructure. Key concern: vendor lock-in and data portability. Contractual provisions for data export and service continuity would need to be secured. This dimension raises concerns that are addressable.

**E — Endurance:** Cloud-based delivery reduces hardware obsolescence risk. However, the company becomes dependent on the vendor's continued service and pricing. Regulatory exposure is low (route optimization is not classified as high-risk under the EU AI Act). Knowledge concentration risk is moderate — one IT manager manages the integration. Concerns are addressable.

**Overall recommendation: Modify.** No dimension reveals fundamental problems, but Sufficiency, Power, and Endurance each raise issues that warrant action: secure data portability guarantees, establish fallback to rule-based routing, and document integration knowledge to reduce key-person dependency.

The scenario shows what SCOPE does in practice: it surfaces specific risks (vendor lock-in, knowledge concentration) that might otherwise go unexamined, confirms that the environmental case is sound, and arrives at a qualified "yes" rather than an uncritical one.

---

## 6. Discussion

### 6.1 Theoretical Contributions

SCOPE aims to contribute to the discussion on sustainable AI governance in three ways. First, by integrating sufficiency thinking from sustainability science (Sachs, 1993; Princen, 2005; Santarius et al., 2022) into AI evaluation, it attempts to challenge the implicit growth orientation of both the AI industry and much of AI governance research. The assumption that AI adoption is inherently desirable, and that governance should focus on *how* rather than *whether*, is rarely questioned in existing frameworks. SCOPE seeks to make this question explicit.

Second, SCOPE's pre-decision orientation addresses what appears to be a timing problem. Most existing instruments evaluate AI systems that have already been built or are under development. By the time an EU AI Act conformity assessment is conducted, the decision to adopt AI has long been made. SCOPE is designed to intervene earlier, when the range of possible decisions, including the decision not to use AI, is still open. Whether this earlier intervention proves practical in organizational reality remains to be tested.

Third, by grounding the Outcomes dimension in Doughnut Economics and the Endurance dimension in the planetary boundaries framework, SCOPE attempts to anchor AI governance in established sustainability science. The intention is to give assessors concrete normative reference points: is this adoption compatible with a safe and just operating space? Most existing frameworks lack this connection to empirically grounded sustainability thresholds, though whether SCOPE achieves it in sufficient depth is a question for future empirical work.

### 6.2 Practical Implications

If the framework proves useful in practice, its most likely value lies in accessibility. SCOPE is designed to be applied without specialized ML expertise. The structured questions and four decision outcomes are intended for management and governance boards, not only technical teams — addressing a common limitation of existing frameworks that require significant technical knowledge.

The sufficiency dimension may also have policy implications. The EU AI Act classifies systems by risk level and imposes corresponding obligations, but it does not ask whether a given AI application is necessary in the first place. A sufficiency-informed lens could strengthen proportionality assessments and support more targeted regulation, though this would require further development beyond what SCOPE currently offers.

In education, where the framework has seen its first application, SCOPE extends responsible AI teaching beyond the "fairness, accountability, and transparency" framing that currently dominates AI ethics curricula. Including environmental sustainability and sufficiency prepares students for a professional environment in which sustainability reporting (CSRD) and environmental regulation increasingly intersect with AI governance. Initial experience from using SCOPE in a master's-level course suggests that students engage productively with the sufficiency question in particular, though systematic evaluation of learning outcomes is still needed.

### 6.3 Limitations and Future Research

SCOPE has several limitations that should be acknowledged.

**Operationalization.** SCOPE currently operates at the principles level. Each dimension is assessed through qualitative judgment, not quantitative measurement. A natural next step would be to develop measurable indicators for each dimension, similar to the 67 indicators in the SustAIn/SCAIS framework (Rohde et al., 2024), which would make assessments more reliable and comparable.

**Empirical validation.** The framework has been developed theoretically and applied in an educational setting. It has not yet been tested in real organizational decision-making. Doing so, across different industries and organization sizes, would reveal which dimensions work well in practice and which need refinement.

**Quantitative thresholds for Carbon.** The Carbon dimension currently relies on relative assessment. Science-based thresholds, for example aligned with the Science Based Targets initiative (SBTi), would make the evaluation more rigorous. But determining at what point an AI system's environmental footprint becomes unacceptable depends on context, and the framework currently leaves this judgment to the assessor.

**Weighting and trade-offs.** SCOPE treats all five dimensions as equally important. In practice, context matters: a company with science-based climate targets may need to prioritize Carbon, while a public-sector deployment affecting citizens' rights may need to prioritize Power. How to handle these trade-offs is an open question the framework does not yet answer.

**Inter-rater reliability.** Different assessors evaluating the same AI project may well reach different conclusions. Testing whether SCOPE produces consistent results across assessor groups would help identify where the framework is too ambiguous and where it works as intended.

**Global South perspective.** SCOPE was developed in a European institutional context, like most frameworks in this field. AI governance challenges in the Global South differ in important ways, and whether SCOPE is applicable or relevant there has not been examined.

---

## 7. Conclusion

The SCOPE framework is an attempt to address three gaps in how AI adoption is currently evaluated: the divide between ethics and sustainability, the neglect of sufficiency as a governance question, and the scarcity of tools designed for use before implementation decisions are made.

SCOPE does not replace existing frameworks. It complements regulatory instruments (EU AI Act), management systems (ISO/IEC 42001), and technical tools (SustAIn/SCAIS, IBM AIF360) by functioning as an initial filter: does this proposed AI adoption warrant further assessment at all? Its core contribution is normative. The first question about any AI project should not be "How do we build it?" but "Should we build it?"

The framework has clear limitations, as discussed in Section 6.3. It operates at the principles level, lacks quantitative thresholds, and has been tested only in educational settings. But the underlying argument, that the decision to adopt AI deserves the same rigour as the decision about how to implement it, seems difficult to dispute. If SCOPE prompts even one organization to pause and ask whether a simpler solution would suffice, it will have served its purpose.

---

## References

Arthur, W. B. (1989). Competing technologies, increasing returns, and lock-in by historical events. *Economic Journal*, *99*(394), 116–131. https://doi.org/10.2307/2234208

Berry, C., & Stockman, T. (2024). Small is beautiful in the age of generative AI: Revisiting Schumacher's intermediate technology. *AI & Society*. https://doi.org/10.1007/s00146-024-01875-6

Birhane, A. (2020). Algorithmic colonization of Africa. *SCRIPTed*, *17*(2), 389–409. https://doi.org/10.2966/scrip.170220.389

Buolamwini, J., & Gebru, T. (2018). Gender shades: Intersectional accuracy disparities in commercial gender classification. *Proceedings of Machine Learning Research*, *81*, 77–91. https://proceedings.mlr.press/v81/buolamwini18a.html

Epoch AI. (2025). Trends in AI compute. https://epochai.org/trends-in-ai-compute

European Parliament. (2024). *Regulation (EU) 2024/1689 laying down harmonised rules on artificial intelligence (Artificial Intelligence Act)*. Official Journal of the European Union. https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai

Fanning, A. L., & Raworth, K. (2025). Monitoring human wellbeing and ecological sustainability with the Doughnut. *Nature*. https://doi.org/10.1038/s41586-025-08616-z

Gmyrek, P., Berg, J., & Bescond, D. (2025). *Generative AI and jobs: A refined global index of occupational exposure* (ILO Working Paper No. 140). International Labour Organization. https://doi.org/10.54394/HETP0387

Google. (2024). *2024 Environmental Report*. https://sustainability.google/reports/google-2024-environmental-report/

Gray, M. L., & Suri, S. (2019). *Ghost work: How to stop Silicon Valley from building a new global underclass*. Houghton Mifflin Harcourt.

Hugging Face. (n.d.). *Model Card Guidebook*. https://huggingface.co/docs/hub/en/model-card-guidebook

IBM Research. (2018). *AI Fairness 360* [Software toolkit]. https://aif360.res.ibm.com/

IEEE. (2021). *IEEE 7000-2021: Standard model process for addressing ethical concerns during system design*. IEEE Standards Association. https://standards.ieee.org/standard/7000-2021.html

International Energy Agency. (2025). *Data centres, AI and energy*. https://www.iea.org/reports/data-centres-ai-and-energy

International Telecommunication Union. (2025). *Facts and Figures 2025*. https://www.itu.int/en/ITU-D/Statistics/Pages/stat/default.aspx

ISO. (2023). *ISO/IEC 42001:2023 — Information technology — Artificial intelligence — Management system*. https://www.iso.org/standard/42001

Kaack, L. H., Donti, P. L., Strubell, E., Kamiya, G., Creutzig, F., & Rolnick, D. (2022). Aligning artificial intelligence with climate change mitigation. *Nature Climate Change*, *12*, 518–527. https://doi.org/10.1038/s41558-022-01377-7

Li, P., Yang, J., Islam, M. A., & Ren, S. (2023). Making AI less "thirsty": Uncovering and addressing the secret water footprint of AI models. *arXiv*. https://doi.org/10.48550/arXiv.2304.03271

Linz, M. (2012). *Weder Mangel noch Übermaß: Warum Suffizienz unentbehrlich ist*. Oekom Verlag.

Luccioni, A. S., Strubell, E., & Crawford, K. (2025). Power and accountability in AI: Measuring the environmental costs of AI compute. *Proceedings of the ACM Conference on Fairness, Accountability, and Transparency (FAccT '25)*. ACM.

Luccioni, A. S., Viguier, S., & Ligozat, A.-L. (2023). Estimating the carbon footprint of BLOOM, a 176B parameter language model. *Journal of Machine Learning Research*, *24*(253), 1–15.

Mesicek, R. (2025). *Sustainability and AI for Green — Course Repository* [Course materials]. University of Applied Sciences IMC Krems. https://github.com/romanmesicek/rai-sai25

Microsoft. (2022). *Microsoft Responsible AI Impact Assessment Guide*. https://blogs.microsoft.com/wp-content/uploads/prod/sites/5/2022/06/Microsoft-RAI-Impact-Assessment-Guide.pdf

Mitchell, M., Wu, S., Zaldivar, A., Barnes, P., Vasserman, L., Hutchinson, B., Spitzer, E., Raji, I. D., & Gebru, T. (2019). Model cards for model reporting. *Proceedings of the Conference on Fairness, Accountability, and Transparency*, 220–229. https://doi.org/10.1145/3287560.3287596

Mohamed, S., Png, M.-T., & Isaac, W. (2020). Decolonial AI: Decolonial theory as sociotechnical foresight in artificial intelligence. *Philosophy & Technology*, *33*(4), 659–684. https://doi.org/10.1007/s13347-020-00405-8

Morozov, E. (2013). *To save everything, click here: The folly of technological solutionism*. PublicAffairs.

NIST. (2023). *Artificial Intelligence Risk Management Framework (AI RMF 1.0)* (NIST AI 100-1). National Institute of Standards and Technology. https://doi.org/10.6028/NIST.AI.100-1

Obermeyer, Z., Powers, B., Vogeli, C., & Mullainathan, S. (2019). Dissecting racial bias in an algorithm used to manage the health of populations. *Science*, *366*(6464), 447–453. https://doi.org/10.1126/science.aax2342

OECD. (2024, May 3). OECD updates AI Principles to stay abreast of rapid technological developments. https://www.oecd.org/en/about/news/press-releases/2024/05/oecd-updates-ai-principles-to-stay-abreast-of-rapid-technological-developments.html

Patterson, D., Gonzalez, J., Le, Q., Liang, C., Munguia, L.-M., Rothchild, D., So, D., Texier, M., & Dean, J. (2021). Carbon emissions and large neural network training. *arXiv*. https://doi.org/10.48550/arXiv.2104.10350

Princen, T. (2005). *The logic of sufficiency*. MIT Press.

Raworth, K. (2017). *Doughnut economics: Seven ways to think like a 21st-century economist*. Random House Business Books.

Richardson, K., Steffen, W., Lucht, W., Bendtsen, J., Cornell, S. E., Donges, J. F., Drüke, M., Fetzer, I., Bala, G., von Bloh, W., Feulner, G., Fiedler, S., Gerten, D., Gleeson, T., Hofmann, M., Huiskamp, W., Kummu, M., Mohan, C., Nogués-Bravo, D., ... Rockström, J. (2023). Earth beyond six of nine planetary boundaries. *Science Advances*, *9*(37), eadh2458. https://doi.org/10.1126/sciadv.adh2458

Roberts, H., Cowls, J., Morley, J., Taddeo, M., Wang, V., & Floridi, L. (2021). The Chinese approach to artificial intelligence: An analysis of policy, ethics, and regulation. *AI & Society*, *36*, 59–77. https://doi.org/10.1007/s00146-020-00992-2

Rohde, F., Wagner, J., Reinhard, P., Petschow, U., Meyer, A., Grunewald, O., & Mollen, A. (2024). Broadening the perspective for sustainable artificial intelligence: Sustainability criteria and indicators for Artificial Intelligence systems. *Current Opinion in Environmental Sustainability*, *66*, 101411. https://doi.org/10.1016/j.cosust.2023.101411

Sachs, W. (1993). Die vier E's: Merkposten für einen maßvollen Wirtschaftsstil. *Politische Ökologie*, *11*(33), 69–72.

Saetra, H. S. (2023). The AI ESG protocol: Evaluating and disclosing the environment, social, and governance implications of artificial intelligence capabilities, assets, and activities. *Sustainable Development*, *31*(2), 1027–1037. https://doi.org/10.1002/sd.2438

Santarius, T., Bieser, J. C. T., Frick, V., Höjer, M., Gossen, M., Hilty, L. M., Kern, E., Pohl, J., Rohde, F., & Lange, S. (2022). Digital sufficiency: Conceptual considerations for ICTs on a finite planet. *Annals of Telecommunications*, *78*, 277–295. https://doi.org/10.1007/s12243-022-00914-x

Santoni de Sio, F., & Mecacci, G. (2021). Four responsibility gaps with artificial intelligence: Why they matter and how to address them. *Philosophy & Technology*, *34*, 1057–1084. https://doi.org/10.1007/s13347-021-00450-x

Schumacher, E. F. (1973). *Small is beautiful: Economics as if people mattered*. Blond & Briggs.

Schwartz, R., Dodge, J., Smith, N. A., & Etzioni, O. (2020). Green AI. *Communications of the ACM*, *63*(12), 54–63. https://doi.org/10.1145/3381831

Sculley, D., Holt, G., Golovin, D., Davydov, E., Phillips, T., Ebner, D., Chaudhary, V., Young, M., Crespo, J.-F., & Dennison, D. (2015). Hidden technical debt in machine learning systems. *Advances in Neural Information Processing Systems*, *28*, 2503–2511.

Strubell, E., Ganesh, A., & McCallum, A. (2019). Energy and policy considerations for deep learning in NLP. *Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics*, 3645–3650. https://doi.org/10.18653/v1/P19-1355

The Shift Project. (2019). *Lean ICT: Towards digital sobriety*. https://theshiftproject.org/en/lean-ict-2/

UNCTAD. (2024). *Digital Economy Report 2024*. https://unctad.org/publication/digital-economy-report-2024

UNESCO. (2021). *Recommendation on the Ethics of Artificial Intelligence*. https://unesdoc.unesco.org/ark:/48223/pf0000381137

Verdecchia, R., Sallou, J., & Cruz, L. (2023). A systematic review of Green AI. *WIREs Data Mining and Knowledge Discovery*, *13*(4), e1507. https://doi.org/10.1002/widm.1507

World Economic Forum. (2025). *Future of Jobs Report 2025*. https://www.weforum.org/publications/the-future-of-jobs-report-2025/

---

## Appendix: SCOPE Quick-Reference Card

| | Dimension | Core Question |
|---|---|---|
| **S** | Sufficiency | Is AI necessary — or are there simpler paths to the goal? |
| **C** | Carbon | What does the solution consume — and what does it actually save? |
| **O** | Outcomes | Who benefits — and who bears costs or risks? |
| **P** | Power | Who controls the system — and who can object? |
| **E** | Endurance | Will this solution still work and make sense in 10 years? |

### Decision Outcomes

| Outcome | When to use |
|---------|-------------|
| **Implement** | No dimension raises fundamental concerns |
| **Modify** | Concerns exist but are addressable through redesign or safeguards |
| **Reject** | Multiple dimensions reveal fundamental problems |
| **Defer** | Too many uncertainties; more information needed before deciding |

---

*SCOPE AI Framework — Concept Paper v1.0*
*Sustainability Skills Academy, Austria*
*Correspondence: roman.mesicek@sustainability-skills.at*
*ORCID: https://orcid.org/0000-0002-8216-2278*

*This work is licensed under a Creative Commons Attribution 4.0 International License (CC BY 4.0).*
*Source repository: https://github.com/romanmesicek/rai-sai25*
