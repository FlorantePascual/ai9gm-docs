# AI-Centric IT Governance Model

**Normative reference. Specification v0.9 (Draft for Review).**

| | |
|---|---|
| **Specification** | AI9GM v0.9 |
| **Status** | Draft for Review. Not accredited. No conformity assessment exists. |
| **Editor** | Florante Pascual |
| **Published by** | Florante Pascual |
| **Revised** | 17 August 2026 |
| **Supersedes** | AI9GM (unversioned) |
| **Companion** | STRATA Protocol, strataprotocol.org |

---

## 0. How to read this document

This is the normative reference for AI9GM. Where any other AI9GM material conflicts with this document, this document controls.

Narrative material (the manifesto, the homepage, articles) references this specification. It does not restate layer definitions. That rule exists because every unversioned restatement drifts, and drift is what produced the conflicting drafts this version replaces.

### 0.1 Conventions

**Single-owner rule.** No focus area belongs to more than one layer. Where two layers both act on a subject, the split is expressed as declared inputs and outputs, never as duplicated ownership. Section 4 carries the ownership index that enforces this.

**Dependency ordering.** Layers are numbered by dependency, not by importance or value. Weakness low in the stack constrains everything above it. Weakness high in the stack leaves everything below it directionless. Layer 6 is not the goal and Layer 1 is not the starting point for every organization.

**Operate versus require.** Layers 3 and 4 divide on a single line, and the line is load-bearing throughout the specification.

> Layer 3 operates controls and produces evidence.
> Layer 4 decides which controls are required, sets risk appetite and verifies the evidence.

Two tests resolve any disputed assignment. *Who is answerable if the control did not run?* That is Layer 3. *Who is answerable if the control was never required in the first place?* That is Layer 4.

**Separation of build and acceptance.** The role that builds a capability never accepts the risk of that capability failing. The role that sets an acceptance threshold never authorizes production use against it.

This rule is what makes the operate-versus-require distinction enforceable rather than descriptive. Without it, a layer read in isolation appears to permit a builder to validate their own work and approve its release. It applies at every layer, not only at the Layer 3 and Layer 4 boundary.

**Delegated band.** A decision right may be split at a published threshold. Below the threshold the decision is operational and sits with the executing role. At or above it, the same decision becomes a risk decision and moves to the role that holds risk authority.

A delegated band has four required properties. It states the measure. It states the threshold value. It names the role on each side. It carries a review cycle.

Layer 4 publishes every threshold. Risk-related thresholds are published as a determination mechanism, because an organization's risk limits are its own and a published number would be adopted without reasoning. Operational thresholds are published as default values, marked as a starting point rather than a standard, because an organization with no basis for setting one needs somewhere to begin.

A delegated band with no published threshold is inert, and any decision right depending on one cannot be exercised.

Delegated bands are how the framework preserves operational speed without allowing operational roles to accumulate risk authority by default.

**Layer and stratum.** Within AI9GM, *layer* refers exclusively to the six governance layers. STRATA Protocol uses *stratum* for its five delivery strata, and *layer* within Stratum 2 for its derivation layers. The two vocabularies do not collide, because STRATA's layers are scoped inside one of its strata and are always named as Stratum 2 derivation layers. Where this specification references STRATA, it names strata by number.

Both frameworks apply the same layering dependency principle: a layer constrains everything above it, and removing one costs the integrity of everything resting on it. The convergence is deliberate.

**Proportionality.** All six layers apply at every organization size. What changes is formality, evidence weight and the number of distinct people holding the decision rights. One person holding six roles is a valid implementation.

**Identifier permanence.** Every identifier this specification publishes resolves permanently, either to its current definition or to a tombstone stating what it was, when it stopped being normative and why. Retirement is a state, not a deletion.

Identifiers are never reused, including after removal. A successor is linked and never redirected to, because a reader who cited an identifier is entitled to see what they cited rather than what replaced it. This applies to decisions, layers, focus areas, thresholds and artifacts.

Each threshold carries a permanent identifier in the form `THR-{NN}`, assigned once at section 5A of the Layer 4 specification and never reused. Each artifact carries a permanent identifier in the form `L{n}-ART-{k}`, where n is the layer and k is the position in that layer's artifact table. Both conventions follow the decision and focus area forms above and are assigned once, per the identifier permanence rule in this section.

**Evidence currency.** A record derived from other records is valid only while every record it references is valid. Where a referenced record expires, is withdrawn or is superseded, the derived record expires with it.

A derived record may state an earlier expiry than its references. It may never state a later one.

This applies wherever one record rests on another: a composite accountability record on domain risk acceptances, a deployment authorization on validation evidence, a classification record on the materiality mechanism it was determined under, a model card on its training data manifest, an interface fitness record on the specification version it was declared against.

**Decision triggers.** Every decision states at least one event that fires it, or states explicitly that it fires only on a cycle. A decision with no stated trigger cannot be distinguished from one whose trigger was omitted.

Where the triggering event is one nobody observes, the specification states how it is detected, or states that detection is unresolved. A trigger that fires on an act no process witnesses is not a trigger. Three decisions currently carry this condition: L2-02 third-party admission, L3-12 feature reuse and L4-AUT-04 model reuse.

**Artifact scoping.** Artifacts are not required uniformly. Each is scoped on one of two axes.

**Organization-level artifacts** exist once regardless of how many AI systems run: registers, policies, catalogs, the threshold table, the strategy. These are required from a stated maturity level.

**System-level artifacts** exist once per AI system, model, interface or event: model cards, fitness declarations, risk acceptances, authorizations, impact assessments. These are required per instance according to the system's consequence class and materiality.

An artifact list read without its scoping column overstates what any given organization must produce. Seventy-one artifact types exist across the six layers. No organization produces all of them, and a small organization at Level 2 with no material systems produces a fraction. The minimum viable set is published separately.

### 0.2 What this specification does not do

It confers no certification. It grants no accreditation. It does not make an organization compliant with the EU AI Act, ISO/IEC 42001 or any other instrument. It organizes the work. Performing the work remains the adopting organization's responsibility.

### 0.3 Name

AI9GM is a numeronym, following i18n, l10n, a11y and k8s.

**AI** + *CentricIT* (9 letters) + **GM** = **AI**-*Centric IT* **G**overnance **M**odel

The nine counts letters. It does not count layers, dimensions or principles.

---

## 1. Scope

AI9GM is a meta-framework. It sits above the governance instruments an enterprise already runs and specifies how they connect for AI.

It answers one question that ISO/IEC 42001, NIST AI RMF, COBIT, ITIL, TOGAF and ISO/IEC 27001 do not answer between them: **how do these disciplines fit together inside an enterprise where AI influences consequential decisions?**

The failures AI9GM addresses do not occur inside any single framework. They occur in the seams. A model trained by one team, deployed by a second, procured by a third and relied upon by a fourth can pass every individual control while leaving no one accountable for the outcome.

AI9GM governs the seams by allocating decision rights across six interdependent layers.

---

## 2. The six layers

| # | Layer | Epithet | Governs | Central question | Strategic focus |
|---|-------|---------|---------|------------------|-----------------|
| 1 | Foundation | The Digital Backbone | Infrastructure, operations, service management | Can it run? | Stability and scale |
| 2 | Structural | The Digital Fabric | Applications, integration, architecture, standards | Can it connect? | Connectivity and cohesion |
| 3 | Intelligence | The Brain & Shield | AI, data, security controls in operation | Can it be trusted? | Trust and insight |
| 4 | **Control** | The Control Tower | Policy, risk decisions, compliance, assurance, cost | Who is accountable? | Accountability and oversight |
| 5 | Execution | The Leadership Engine | Delivery, leadership, talent, change | Can it be built? | Delivery and adoption |
| 6 | Strategic | The Enterprise Compass | Alignment, innovation, sustainability | Should it be built? | Vision and change |

**Change from prior versions.** Layer 4 was named *Governance*. It is now named **Control**. A layer named Governance inside a model named the Governance Model is a naming collision, and it obscured exactly the distinction that Layer 4 exists to draw. The epithet is unchanged.

---

## 3. Layer definitions

Each layer below carries its purpose and its focus areas. The full specification for each layer, covering scope boundary, inputs, outputs, decision rights, artifacts, metrics, crosswalk, maturity descriptors and anti-patterns, is published as a separate document per layer.

Each focus area carries a permanent identifier in the form `L{n}-FA-{k}`, where n is the layer and k is the position in that layer's list. Identifiers are assigned once and are never reused, per the identifier permanence convention at section 0.1.

### Layer 1. Foundation (The Digital Backbone)

**Purpose.** Provide and operate the compute, storage, network and service capacity that every layer above depends on, at a level of availability and performance that AI workloads can be planned against.

**Focus areas.**

1. **L1-FA-01.** Infrastructure and Cloud Strategy. On-premise, cloud and hybrid placement, capacity architecture, accelerator provisioning.
2. **L1-FA-02.** Asset and Configuration Management. Asset tracking, CMDB, lifecycle management. Models and datasets are configuration items.
3. **L1-FA-03.** Operations Management. Monitoring, maintenance, automation, DevOps and SRE practice.
4. **L1-FA-04.** Availability and Capacity Management. Uptime, performance, disaster recovery, capacity forecasting.
5. **L1-FA-05.** Incident and Problem Management. Incident resolution and root cause elimination.
6. **L1-FA-06.** Service Desk and IT Support. User support, ticketing, service levels, self-service.

**Why it matters for AI.** AI workloads make demands that ordinary application infrastructure was not sized for. A weak Foundation layer does not degrade the layers above it gracefully. It caps them.

---

### Layer 2. Structural (The Digital Fabric)

**Purpose.** Connect enterprise systems under declared contracts so process and data move between them, and maintain the architecture standards that determine what gets built and with what.

**Focus areas.**

*Applications and Integration*

1. **L2-FA-01.** Enterprise Applications. ERP, CRM, SCM, HRMS and other business-critical systems.
2. **L2-FA-02.** Custom Software Development. Internal and external engineering. Where AI assists development, delivery governance is held by STRATA Protocol: project classification at Stratum 1, the copilot authority chain at Stratum 3 and the artifact trail at Stratum 5. AI9GM does not restate these.
3. **L2-FA-03.** Application Lifecycle Management. Development, testing, deployment, maintenance.
4. **L2-FA-04.** Integration and Middleware. API management, service orchestration, microservices, event transport.
5. **L2-FA-05.** User Experience, Accessibility and Machine Consumability. Human interface design, plus the completeness properties an interface requires when its consumer cannot ask questions: accurate and complete specification, schemas carrying real examples and honest descriptions, documented error conditions, discoverable authentication and explicit relationships between operations.

*Architecture and Standards*

6. **L2-FA-06.** Enterprise Architecture Frameworks. TOGAF, Zachman.
7. **L2-FA-07.** Service Management and ITSM Alignment. ITIL and COBIT alignment of services to business need.
8. **L2-FA-08.** IT Product Management. IT systems managed as products with roadmaps.
9. **L2-FA-09.** Standards and Best Practices. Interoperability and technical standards adherence.
10. **L2-FA-10.** Technology Roadmaps and Rationalization. Redundancy elimination, portfolio alignment.

**Why it matters for AI.** Fragmented systems produce fragmented intelligence.

Layer 2 moves data and publishes the contracts that describe it. It does not decide whether the data is fit for a given use, which belongs to Layer 3.

The interface contract carries more weight than it used to. Where the consumer of an interface is an autonomous system rather than a developer, specification completeness stops being a quality attribute and becomes a functional requirement. That consumer has no context beyond the surface and no route to ask for the rest. Knowledge that previously sat with the team running a system has to exist in the machine-readable contract, because nobody is left in the path to supply it.

---

### Layer 3. Intelligence (The Brain & Shield)

**Purpose.** Build and operate the model, data and security controls that make AI outputs usable, and produce the evidence that those controls ran.

Layer 3 operates controls. It does not decide which controls are mandatory and it does not accept residual risk. Both belong to Layer 4.

**Focus areas.**

*AI and Data*

1. **L3-FA-01.** AI/ML Strategy and Automation. Model development, MLOps, deployment pipelines, drift detection, bias and fairness testing.
2. **L3-FA-02.** Data Architecture and Management. Lakes, warehouses, structured and unstructured data design.
3. **L3-FA-03.** Data Quality and Master Data Management. Accuracy, consistency, lineage, mastering. Fitness determination covers data reaching a model through an interface, not only data held in a store.
4. **L3-FA-04.** Data Governance Operations. Classification, retention execution, consent enforcement, ethical AI controls in operation.
5. **L3-FA-05.** Business Intelligence and Analytics. Dashboards, reporting, predictive analytics.

*Security Operations*

6. **L3-FA-06.** Cybersecurity Strategy and Threat Management. Cyber defense, threat intelligence, SOC operations.
7. **L3-FA-07.** **Privacy & Security Engineering.** Technical implementation of ISO 27001, NIST, GDPR, HIPAA and PCI-DSS requirements: minimization, pseudonymization, encryption at rest and in transit, consent enforcement, logging.
8. **L3-FA-08.** Identity and Access Management. SSO, MFA, role-based access control, privileged access.
9. **L3-FA-09.** Security Operations and Incident Response. SIEM, forensic analysis, response execution.
10. **L3-FA-10.** **Vulnerability Management.** Continuous assessment, penetration testing, remediation tracking.

**Resolved overlaps from the prior version.**

Focus area 7 was *Privacy & Compliance* and listed the same regulations as Layer 4's Compliance Management. Regulatory interpretation, lawfulness determination, DPIA sign-off, attestation and regulator liaison are decisions and remain in Layer 4. Layer 3 implements the technical controls those decisions require.

Focus area 10 was *Risk & Vulnerability Management* and included audits, which Layer 4 already owned under Auditing and Reporting. Audit moves to Layer 4 in full. Enterprise risk assessment, appetite and acceptance were already Layer 4 and remain there. Layer 3 retains scanning, testing and remediation.

Focus area 4 was *Data Governance & Compliance*. Policy authorship and compliance determination move to Layer 4. Layer 3 retains execution.

No focus area was deleted. Three labels were narrowed.

**Why it matters for AI.** A model is only as good as the data it learns from and only as safe as the controls around it. Layer 3 produces the evidence that Layer 4 verifies.

---

### Layer 4. Control (The Control Tower)

**Purpose.** Set policy, allocate accountability, decide risk and verify that required controls operated.

Layer 4 decides. It does not build or run controls.

**Focus areas.**

*Governance Frameworks and Policy*

1. **L4-FA-01.** IT and AI Governance Frameworks. COBIT, ITIL, ISO/IEC 38500, ISO/IEC 42001 adoption decisions.
2. **L4-FA-02.** Policy Development and Enforcement. AI policy, standard operating procedures, the mandatory control catalog.
3. **L4-FA-03.** **Auditing and Reporting.** Internal and external audit, evidence review, attestation, board and executive reporting, IT ethics.

*Risk and Compliance*

4. **L4-FA-04.** **Risk Management.** Enterprise and AI risk assessment, risk appetite, mitigation planning, residual risk acceptance, AI system classification.
5. **L4-FA-05.** **Compliance Management.** Regulatory interpretation and adherence determination across SOX, GDPR, HIPAA, PCI-DSS, ISO/IEC 42001 and the EU AI Act. DPIA sign-off and regulator liaison.

*IT Financial Governance*

6. **L4-FA-06.** IT Budgeting and Cost Optimization. CapEx and OpEx, chargeback and showback.
7. **L4-FA-07.** Cloud and SaaS Cost Management. Usage optimization, cloud cost governance, model training and inference cost accountability.
8. **L4-FA-08.** Technology Investment Planning. ROI analysis, emerging technology investment appraisal.

*Vendor and Partner Governance*

9. **L4-FA-09.** Procurement and Contract Management. Vendor negotiation, service levels, licensing, model licensing and training-data provenance terms.
10. **L4-FA-10.** Vendor Risk Management. Vendor security, compliance and performance assessment.

*Accountability*

11. **L4-FA-11.** Strategic Oversight and Accountability. Named ownership per AI system, decision gates, escalation paths, ethics review, metrics tied to business goals.

**Why it matters for AI.** Without Layer 4, AI produces uncontrolled cost, legal exposure and unaccountable decisions. Every control Layer 3 runs exists because Layer 4 required it.

---

### Layer 5. Execution (The Leadership Engine)

**Purpose.** Convert authorized intent into delivered capability through sequencing, delivery discipline and the people who do the work.

**Focus areas.**

*Strategy and Portfolio Execution*

1. **L5-FA-01.** IT Portfolio Management. Alignment of initiatives to business goals, prioritization.
2. **L5-FA-02.** PMO and Delivery Governance. Execution policy, delivery risk mitigation.
3. **L5-FA-03.** Change Management and Digital Adoption.

*Project Delivery*

4. **L5-FA-04.** Delivery Methodologies. Agile, waterfall and hybrid selection.

   Where AI assists development, delivery governance is held by STRATA Protocol and its phase-gated execution loop at Stratum 4. STRATA is not a fourth option alongside agile, waterfall and hybrid. It sits above the methodology choice and governs how a copilot operates inside whichever one is selected. An organization running agile with AI assistance runs both.
5. **L5-FA-05.** Resource and Capacity Planning. Staffing, skills allocation.
6. **L5-FA-06.** KPIs and Performance Metrics. OKRs, critical success factors, delivery measures.

*Leadership and Culture*

7. **L5-FA-07.** IT Leadership and Culture. CIO, CTO, CAIO and CISO leadership, executive alignment, innovation tone.

*Talent*

8. **L5-FA-08.** Talent Acquisition and Development. Hiring, training, succession, retention, AI literacy.

*Workforce Enablement*

9. **L5-FA-09.** Workforce Collaboration and Productivity. Tooling, hybrid work enablement, human and AI task allocation.

**Why it matters for AI.** Execution determines whether AI becomes delivered capability or sunk cost.

---

### Layer 6. Strategic (The Enterprise Compass)

**Purpose.** Decide which AI capabilities the organization should hold, why, and what governance capability it must build to hold them responsibly.

**Focus areas.**

1. **L6-FA-01.** IT Strategy and Business Alignment.
2. **L6-FA-02.** Emerging Technologies and Trends. AI, quantum computing, blockchain, edge computing evaluation.
3. **L6-FA-03.** Digital Change and Innovation Labs. Prototyping, research, new business model testing.
4. **L6-FA-04.** Enterprise Agility and Competitive Advantage.
5. **L6-FA-05.** Sustainability and Green IT. Energy and carbon accountability for training and inference.

**Why it matters for AI.** Layer 6 decides what should be built. Without it, the five layers below execute efficiently in no particular direction.

---

## 4. Focus area ownership index

This index enforces the single-owner rule. Any subject that appears contested is listed here with its owning layer and the boundary that separates it from the layer it is often confused with.

| Subject | Owner | Boundary |
|---|---|---|
| Master data management | **L3** | Defining the master record is a semantic act. L2 distributes the mastered record to consuming systems. |
| Identity and access management | **L3** | L3 operates IAM. L4 sets the access policy that IAM enforces. |
| Data pipelines and integration transport | **L2** | L2 moves data. L3 determines whether the data is fit for use. |
| Data architecture and modeling | **L3** | L3 designs stores and semantics. L1 provides the underlying storage capacity. |
| API and interface specification as an artifact | **L2** | Authoring, versioning and publishing the contract is a Layer 2 deliverable. |
| Fitness of an interface consumed by an AI system | **L3** | Same pattern as data domains. A Data Steward declares an interface fit for AI consumption, or does not. L2 produces the contract, L3 assesses it. |
| Vulnerability scanning and penetration testing | **L3** | Operating a control. |
| Audit and attestation | **L4** | Verifying that controls operated. |
| Enterprise and AI risk assessment | **L4** | A decision. L3 supplies technical inputs. |
| Risk appetite and residual risk acceptance | **L4** | Exclusively L4. Never delegated to L3. |
| Privacy control implementation | **L3** | Minimization, pseudonymization, encryption, consent enforcement. |
| Privacy and regulatory determination | **L4** | Lawfulness, DPIA sign-off, regulator liaison. |
| Security incident response execution | **L3** | Running the response. |
| Major incident accountability and disclosure decisions | **L4** | Deciding what is disclosed and to whom. |
| Model development and MLOps | **L3** | Building and running the model. |
| Model deployment approval | **L4** | Authorizing production use. |
| Cloud cost execution and optimization | **L1** | Operating within the envelope. |
| Cloud cost governance and the envelope itself | **L4** | Setting and enforcing the envelope. |
| Infrastructure capacity operation | **L1** | Provisioning and running capacity. |
| Capacity investment approval | **L4** | Authorizing spend above threshold. |
| Delivery methodology selection | **L5** | How work is executed. |
| Architecture standards and technology selection | **L2** | What is built and with what. |
| Portfolio prioritization | **L5** | Sequencing and resourcing the work. |
| Investment prioritization against business strategy | **L6** | Deciding which outcomes are worth pursuing. |

---

## 5. Relationship to other frameworks

AI9GM does not replace any instrument listed here. Each layer specification carries a crosswalk marking full, partial or absent coverage per instrument.

| Instrument | Relationship |
|---|---|
| ISO/IEC 42001 | Provides AI management system controls. AI9GM allocates who decides and who verifies them. |
| NIST AI RMF | Provides risk function structure. AI9GM places those functions across Layers 3 and 4. |
| COBIT | Provides IT control objectives. AI9GM shows which layer owns each objective for AI. |
| ITIL 4 | Provides service management practice. Concentrated in Layers 1 and 2. |
| TOGAF | Provides architecture method. Concentrated in Layer 2. |
| ISO/IEC 27001 | Provides the security control set. Operated in Layer 3, required and audited in Layer 4. |
| ISO/IEC 38500 | Provides corporate IT governance principles. Concentrated in Layers 4 and 6. |
| EU AI Act | A legal obligation, not a framework. Mapped per layer, with the operator and decision-maker named. |
| **STRATA Protocol** | Companion framework by the same editor, governing AI-assisted software delivery through five strata: classification, derivation, authority chain, execution loop and artifact trail. AI9GM governs the enterprise. STRATA governs the build. |

**On the relationship between the two frameworks.** STRATA and AI9GM make the same governance move at different scopes. STRATA's authority chain constrains what an AI copilot may do inside a codebase. AI9GM allocates decision rights for AI across an enterprise. Both treat an AI system as a governed actor operating inside a stated mandate rather than as a tool that either works or does not.

Three points of contact are load-bearing, and neither framework restates the other:

- **Classification.** STRATA Stratum 1 classifies a *project* to set delivery depth. AI9GM Layer 4 classifies an *AI system* by consequence to set the evidence bar. Different objects, independent classifications. Where a project delivers an AI system both apply, and neither substitutes for the other.
- **Human gating.** STRATA Stratum 4 holds that the human engineer is the gate rather than a reviewer, and that no phase advances on the copilot's judgment alone. That is a working implementation of separation of build and acceptance, applied to one autonomous actor.
- **Evidence.** STRATA Stratum 5 produces decision records, sign-off records and a deviation log. Where AI9GM requires evidence for a decision governed by STRATA, the STRATA artifact is that evidence and no parallel record is created.

---

## 6. Maturity

One model applies across all six layers, aligned to CMMI naming because the intended readership already works with it.

| Level | Name | Descriptor |
|---|---|---|
| 1 | Initial | Governance occurs per project, if at all. No inventory of AI systems. |
| 2 | Managed | Governance exists where someone insisted on it. Inconsistent between teams. Partial inventory. |
| 3 | Defined | Documented decision rights and required artifacts across all six layers, applied consistently. |
| 4 | Quantitatively Managed | Governance effectiveness is measured per layer. Deviations are detected, not discovered. |
| 5 | Optimizing | Governance adapts from measured outcomes. Controls automated. The pipeline generates the evidence. |

Maturity is scored per layer. Composite organizational scores are not produced under this specification. A single number conceals the only finding the assessment generates, which is the shape of the imbalance between layers.

Each layer specification carries level descriptors written for that layer specifically.

---

## 7. Conformance

No conformance regime exists at v0.9. An organization may state that it uses AI9GM as a reference model. No organization, individual or engagement may be described as AI9GM certified, accredited, assessed or compliant.

---

## 8. Change log

**v0.9, 15 August 2026.** First versioned release.

- Layer 4 renamed from *Governance* to *Control*.
- Layer 3 focus area *Privacy & Compliance* renamed to *Privacy & Security Engineering* and scoped to technical implementation.
- Layer 3 focus area *Risk & Vulnerability Management* renamed to *Vulnerability Management*. Audit moved to Layer 4.
- Layer 3 focus area *Data Governance & Compliance* renamed to *Data Governance Operations*. Policy authorship moved to Layer 4.
- Layer 4 focus areas expanded to name AI system classification, model deployment authorization, training-data provenance terms and model licensing.
- Single-owner rule adopted. Focus area ownership index added at section 4.
- Dependency ordering stated explicitly.
- Maturity model adopted. Per-layer scoring mandated, composite scoring prohibited.
- STRATA Protocol declared as companion framework.
- Numeronym documented.
- Artifact scoping convention added. All 71 artifacts across the six layers carry a required-from value on one of two axes.
- Evidence currency and decision trigger conventions added, closing KL-53 and KL-54. The trigger convention extended to require stated detectability, per Phase 4 recommendation R7.
- Consequence classification mechanism published at Layer 4 §5B, closing KL-51.
- Interface fitness records version-bound, closing KL-52.
- Nine Governance Dimensions, five Lifecycle Stages and all certification references removed. These appeared in unpublished drafts and were never part of this specification.

**v0.9 amendment, 17 August 2026. Decision notes findings.**

Eleven recommendations arising from writing interpretations and decision notes for all 94 decisions. Each was a gap in a relationship between decisions rather than in a decision itself.

- L4-AUT-02 and L4-AUT-03 are decided together; neither takes effect without the other.
- An autonomy increase removing a human step triggers L5-12 work reallocation.
- L4-CLS-03 moves to the Business Owner, confirmed by the Business Accountable Executive once named, resolving an ordering conflict with L4-CLS-06.
- L4-ASR-02 requires a domain risk acceptance where remediation extends beyond the period in the risk appetite statement.
- L3-02 threshold records include drift bounds, which define the L3-10 and L3-11 delegated band.
- L5-01 gains the L6-03 capability decision record as an entry condition.
- L5-05 gains a model purpose statement as an entry condition, giving L4-AUT-04 a trigger.
- L5-14 distinguished from L5-05 explicitly, and gains competence evidence for oversight roles.
- L6-05 evidence covers retained oversight competence and re-triggers L5-10.
- L1-04 and L5-02 deferral records carry a reconsideration date.
- Trigger detectability stated for L2-02, L3-12 and L4-AUT-04.
- Identifier permanence convention added, specifying that retired identifiers resolve to tombstones rather than to errors or redirects.

**v0.9 amendment, 17 August 2026. STRATA Protocol boundary.**

- Section 0.1 gains a *layer and stratum* terminology rule. STRATA uses *layer* internally for its derivation vocabulary, which collides with the six AI9GM layers. References to STRATA name strata by number only.
- Section 0.1 delegated band states the publication policy: determination mechanism for risk thresholds, marked default values for operational thresholds.
- Layer 2 focus area 2 and Layer 5 focus area 4 reference specific strata rather than the protocol generally.
- Layer 5 focus area 4 states that STRATA is orthogonal to methodology choice rather than an alternative to it.
- Section 5 gains the three load-bearing points of contact, so neither framework restates the other.

**v0.9 amendment, 17 August 2026. Conventions and cross-layer gaps.**

Arising from the drafting of Layers 2 and 3.

- Section 0.1 gains two conventions: **separation of build and acceptance**, and **delegated band**.
- The delegated band pattern had appeared independently at three layers before being named. Layer 4 publishes all thresholds.
- Layer 1 gains an output: data access source reconciliation for AI workloads, consumed by Layer 2. This makes shadow data access detectable, which no layer previously owned.
- Layer 2 interface contract standard gains an action surface requirement, distinguishing interfaces an autonomous consumer reads from those it invokes to act.
- Determination of EU AI Act value-chain status change is allocated to Layer 4, triggered by mandatory consultation on the Layer 3 model release decision where the model derives from a third-party base.
- Governance of autonomous action surfaces is scoped as a cross-cutting overlay for v1.0, alongside the lifecycle overlay.

**v0.9 amendment, 17 August 2026. Machine-consumable interfaces.**

Incorporated after evaluating an outside observation on the shift in API consumers from human developers to autonomous systems. The observation was tested against the Layer 2 and Layer 3 boundary and found to expose a real gap.

- Layer 2 focus area 5 renamed from *User Experience and Accessibility* to *User Experience, Accessibility and Machine Consumability*, with the completeness properties stated.
- Layer 2 rationale extended to state the change in what interface completeness means when the consumer cannot ask questions.
- Layer 3 focus area 3 scoped to cover fitness determination for data reaching a model through an interface, not only data held in a store.
- Ownership index gains two entries separating the interface contract as a Layer 2 artifact from its fitness assessment as a Layer 3 determination.
- Decision-rights register gains one Layer 2 decision: declare an interface fit for consumption by an autonomous or AI system.

The boundary rule is unchanged. What changed is recognition that an interface description carries semantic content, so an inaccurate description consumed by an autonomous system is an input integrity defect rather than a documentation defect.

**Planned for v1.0.**

- Ten-field specifications published for all six layers.
- Consolidated decision-rights register.
- Full crosswalk with clause-level references.
- Lifecycle overlay as a cross-cutting axis over the six layers.
