# Layer 4. Control

Layer 4

The Control Tower

Who is accountable?

![Diagram of Layer 4 Control, The Control Tower.](../../assets/layer4.webp)

## Purpose

Set policy, allocate accountability, decide risk and verify that required controls operated.

## Scope boundary

| Excluded | Owned by | Boundary |
| --- | --- | --- |
| Implementation of any control | L3 | L4 states which controls are required. L3 chooses how and runs them. |
| Model development, validation execution, drift monitoring | L3 | L4 sets the evidence bar. L3 produces the evidence. |
| Interface contract authoring and versioning | L2 | L4 requires the contract standard. L2 writes and publishes it. |
| Technology selection and architecture standards | L2 | L4 governs the exception path, not the selection. |
| Infrastructure operation and capacity provisioning | L1 | L4 sets the envelope. L1 spends within it. |
| Portfolio prioritization and delivery sequencing | L5 | L4 decides what is permitted. L5 decides what happens and when. |
| Whether a business capability should exist at all | L6 | L4 governs how it proceeds, not whether it is worth pursuing. |
| Vendor technical admission | L2 | The Architecture Review Board admits technically. L4 contracts and accepts vendor risk. |


Layer 4 decides and verifies. It does not build, operate or execute anything it decides about.

**The boundary most often crossed in practice.** Where Layer 3 is weak, Layer 4 absorbs execution. The risk function starts running model validation because nobody else will, the compliance team builds the evidence pack itself, and the audit function writes the control it later tests.

Each step is well-intentioned and each destroys the separation this layer exists to create. A Layer 4 that produces the evidence it verifies is not governing. It is doing Layer 3's work with less capability and no independent check.

The **separation of build and acceptance** convention in section 0.1 of the normative reference applies to this layer in the reverse direction from Layer 3. Layer 3 must not accept. Layer 4 must not build.

## Inputs

| Item | From | Form |
| --- | --- | --- |
| Validation, bias and performance evidence | 3 | Test reports bound to a model version |
| Drift telemetry, data quality and lineage records | 3 | Continuous monitoring against stated thresholds |
| Security telemetry, vulnerability and incident records | 3 | Registers with severity, SLA and closure evidence |
| Access grant and review records | 3 | Grants with justification and review dates |
| Architecture exception register | 2 | Open exceptions with expiry and the risk each carries |
| Application portfolio inventory | 2 | Systems with criticality, ownership and lifecycle state |
| Service performance, recovery and configuration evidence | 1 | SLO attainment, tested recovery results, CMDB coverage |
| Cost actuals attributed per model and initiative | 1 | Monthly attribution report |
| Delivery gate records | 5 | Stage gate entry and exit evidence |
| Business strategy and intended outcomes | 6 | Approved strategy with measurable outcomes |
| Board risk direction | external | Risk appetite direction and reporting expectations |
| Regulatory instruments, guidance and enforcement practice | external | Obligations, deadlines, interpretive guidance |
| Vendor assessments and contracted terms | 2 | Security, compliance and provenance positions |

## Outputs

| Item | To | Form |
| --- | --- | --- |
| AI policy set | 1 | Approved policy with version and effective date |
| AI policy set | 2 | Approved policy with version and effective date |
| AI policy set | 3 | Approved policy with version and effective date |
| AI policy set | 5 | Approved policy with version and effective date |
| AI policy set | 6 | Approved policy with version and effective date |
| Mandatory control catalog by consequence class | 1 | Required controls mapped to source instruments |
| Mandatory control catalog by consequence class | 2 | Required controls mapped to source instruments |
| Mandatory control catalog by consequence class | 3 | Required controls mapped to source instruments |
| Mandatory control catalog by consequence class | 5 | Required controls mapped to source instruments |
| Published delegated band thresholds | 1 | The table at section 5A |
| Published delegated band thresholds | 2 | The table at section 5A |
| Published delegated band thresholds | 3 | The table at section 5A |
| Published delegated band thresholds | 5 | The table at section 5A |
| Published delegated band thresholds | 6 | The table at section 5A |
| AI system register with classification and named accountability | 1 | One row per governed AI system. Issues the AI system identifier carried by the L1 CMDB and the L3 model registry. |
| AI system register with classification and named accountability | 2 | One row per governed AI system. Issues the AI system identifier carried by the L1 CMDB and the L3 model registry. |
| AI system register with classification and named accountability | 3 | One row per governed AI system. Issues the AI system identifier carried by the L1 CMDB and the L3 model registry. |
| AI system register with classification and named accountability | 5 | One row per governed AI system. Issues the AI system identifier carried by the L1 CMDB and the L3 model registry. |
| AI system register with classification and named accountability | 6 | One row per governed AI system. Issues the AI system identifier carried by the L1 CMDB and the L3 model registry. |
| Deployment authorizations | 3 | Authorization referencing the validation evidence relied on |
| Deployment authorizations | 5 | Authorization referencing the validation evidence relied on |
| Risk appetite statement and domain limits | 2 | Appetite by domain with acceptance limits |
| Risk appetite statement and domain limits | 3 | Appetite by domain with acceptance limits |
| Regulatory obligation register and determinations | 2 | Applicability by system, with the obligation set |
| Regulatory obligation register and determinations | 3 | Applicability by system, with the obligation set |
| Regulatory obligation register and determinations | 5 | Applicability by system, with the obligation set |
| Cost envelope and chargeback model | 1 | Approved envelope with allocation method |
| Cost envelope and chargeback model | 5 | Approved envelope with allocation method |
| Vendor contract terms including provenance and audit rights | 2 | Contracted positions the estate must operate within |
| Vendor contract terms including provenance and audit rights | 3 | Contracted positions the estate must operate within |
| Aggregate exposure assessment | 6 | Estate-level concentration, correlation and cumulative decisioning position |
| Aggregate exposure assessment | external | Estate-level concentration, correlation and cumulative decisioning position |
| Audit findings and agreed management responses | 1 | Findings with owner and remediation date |
| Audit findings and agreed management responses | 2 | Findings with owner and remediation date |
| Audit findings and agreed management responses | 3 | Findings with owner and remediation date |
| Audit findings and agreed management responses | 5 | Findings with owner and remediation date |
| Audit findings and agreed management responses | 6 | Findings with owner and remediation date |
| Board and executive reporting | external | Reporting pack on a stated cadence |
| Board and executive reporting | 6 | Reporting pack on a stated cadence |


Layer 4 is the only layer whose outputs are consumed by all five others. Where Layer 3 is an evidence factory, **Layer 4 is the authority source**. Every mandatory control, threshold and authorization elsewhere in the framework originates here.

The practical consequence is that a weak Layer 4 does not produce visible failure. It produces five layers operating on their own judgment, each competently, with no shared basis.

## Decision rights

### POL. Policy and framework

| ID | Decision | Decides | Consulted | Executes | Evidence | Delegated band | Interpretation |
| --- | --- | --- | --- | --- | --- | --- | --- |
| L4-POL-01 | Adopt or amend AI policy | AI Governance Board | CISO, DPO, General Counsel and CAIO | Policy owner | Approved policy, version, effective date |  | Set the organization's stated position on how AI is governed. Policy states intent; the control catalog is what makes it actionable. |
| L4-POL-02 | Adopt a governance framework or management system standard | AI Governance Board | CIO, CAIO and Head of Internal Audit | Policy owner | Adoption decision with scope and target state |  | Decide the organization will run ISO 42001, COBIT or similar, with a stated scope and target state. |
| L4-POL-03 | Define the mandatory control catalog per consequence class | AI Governance Board | CISO, DPO and Head of Internal Audit | CISO | Control catalog mapped to source instruments, stating the consequence class scheme in use and its derivation from the section 5B factors |  | Decide which controls are compulsory for which class of system. Without this, Layer 3 implements what seems reasonable and Layer 4 verifies against a standard it never published. |
| L4-POL-04 | Grant an exception to policy, within the delegated band | Head of Risk | Policy owner and CISO | Requesting owner | Time-bounded exception with expiry and remediation owner | Delegated | Permit a departure from policy that does not weaken a mandatory control, time-bounded and remediation-owned. |
| L4-POL-05 | Grant an exception to policy, at or above the delegated band | AI Governance Board | Head of Risk and General Counsel | Requesting owner | Board-recorded exception with review date | Delegated | Where the departure reaches a mandatory control, the exception becomes a board-level acceptance. |

### CLS. Classification and thresholds

| ID | Decision | Decides | Consulted | Executes | Evidence | Delegated band | Interpretation |
| --- | --- | --- | --- | --- | --- | --- | --- |
| L4-CLS-01 | Publish and revise the delegated band thresholds | AI Governance Board | Head of Risk, CFO, CISO and CAIO | Policy owner | The threshold table at section 5A, with review dates |  | Set and maintain the ten thresholds other layers depend on. A band with no published threshold is inert and the decisions relying on it cannot be exercised. |
| L4-CLS-02 | Define the AI system materiality mechanism | AI Governance Board | Head of Risk and General Counsel | Head of Risk | Published materiality determination mechanism |  | Decide what makes a system significant enough to govern formally, across eleven dimensions. Materiality is the gate; consequence class is the depth behind it. |
| L4-CLS-03 | Determine whether an initiative meets the threshold for formal AI governance | Business Owner | CAIO and Head of Risk | Business Owner | Determination record, documented proportionately to materiality. Confirmed by the Business Accountable Executive once named under L4-CLS-06. | Delegated | Decide whether this initiative crosses materiality at all. A negative determination is still a decision and is recorded proportionately. |
| L4-CLS-04 | Classify an AI system by consequence, at or above materiality | AI Risk Committee | Business Accountable Executive, Model Owner, CISO and General Counsel | Model Owner | Classification record with rationale and review trigger | Delegated | Determine how severely this system's failure would land, and therefore which controls it must carry. Materiality decides that classification happens; consequence decides how much it requires. |
| L4-CLS-05 | Classify an AI system by consequence, below materiality | Business Accountable Executive | Model Owner and CAIO | Model Owner | Classification record proportionate to materiality | Delegated | The same judgment at lighter weight, held by the accountable executive rather than a committee. |
| L4-CLS-06 | Name the Business Accountable Executive for an AI system | AI Governance Board | CIO and business unit head | Business Owner | Register entry naming a person, never a body |  | Put one person's name against one system. Always a person, never a body, and named before the build rather than at go-live. |

### AUT. Authorization

| ID | Decision | Decides | Consulted | Executes | Evidence | Delegated band | Interpretation |
| --- | --- | --- | --- | --- | --- | --- | --- |
| L4-AUT-01 | Authorize a model for production use | Business Accountable Executive | Model Owner, CISO, DPO and Head of Risk | Platform Owner | Authorization referencing the validation evidence relied on and each domain acceptance |  | Decide the validation evidence is sufficient and the system may run. Distinct from the technical judgment that produced the evidence, and held by someone who did not produce it. |
| L4-AUT-02 | Authorize the business actions an agent may take | Business Accountable Executive, or an executive with appropriate delegated authority | CAIO, Head of Risk and General Counsel | Model Owner | Action authorization naming permitted actions and limits | Delegated | Decide what an agent is permitted to do in the business, and up to what value. Answers what it may do, not how independently. |
| L4-AUT-03 | Authorize or certify the level of autonomy and its controls | CAIO, or the AI Risk function | CISO, Head of Risk and Model Owner | Model Owner | Autonomy certification with control set and review cycle. An increase removing a human step triggers L5-12 work reallocation. | Delegated | Decide how much independence the agent exercises and under what controls. Irreversible or high-impact actions default to human confirmation regardless of value. |
| L4-AUT-04 | Authorize reuse of a model for a purpose outside its stated intent | Business Accountable Executive | DPO, General Counsel and Model Owner | Model Owner | Purpose extension record with the original intent stated |  | Decide a model validated for one use may serve another. The original validation does not transfer, and the model card describes the first purpose. |
| L4-AUT-05 | Withdraw a model from production on risk grounds | Business Accountable Executive | Model Owner, Head of Risk and business unit head | Platform Owner | Withdrawal decision, impact assessment, notification record |  | Decide a system stops running. The accountable executive holds this because withdrawal is a business decision with a risk trigger. |
| L4-AUT-06 | Compel withdrawal on unresolved domain risk | Domain owner: CISO, DPO or Head of Risk | Business Accountable Executive | Platform Owner | Compelled withdrawal record with the domain basis stated |  | A domain owner stops a system over the accountable executive's position. A safety valve. Routine use means the accountable executive has been displaced. |

### RSK. Risk acceptance

| ID | Decision | Decides | Consulted | Executes | Evidence | Delegated band | Interpretation |
| --- | --- | --- | --- | --- | --- | --- | --- |
| L4-RSK-01 | Set enterprise AI risk appetite | AI Governance Board | Head of Risk, CFO and board | Head of Risk | Risk appetite statement with domain limits, board minute |  | State how much risk the organization will carry, by domain, in each domain's own units. Every acceptance limit below derives from this. |
| L4-RSK-02 | Accept residual risk within a risk domain | Domain owner: CISO for security, DPO for privacy, Head of Risk for enterprise | Model Owner and Head of Internal Audit | Model Owner | Signed, time-bounded domain risk acceptance | Delegated | A domain owner accepts what remains after controls, within their domain and within their limit, time-bounded. |
| L4-RSK-03 | Accept the composite decision to deploy and operate an AI system | Business Accountable Executive | Domain owners, Model Owner and Head of Internal Audit | Model Owner | Composite accountability record referencing each domain acceptance |  | One named executive accepts the whole, referencing each domain acceptance. Its absence produces systems where every part was approved and the whole was never decided. |
| L4-RSK-04 | Accept risk above a domain acceptance limit | AI Governance Board | Domain owner and Head of Risk | Head of Risk | Board-recorded acceptance with expiry | Delegated | Where a domain owner's limit is exceeded, the acceptance moves to the board with an expiry. |
| L4-RSK-05 | Arbitrate a material or unresolved conflict between domain owners | AI Risk Committee | Domain owners and Business Accountable Executive | Business Accountable Executive | Arbitration record stating the conflict and the resolution |  | Resolve a disagreement two domain owners cannot settle. The committee arbitrates and does not assume ownership of the risk. |
| L4-RSK-06 | Accept the aggregate AI exposure position across the estate | AI Governance Board | Head of Risk, CISO, CFO and CAIO | Head of Risk | Aggregate exposure assessment with the accepted position stated |  | Accept what the systems amount to together: provider concentration, correlated failure, cumulative decisioning. Forty individually acceptable systems are not automatically an acceptable estate. |

### REG. Compliance and regulatory

| ID | Decision | Decides | Consulted | Executes | Evidence | Delegated band | Interpretation |
| --- | --- | --- | --- | --- | --- | --- | --- |
| L4-REG-01 | Determine regulatory applicability for an AI system | General Counsel | DPO, Business Owner and Compliance | Compliance | Applicability assessment, obligation register entry |  | Decide which obligations attach to this system. Applicability is determined, not assumed, and it changes when the system changes. |
| L4-REG-02 | Determine whether a modification to a third-party model changes value-chain status | General Counsel | DPO, Model Owner and Vendor Lead | Compliance | Status determination describing the modification and the resulting obligation set |  | Decide whether fine-tuning or repurposing has moved the organization from deployer to provider, and what obligations follow. Triggered by the Layer 3 release decision so it does not depend on someone remembering. |
| L4-REG-03 | Determine the lawfulness basis for using data in model training | DPO | General Counsel and Data Steward | Data Steward | Lawfulness determination, retained with the training data manifest |  | Decide on what legal basis this data may train this model. Ambiguity is itself the finding, and a determination that resolves it is the evidence. |
| L4-REG-04 | Sign off a data protection impact assessment | DPO | General Counsel, Business Owner and CISO | DPO | Completed assessment with sign-off record |  | Accept that privacy risk has been assessed and mitigated to a stated position. |
| L4-REG-05 | Sign off a fundamental rights impact assessment where required | General Counsel | DPO, Business Accountable Executive and affected business unit | Compliance | Completed assessment with sign-off record |  | Accept that the system's effect on rights has been assessed. Distinct from privacy, and required for a narrower set of systems. |
| L4-REG-06 | Approve public disclosure of an AI-related incident | General Counsel | CISO, Business Accountable Executive and Communications | Communications | Disclosure decision record, regulator notification where required |  | Decide what is said, to whom and when. Legal owns this because disclosure is a legal exposure before it is a communications question. |

### FIN. Financial

| ID | Decision | Decides | Consulted | Executes | Evidence | Delegated band | Interpretation |
| --- | --- | --- | --- | --- | --- | --- | --- |
| L4-FIN-01 | Set the AI cost envelope and chargeback model | CFO | CIO, CAIO and Platform Owner | Finance | Approved envelope with allocation method |  | Decide the spending boundary and how cost is attributed back. An envelope that cannot be broken down per model cannot be governed. |
| L4-FIN-02 | Approve the investment appraisal method and hurdle rate for AI initiatives | CFO | CIO and Portfolio Board | Finance | Published appraisal method |  | Decide how an AI business case is assessed. Method, not individual cases. |
| L4-FIN-03 | Approve training and inference cost accountability per model | CFO | CAIO and Platform Owner | Finance | Cost accountability model with attribution basis |  | Decide who carries the running cost of each model and on what attribution basis. |

### VEN. Vendor

| ID | Decision | Decides | Consulted | Executes | Evidence | Delegated band | Interpretation |
| --- | --- | --- | --- | --- | --- | --- | --- |
| L4-VEN-01 | Approve an AI vendor or model license | Vendor Lead | CISO, DPO and General Counsel | Vendor Lead | Contract with provenance, liability and audit terms |  | Contract for an external model, including provenance, liability and audit terms. Distinct from the technical admission at L2-02. |
| L4-VEN-02 | Approve contractual training-data provenance and audit rights | General Counsel | Vendor Lead, DPO and Model Owner | Vendor Lead | Contracted provenance position |  | Decide what the vendor must warrant about its training data and what the organization may verify. Frequently the only lever over a model nobody can inspect. |
| L4-VEN-03 | Accept vendor risk, or grant an exception to a vendor security standard | CISO | Vendor Lead and Head of Risk | Vendor Lead | Time-bounded vendor risk acceptance |  | Accept that a vendor falls short of standard and the relationship proceeds anyway, time-bounded. |

### ASR. Assurance

| ID | Decision | Decides | Consulted | Executes | Evidence | Delegated band | Interpretation |
| --- | --- | --- | --- | --- | --- | --- | --- |
| L4-ASR-01 | Commission an audit of AI controls | Head of Internal Audit | AI Governance Board | Internal Audit | Audit plan with scope and basis |  | Decide what is examined and against what basis. |
| L4-ASR-02 | Accept the management response to an audit finding | AI Governance Board | Head of Internal Audit and finding owner | Finding owner | Agreed response with owner and remediation date. Where remediation extends beyond the period stated in the risk appetite statement, a domain risk acceptance under L4-RSK-02 is required for the intervening exposure. |  | Decide the proposed remediation is sufficient and accept the exposure until it lands. |
| L4-ASR-03 | Approve the board reporting set and cadence | AI Governance Board | Head of Risk, CIO and Head of Internal Audit | Policy owner | Reporting specification with cadence |  | Decide what the board sees about AI and how often. |


Thirty-eight decisions, grouped by class. Grouping rather than trimming is deliberate: this layer holds every authorization the other five exclude, and a reader needs to find the relevant six rather than read all thirty.

**L4-AUT-02 and L4-AUT-03 are decided together and neither takes effect without the other.** One authorizes what an agent may do in the business; the other certifies how independently it does it. They are held by different roles deliberately, and separating them in time produces an agent authorized to act with no certified autonomy position, or a certified autonomy position for actions nobody authorized.

**An autonomy increase that removes a human step is a reallocation of work.** Where L4-AUT-03 moves a system from acting on confirmation to acting with notification, or from notification to autonomous, work has moved from a person to a system whether or not anyone described it that way. That triggers L5-12, and without the trigger the aggregate position at L6-05 undercounts by exactly the amount autonomy has advanced.

**The last row is a safety valve and it should be used rarely.** A domain owner who cannot compel withdrawal holds accountability without authority. A domain owner who compels routinely has replaced the accountable executive.

**Triggers.** Two decisions in this layer previously stated a review cycle and no event, which made them decisions that get made late or skipped.

**L4-CLS-01, publish and revise the delegated band thresholds.** Fires on a regulatory change affecting an obligation in the register. On an incident in which a delegated band is implicated. When a band produces an outcome the AI Governance Board would not have accepted, which is the important trigger and the hardest to detect.

**L4-RSK-06, accept the aggregate exposure position.** Fires when provider concentration crosses the limit set at L6-04. When a new production system enters a data domain that already feeds a stated number of systems. On a provider event affecting the estate: deprecation, material pricing change, safety intervention or extended outage.

L4-RSK-06 and L6-04 form a control loop. The exposure assessment triggers posture revision, and the posture sets the limit that triggers the assessment. This is intentional.

**On aggregate exposure.** The last row assesses the estate rather than any system in it. It exists because per-system acceptance cannot detect concentration, correlation or cumulative effect, and because no instrument in section 8 requires it. Section 6 states the artifact and its scope.

**On convening the AI Risk Committee.** The committee arbitrates. It does not hold routine risk acceptance and it does not meet on a calendar. It convenes when any one of the following occurs: a domain owner declines to accept a risk the Business Accountable Executive intends to proceed against; two domain owners reach incompatible positions on the same system; a system at or above materiality requires classification; a domain owner compels withdrawal under section 5.3.

A committee with no trigger acquires routine decisions that belong to named individuals, which is the failure the composite accountability model exists to prevent.

## Artifacts

| ID | Name | Owner | Review | Scope | Required from |
| --- | --- | --- | --- | --- | --- |
| L4-ART-01 | AI system register, with classification, materiality and named Business Accountable Executive | Head of Risk | Continuous, reconciled quarterly against L3 model registry and L1 CMDB | organization | Level 2 |
| L4-ART-02 | AI policy set with version and effective date | Policy owner | Annually | organization | Level 2 |
| L4-ART-03 | Mandatory control catalog by consequence class | CISO | Semi-annually, or on regulatory change | organization | Level 2 |
| L4-ART-04 | Published threshold table, per section 5A | Policy owner | Annually | organization | Level 2 |
| L4-ART-05 | Regulatory obligation register with applicability per system | Compliance | On regulatory change | organization | Level 2 |
| L4-ART-06 | Policy exception register | Head of Risk | Monthly | organization | Level 2 |
| L4-ART-07 | Risk appetite statement with domain acceptance limits | Head of Risk | Annually, board approved | organization | Level 3 |
| L4-ART-08 | Aggregate exposure assessment across the AI estate | Head of Risk | Per board reporting cycle | organization | Level 3 |
| L4-ART-09 | Cost envelope and chargeback model | Finance | Annually | organization | Level 3 |
| L4-ART-10 | Vendor register with contracted provenance and audit terms | Vendor Lead | On contract change | organization | Level 3 |
| L4-ART-11 | Audit plan, findings and agreed management responses | Head of Internal Audit | Per audit cycle | organization | Level 4 |
| L4-ART-12 | Board reporting pack | Policy owner | Per approved cadence | organization | Level 4 |
| L4-ART-13 | Composite accountability records per deployed system | Business Accountable Executive | On material change to the system | system | per production AI system |
| L4-ART-14 | Deployment authorization records | Business Accountable Executive | Per authorization | system | per production AI system |
| L4-ART-15 | Domain risk acceptance records, time-bounded | Domain owners | On expiry | system | at or above materiality |
| L4-ART-16 | Agent action authorizations and autonomy certifications | Business Accountable Executive, CAIO | Per stated review cycle | system | per system acting without human confirmation |
| L4-ART-17 | Impact assessment records, data protection and fundamental rights | DPO, General Counsel | Per assessment | system | where legally required |
| L4-ART-18 | Value-chain status determinations | Compliance | On model modification | system | per modification of a third-party base |


**Scoping.** Organization-level artifacts are required from the stated maturity level. System-level artifacts are required per AI system, model, interface or event according to the condition stated. Artifacts in bold are part of the Level 2 minimum. See the minimum viable set document for what this amounts to at small scale.

**The AI system identifier.** The AI system register issues one identifier per governed system. The Layer 1 CMDB and the Layer 3 model registry each carry it as a foreign key on the items belonging to that system. This is what makes quarterly reconciliation possible rather than aspirational. Without a shared key, reconciling three registers means matching on names, and names diverge.

Reconciliation is performed by the Head of Risk as register owner. Internal Audit tests it during the audit cycle rather than performing it, because a function that reconciles its own register cannot verify the result.

The failure it detects runs in both directions. A model in the Layer 3 registry with no AI system identifier is running without accountability. A register entry with no corresponding configuration item may be a governance record for something that is not running at all.

**Aggregate exposure assessment.** Scope is stated below. Method is not prescribed, because prescribing one now would mean inventing one. The assessment covers, at minimum: provider concentration; correlated failure through shared data; cumulative automated decisioning.

Each is invisible to per-system assessment, and each is where an estate of individually acceptable systems becomes collectively unacceptable.

**The AI system register is the artifact everything else depends on.** Policy applies to systems. Classification applies to systems. Accountability names a person for a system. Without a register, every other artifact in this table describes something that cannot be enumerated, and the layer governs an estate it cannot list. It is also the artifact most likely to be assumed to exist. Layer 1 holds a CMDB and Layer 3 holds a model registry, and both are frequently mistaken for it. They hold different objects.

## Metrics

| Name | Unit | Guidance |
| --- | --- | --- |
| Production AI systems with a named Business Accountable Executive | Percentage | Target 100. A system without a name has no accountability regardless of how many controls it carries. |
| Production AI systems with a classification record current to the running configuration | Percentage | Stale classification sets the wrong evidence bar |
| Risk acceptances past their stated expiry | Count | Accumulates silently. The most common finding in any assurance review. |
| Audit findings past their agreed remediation date | Count | Measures whether the layer's own verification produces change |
| Delegated band thresholds published and within review cycle | Count against the ten | A framework whose thresholds have lapsed has inert decision rights across four layers |


The fifth metric is deliberately self-referential. This layer's most common failure is issuing requirements it never revisits, and no other layer can detect that.

## Crosswalk

| Instrument | Coverage | Reference |
| --- | --- | --- |
| ISO/IEC 38500 | full | Evaluate, Direct, Monitor model. Responsibility, strategy, acquisition, performance, conformance, human behavior. |
| COBIT 2019 | full | EDM01 through EDM05 governance framework, benefits, risk, resource and stakeholder transparency. APO01 managed framework, APO06 budget and costs, APO10 vendors, APO12 risk. MEA01 through MEA04 performance, compliance and assurance. |
| ISO/IEC 42001 | full | Clauses 4 through 10 management system: context, leadership, policy, planning, support, operation, performance evaluation, internal audit, management review, improvement. |
| NIST AI RMF | partial | Full for GOVERN, partial for MANAGE. GOVERN 1 through 6 map to policy, accountability, workforce, risk and third-party governance. MEASURE sits at Layer 3. |
| EU AI Act | full | Full for the governance obligations. Article 9 risk management system, Article 17 quality management system, Article 22 authorized representative, Article 25 value chain responsibility, Article 26 deployer obligations, Article 27 fundamental rights impact assessment. Technical execution sits at Layer 3. |
| ISO 31000 | partial | Risk management principles and process. Provides the method, not the AI-specific allocation. |
| ISO/IEC 23894 | partial | Risk identification, analysis and treatment decisions. Provides AI-specific risk method without allocating who decides. |
| ISO/IEC 27001:2022 | partial | Clause 5 leadership, clause 6 planning, clause 9 performance evaluation and internal audit. Annex A controls sit at Layer 3. |
| ITIL 4 | partial | Governance, risk and compliance practice, continual improvement |
| TOGAF 10 | partial | Architecture governance and the Architecture Board, which this layer's exception path routes around rather than through |
| STRATA Protocol | companion | Where a Stratum 5 artifact satisfies an evidence requirement here, it is the evidence and no parallel record is created |


**Two gaps this crosswalk exposes.** No instrument in the list requires a single named person accountable for the composite decision to deploy and operate an AI system. Each requires roles, responsibilities and defined accountability in general terms. None forces one name against one system. That requirement is AI9GM's, and it is the requirement most likely to be resisted, because it converts a distributed comfort into an individual exposure.

None governs aggregate exposure. Every instrument assesses AI systems individually. An organization can hold forty systems, each classified correctly, each within domain appetite, each with a valid acceptance, and no view of what they amount to together.

AI9GM v0.9 addresses this with the aggregate exposure assessment at section 6 and the acceptance decision at section 5.4. Scope is stated and method is not prescribed. This is the second contribution the framework makes beyond the instruments it crosswalks against.

## Maturity descriptors

| Level | Name | Descriptor |
| --- | --- | --- |
| 1 | Initial | Policy exists as a document nobody applies, or does not exist. No register of AI systems, so policy applies to nothing enumerable. Risk is discussed when something goes wrong. Accountability is assumed to sit with whoever built the system. Audit has not looked at AI. |
| 2 | Managed | AI policy is approved and circulated. Some systems are registered. Risk acceptance happens for the systems someone escalated, usually verbally or in a meeting record. Classification exists as a concept without a published mechanism. Cost is visible in aggregate. Vendor contracts are signed without AI-specific provenance terms. |
| 3 | Defined | Every production AI system is registered, classified against a published mechanism and carries one named Business Accountable Executive. The mandatory control catalog is published per consequence class. All ten delegated band thresholds are published. Risk acceptances are signed, time-bounded and held by domain owners, with a composite record above them. Regulatory applicability is determined per system rather than assumed. An aggregate exposure assessment is produced on the board reporting cycle. Layer 4 does not produce the evidence it verifies. |
| 4 | Quantitatively Managed | Register completeness, classification currency, acceptance expiry and finding remediation are measured and reported on cycle. Threshold review is scheduled rather than triggered by failure. Control catalog coverage against the source instruments is measured. Cost is attributed per model and governed against envelope rather than reported after the fact. Audit tests the decision records, not only the controls. |
| 5 | Optimizing | Evidence arrives as a stream from Layer 3 rather than as a submission, so verification is continuous. Acceptances expire and block continued operation until renewed. Classification re-evaluates automatically when a system's configuration or data scope changes. Aggregate exposure across the AI estate is computed and governed alongside per-system risk. Thresholds are revised from measured outcomes rather than from incident. |


The distance between levels 2 and 3 is dominated by two artifacts that do not exist at level 2: the AI system register and the published threshold table. Both are modest documents. Neither is technically difficult. Both require someone to make decisions that have been comfortable to leave open.

## Anti-patterns

### The unenumerable estate

AI policy is approved, current and well written. No register of AI systems exists, so nobody can state which systems the policy governs. Compliance is asserted against a population that has never been counted.

Detection: Detected by asking for the list of production AI systems and comparing whatever arrives against accelerator consumption and vendor invoices.

### Policy without a catalog

Policy states that AI systems must be secure, fair and compliant. No control catalog translates that into which controls are mandatory for which class of system. Layer 3 implements what it judges reasonable, which varies by team, and Layer 4 verifies against a standard it never published.

Detection: Detected by asking Layer 3 which controls are mandatory for a high-consequence system and comparing two teams' answers.

### The committee in the D column

Risk acceptance is signed by a body. Every member was present, none is accountable, and the record names a meeting rather than a person.

Detection: Detected by reading the last five risk acceptances and checking whether a single name appears in the decides field.

### Layer 4 doing Layer 3's work

The risk or compliance function runs validation, assembles the evidence pack and then verifies it. Capability that should sit in Layer 3 has migrated upward, and independent verification no longer exists anywhere.

Detection: Detected by asking who produced the evidence in the last deployment authorization and whether the same function signed it.

### The perpetual acceptance

Risk acceptances carry no expiry, or carry one that passed and was never revisited. A time-bounded decision became a permanent condition without anyone deciding it should.

Detection: Detected by sorting the acceptance register by expiry and counting entries past it.

### Aggregate blindness

Every system is individually classified, individually within appetite and individually accepted. No view exists of concentration in one vendor's model, correlated failure across systems sharing a data domain, or cumulative automated decisioning affecting the same population. Forty acceptable systems are assumed to be an acceptable estate.

Detection: Detected by asking what proportion of production AI systems depend on a single model provider, and receiving no answer.

### The composite signature that became a formality

The same executive re-signs the same system repeatedly without any change to it, because a short-dated domain acceptance keeps expiring underneath. The signature is now administration rather than a decision. The finding is about the acceptance durations rather than about the convention that produced the expiry.

Detection: Detected by counting how many times one composite accountability record was renewed in a year against how many material changes the system underwent.

### Assurance theater

Audits are commissioned, findings are issued and management responses are agreed. Nothing tracks whether the responses happened. The audit cycle produces documents rather than change.

Detection: Detected by counting findings past their agreed remediation date, which is metric four for exactly this reason.
