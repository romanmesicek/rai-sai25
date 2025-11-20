---
marp: true
theme: neutral
size: 16:9
paginate: true
order: 7
---

<!-- description: The AI/Sustainability Paradox - Positive and Negative Impacts -->

<!-- _class: title -->


# AI
## The Artificial Intelligence/Sustainability Paradox

IMC University of Applied Sciences Krems, Austria
Roman Mesicek


SAG Part 3 Cases

###### Full reference list available at [GitHub](https://github.com/romanmesicek/rai-sai25/blob/main/resources/references.md)

---
<!-- _class: chapter -->

# Positive Cases
## Learning from Success Stories

<!--
We'll examine 4 cases where AI demonstrates measurable sustainability benefits.
Focus on quantified outcomes, success factors, and transferability.
Each case includes limitations to maintain critical perspective.
-->

---
<!-- _class: compact -->

# Case 1: DeepMind Data Center Cooling
## AI-Driven Efficiency Success

**Technology**: Reinforcement learning for cooling optimization
**Implementation**: Google data centers globally since 2016

**Quantified Results**:
- 40% reduction in cooling energy consumption
- 15% improvement in Power Usage Effectiveness (PUE)
- 30% reduction in total energy overhead
- Consistent performance across diverse climates

**Technical Approach**:
- Neural networks analyze 120+ variables (temperatures, pump speeds, weather)
- Predictions every 5 minutes with 99.6% accuracy
- Automatic adjustments without human intervention
- Self-improving through continuous learning

###### Sources: Evans & Gao, 2016; Gao, 2014

<!--
Show time-series graph displaying PUE improvement from 2016-2024.
Emphasize this is operational efficiency only - doesn't address growth.
Key point: Best-in-class efficiency still resulted in 48% emissions increase.
-->

---
<!-- _class: compact -->

# Case 1: Analysis & Transferability

**Success Factors**:
- Controlled environment with comprehensive sensor coverage
- Clear optimization target (PUE metric)
- Immediate feedback loops enable rapid learning
- High baseline consumption justifies investment

**Limitations Identified**:
- Requires significant upfront infrastructure investment
- Only addresses operational efficiency, not absolute consumption
- Google's total emissions still increased 48% (2019-2023)
- Rebound effect: Efficiency gains enabled expansion

**Transferability Assessment**:
- Applicable to: Industrial facilities, commercial buildings, district cooling
- Requirements: €100k-500k initial investment, technical expertise
- Payback period: 18-24 months in high-consumption facilities
- Not viable for: Small buildings (<5,000m²), residential applications

###### Sources: IEA, 2023; Google, 2024

<!--
Display waterfall chart showing efficiency gains versus absolute growth.
Critical insight: 6X efficiency improvement, but 10X demand growth.
This exemplifies the core paradox we're exploring.
-->

---
<!-- _class: compact -->

# Case 2: John Deere See & Spray
## Targeted Herbicide Application

**Technology**: Computer vision + deep learning for weed identification
**Deployment**: 10,000+ units globally, 2.5 million hectares covered

**Measured Outcomes**:
- 77% reduction in herbicide use per hectare
- €25-50/hectare cost savings for farmers
- 95% weed detection accuracy at 20 km/h speed
- 60% reduction in chemical runoff to waterways

**System Architecture**:
- 36 cameras scanning 36 meters width
- Processing 20GB data per hour
- Real-time classification of 20 plant species
- Millisecond spray decisions at field speed

###### Sources: Fennimore & Cutulle, 2019; Blue River Technology, 2023

<!--
Show before/after herbicide application maps demonstrating precision.
Emphasize environmental benefits: less chemical use, water protection.
Note the high entry barrier excluding small farmers.
-->

---
<!-- _class: compact -->

# Case 2: Systemic Implications

**Environmental Benefits Documented**:
- 8,500 tonnes less herbicide annually (current deployment)
- 40% reduction in soil contamination levels
- 30% improvement in beneficial insect populations
- Potential 90% reduction if universally adopted

**Economic Barriers**:
- Initial investment: €250,000 minimum
- Requires 100+ hectares for economic viability
- Annual software license: €15,000
- Excludes 94% of global farms (<5 hectares)

**Market Concentration Effects**:
- John Deere captures 100% of efficiency data
- Proprietary formats prevent interoperability
- Creates dependency on single vendor
- Small farms increasingly uncompetitive

###### Sources: FAO, 2024; GRAIN, 2024

<!--
Display pyramid showing farm size distribution versus technology access.
94% of farms globally are too small to benefit.
This technology deepens agricultural inequality while improving efficiency.
-->

---
<!-- _class: compact -->

# Case 3: Austrian Power Grid AI
## Renewable Energy Balancing

**System**: APG (Austrian Power Grid) AI forecasting platform
**Coverage**: 9.5 million consumers, 72% renewable sources

**Performance Metrics**:
- 48-hour demand prediction: 94% accuracy
- 22% reduction in fossil fuel backup requirements
- €12 million annual balancing cost savings
- 15% improvement in wind/solar integration

**Technical Implementation**:
- 8,000 grid sensors providing real-time data
- Weather pattern analysis from 200 stations
- Machine learning models updated every 15 minutes
- Integration with European grid network (ENTSO-E)

###### Sources: APG, 2024; Austrian Energy Agency, 2024

<!--
Show dashboard visualization of real-time grid balance with AI predictions.
Austria's 73% renewable electricity makes this particularly relevant.
Local example students can relate to - possibly arrange site visit.
-->

---
<!-- _class: compact -->

# Case 3: Regional Energy Transition

**Enabling Higher Renewable Penetration**:
- Supports Austria's 2030 target: 100% renewable electricity
- Reduces curtailment of renewable sources by 30%
- Enables 5GW additional renewable capacity without grid expansion
- Cross-border optimization with Germany, Switzerland

**System Requirements**:
- 50 servers running continuously: 438 MWh/year
- Cybersecurity infrastructure: €2 million annually
- 15 specialized AI engineers
- Real-time data from 8 neighboring countries

**Scalability Analysis**:
- Applicable to grids >1GW capacity
- Requires smart meter penetration >80%
- Investment: €50-100 per consumer
- ROI achieved within 2-3 years at current energy prices

###### Sources: European Commission, 2023; ENTSO-E, 2024

<!--
Display map showing interconnected European grid with data flows.
Highlight Austria's strategic position in European energy transition.
Note: System's own energy consumption is significant but justified by gains.
-->

---
<!-- _class: compact -->

# Case 4: AMP Robotics Material Recovery
## AI-Powered Waste Sorting

**Technology**: Computer vision + robotics for recyclable identification
**Deployment**: 300+ facilities across 25 countries

**Operational Performance**:
- 80 items sorted per minute (2x human rate)
- 95% material identification accuracy
- 99% uptime with predictive maintenance
- 10% increase in material recovery rates

**Material Recognition Capabilities**:
- 50+ plastic polymer types identified
- Color sorting within material streams
- Contamination detection to 2% threshold
- Market-grade quality assurance

###### Sources: Ellen MacArthur Foundation, 2019; AMP Robotics, 2024

<!--
Show Sankey diagram of waste streams before and after AI sorting.
Emphasize circular economy contribution - keeping materials in use.
Note this addresses symptom (poor sorting) not cause (overconsumption).
-->

---
<!-- _class: compact -->

# Case 4: Circular Economy Impact

**Resource Recovery Improvements**:
- 2.5 million tonnes additional materials recovered annually
- 40% reduction in recyclables sent to landfill
- €180 million value recovered from waste streams
- 3.2 million tonnes CO₂ avoided through material substitution

**Economic Model**:
- System cost: €500,000 per line
- Payback period: 14-18 months
- Labor cost reduction: 60%
- Quality premiums: 15-20% higher prices

**Systemic Limitations**:
- Addresses sorting, not reduction in waste generation
- Requires steady waste stream for economics
- May reduce incentive for waste prevention
- Energy intensity: 250 kWh per tonne processed

###### Sources: Nature, 2024; Zero Waste Europe, 2024

<!--
Display cost-benefit analysis comparing human versus AI sorting.
Key insight: Profitable because it processes waste, not prevents it.
Risk of lock-in to waste-dependent business models.
-->

---
<!-- _class: chapter -->

# Negative Cases
## Understanding Systemic Failures

<!--
Now examining 4 cases where AI exacerbates sustainability challenges.
Focus on rebound effects, inequality, and unintended consequences.
These aren't failures of technology but of implementation and governance.
-->

---
<!-- _class: compact -->

# Case 5: Google's Efficiency Paradox
## When Optimization Increases Consumption

**Context**: Industry-leading efficiency meets exponential growth
**Period analyzed**: 2019-2023

**Efficiency Achievements**:
- 6X improvement in computational efficiency
- PUE reduced from 1.21 to 1.10 (world-leading)
- 100% renewable energy (annual matching basis)
- 90% carbon-free energy in 5 data center regions

**Absolute Impact Reality**:
- Total emissions increased 48%
- Scope 3 emissions increased 65%
- Energy consumption increased 34%
- Water consumption increased 20%

###### Sources: Google, 2024; Nature, 2024

<!--
Show dual-axis chart: efficiency gains versus absolute consumption.
This is THE canonical example of Jevons Paradox in AI.
Google does everything right technically but still fails systemically.
-->

---
<!-- _class: compact -->

# Case 5: Systemic Failure Analysis

**Root Causes Identified**:
- Compute demand grew 10X while efficiency improved 6X
- AI workloads increased from 10% to 40% of total
- Each efficiency gain enabled new use cases
- Marginal cost reductions drove usage expansion

**Hidden Emissions (Not in Reports)**:
- Customer device energy: ~30% additional
- Network infrastructure: ~20% additional
- Induced behavioral changes: Unquantified
- Competitive arms race effects: Accelerating

**Industry-Wide Pattern**:
- Microsoft: +29% emissions (2020-2023)
- Meta: +66% emissions (2019-2023)
- Amazon: +39% emissions (2019-2023)
- All achieved "efficiency improvements"

###### Sources: Science, 2024; Carbon Disclosure Project, 2024

<!--
Display industry comparison of efficiency claims versus actual emissions.
Every major tech company shows same pattern - efficiency up, emissions up more.
This challenges the entire "green AI" narrative.
-->

---
<!-- _class: compact -->

# Case 6: Amazon Delivery Optimization
## Efficiency Enabling Overconsumption

**AI Implementation**: Route optimization across 200,000 daily routes
**Scale**: 100 million packages routed by machine learning

**Efficiency Metrics**:
- 16% reduction in miles per package
- 20% improvement in delivery density
- 25% reduction in failed first attempts
- 30% faster delivery times achieved

**Consumption Explosion**:
- 2-day delivery increased purchases 30%
- Same-day delivery increased purchases 45%
- Total deliveries increased 65%
- Net transport emissions increased 18%

###### Sources: Amazon, 2024; Transportation Research Part D, 2024

<!--
Show flow diagram illustrating how efficiency gains are offset by volume.
Classic rebound effect: Making something cheaper/easier increases demand.
The convenience enabled by AI optimization drives overconsumption.
-->

---
<!-- _class: compact -->

# Case 6: Urban Impact Assessment

**Environmental Externalities**:
- 40% increase in urban delivery vehicles
- 2.3X increase in packaging waste
- 35% increase in PM2.5 from delivery traffic
- Return rate: 30% (double emissions per item)

**Social Costs**:
- Gig drivers average €8.50/hour after expenses
- No benefits, unstable income patterns
- 40% of miles driven without packages (deadheading)
- Algorithm-determined routes unsafe in 15% of cases

**Urban Planning Disruption**:
- Retail space decreased 20% in city centers
- Warehouse land use increased 300%
- Traffic congestion cost: €2.1 billion annually (EU)
- Public space occupation by delivery vehicles

###### Sources: T&E, 2024; European Environment Agency, 2024

<!--
Display urban heat map showing delivery vehicle concentration.
Cities like Vienna experiencing transformation due to delivery optimization.
Efficiency in logistics reshapes urban form with hidden costs.
-->

---
<!-- _class: compact -->

# Case 7: Precision Agriculture Inequality
## Technology Deepening Rural Disparities

**Global Agricultural Structure**:
- 2.6 billion people depend on small farms (<5 hectares)
- 84% of farms worldwide are smallholder operations
- These farms produce 35% of global food supply
- Average farm size: 1.6 hectares globally, 16 hectares EU

**Technology Access Reality**:
- Precision agriculture requires 100+ hectares for ROI
- Initial investment: €250,000-500,000
- Only 3% of Global South farmers have access
- 94% of AI benefits accrue to large operations

**Market Concentration Acceleration**:
- Small farm bankruptcies increased 40% (2020-2024)
- Land consolidation rate doubled
- 4 companies control 70% of agricultural AI
- Same companies control seed/chemical markets

###### Sources: FAO, 2024; Via Campesina, 2024

<!--
Show global map comparing technology access versus farm size distribution.
This exemplifies how AI can deepen existing inequalities.
Efficiency gains concentrated among those already advantaged.
-->

---
<!-- _class: compact -->

# Case 7: Data Colonialism Pattern

**Data Extraction Dynamics**:
- John Deere collects 5TB per farm per season
- Farmers don't own their operational data
- Data used for commodity speculation
- Proprietary formats prevent portability

**Economic Displacement**:
- Traditional knowledge devalued/displaced
- Local seed varieties eliminated
- Input costs increased 200% with tech adoption
- Debt-driven farm consolidation accelerating

**Food Security Implications**:
- Crop diversity decreased 60% in tech-intensive regions
- Resilience to climate shocks reduced
- Local food systems disrupted
- Import dependency increased 35%

###### Sources: GRAIN, 2024; ETC Group, 2023

<!--
Display power structure diagram showing data and control flows.
New form of colonialism - data extraction from Global South.
Parallels historical patterns of resource extraction.
-->

---
<!-- _class: compact -->

# Case 8: Industry 4.0 Labor Displacement
## Siemens Amberg "Lights-Out" Factory

**Automation Achievement**:
- 99.99885% quality rate (1 defect per 100,000)
- 75% of production steps fully automated
- 50 million data points analyzed daily
- 30% productivity improvement

**Employment Impact**:
- Workforce reduced from 1,200 to 400
- Remaining jobs: 85% require engineering degrees
- Average wage increased 40%
- Total wage bill decreased 50%

**Replication Pattern (EU Manufacturing)**:
- 3.5 million manufacturing jobs at risk by 2030
- 500,000 new technical positions created
- Net loss: 3 million positions
- Skills mismatch: 70% displaced workers unqualifiable

###### Sources: Siemens, 2024; OECD, 2024

<!--
Show waterfall chart: job losses versus gains by skill level.
High-skill jobs increase, middle-skill jobs disappear.
Social contract of industrial employment breaking down.
-->

---
<!-- _class: compact -->

# Case 8: Regional Deindustrialization

**Failed Reshoring Promise**:
- Adidas Speedfactory (Germany): Closed after 3 years
- 160 jobs created vs. 10,000 previously offshored
- Production still cheaper in Asia with automation
- €100 million investment written off

**Structural Unemployment Emerging**:
- Manufacturing regions: 25% youth unemployment
- Retraining programs: 15% success rate
- Social costs: €45 billion annually (EU)
- Regional inequality increasing

**Supply Chain Implications**:
- Automation enables further concentration
- 10 mega-factories replace 1,000 smaller ones
- Transport emissions increase despite local production
- Resilience decreased through centralization

###### Sources: MIT Technology Review, 2024; European Commission, 2024

<!--
Display regional map showing manufacturing job losses concentration.
Automation doesn't bring jobs back - it eliminates them globally.
Political promise of reshoring through AI proving false.
-->

---
<!-- _class: chapter -->

# Analysis & Synthesis
## Patterns Across Cases

<!--
Now we synthesize learnings from all 8 cases.
Identify recurring patterns, success factors, and failure modes.
Prepare students for design workshop with critical framework.
-->

---
<!-- _class: compact -->

# Pattern Recognition

**Success Patterns**:
- Clear, measurable optimization targets
- Controlled environments with rich data
- Immediate economic benefits align with sustainability
- Existing infrastructure can be adapted

**Failure Patterns**:
- Efficiency gains enable consumption growth
- Benefits concentrate among already-advantaged
- Externalities ignored in optimization
- Systemic effects overwhelm local improvements

**Critical Factors**:
- Scale of deployment determines net impact
- Geographic location affects carbon intensity 5-13X
- Market structure shapes distribution of benefits
- Regulatory framework essential for positive outcomes

