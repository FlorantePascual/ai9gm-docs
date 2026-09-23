# Decision rights

## Foundation

Layer 1

[Layer 1 decision rights](./layers/l1-foundation.md#decision-rights)

| ID | Decision | Decides | Consulted | Executes | Evidence | Delegated band | Interpretation |
| --- | --- | --- | --- | --- | --- | --- | --- |
| L1-01 | Hosting placement for an AI workload (on-premise, cloud, hybrid) | Architecture Review Board | Platform Owner, CISO and CFO | Platform Owner | Placement record with cost, latency and data-residency rationale |  | Decide where a workload physically runs, weighing cost, latency and where the data is legally permitted to sit. Residency usually decides this before performance does. |
| L1-02 | Capacity expansion as an operating resource, above the delegated band | CFO | Platform Owner and CAIO | Platform Owner | Capacity business case, approved envelope | Delegated | Approve more capacity to serve demand that already exists. The question is whether the growth is real and sustained, not whether the capability is worth having. |
| L1-03 | Capacity expansion as an investment, where new capability rather than existing growth is being funded | Portfolio Board | CFO, Platform Owner and CAIO | Platform Owner | Investment decision record with the capability it enables | Delegated | Approve capacity for something not yet in production. This is an investment decision wearing an infrastructure request, and it routes to the Portfolio Board for that reason. |
| L1-04 | Capacity allocation between competing AI initiatives | Portfolio Board | Platform Owner and CAIO | Platform Owner | Allocation record naming the deferred initiative and the date by which the deferral is reconsidered |  | Decide which initiative gets scarce capacity and which waits. The deferred initiative is named in the record, because an unnamed deferral is a portfolio decision made inside a ticket queue. |
| L1-05 | Service level objective for an AI service | Service Owner | Business Owner and Platform Owner | Head of Operations | Published SLO in the service catalog, with consequence class |  | Set the availability and performance the service is held to. The objective follows from what happens when the service is unavailable, not from what the platform can comfortably deliver. |
| L1-06 | Production change to the AI platform | Change Advisory Board | Platform Owner and Model Owner | Platform Owner | Change record with rollback plan and test evidence |  | Authorize a change to the platform AI systems run on, with a tested rollback. Standard change control, applied to a substrate whose failures are less visible than application failures. |
| L1-07 | Emergency change without prior CAB approval | Head of Operations | Platform Owner | Platform Owner | Emergency change record, retrospective CAB review within five working days |  | Proceed with an urgent change ahead of approval. The control is not the approval, it is the retrospective review inside a stated window. |
| L1-08 | Major incident declaration for a production AI service | Head of Operations | Service Owner and CISO | Head of Operations | Incident record, timeline, post-incident review |  | Decide that a degradation is severe enough to invoke major incident handling. Under-declaring is the common error, because AI service degradation is often gradual rather than binary. |
| L1-09 | Infrastructure decommission supporting a production model | Platform Owner | Model Owner and Business Owner | Platform Owner | Decommission record, artifact and data disposition |  | Retire infrastructure a production model depends on, having established what happens to the model artifacts and data on it. |
| L1-10 | Recovery invocation during a disaster event | Head of Operations | Platform Owner and Business Owner | Platform Owner | Invocation record, achieved recovery point and time |  | Decide to fail over or restore. For AI systems this includes model weights and feature stores, not only databases, and a plan that omits them restores everything the model needs except the model. |

## Structural

Layer 2

[Layer 2 decision rights](./layers/l2-structural.md#decision-rights)

| ID | Decision | Decides | Consulted | Executes | Evidence | Delegated band | Interpretation |
| --- | --- | --- | --- | --- | --- | --- | --- |
| L2-01 | Approve an integration pattern for AI system data access | Architecture Review Board | Head of Enterprise Architecture, CISO and Platform Owner | Engineering | Approved pattern in the standards register with review date |  | Decide how AI systems are permitted to reach data. Approving the pattern once prevents each team inventing its own and prevents direct store access becoming the default. |
| L2-02 | Admit a third-party model or AI API into the estate | Architecture Review Board | Vendor Lead, CISO, DPO and Model Owner | Engineering | Technical admission record referencing the vendor assessment |  | Decide that an external model may be used at all, on technical grounds. Admission is not procurement and not authorization to deploy; both happen at Layer 4. |
| L2-03 | Approve a technology selection or platform standard | Architecture Review Board | Head of Enterprise Architecture and CTO | Engineering | Standards register entry with review date |  | Decide what the organization builds with. Every selection is a commitment with an exit cost, which is why the register carries review dates. |
| L2-04 | Set the interface contract standard for the estate | Head of Enterprise Architecture | CTO, CISO and Data Steward | Engineering | Published contract standard covering schema descriptions, examples, error conditions, authentication discovery and action surface classification |  | Define what a complete interface specification contains, including whether an interface is classified as read-only or action-bearing for autonomous consumers. |
| L2-05 | Declare an interface fit for consumption by an autonomous or AI system | Data Steward | Head of Enterprise Architecture, Model Owner and CISO | Engineering | Interface fitness record covering schema completeness, documented error conditions, review date and the interface specification version it was declared against |  | Judge whether an interface is described accurately and completely enough that a consumer unable to ask questions can act on it correctly. This replaces the informal consultation a developer used to perform by asking someone. |
| L2-06 | Grant an exception to an architecture standard, within the delegated band | Head of Enterprise Architecture | Architecture Review Board | Engineering | Time-bounded exception record with expiry and named remediation owner | Delegated | Permit a departure from standard that does not weaken a mandatory control, time-bounded with a named remediation owner. |
| L2-07 | Grant an exception to an architecture standard, at or above the delegated band | Head of Risk | Head of Enterprise Architecture and CISO | Engineering | Risk acceptance record in the risk register, not the exception register | Delegated | Where the departure weakens a control the catalog marks required, the decision stops being architectural and becomes a risk acceptance. It leaves the layer for that reason. |
| L2-08 | Approve a breaking change to a published interface | Product or Service Owner | Head of Enterprise Architecture, consuming teams and Data Steward | Engineering | Deprecation notice, migration window, consumer notification record. Autonomous consumers are notified by fitness invalidation rather than by message. |  | Decide to change a contract consumers depend on. Where a consumer is autonomous, it will not complain; it will fail or produce wrong output quietly. |
| L2-09 | Authorize AI-assisted development on a codebase | CTO | Head of Enterprise Architecture and CISO | Engineering | STRATA Stratum 1 classification record and the Stratum 3 authority chain, versioned with the codebase |  | Decide that a copilot may operate on this code, under the STRATA authority chain. The classification and authority chain are versioned with the codebase. |
| L2-10 | Retire or replace an application in the portfolio | Head of Enterprise Architecture | Business Owner and PMO Lead | Engineering | Rationalization decision, migration plan, data disposition |  | Decide a system leaves the estate, with a migration path and a disposition for its data. |

## Intelligence

Layer 3

[Layer 3 decision rights](./layers/l3-intelligence.md#decision-rights)

| ID | Decision | Decides | Consulted | Executes | Evidence | Delegated band | Interpretation |
| --- | --- | --- | --- | --- | --- | --- | --- |
| L3-01 | Approve a model for release to validation | Model Owner | CAIO, Data Steward and General Counsel | ML Engineering | Model card, training data manifest, version tag. Value-chain status determination where a third-party base was modified |  | Declare a model version ready to be tested against its thresholds. Where the model derives from a third-party base, this decision triggers a mandatory value-chain consultation. |
| L3-02 | Set technical acceptance thresholds for a model | Model Owner | Business Owner and CAIO | ML Engineering | Threshold record with rationale, bound to the model version. Includes drift bounds, which define the delegated band at L3-10 and L3-11. |  | Decide what accuracy, fairness and drift figures count as good enough. **Set before validation runs, not after**, or the threshold is chosen to fit the result. |
| L3-03 | Declare a data domain fit for use in a production model | Data Steward | Chief Data Officer and Model Owner | Data Engineering | Data quality report, lineage record, classification |  | Judge whether the data is accurate, complete and lineage-traceable enough that a decision may rest on it. Fit for one purpose is not fit for all purposes. |
| L3-04 | Declare an interface fit for consumption by an autonomous or AI system | Data Steward | Head of Enterprise Architecture, Model Owner and CISO | Engineering | Interface fitness record covering schema completeness, documented error conditions, review date and the interface specification version it was declared against |  | Same decision as L2-05, exercised here. One record, not two. Layer 2 authors the contract; Layer 3 judges whether it can be relied on. |
| L3-05 | Define the master record for a data entity | Chief Data Officer | Data Steward and Head of Enterprise Architecture | Data Engineering | Master data definition with survivorship rules |  | Decide which source is authoritative for an entity and how conflicts resolve. Canonical for the enterprise is not automatically fit for a given model, which is why AI fitness requirements are a separate decision. |
| L3-06 | Approve access to a classified data set | Data Steward | CISO and DPO | IAM operations | Access grant record with justification and review date |  | Grant access with a stated justification and a review date. Grants past review accumulate silently and are the most common assurance finding. |
| L3-07 | Select the technical implementation of a required control | CISO | DPO and Head of Enterprise Architecture | Security Engineering | Control design record with test evidence |  | Choose how a mandatory control is built. Layer 4 decides the control is required; this decides what it looks like. |
| L3-08 | Prioritize remediation of a detected vulnerability | CISO | Platform Owner and Model Owner | Security Engineering | Vulnerability record, remediation SLA, closure evidence |  | Decide what gets fixed first against the SLA in the control catalog. Model endpoints and training pipelines are frequently outside the scope that produced the finding. |
| L3-09 | Execute containment during a security incident | CISO | Head of Operations | Security Operations | Incident log, containment actions, forensic record |  | Act to limit an incident in progress. Containment is a technical decision; what gets disclosed and to whom is not, and belongs at Layer 4. |
| L3-10 | Retrain a model on detected drift, within the delegated band | Model Owner | Business Owner | ML Engineering | Retraining record referencing the drift trigger | Delegated | Refresh a model where drift stays inside the thresholds recorded at authorization. Operational, and it stays with the Model Owner. |
| L3-11 | Retrain, restrict or escalate on drift, at or beyond the delegated band | Business Accountable Executive | Model Owner, Head of Risk and CAIO | ML Engineering | Escalation record and the resulting Layer 4 decision | Delegated | Where drift breaches a recorded threshold, the decision stops being maintenance and becomes a risk decision about whether the system should keep operating. |
| L3-12 | Approve reuse of a feature set or derived dataset across models | Chief Data Officer | Data Steward and Model Owner | Data Engineering | Reuse approval with lineage from the originating purpose |  | Decide that data built for one purpose may serve another. The original lawfulness basis travels with it, and this is the mechanism by which consent boundaries fail quietly. |

## Control

Layer 4

[Layer 4 decision rights](./layers/l4-control.md#decision-rights)

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

## Execution

Layer 5

[Layer 5 decision rights](./layers/l5-execution.md#decision-rights)

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

## Strategic

Layer 6

[Layer 6 decision rights](./layers/l6-strategic.md#decision-rights)

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
