# Layer 5. Execution

Layer 5

The Leadership Engine

Can it be built?

![Diagram of Layer 5 Execution, The Leadership Engine.](../../assets/layer5.webp)

## Purpose

Convert authorized intent into delivered capability through sequencing, delivery discipline and the people who do the work.

## Scope boundary

| Excluded | Owned by | Boundary |
| --- | --- | --- |
| Whether a business capability should exist | L6 | L5 delivers it. L6 decides it is worth having. |
| Whether a system is permitted to operate | L4 | L5 runs delivery gates. L4 authorizes production use. |
| Risk acceptance of any kind | L4 | A delivery gate is not a risk decision and must not become one. |
| AI system classification and materiality | L4 | L5 consumes the classification as a delivery constraint. |
| Architecture standards and technology selection | L2 | L5 sequences the work. L2 decides what it is built with. |
| Model development and validation | L3 | L5 schedules it. L3 performs it. |
| Infrastructure capacity provisioning | L1 | L5 forecasts demand. L1 provisions against it. |
| Phase gating of AI-assisted development | STRATA Stratum 4 | L5 references the execution loop. It does not restate it. |


Layer 5 delivers what Layer 6 chose and Layer 4 permitted. It decides neither.

**The boundary most often crossed in practice.** A delivery gate becomes an authorization by default.

An initiative passes every stage gate the PMO defined. Requirements were signed off, testing completed, the business declared itself ready. The system goes live. It has no classification record, no named Business Accountable Executive and no Layer 4 deployment authorization, because every gate tested delivery readiness and none tested governance readiness.

Nobody bypassed a control. The controls were all in the other layer, and the gate never asked for them.

This is the Layer 5 seam and it is the most common route by which an ungoverned AI system reaches production. Section 5 addresses it by making Layer 4 evidence a gate entry condition rather than a parallel process.

## Inputs

| Item | From | Form |
| --- | --- | --- |
| Approved strategy and intended outcomes | 6 | Strategy with measurable outcomes and priority |
| Mandatory control catalog by consequence class | 4 | Delivery constraints applicable per system class |
| Published delegated band thresholds | 4 | Section 5A of the Layer 4 specification |
| AI system classification and materiality determinations | 4 | Classification record per initiative delivering an AI system |
| Deployment authorizations | 4 | Authorization records, consumed as gate entry conditions |
| Cost envelope and appraisal method | 4 | Funding boundary and hurdle rate |
| Capacity constraints and lead times | 1 | Forecast that bounds what can be scheduled |
| Architecture standards and rationalization plan | 2 | What the delivery must conform to |
| STRATA artifact trail per codebase | 2 | Classification record, authority chain, phase sign-offs, deviation log |
| Model readiness and validation status | 3 | Evidence that a model is ready for a gate |
| Skills inventory | external | Current capability against demand |

## Outputs

| Item | To | Form |
| --- | --- | --- |
| Prioritized portfolio with a stated sequence | 1 | Sequenced initiatives with dependencies named |
| Prioritized portfolio with a stated sequence | 2 | Sequenced initiatives with dependencies named |
| Prioritized portfolio with a stated sequence | 3 | Sequenced initiatives with dependencies named |
| Resource and capacity demand forecast | 1 | Demand by workload class and period |
| Stage gate records with entry and exit evidence | 4 | Gate records referencing the Layer 4 authorizations relied on |
| Delivery performance reporting | 4 | Against the measures set at section 7 |
| Delivery performance reporting | 6 | Against the measures set at section 7 |
| Change adoption evidence | 4 | Training completion, usage, competence assessment |
| Change adoption evidence | 6 | Training completion, usage, competence assessment |
| Capability and skills plan | 6 | Gap assessment with hiring and development actions |
| AI literacy records per role | 4 | Requirement, completion and competence assessment |
| Benefit realization assessment | 6 | Measured outcome against the case that funded the work |
| Lessons and deviation records | 2 | What changed from plan, why, and what it implies |
| Lessons and deviation records | 6 | What changed from plan, why, and what it implies |


**Output 8 closes the loop that most organizations leave open.** Layer 6 funds an initiative against a stated benefit. Unless Layer 5 measures whether the benefit arrived, Layer 6 decides the next investment on the same evidence it used for the last one.

## Decision rights

| ID | Decision | Decides | Consulted | Executes | Evidence | Delegated band | Interpretation |
| --- | --- | --- | --- | --- | --- | --- | --- |
| L5-01 | Prioritize and fund an AI initiative | Portfolio Board | CIO, CFO, Business Owner and CAIO | PMO Lead | Portfolio decision record with funding allocation. Entry conditions: a traceable strategic outcome, and the L6-03 capability decision record stating why AI. |  | Decide this initiative proceeds and is resourced. From v0.9, a traceable strategic outcome is an entry condition, so funding cannot set strategy by accumulation. |
| L5-02 | Sequence initiatives against capacity constraints | PMO Lead | Platform Owner, CTO and Portfolio Board | PMO Lead | Sequence record naming what was deferred and the date by which the deferral is reconsidered |  | Decide the order, bounded by Layer 1 lead times. The record names what was deferred. |
| L5-03 | Select the delivery methodology for an initiative | PMO Lead | CTO and Business Owner | Delivery team | Delivery approach record. Where AI assists development, STRATA governs regardless of the methodology selected. |  | Choose agile, waterfall or hybrid. Where AI assists development, STRATA applies on top of whichever is chosen rather than instead of it. |
| L5-04 | Approve a stage gate for an initiative below materiality | PMO Lead | Business Owner and Model Owner | Delivery team | Gate record with entry and exit evidence | Delegated | Confirm the initiative has met the entry and exit criteria for this phase. |
| L5-05 | Approve the production readiness gate for an initiative at or above materiality | PMO Lead | Business Accountable Executive, Model Owner and Head of Risk | Delivery team | Gate record. The Layer 4 deployment authorization is a mandatory entry condition. Absent it, the gate cannot be approved. Where the initiative consumes an existing model, a statement that its use sits within that model card's stated purpose, or an L4-AUT-04 approval. | Delegated | Confirm delivery readiness. The Layer 4 authorization is a mandatory entry condition, which is what stops the delivery pipeline from becoming an authorization bypass. |
| L5-06 | Determine that a pilot has become a production system | Business Accountable Executive | PMO Lead, CAIO and Head of Risk | PMO Lead | Transition record triggering Layer 4 classification | Delegated | Decide the pilot has crossed into production and now requires classification. Without this decision, pilot status functions as a governance exemption nobody granted. |
| L5-07 | Allocate scarce specialist capacity between initiatives | PMO Lead | CTO and Portfolio Board | PMO Lead | Allocation record naming the initiative deferred |  | Decide who works on what when there is not enough of them. |
| L5-08 | Stop or reset a failing initiative | Portfolio Board | PMO Lead, Business Owner and CFO | PMO Lead | Stop decision with the lessons record |  | Decide an initiative ends or restarts, with the lessons recorded. |
| L5-09 | Approve the AI capability and hiring plan | Head of Talent | CIO, CAIO and CFO | Head of Talent | Capability plan with skills gap assessment |  | Decide what capability the organization builds or buys against the gap assessment. |
| L5-10 | Set the AI literacy requirement for a role | Head of Talent | CAIO, CISO and business unit head | Head of Talent | Requirement per role, with completion and competence records. Re-set on acceptance of an aggregate reallocation position under L6-05. |  | Decide what a person in this role must understand about AI. Competence, not completion, and Article 4 has applied since February 2025. |
| L5-11 | Authorize workforce use of a general-purpose AI tool | CIO | CISO, DPO, Head of Talent and General Counsel | IT | Tooling authorization with the data boundary stated |  | Decide which tools staff may use and where the data boundary sits. Unauthorized adoption happens regardless; the register makes its absence detectable. |
| L5-12 | Reallocate work from people to an AI system | Business Owner | Head of Talent, CAIO and Head of Risk | Change team | Reallocation record stating the work moved, the basis and the workforce consequence. Where the reallocation materiality threshold is met, an aggregate position is required at Layer 6. | Delegated | Decide work moves from a person to a system. Distinct from what an agent may do: this is what a person will stop doing. Head of Talent is consulted without exception. |
| L5-13 | Approve the change adoption plan for a material AI system | Business Owner | PMO Lead and Head of Talent | Change team | Adoption plan with completion evidence |  | Decide how the organization is prepared for the system to arrive. |
| L5-14 | Declare an initiative ready for business adoption | Business Owner | PMO Lead and Model Owner | Change team | Readiness record with training completion evidence, and competence evidence for any role holding human oversight |  | Decide the business can now rely on it, with training completed. |


Three allocations carry the weight of this layer.

**L5-01 and L5-05 carry the framework's two enforcement points.** Funding and the production gate are the points every initiative must pass through, which makes them where decisions taken elsewhere become enforceable. Three entry conditions sit here for that reason: the traceable strategic outcome and the capability decision record at funding, and the Layer 4 authorization plus the model purpose statement at the gate. Each fixes a decision in another layer whose own trigger is weak.

**L5-05 and L5-14 are different decisions and must not collapse.** L5-05 asks whether the system works. L5-14 asks whether the organization is ready to use it. Both sit near the same point in a delivery cycle and both produce a readiness record, and where they merge it is adoption readiness that disappears, because the gate carrying a mandatory entry condition survives. The result is a system deployed correctly into a business that cannot use it.

**The production readiness gate has a Layer 4 entry condition.** This single row is what stops the delivery pipeline from becoming an authorization bypass. The PMO still decides delivery readiness, which is its competence. It cannot decide governance readiness, and it cannot proceed without evidence that someone who could has.

**Pilot transition is a named decision, not a drift.** Pilots become production systems by usage rather than by decision, and while a system is called a pilot the classification and authorization requirements never trigger. Making the transition a decision with a named owner is what stops indefinite pilot status from functioning as a governance exemption. The threshold that defines it is recorded as an open item.

**Work reallocation is a decision with a mandatory consultation, not an efficiency outcome.** The Business Owner decides, because it is a business process decision and the process is theirs. The Head of Talent is consulted without exception, because the consequence is a workforce one and the deciding role has no reason to surface it.

The decision is distinct from the autonomous action authorization at Layer 4. That one asks what an agent may do. This one asks what a person will stop doing, which affects a different set of people and carries a different accountability.

Individual reallocations sit here. Where they cross the reallocation materiality threshold published at Layer 4, the cumulative position is assessed at Layer 6. The structure mirrors aggregate exposure: distributed decisions, central assessment of what they amount to.

**Workforce AI tooling is authorized, not assumed.** Individual adoption of general-purpose AI tools happens whether or not anyone authorizes it. The decision exists so a data boundary is stated somewhere, and so the absence of an authorization is a detectable condition rather than an unexamined one.

## Artifacts

| ID | Name | Owner | Review | Scope | Required from |
| --- | --- | --- | --- | --- | --- |
| L5-ART-01 | AI literacy requirements per role, with completion and competence records | Head of Talent | Annually, on role change | organization | Level 2 |
| L5-ART-02 | Workforce AI tooling authorization register with data boundaries | CIO | On change | organization | Level 2 |
| L5-ART-03 | Pilot register with transition status and stated end date | PMO Lead | Monthly | organization | Level 2 |
| L5-ART-04 | Portfolio register with sequence and dependencies | PMO Lead | Per planning cycle | organization | Level 3 |
| L5-ART-05 | Resource and capacity demand forecast | PMO Lead | Quarterly, published to L1 | organization | Level 3 |
| L5-ART-06 | Skills inventory and AI capability plan | Head of Talent | Semi-annually | organization | Level 3 |
| L5-ART-07 | Benefit realization assessments | PMO Lead | At a stated interval after go-live | organization | Level 4 |
| L5-ART-08 | Lessons and deviation records | PMO Lead | Per initiative | organization | Level 4 |
| L5-ART-09 | Stage gate records with entry and exit evidence | PMO Lead | Per gate | system | per initiative delivering an AI system |
| L5-ART-10 | Change adoption plans and completion evidence | Business Owner | Per material system | system | at or above materiality |
| L5-ART-11 | Work reallocation records with stated workforce consequence | Business Owner | Per reallocation, aggregated to L6 | system | per reallocation |


**Scoping.** Organization-level artifacts are required from the stated maturity level. System-level artifacts are required per AI system, model, interface or event according to the condition stated. Artifacts in bold are part of the Level 2 minimum. See the minimum viable set document for what this amounts to at small scale.

EU AI Act Article 4 has applied since February 2025 and is independent of the Annex III deferrals.

**The pilot register is the artifact this layer is usually missing.** Organizations can list their projects and their production systems. The set between the two, running against real data with real users and no governance trigger, is rarely enumerated anywhere.

## Metrics

| Name | Unit | Guidance |
| --- | --- | --- |
| Material AI systems reaching production with a Layer 4 authorization recorded before go-live | Percentage | Target 100. Any other value means the gate entry condition is not operating. |
| Initiatives delivering an AI system with a named Business Accountable Executive before the first gate | Percentage | Naming at go-live means nobody was accountable during the build |
| Pilots past their stated transition review date | Count | Rising counts mean pilot status is functioning as an exemption |
| Roles with an AI literacy requirement met and competence assessed | Percentage | Completion alone is not competence. Both are counted. |
| Funded initiatives with a benefit realization assessment completed at the stated interval | Percentage | Measures whether Layer 6 gets evidence or assertion |


Delivery velocity, on-time completion and budget variance are excluded. All three measure whether delivery is working, not whether it is governed, and all three belong in portfolio reporting.

## Crosswalk

| Instrument | Coverage | Reference |
| --- | --- | --- |
| COBIT 2019 | full | APO05 managed portfolio, APO07 managed human resources, BAI01 managed programs, BAI05 managed organizational change, BAI11 managed projects |
| PMI portfolio and program standards | full | Portfolio management, program management, benefits realization management |
| ITIL 4 | partial | Change enablement, organizational change management, workforce and talent management, project management practice |
| ISO/IEC 42001 | partial | Clause 7 support: competence, awareness, communication. Clause 7.2 competence bears directly on AI literacy. |
| NIST AI RMF | partial | GOVERN 2 accountability structures, GOVERN 3 workforce competence and diversity |
| EU AI Act | partial | Article 4 AI literacy, applicable since February 2025 and independent of the high-risk deferrals. Article 26(2) requires deployers to assign human oversight to people with the necessary competence, training and authority. |
| ISO/IEC 27001:2022 | partial | A.6.3 awareness and training, A.6.1 screening |
| TOGAF 10 | partial | Implementation governance, migration planning |
| ISO/IEC 38500 | partial | Human behavior principle |
| STRATA Protocol | companion | Stratum 4 execution loop governs phase gating for AI-assisted development. Stratum 5 artifacts satisfy evidence requirements here without duplication. |


**Two gaps this crosswalk exposes.** No delivery framework gates on governance readiness. COBIT, PMI and ITIL all specify stage gates and all specify them against delivery criteria: requirements complete, testing passed, business ready. None makes an authorization from a governance function a mandatory entry condition. The provision at section 5 is AI9GM's, and it is the mechanism that closes the seam described at section 2.

No instrument governs the reallocation of work between humans and AI. Focus area 9 names workforce collaboration and productivity. Every instrument in this list addresses training people to work with AI systems. None addresses who decides that a task moves from a person to a system, on what basis, or who is accountable for the workforce consequence.

AI9GM v0.9 allocates it at section 5: Business Owner decides, Head of Talent is consulted without exception, and the cumulative position is assessed at Layer 6 above the reallocation materiality threshold.

## Maturity descriptors

| Level | Name | Descriptor |
| --- | --- | --- |
| 1 | Initial | AI initiatives start where someone had budget and enthusiasm. No portfolio view. Gates exist for large projects and not for AI work, which is treated as experimental. Pilots run indefinitely. Nobody can list which AI initiatives are underway. AI literacy is assumed from job title. |
| 2 | Managed | A portfolio register exists and covers funded initiatives. Stage gates are applied to AI work using the general project template. Some pilots have end dates. Capacity is planned for the initiatives that asked. AI literacy training is offered and completion is tracked. Business Accountable Executives are named at go-live. |
| 3 | Defined | Every initiative delivering an AI system names its Business Accountable Executive before the first gate. The production readiness gate carries the Layer 4 authorization as a mandatory entry condition. Pilots are registered with transition review dates and a named owner for the transition decision. AI literacy requirements are set per role and competence is assessed, not just completion. Benefit realization is assessed at a stated interval. Workforce AI tooling is authorized with a stated data boundary. |
| 4 | Quantitatively Managed | Gate compliance, pilot age, literacy competence and benefit realization are measured and reported to Layer 4 and Layer 6. Capacity demand forecasts are compared against Layer 1 actuals and the forecast method is corrected from the variance. Deferred initiatives are tracked, so the cost of sequencing decisions is visible rather than absorbed. |
| 5 | Optimizing | Gate entry conditions are enforced by the delivery toolchain rather than checked by a person, so an initiative cannot reach a production gate without its authorization attached. Pilot transition triggers automatically on usage thresholds rather than waiting for a review date. Capability planning is driven by portfolio composition rather than by requisition. Benefit outcomes feed Layer 6 as evidence in the next funding cycle rather than as a retrospective. |


The distance between levels 2 and 3 is dominated by one change that costs nothing and is resisted anyway: naming the Business Accountable Executive before the build rather than at go-live. Naming at go-live means the entire build ran without an accountable person, and the name selected is whoever was available rather than whoever should hold it.

## Anti-patterns

### The ungoverned go-live

An initiative passes every delivery gate and reaches production without a classification, a named accountable executive or a deployment authorization. No control was bypassed. The gates tested delivery readiness and nothing tested governance readiness.

Detection: Detected by taking the last five AI systems to reach production and checking whether a Layer 4 authorization predates each go-live date.

### Pilot purgatory

A system has run as a pilot for eighteen months against production data with real users. Because it is a pilot, classification never triggered, no authorization was sought and no accountable executive was named. Pilot status has become a governance exemption that nobody granted.

Detection: Detected by listing every pilot with its start date and asking which are serving real users.

### The unnamed initiative

No Business Accountable Executive exists until go-live. The entire build ran without an accountable person, and the name attached at the end belongs to whoever was available rather than whoever should hold it.

Detection: Detected by comparing the date on the accountability record against the initiative start date.

### Literacy as a completion certificate

AI literacy training is assigned, completed and reported at high percentages. Nobody assessed whether the people exercising human oversight over a production system can actually recognize when its output is wrong. Article 26(2) requires competence, and a completion rate does not evidence it.

Detection: Detected by asking an oversight-assigned person to describe the failure mode they are watching for.

### Benefits asserted, never measured

Initiatives are funded against stated benefits. No assessment happens after go-live. Layer 6 funds the next initiative on the same class of assertion that justified the last one, with no evidence about whether the last one worked.

Detection: Detected by asking for the realized benefit of the three largest AI initiatives completed more than a year ago.

### Shadow tooling

The workforce adopts general-purpose AI tools individually, through personal accounts and browser extensions. No authorization exists, no data boundary is stated and nobody can say what corporate information has been pasted into which service.

Detection: Detected by reconciling outbound traffic and expense claims against the tooling authorization register.
