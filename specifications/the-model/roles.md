# Roles

**Revision 3. Section 3 retired to an index. The six layer specifications hold the authoritative allocations.**

*Supports AI9GM v0.9. Editor: Florante F. Pascual, Jr.*

---

## How to use this document

Decision rights cannot be allocated until the roles that hold them exist. This document defines the roles. **The six layer specifications allocate decisions against them, and those specifications are authoritative.**

This register holds three things that exist nowhere else: the role set at section 1, the reasoning behind four contested allocations at section 2, and the decisions that had no owner in any framework at section 4. Section 3 is an index to the specifications, not a copy of them.

Read section 1 first. Every allocation across six specifications depends on these names, so renaming a role means reworking seven documents.

The rule that generates most of this register: **the role that executes a control never accepts the risk of that control failing.** Separating D from X is the entire point.

---

## 1. Role set

### 1.1 Decision-making bodies

| Body | Abbrev | Composition | Owns |
|---|---|---|---|
| **AI Governance Board** | AIGB | Chaired by CIO or CAIO. CFO, CISO, General Counsel, business unit heads. | Policy adoption, AI system classification standards, risk appetite, escalated exceptions. |
| **AI Risk Committee** | AIRC | Chaired by Head of Risk. CISO, DPO, Model Owners, Internal Audit observing. | Arbitration of material or unresolved conflicts between domain owners. Classification of systems at or above materiality. |
| **Architecture Review Board** | ARB | Chaired by Head of Enterprise Architecture. CTO, Security Architect, Platform Owner. | Technology selection, integration patterns, third-party model and API admission. |
| **Change Advisory Board** | CAB | Chaired by Head of Operations. Platform Owner, Service Owner. | Production change authorization for infrastructure and platform. |
| **Portfolio Board** | PB | Chaired by CIO. CFO, business unit heads, PMO Lead. | Initiative prioritization, funding allocation, sequencing. |

Abbreviations are provided so a reader encountering one elsewhere can resolve it. **This register and the six layer specifications spell bodies and roles out in full.** Abbreviated forms in a decision table are the most common cause of a reader misattributing a decision, and the space saved is not worth it.

Note that the AI Risk Committee's scope narrowed after the Q3 answer at section 3. It arbitrates and classifies. It does not hold routine risk acceptance, and it convenes on the triggers stated in Layer 4 section 5.4 rather than on a calendar.

### 1.2 Named individual roles

| Role | Abbrev | Primary layer |
|---|---|---|
| Chief Executive Officer, or equivalent | CEO | 6 |
| Chief Information Officer | CIO | 4, 5, 6 |
| Chief Technology Officer | CTO | 2, 5 |
| Chief AI Officer | CAIO | 3, 4, 6 |
| Chief Information Security Officer | CISO | 3, 4 |
| Chief Financial Officer | CFO | 4 |
| Chief Data Officer | CDO | 3 |
| Data Protection Officer | DPO | 4 |
| General Counsel | GC | 4 |
| Head of Risk | RSK | 2, 4 |
| Head of Enterprise Architecture | EA | 2 |
| Infrastructure and Platform Owner | PLAT | 1 |
| Head of Operations | OPS | 1 |
| Service Owner (per service) | SVC | 1 |
| Model Owner (per model) | MO | 3 |
| Data Steward (per domain) | DS | 3 |
| Business Owner (per AI system) | BO | 4, 6 |
| Business Accountable Executive (per AI system) | BAE | 4 |
| Head of Delivery / PMO Lead | PMO | 5 |
| Head of Talent | TAL | 5 |
| Vendor and Procurement Lead | VEN | 4 |
| Head of Internal Audit | AUD | 4 |

**Business Accountable Executive.** One named executive is accountable for the overall decision to deploy and operate a given AI system. Where materiality is low this is the Business Owner. Where it is high it is an executive holding appropriate delegated authority. The role is per system and it is always a person, never a body.

Risk domains retain their own named accountable owners. The CISO accepts security risk, the DPO accepts privacy risk and the Head of Risk accepts enterprise risk, each within their domain. The Business Accountable Executive is accountable for the composite decision to proceed, not for each domain judgment underneath it.

The AI Risk Committee arbitrates material or unresolved conflicts between domain owners. It does not routinely assume risk ownership, and a committee appearing in the **D** column of a risk acceptance is a sign the accountable executive was not named.

**Model Owner and Business Owner are the two roles most often left unnamed, and their absence is the single most common cause of the seam failures AI9GM exists to address.** Model Owner is accountable for the model as a technical artifact. Business Owner is accountable for the decision the model influences. They are different people and neither substitutes for the other.

### 1.3 Role collapse at smaller scale

Proportionality applies to role count, not to decision count. Every decision in section 3 still gets made. Fewer people make them.

| Organization size | Collapse pattern |
|---|---|
| Under 50 | Founder or CTO holds CIO, CTO, CAIO and Portfolio Board. One named Model Owner per model. One named Business Owner per system. Risk acceptance is a logged founder decision. No standing committees. |
| 50 to 500 | CIO or CTO chairs a single combined AI Governance Board that absorbs the Risk Committee and Architecture Review Board. Dedicated CISO. Model Owner and Business Owner remain separate people. |
| 500 plus | Full role set as listed. Separate bodies. |
| Public sector and regulated | Full role set, plus external audit and a documented appeal path for decisions affecting individuals. |

The one rule that does not collapse: **the person who accepts residual risk is never the person who built the thing.** At any size.

---

## 2. Resolved allocation questions

Four allocations could not be settled from the source material and were put to the editor. The answers shape the whole framework, so the reasoning is recorded here rather than left implicit in a table.

### 2.1 Capacity expansion: CFO or Portfolio Board

The CFO owns capacity as an operating resource. The Portfolio Board owns capacity as an investment decision.

The split is by what the spend buys, not by its size, so the same amount routes differently depending on whether it funds growth in existing demand or a capability not currently in production.

*Applied at [Layer 1 section 2](./layers/l1-foundation.md#L1-02) (`L1-02`) and [Layer 1 section 3](./layers/l1-foundation.md#L1-03) (`L1-03`).*

### 2.2 Master data: Chief Data Officer or CAIO

The Chief Data Officer owns the canonical definition. The CAIO owns AI interpretation and fitness requirements. Neither overrides the other automatically, and unresolved conflicts escalate to the AI Governance Board.

This creates two decisions where there was one, and the separation is the point. A definition that is canonical for the enterprise is not automatically fit for a given model.

*Applied at [Layer 3 section 5](./layers/l3-intelligence.md#L3-05) (`L3-05`).*

### 2.3 Residual risk acceptance

Each risk domain has a named accountable owner who accepts within that domain. A single named Business Accountable Executive is accountable for the overall decision to deploy and operate the system. The AI Risk Committee arbitrates material or unresolved conflicts and does not routinely assume risk ownership.

This produces three decisions where the draft had one, and the third is the one most organizations lack. Domain acceptances with no composite accountability record leave a system where every part was approved and the whole was never decided.

*Applied at [Layer 4 section RSK-02](./layers/l4-control.md#L4-RSK-02) (`L4-RSK-02`), [Layer 4 section RSK-03](./layers/l4-control.md#L4-RSK-03) (`L4-RSK-03`) and [Layer 4 section RSK-05](./layers/l4-control.md#L4-RSK-05) (`L4-RSK-05`).*

### 2.4 Whether to use AI at all

The decision is a business-capability decision owned by the Business Owner. The CAIO and Head of Risk are consulted on AI suitability, enterprise implications and risk. It is documented at a level proportionate to its materiality, and that includes a decision not to use AI. Formal AI governance triggers only where defined risk, materiality or strategic thresholds are met.

Those thresholds are delegated bands published at Layer 4 section 5A. Without them this decision defaults to full documentation on every capability, which is the outcome proportionality exists to prevent.

*Applied at [Layer 6 section 3](./layers/l6-strategic.md#L6-03) (`L6-03`).*

### 2.5 Interface fitness, and why the Data Steward holds it

Not an editor question, but the allocation with the least precedent and the one most likely to be queried.

Informal consultation used to close the gap in an incomplete interface specification. A developer asked the team that owned the system. An autonomous consumer cannot ask, so the **C** column has nowhere to happen. The Data Steward's fitness declaration is what replaces it.

**D** sits with the Data Steward rather than with Enterprise Architecture. Architecture owns whether the contract is well-formed. Whether a decision may rest on it is a data judgment, and it follows the pattern already applied to data domains.

*Applied at [Layer 2 section 5](./layers/l2-structural.md#L2-05) (`L2-05`) and [Layer 3 section 4](./layers/l3-intelligence.md#L3-04) (`L3-04`).*

---

## 3. Decision rights index

Section 3 is an index replaced by a link, because a second copy of an allocation drifts from the first.

[Decision rights](./decision-rights.md)

---

## 4. Decisions previously without an owner

All six are now allocated. Item 4 remains partially deferred, as noted.

**1. Retraining versus monitoring on drift.** Model Owner within the delegated band, escalating to the Business Accountable Executive at or beyond it. Applied to the Layer 3 register and specification.

**2. Use of customer data for model training where consent is ambiguous.** DPO decides, General Counsel consulted. Ambiguity is itself the finding, and a determination that resolves it is the evidence.

**3. Retention period for model inputs and outputs held as audit evidence.** DPO decides, Internal Audit consulted. Layer 3 executes.

**4. Authorization for an agent to act without human confirmation.**

Two separate authorizations, because they answer different questions. The first asks what the agent may do in the business. The second asks how much independence it may exercise and under what controls.

[Layer 4 section AUT-02](./layers/l4-control.md#L4-AUT-02) (`L4-AUT-02`) and [Layer 4 section AUT-03](./layers/l4-control.md#L4-AUT-03) (`L4-AUT-03`) allocate the two authorizations. Both also appear on the [decision rights](./decision-rights.md) page.

Thresholds inherit from existing financial delegation limits, supplemented by AI-specific per-transaction and aggregate limits. Inheritance matters: an organization that already knows what a director may approve does not need a parallel scheme, and building one produces two conflicting authorities.

**High-impact or irreversible actions default to human confirmation regardless of monetary value.** Value is a poor proxy for consequence. Deleting a records archive, sending a regulatory filing or terminating an account may carry no transaction value at all.

The remaining specification of action surfaces, covering permitted invocations, confirmation mechanics and retained records, is scoped as a cross-cutting overlay for v1.0. The two authorizations above are settled now because interfaces and agents being built this year need them.

**5. Accountability where an AI-assisted development tool introduces a defect.** CTO under STRATA Protocol, referenced from Layer 2.

**6. Accountability where an agent acts correctly on an interface description that was wrong.** The Data Steward is accountable for the fitness declaration. The authorizing role at Layer 4 retains accountability for the outcome. A correct fitness declaration against an incorrect contract escalates to Layer 2 as an interface defect, not to Layer 3 as a model defect.
