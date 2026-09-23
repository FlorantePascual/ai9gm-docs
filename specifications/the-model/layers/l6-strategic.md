# Layer 6. Strategic

Layer 6

The Enterprise Compass

Should it be built?

![Diagram of Layer 6 Strategic, The Enterprise Compass.](../../assets/layer6.webp)

## Purpose

Decide which AI capabilities the organization should hold, why, and what governance capability it must build to hold them responsibly.

## Scope boundary

| Excluded | Owned by | Boundary |
| --- | --- | --- |
| Whether a system is permitted to operate | L4 | L6 decides the capability is worth having. L4 decides it may run. |
| Prioritization, sequencing and funding allocation | L5 | L6 states the outcome. L5 decides the order and the resourcing. |
| Model sourcing implementation and vendor contracting | L2, L4 | L6 sets the sourcing posture. L2 admits, L4 contracts. |
| Risk acceptance of any kind | L4 | Strategic ambition is not a risk acceptance. |
| Architecture, technology and platform selection | L2 | L6 decides the capability. L2 decides what builds it. |
| Individual work reallocation decisions | L5 | L6 assesses the cumulative position, not the individual case. |


Layer 6 decides whether and why. It decides nothing about how.

**The boundary most often crossed in practice, and it runs downward rather than upward.** Every other layer in this framework has a seam where it accumulates authority belonging above it. Layer 6 has the opposite problem. It cedes authority it holds.

The mechanism is ordinary. The Portfolio Board funds initiatives. Initiatives get delivered. Someone then writes a strategy document describing what the organization is doing with AI, and it describes the sum of what was already funded. The strategy is coherent, accurate and entirely retrospective. It directed nothing.

An organization in this condition has a Layer 5 that sets strategy through funding decisions and a Layer 6 that documents it afterward. Nobody chose this and it is difficult to see from inside, because the strategy document exists and reads well.

The closure is the same shape used at Layer 5. A funding decision requires a traceable strategic outcome as an entry condition. The Portfolio Board still decides what gets funded and when, which is its competence. It cannot fund toward an outcome nobody stated.

## Inputs

| Item | From | Form |
| --- | --- | --- |
| Aggregate exposure assessment | 4 | Provider concentration, correlated failure, cumulative decisioning |
| AI system materiality mechanism | 4 | The threshold that determines what requires formal governance |
| Investment appraisal method and hurdle rate | 4 | The basis on which a case is assessed |
| Regulatory obligation position | 4 | What the organization is already committed to |
| Benefit realization assessments | 5 | Measured outcomes of completed initiatives |
| Capability and skills plan | 5 | What the organization can currently do and what it cannot |
| Aggregate work reallocation position | 5 | Cumulative effect of reallocation decisions above threshold |
| Capacity constraints and lead times | 1 | What any strategy can actually schedule |
| Technology roadmap and rationalization plan | 2 | Existing commitments and their end dates |
| Maturity assessment per layer | 1 | Current governance capability against target |
| Maturity assessment per layer | 2 | Current governance capability against target |
| Maturity assessment per layer | 3 | Current governance capability against target |
| Maturity assessment per layer | 4 | Current governance capability against target |
| Maturity assessment per layer | 5 | Current governance capability against target |
| Market, competitive and regulatory direction | external | Context the organization does not control |


**Input 10 is the one that makes this layer a governance layer rather than a planning function.** Strategy set without a view of the organization's governance maturity produces commitments the other five layers cannot support.

## Outputs

| Item | To | Form |
| --- | --- | --- |
| Enterprise AI strategy with measurable outcomes | 1 | Stated outcomes with the measure and the interval |
| Enterprise AI strategy with measurable outcomes | 2 | Stated outcomes with the measure and the interval |
| Enterprise AI strategy with measurable outcomes | 3 | Stated outcomes with the measure and the interval |
| Enterprise AI strategy with measurable outcomes | 4 | Stated outcomes with the measure and the interval |
| Enterprise AI strategy with measurable outcomes | 5 | Stated outcomes with the measure and the interval |
| Target maturity level per layer | 1 | The governance capability the strategy requires, per layer |
| Target maturity level per layer | 2 | The governance capability the strategy requires, per layer |
| Target maturity level per layer | 3 | The governance capability the strategy requires, per layer |
| Target maturity level per layer | 4 | The governance capability the strategy requires, per layer |
| Target maturity level per layer | 5 | The governance capability the strategy requires, per layer |
| Capability decisions, including decisions not to use AI | 4 | Decision records documented proportionately to materiality |
| Capability decisions, including decisions not to use AI | 5 | Decision records documented proportionately to materiality |
| Model sourcing posture | 2 | Build, buy or multi-provider position with the concentration limit |
| Model sourcing posture | 4 | Build, buy or multi-provider position with the concentration limit |
| Aggregate work reallocation position | 5 | Accepted cumulative effect with the workforce consequence stated |
| Aggregate work reallocation position | external | Accepted cumulative effect with the workforce consequence stated |
| Sustainability targets for AI workloads | 1 | Energy and carbon targets with the measurement method |
| Sustainability targets for AI workloads | 4 | Energy and carbon targets with the measurement method |
| Emerging technology evaluation charters | 5 | Scope with kill criteria and a decision date |
| Strategic outcome assessments | external | Measured results against the stated outcomes |
| Strategic outcome assessments | 5 | Measured results against the stated outcomes |


**Output 2 is what makes the framework operable as a plan rather than as a description.** An organization that states a target maturity per layer has converted a governance model into a roadmap. One that does not has six layers and no destination.

## Decision rights

| ID | Decision | Decides | Consulted | Executes | Evidence | Delegated band | Interpretation |
| --- | --- | --- | --- | --- | --- | --- | --- |
| L6-01 | Approve the enterprise AI strategy | CEO or equivalent | CIO, CAIO, CFO and executive committee | CIO | Approved strategy with measurable outcomes and intervals |  | Decide what the organization is trying to achieve with AI, with measures and intervals. Without measures it is a statement of intent, and funding cannot trace to it. |
| L6-02 | Set the target maturity level per AI9GM layer | CIO | CAIO, CISO, Head of Risk and CFO | Layer owners | Target state per layer with the date and the gap |  | Decide what governance capability the organization should hold, per layer. This converts the framework from a description into a roadmap and is what makes the assessment a gap analysis. |
| L6-03 | Decide whether a business capability should use AI at all | Business Owner | CAIO and Head of Risk | Business Owner | Capability decision record, documented proportionately to materiality, stating the option not taken |  | Decide, for this capability, whether AI is the right answer. A decision not to use AI is recorded, because an organization that never documents restraint cannot distinguish judgment from inattention. |
| L6-04 | Set the model sourcing posture and concentration limit | CIO | CAIO, CFO, Head of Risk and Head of Enterprise Architecture | Head of Enterprise Architecture | Sourcing posture with the concentration position stated |  | Decide build, buy or multi-provider, and how much dependence on one provider is acceptable. Without a posture the estate consolidates by convenience. |
| L6-05 | Accept the aggregate work reallocation position | CEO or equivalent | Head of Talent, Head of Risk and business unit heads | Head of Talent | Accepted position with the workforce consequence stated, including whether the organization retains enough practice to exercise oversight competently over the systems taking the work | Delegated | Accept what the individual reallocation decisions amount to across the organization. |
| L6-06 | Approve a strategic initiative where required layer maturity is not yet in place | CEO or equivalent | CIO, Head of Risk and AI Governance Board | CIO | Approval with the maturity gap named and a remediation plan bound to it |  | Proceed past a governance gap, with the gap named in the approval and a remediation plan bound to it. Permitted deliberately: the failure being prevented is ambition nobody wrote down as a risk. |
| L6-07 | Decide that an emerging technology warrants evaluation | CAIO | CTO and CIO | Innovation lead | Evaluation charter with scope, kill criteria and decision date |  | Decide something is worth a bounded look, with kill criteria and a decision date. Evaluations without kill criteria are pilots under a different name. |
| L6-08 | Approve a business model change enabled by AI | CEO or equivalent, board where material | CIO, CFO and General Counsel | Business Owner | Board decision record |  | Decide the organization will operate differently because of what AI makes possible. |
| L6-09 | Set sustainability and energy accountability targets for AI workloads | CIO | CFO, Platform Owner and CAIO | Platform Owner | Target statement with the measurement method |  | Decide what the organization commits to on energy and carbon for AI, and how it is measured. A target with no measurement method is a statement. |
| L6-10 | Discontinue an AI capability on strategic grounds | Business Owner | CIO, CFO and Business Accountable Executive | PMO Lead | Discontinuation decision with the disposition of data and models |  | Decide a capability ends for reasons other than risk, with data and models dispositioned. |


Three allocations carry the weight of this layer.

**Triggers.** Two decisions in this layer previously stated a cycle and no event.

**L6-04, set the model sourcing posture and concentration limit.** Fires when the Layer 4 aggregate exposure assessment reports concentration above the stated limit. On admission of a model from a provider not currently in the estate.

**L6-05, accept the aggregate work reallocation position.** Fires when cumulative reallocation crosses the workforce reallocation materiality threshold published at Layer 4 §5A. That threshold previously existed with nothing firing against it.

L6-04 and the Layer 4 aggregate exposure acceptance form a control loop, and it is intentional. The assessment triggers posture revision; the posture sets the limit that triggers the assessment.

**The decision not to use AI is a recorded decision.** Under the proportionality rule it is documented at a level matching its materiality, and for most capabilities that is a short entry. It is recorded because an organization that never documents restraint cannot distinguish between a capability it examined and rejected and one it never considered. The first is judgment. The second is a gap. From the outside they look identical, and after eighteen months they look identical from the inside too.

**Aggregate reallocation can remove the competence oversight depends on.** A function that no longer performs a task cannot competently review a system doing it, and EU AI Act Article 26(2) requires that competence in anyone assigned human oversight. Layer 5 sets AI literacy requirements per role and nothing else connects the two, so an organization can satisfy the literacy requirement with training while quietly removing the experience that made the training meaningful. Acceptance of a position under this decision re-triggers L5-10.

**Maturity targets are set here, per layer.** This is the decision that turns AI9GM from a description into something an organization can be measured against. It also constrains ambition honestly: a strategy requiring level 4 Control cannot be approved by an organization sitting at level 1 without the row below.

**Proceeding past a maturity gap is permitted and must be named.** Organizations will pursue AI capabilities their governance cannot yet support, and a framework that forbids it will be ignored rather than followed. The requirement is that the gap is stated in the approval and carries a remediation plan bound to the same decision. The failure this prevents is not ambition. It is ambition that nobody wrote down as a risk.

## Artifacts

| ID | Name | Owner | Review | Scope | Required from |
| --- | --- | --- | --- | --- | --- |
| L6-ART-01 | Enterprise AI strategy with measurable outcomes and intervals | CIO | Annually | organization | Level 3 |
| L6-ART-02 | Target maturity per layer, with current state and gap | CIO | Annually, assessed semi-annually | organization | Level 3 |
| L6-ART-03 | Capability decision register, including decisions not to use AI | Business Owner | On decision | organization | Level 3 |
| L6-ART-04 | Model sourcing posture with concentration limit | CIO | Annually, or on aggregate exposure finding | organization | Level 4 |
| L6-ART-05 | Aggregate work reallocation position | Head of Talent | Per assessment cycle | organization | Level 4 |
| L6-ART-06 | Sustainability targets and measurement method for AI workloads | CIO | Annually | organization | Level 4 |
| L6-ART-07 | Strategic outcome assessments against stated measures | CIO | Per stated interval | organization | Level 4 |
| L6-ART-08 | Emerging technology evaluation charters with kill criteria and decision dates | CAIO | Per evaluation | system | per evaluation |
| L6-ART-09 | Maturity gap approvals with bound remediation plans | CIO | On approval, tracked to closure | system | per approval |


**Scoping.** Organization-level artifacts are required from the stated maturity level. System-level artifacts are required per AI system, model, interface or event according to the condition stated. Artifacts in bold are part of the Level 2 minimum. See the minimum viable set document for what this amounts to at small scale.

**The capability decision register is the artifact nobody has.** Organizations keep records of what they decided to build. Almost none keep records of what they decided not to build, which means the reasoning is lost, the same proposal returns every eighteen months, and the organization relearns the same conclusion at full cost.

## Metrics

| Name | Unit | Guidance |
| --- | --- | --- |
| Layers at or above their target maturity | Count against six | The framework's own measure. A profile, never a composite score. |
| Funded AI initiatives traceable to a stated strategic outcome | Percentage | Below 100 means Layer 5 is setting strategy through funding |
| Capability decisions with a documented outcome, including decisions not to use AI | Percentage | Measures whether restraint is visible |
| Emerging technology evaluations closed against their stated kill criteria | Percentage | Evaluations that never close are pilots with a different name |
| Strategic outcomes with a measured result at the stated interval | Percentage | Measures whether the strategy is assessed or asserted |


Revenue, market position and competitive measures are excluded. All are outcomes the strategy pursues rather than measures of whether this layer is governed.

## Crosswalk

| Instrument | Coverage | Reference |
| --- | --- | --- |
| ISO/IEC 38500 | full | Evaluate, Direct, Monitor. Responsibility, strategy, acquisition, performance, conformance principles. |
| COBIT 2019 | full | EDM01 governance framework setting, EDM02 benefits delivery, EDM03 risk optimization, APO02 managed strategy, APO04 managed innovation |
| TOGAF 10 | partial | ADM Phase A Architecture Vision, Business Architecture, Architecture Vision stakeholder management |
| ISO/IEC 42001 | partial | Clause 4 context of the organization, clause 5 leadership and AI policy, clause 6.2 AI objectives and planning |
| ITIL 4 | partial | Strategy management, portfolio management, continual improvement |
| NIST AI RMF | partial | GOVERN 1, policies and processes aligned to organizational strategy and risk tolerance |
| ISO/IEC 27001:2022 | partial | Clause 4 context, clause 6.2 objectives |
| Greenhouse Gas Protocol, CSRD | partial | Scope 2 and 3 accounting applicable to AI workload energy. Covers focus area 5 only. |
| PMI portfolio and program standards | partial | Portfolio strategic alignment |
| EU AI Act | none | The regulation governs systems and their providers and deployers. It does not govern whether an organization should pursue an AI capability. |
| STRATA Protocol | none | STRATA governs delivery. It has no strategic layer and does not claim one. |


**Two gaps this crosswalk exposes.** No instrument requires an organization to record a decision not to use AI. Every framework listed governs the AI an organization has. None creates a record of the AI it considered and declined, which means restraint leaves no evidence and cannot be distinguished from inattention.

No instrument makes governance capability a precondition of strategic ambition. Each specifies what good governance looks like. None requires an organization to state what governance capability its strategy needs, or to name the gap when it proceeds without it. The maturity target and the gap approval at section 5 are AI9GM's, and together they are the mechanism that connects the strategic layer to the five beneath it rather than leaving it as an aspiration on top.

## Maturity descriptors

| Level | Name | Descriptor |
| --- | --- | --- |
| 1 | Initial | AI activity happens where budget and enthusiasm coincided. No stated AI strategy, or one that names technologies rather than outcomes. Decisions not to use AI are not decisions, because nobody was asked. Governance capability is not considered when commitments are made. |
| 2 | Managed | An AI strategy document exists and is broadly accurate. It was largely assembled from initiatives already underway. Outcomes are stated in general terms without measures or intervals. Emerging technology evaluations run without kill criteria. Sourcing happens by procurement convenience rather than by posture. |
| 3 | Defined | The strategy states outcomes with measures and intervals, and funding at Layer 5 requires traceability to one of them. A target maturity level is set per AI9GM layer. Capability decisions are recorded, including decisions not to proceed, documented proportionately to materiality. A model sourcing posture with a concentration limit is published. Evaluations carry kill criteria and decision dates. Where a strategic initiative outruns governance capability, the gap is named in the approval and a remediation plan is bound to it. |
| 4 | Quantitatively Managed | Strategic outcomes are measured at the stated intervals and the results inform the next cycle. Maturity is assessed per layer against target and the trajectory is tracked rather than the position. Aggregate exposure and aggregate reallocation are reviewed as strategic positions rather than as risk reports. Benefit realization from Layer 5 is used as evidence in funding decisions. |
| 5 | Optimizing | Strategy is revised from measured outcomes on a defined cycle rather than annually by convention. Maturity targets are adjusted from what the estate actually requires rather than from ambition. Sourcing posture responds to measured concentration before it becomes exposure. The capability decision register is consulted before new proposals, so the organization stops relearning conclusions it already reached. |


The distance between levels 2 and 3 is the largest in the framework, and it is almost entirely about sequence. At level 2 the strategy describes what was funded. At level 3 the funding requires a strategy to point at. No new capability is needed. The order of two existing activities has to be reversed, and that is harder than it sounds because it means the Portfolio Board has to decline a good proposal that serves no stated outcome.

## Anti-patterns

### Retroactive strategy

The AI strategy document is accurate, coherent and describes the sum of what was already funded. It directed nothing. Layer 5 is setting strategy through funding decisions and Layer 6 is documenting the result.

Detection: Detected by comparing the approval date of the strategy against the start dates of the initiatives it describes.

### The unrecorded no

Every capability the organization decided against left no trace. The same proposal returns every eighteen months and is evaluated from scratch at full cost. From outside, an organization that examined and declined AI for a process is indistinguishable from one that never considered it.

Detection: Detected by asking for three capabilities the organization decided not to pursue in the last two years, and why.

### Ambition without maturity

The strategy commits to autonomous operations, agentic workflows or AI-native processes. Layer 4 has no AI system register and no published thresholds. The commitment was made without anyone stating what governance capability it required.

Detection: Detected by reading the strategy's commitments against the current maturity profile, layer by layer.

### Evaluations that never close

The innovation function runs a portfolio of emerging technology evaluations. None has kill criteria and none has concluded. Evaluation has become a permanent state and the organization has pilots under a different name.

Detection: Detected by listing open evaluations with their start dates and asking which have a decision date.

### Concentration by default

No sourcing posture exists, so every team selects the provider that was easiest at the time, and they converge on the same one. The organization holds a strategic dependency it never chose and cannot easily reverse.

Detection: Detected by the provider concentration figure in the Layer 4 aggregate exposure assessment, compared against any document stating an intended position.

### Sustainability asserted

Energy and carbon targets are published for AI workloads. Nothing measures energy per training run or per inference, and Layer 1 was never asked to. The target is a statement rather than a position.

Detection: Detected by asking for the measured figure the target is tracked against.
