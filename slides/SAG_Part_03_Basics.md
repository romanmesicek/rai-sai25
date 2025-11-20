---
marp: true
theme: neutral
size: 16:9
paginate: true
order: 6
---

<!-- description: The AI/Sustainability Paradox - Positive and Negative Impacts -->

<!-- _class: title -->


# AI
## The Artificial Intelligence/Sustainability Paradox

IMC University of Applied Sciences Krems, Austria
Roman Mesicek


SAG Part 3 Basics

###### Full reference list available at [GitHub](https://github.com/romanmesicek/rai-sai25/blob/main/resources/references.md)


<!--
Speaker notes:
- Image suggestion: Split image - data center on left, flourishing forest on right
- Opening question for audience: "How many of you used AI today? Now estimate the energy cost."
- Build tension between innovation promise and environmental reality
-->

---

# The Paradox We Face

> One ChatGPT query uses electricity to light a bulb for 20 minutes (de Vries, 2023).

vs.

> AI could reduce global emissions by 5 billion tons annually (BCG, 2024).

<br>

## Which number matters more?

![bg right:38% fit](images/pt03_slide02.jpg)



###### Photo by <a href="https://unsplash.com/@cdd20?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Yumu</a> on <a href="https://unsplash.com/photos/a-red-background-with-a-yellow-dotted-arrow-QDHb81lUpbY?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>
      
<!--
Speaker notes:
- Pause after revealing each statement for impact
- This paradox frames our entire discussion
- Audience reflection: "What's your initial instinct?"
- We'll resolve this tension by session end
-->

---

# Our Journey Today

### Act I: What Is
The Growing Environmental and Social Cost of AI

### Act II: What Could Be
AI as Societal Solution Catalyst

### Act III: New Bliss
Navigating the Paradox Responsibly

###### Sources: Duarte, 2010

<!--
Speaker notes:
- Three-act structure borrowed from narrative theory (Duarte sparkline)
- Each act challenges the previous understanding
- Interactive element: Vote now - is AI net positive or negative for environment?
- We'll vote again at the end
-->

---

<!-- _class: chapter -->

# Act I: What Is

## The Growing Societal Costs of AI
## Energy • Carbon • Resources • Society

<!--
Speaker notes:
- Transition: "Let's start with uncomfortable truths"
- This section may challenge tech optimism
- Prepare for cognitive dissonance
-->

---
<!-- _class: compact -->
# AI's Energy Reality

## Current State (2025)

|                              |                        |
|------------------------------|------------------------|
| **Data Centers**             | 3-4% global electricity |
| **AI Workloads**             | 10-15% of data center energy |
| **Growth Rate**              | 30% CAGR through 2030 |
| **2030 Projection**          | 415 → 945 TWh |

<br>

By 2030: AI = Argentina's entire electricity consumption

###### Sources: IEA, 2025; Andrae & Edler, 2015

<!--
Speaker notes:
- Image suggestion: Exponential growth curve chart
- Context: This is BEFORE mass AI adoption
- Question: "Is exponential growth sustainable in finite systems?"
-->

---
<!-- _class: compact -->
# The Cost of Intelligence

## Training Energy Consumption

| Model | Energy | CO₂ Emissions | Equivalent |
|-------|--------|--------------|------------|
| **GPT-3** | 1,287 MWh | 552 tons | 120 cars/year |
| **GPT-4** | ~51,800 MWh | 13,000 tons | 2,800 cars/year |
| **BLOOM** | 433 MWh | 50.5 tons | 11 cars/year |
| **Llama 3** | 2,700 MWh | 1,090 tons | 240 cars/year |

<br>
GPT-4 training = Annual consumption of 13,000-17,000 EU households

###### Sources: Patterson et al., 2022; Luccioni et al., 2022; Besiroglu et al., 2024

<!--
Speaker notes:
- GPT-4 is 40x larger than GPT-3
- Training cost: $100 million in compute alone
- Discussion: "Should we require energy labels for AI models?"
- Note efficiency paradox: Better models require MORE energy
-->

---
<!-- _class: compact -->
# Every Query Counts

## Inference at Scale

**Daily Reality:**
- Google Search: 0.3 Wh
- ChatGPT Query: 2-3 Wh (**10x increase**)
- ChatGPT Daily: 564 MWh (200M users)

**Water Cost per Conversation:**
- 20-50 questions = 500ml water
- 300M weekly users = swimming pool daily

**Hidden Multiplier:** Each response generated 3-5x, best selected

###### Sources: de Vries, 2023; Li et al., 2023

<!--
Speaker notes:
- Image suggestion: Infographic comparing search vs AI query
- Calculation: Your daily AI use = ?
- Most users unaware of resource cost
- Question: "Should AI interfaces show environmental cost?"
-->

---
<!-- _class: compact -->
# Corporate Carbon Reality

## Emissions Growth Despite Pledges

| Company | Emissions Change | Cause |
|---------|-----------------|-------|
| **Google** | +48% since 2019 | 14.3M tons total |
| **Microsoft** | +29% since 2020 | "AI acceleration" |
| **Meta** | +66% since 2019 | Data center expansion |

> "The exponential growth in AI is straining our net-zero commitments" 
> - Microsoft Sustainability Report 2024

###### Sources: Google, 2024; Microsoft, 2024; Meta, 2024

<!--
Speaker notes:
- Contradiction: Net-zero promises vs AI investments
- Image suggestion: Chart showing pledge vs reality divergence
- Discussion: "Can companies be carbon neutral while scaling AI?"
-->

---
<!-- _class: compact -->
# The Water Crisis Nobody Discusses

## AI's Hidden Thirst

**Training Requirements:**
- GPT-3: **700,000 liters** cooling water
- Microsoft Azure: **6.4 million m³** annually (+34% YoY)
- Google: **6.1 billion gallons** in 2023

**Geographic Conflict:**
- **160+ data centers** in water-stressed regions
- Arizona, Singapore, Northern Virginia hotspots
- Competition with agriculture and communities

**Per Query:** 16.9ml water evaporated forever

###### Sources: Li et al., 2023; Mytton, 2021; Microsoft, 2024

<!--
Speaker notes:
- Image suggestion: Map overlay of water stress and data centers
- Meta's Goodyear facility: 56M gallons/year
- Question: "Should data centers be in deserts?"
- Hidden: Most cooling water evaporates, doesn't return
-->

---
<!-- _class: compact -->
# Hardware's Dark Side

## The Physical Foundation

**Critical Materials:**
- **17 rare earth elements** per GPU
- **80% supply** from China
- **<1% recycling rate** for AI hardware

**E-Waste Trajectory:**
- 2025: 54 million tons globally
- 2030: 1.2-5M tons from AI alone
- GPU replacement: every 1-3 years

**Mining Impact:**
- Dysprosium, Terbium, Cobalt extraction
- Child labor in DRC (cobalt)
- Water pollution in rare earth processing

###### Sources: Crawford & Joler, 2018; USGS, 2024; Forti et al., 2020

<!--
Speaker notes:
- Image suggestion: Breakdown of materials in a single GPU
- Salar de Uyuni: 1/3 of world's lithium
- Question: "Is 'clean' tech really clean?"
- E-waste: 54M tons = 10.8M elephants
-->

---
<!-- _class: compact -->
# The Jevons Paradox (Rebound Effect) in AI

## Why Efficiency Gains Fail

**Historical Pattern:**
- Steam engines: 100x efficiency → 1000x coal use
- Cars: 30% fuel efficiency → 50% more driving

**AI's Paradox (2017-2023):**
- **44x efficiency improvement** per query
- **100x increase** in total AI workloads
- **Net result:** 2x total energy consumption

**The Trap:** Lower costs → More use cases → Higher total impact

###### Sources: Koomey et al., 2024; Jevons, 1865

<!--
Speaker notes:
- This is THE critical concept many miss
- Efficiency ≠ Sustainability
- Discussion: "Can we have sustainable growth?"
- Connect to Session 1: Planetary boundaries are absolute
-->

---
<!-- _class: compact -->
# The Social Cost of AI

## Digital Inequality Deepens

<div class="cols">

<div class="col">

**Global AI Divide:**
- **90% of AI researchers** in 10 countries
- **2.6 billion people** remain offline
- **72% of data centers** in high-income nations

**Labor Disruption:**
- **47% of jobs** at high automation risk
- **450,000** fossil fuel workers displaced
- **87% lack** retraining access

</div>

<div class="col">

**Environmental Injustice:**
- Data centers in **65% minority communities** (USA)
- **70% e-waste** exported to Global South
- Low-income pay **3x more** per kWh for AI services

</div>

###### Sources: World Bank, 2024; ILO, 2024; Brewster et al., 2023

<!--
Speaker notes:
- Image suggestion: World map showing AI capability vs GDP
- Digital colonialism: Extract data, export waste
- Question: "Who benefits from AI advancement?"
- Connect to Doughnut's social foundation
-->


---

<!-- _class: chapter -->

# Act II: What Could Be

## AI as Solution Catalyst
## Modeling • Energy • Agriculture • Innovation

<!--
Speaker notes:
- Transition: "Now the other side of the paradox"
- Same technology, different application
- Focus on empirical evidence, not promises
-->

---
<!-- _class: compact -->
# Climate Modeling Revolution

## From Months to Hours

**Speed Transformation:**
- Traditional: 90 days for 1000-year simulation
- AI-Enhanced: **12 hours** (University of Washington)
- Impact: Test 100x more scenarios

**Breakthrough Applications:**
- Hurricane paths: 85% accuracy at 7 days
- Regional downscaling: 10km → 1km resolution
- Tipping point detection: 2 years advance warning

**Market Growth:** €266M (2024) → €1.2B (2029)

###### Sources: Bi et al., 2023; University of Washington, 2024

<!--
Speaker notes:
- Image suggestion: Side-by-side simulation comparison
- This changes policy response time dramatically
- Question: "What decisions need faster climate data?"
- Note: AI doesn't replace physics, enhances it
-->

---
<!-- _class: compact -->
# Smart Grid Transformation

## Real Impact at Scale

**Deployment Reality:**
- **74% of utilities** using AI (2024)
- **20% error reduction** in demand forecasting
- **15% peak load** reduction

**Case Studies:**
- DeepMind + UK Grid: **10% efficiency gain**
- Duke Energy + AWS: **30% outage reduction**
- Austria Verbund AG: **18% efficiency gain**

**Renewable Integration:**
- Wind prediction: **20% value improvement**
- Solar forecasting: **92% accuracy**
- Battery optimization: **40% lifetime extension**

###### Sources: IEA, 2024; DeepMind, 2024; Austrian Research Promotion Agency, 2024

<!--
Speaker notes:
- This is happening NOW, not future
- Austria's 78% renewable grid = perfect testbed
- Discussion: "Why isn't this bigger news?"
- Economics driving adoption
-->

---
<!-- _class: compact -->
# Agricultural Revolution

## Beyond Yield Optimization

**Water & Chemical Reduction:**
- Irrigation: **40% water savings** (Israel)
- Pesticides: **97% reduction** potential (ecoRobotix)
- Fertilizer: **30% reduction** with same yield

**Real Deployments:**
- John Deere: 300,000 connected machines
- Full Nature Farms: Serving 40% of US tomatoes
- India: 7 million farmers on AI advisory

**Food Waste:** AI reduces 20% of 1.3B tons annual waste

###### Sources: BCG, 2024; ecoRobotix, 2024; FAO, 2024

<!--
Speaker notes:
- Image suggestion: Before/after field comparison
- 97% pesticide reduction = game changer
- Question: "Why do we still use blanket spraying?"
- Note: Technology exists, adoption is barrier
-->

---
<!-- _class: compact -->
# Transportation & Logistics

## Immediate Carbon Wins

**Google's Fleet Impact (2024):**
- Fuel-efficient routing: **2.7M tons CO₂** saved
- Green Light (traffic): **30% fewer stops**
- Contrails reduction: **54% with American Airlines**

**Logistics Optimization:**
- UPS ORION: **100,000 tons CO₂/year**
- DHL: **15% fuel reduction**
- Maersk + IBM: **20% empty container reduction**

**Urban Impact:** 700+ cities using AI traffic management

###### Sources: Google, 2024; UPS, 2024; C40 Cities, 2024

<!--
Speaker notes:
- These are REALIZED savings, not projections
- Simple algorithm changes = massive impact
- Discussion: "Should fuel-efficient routing be mandatory?"
- Every saved mile counts at scale
-->

---
<!-- _class: compact -->
# Material Science Breakthroughs

## Accelerating Green Innovation

**Discovery Speed:**
- Traditional: 10-20 years per material
- AI-Assisted: **Weeks to months**

**Recent Breakthroughs:**
- DeepMind GNoME: **2.2M new crystals** (45x previous knowledge)
- Microsoft + PNNL: New battery in **80 hours**
- MIT: Concrete that stores energy

**Carbon Capture Materials:**
- 1000+ new MOFs identified
- 10x improvement in CO₂ absorption
- Cost reduction: 70% projected

###### Sources: Merchant et al., 2023; Microsoft Research, 2024; MIT, 2024

<!--
Speaker notes:
- This is chemistry's "AlphaGo moment"
- New materials enable entire green economy
- Question: "What material would change everything?"
- Connect to circular economy potential
-->

---
<!-- _class: compact -->
# Biodiversity & Conservation

## AI as Nature's Guardian

**Wildlife Protection:**
- WWF Kenya: **96% reduction** in elephant poaching
- Rainforest Connection: Illegal logging down **70%**
- Ocean monitoring: 75% of illegal fishing detected

**Species Discovery:**
- BioCLIP: **300+ new species** identified
- iNaturalist: 150M observations, 400K species
- eBird: 1 billion bird observations analyzed

**Ecosystem Monitoring:**
- Amazon: Daily deforestation alerts
- Coral reefs: Bleaching prediction 2 weeks advance
- Migration patterns: Climate adaptation tracking

###### Sources: WWF, 2024; Global Fishing Watch, 2024; Tuia et al., 2024

<!--
Speaker notes:
- Image suggestion: Thermal camera elephant detection
- AI democratizes conservation science
- Discussion: "Can technology save what technology destroyed?"
- Every species matters for ecosystem stability
-->

---
<!-- _class: compact -->
# The Net Impact Equation

## Quantifying the Balance

Potential by 2035:

| Application Area | Annual CO₂ Reduction |
|-----------------|---------------------|
| Energy Systems | 1.2 GtCO₂ |
| Transportation | 0.8 GtCO₂ |
| Manufacturing | 0.6 GtCO₂ |
| Buildings | 1.0 GtCO₂ |
| Agriculture | 0.4-1.4 GtCO₂ |
| **Total Potential** | **4.0-5.0 GtCO₂** |

<br>
**AI's Own Footprint:** 0.4-1.6 GtCO₂

Net Benefit: 2.4-4.6 GtCO₂ (3-8x positive)

###### Sources: BCG, 2024; PwC, 2024; WEF, 2024

<!--
Speaker notes:
- BUT: This is NOT automatic
- Requires intentional deployment
- Question: "Why aren't we achieving this?"
- Currently <10% of AI focused on climate
-->

---

<!-- _class: chapter -->

# Act III: New Bliss

## Navigating the Paradox Responsibly
## Solutions • Governance • Future Pathways

<!--
Speaker notes:
- Synthesis: Both sides are true
- The path forward requires nuance
- Your generation will decide the outcome
-->

---
<!-- _class: compact -->
# Technical Solutions Today

## Efficiency Without Rebound

**Architecture Innovation:**
- Model pruning: **90% size reduction**
- Quantization: **75% memory savings**
- Knowledge distillation: **96% inference energy cut**
- DeepSeek R1: Outperforms at **1/10th size**

**Hardware Evolution:**
- TPUs: **80% less energy** than GPUs
- Neuromorphic chips: **100x efficiency**
- Optical computing: **1000x potential**

**Edge Computing:** 60% reduction in transmission energy

###### Sources: Liu et al., 2025; Google, 2024; Intel, 2024

<!--
Speaker notes:
- Efficiency IS possible without growth
- DeepSeek: Chinese breakthrough changes everything
- Discussion: "Should we regulate model sizes?"
- Note: Mixture of Experts architecture
-->

---
<!-- _class: compact -->
# Green Infrastructure

## Available Now, Underdeployed

**Cooling Revolution:**
- Liquid cooling: **40% energy reduction**
- Stockholm: Heats **25,000 homes** with waste heat
- Free cooling: **65% of year** in Austria

**Renewable Integration:**
- Google: **64% carbon-free** energy
- Microsoft: **100% renewable** by 2025
- **12 GW** clean energy PPAs contracted

**Location Matters:**
- Iceland: 100% renewable, natural cooling
- Austria: 78% renewable grid advantage

###### Sources: Uptime Institute, 2024; RE100, 2024; Austrian Energy Agency, 2024

<!--
Speaker notes:
- Image suggestion: Stockholm district heating diagram
- Austria uniquely positioned for green AI
- Question: "Why build data centers in deserts?"
- Policy could incentivize right locations
-->

---
<!-- _class: compact -->
# Circular AI Economy

## From Linear to Regenerative

**Linear Model (Current):**
Extract → Manufacture → Use (2-3 years) → Dispose

**Circular Model (Achievable):**
Design for longevity → Modular upgrades → Reuse → Refurbish → Recycle

**Impact Potential:**
- **70% material reduction**
- **7-10 year** hardware lifecycle
- **90% recovery rate** possible
- **60% cost savings** long-term

**Austrian Leadership:** Circular Futures platform, 230 companies, €5.7B funding

###### Sources: Ellen MacArthur Foundation, 2024; Austrian Federal Ministry, 2024; EU Commission, 2024

<!--
Speaker notes:
- Fairphone model for servers is possible
- Image suggestion: Circular flow diagram
- Discussion: "Why do we accept planned obsolescence?"
- Connect to R-strategies from Session 2
-->

---
<!-- _class: compact -->
# EU Regulatory Framework

## From Voluntary to Mandatory

**Corporate Sustainability Reporting Directive (CSRD):**
- **50,000 companies** affected
- Scope 3 emissions (includes AI services)
- First reports: 2026 for 2025 data

**EU AI Act Environmental Provisions:**
- High-risk AI: Mandatory impact assessment
- Energy consumption disclosure required
- A-G efficiency rating system

**Digital Product Passport (2027):**
- Full lifecycle tracking
- 90% recyclability target
- Right to repair provisions

###### Sources: European Commission, 2024; EU AI Act, 2024; EU, 2024

<!--
Speaker notes:
- Austria must transpose by June 2025
- Penalties: Up to 5% global turnover
- Question: "Is regulation the answer?"
- Your careers will implement these
-->

---
<!-- _class: compact -->
# The Doughnut Perspective

## Safe and Just Operating Space

**Ecological Ceiling - AI Impact:**
- Climate: **0.5-1%** of global emissions
- Freshwater: **0.2%** of consumption  
- Chemical pollution: **5% annual growth** in e-waste

**Social Foundation - AI Contribution:**
- Energy access: **200M people** via optimization
- Education: **500M students** with AI tutors
- Health: **1.2B served** without doctors

**Current Status:** Pushing BOTH boundaries simultaneously

**Alternative Path:** Selective deployment for maximum social benefit within ecological limits

###### Sources: Raworth, 2017; Stockholm Resilience Centre, 2024; Future Earth, 2024

<!--
Speaker notes:
- Image suggestion: Doughnut with AI impacts mapped
- We're overshooting ceiling AND failing foundation
- Discussion: "Can AI help us thrive in the safe space?"
- Key metric: Social Return on Carbon Investment
-->

---
<!-- _class: compact -->
# Just Transition Imperatives

## Who Wins, Who Loses?

**Current Winners:**
- Tech companies: **€2.3T market cap** increase
- Skilled workers: **45% wage premium**
- Early adopters: **30% productivity gains**

**Current Losers:**
- Displaced workers: **2.3M in routine jobs**
- Global South: **78% of e-waste** burden
- Future generations: Degraded systems inherited

**Transition Finance Needed:**
- Reskilling: **€450B globally**
- Infrastructure: **€1.2T** for sustainable data centers
- Compensation: **€230B** for affected communities

###### Sources: ILO, 2024; UNCTAD, 2024; Just Transition Fund, 2024

<!--
Speaker notes:
- Transition happens regardless - just or unjust?
- Austrian example: Styrian coal region transition
- Question: "Who should pay for transition?"
- Connect to CSR from Session 2
-->

---
<!-- _class: compact -->
# Three Pathways Forward

## Your Choice to Make

**Path 1: Business-as-Usual**
→ 2% global emissions by 2030
→ Deepening inequality
→ Ecological overshoot

**Path 2: Efficiency-First**
→ Carbon neutral with offsets
→ Rebound effects unchecked
→ Social dimensions ignored

**Path 3: Sufficiency & Justice**
→ Selective AI deployment
→ Net negative emissions possible
→ Within Doughnut boundaries

###### Sources: IPCC, 2023; Future Earth, 2024

<!--
Speaker notes:
- No predetermined outcome
- Your generation decides
- Discussion: "Which path is Austria taking?"
- Individual AND systemic action needed
-->

---
<!-- _class: compact -->
# Your Role as Responsible AI Professionals

## Five Principles for Action

**1. Question Necessity**
"Do we need AI for this?" before "How can AI do this?"

**2. Design for Longevity**
Build systems that last 10 years, not 2

**3. Measure Full Impact**
Carbon + Water + Materials + Social costs

**4. Ensure Fair Distribution**
Benefits to those who bear the costs

**5. Challenge Power Structures**
Democratic governance of AI deployment

###### Sources: IEEE, 2024; AI Now Institute, 2024

<!--
Speaker notes:
- These are YOUR tools for change
- Every line of code is a choice
- Question: "Which principle resonates most?"
- Connect to personal agency
-->

---

# Resolving the Paradox

> "Green AI isn't about choosing between innovation and sustainability. It's about ensuring every joule we invest in intelligence returns dividends in planetary health."


<!--
Speaker notes:
- Return to opening vote - has it changed?
- The paradox is false - we need AND thinking
- Your homework: Calculate your AI carbon footprint
- Final question: "What will you do differently tomorrow?"
- Image suggestion: Balanced scale with AI and Earth
-->

---

# Key References & Resources

**Essential Reading:**
- Rohde et al. (2021). Nachhaltigkeitskriterien für künstliche Intelligenz. IÖW.
- Crawford & Joler (2018). Anatomy of an AI System.
- Future Earth (2024). Digital Transformation for Sustainability.

**Organizations to Follow:**
- Climate Change AI (climatechange.ai)
- Green Algorithms (green-algorithms.org)  
- AI Now Institute (ainowinstitute.org)

**Austrian Initiatives:**
- Circular Futures Platform
- Green Tech Cluster Austria
- AIT Austrian Institute of Technology

**Your Next Steps:**
- Calculate your research carbon footprint
- Join Climate Change AI community
- Advocate for green computing at IMC

<!--
Speaker notes:
- QR code for full bibliography (100+ sources)
- Slack channel for ongoing discussion
- Office hours for career guidance
- Thank you - now let's discuss!
-->