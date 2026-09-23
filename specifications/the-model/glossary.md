# Glossary

import MaturityLevelTable from '../../components/publication/MaturityLevelTable.astro';
import { MATURITY_LEVELS } from '../../features/publication/maturity-levels';

*AI9GM v0.9. Controlled vocabulary for the normative reference and the six layer specifications.*

---

## How to use this

Terms are alphabetical. Each entry gives the definition, where the term is defined normatively, and where relevant a **Not to be confused with** note.

The disambiguation notes matter more than the definitions. Most of the confusion this glossary exists to prevent comes from pairs of terms that sound interchangeable and are not: three registers that hold different objects, two accountability roles that cannot substitute for each other, and two classification schemes that answer different questions.

---

## A

### Action surface
The set of operations an autonomous consumer can invoke through an interface to change state, as distinct from operations it invokes to read state. Layer 2 classifies every AI-consumed interface by whether an autonomous consumer reads through it or acts through it. *Layer 2 §5, §6. Full governance of action surfaces is deferred to the v1.0 overlay.*

### Aggregate exposure
The risk position of the AI estate taken together, rather than of any system in it. Covers provider concentration, correlated failure across systems sharing a data domain, and cumulative automated decisioning affecting the same population. Each is invisible to per-system assessment. *Layer 4 §5.4, §6.*

### AI Governance Board
Executive body owning policy adoption, control catalog definition, threshold publication, risk appetite and the naming of Business Accountable Executives. Chaired by the CIO or CAIO. *Role Model §1.1.*

### AI Risk Committee
Body that arbitrates material or unresolved conflicts between risk domain owners, and classifies systems at or above materiality. It does not hold routine risk acceptance and convenes on stated triggers rather than on a calendar. *Role Model §1.1, Layer 4 §5.4.*

### AI system identifier
The single key issued by the AI system register and carried as a foreign key by the Layer 1 CMDB and the Layer 3 model registry. Makes reconciliation across the three registers possible rather than aspirational. *Layer 4 §6.*

### AI system register
The Layer 4 artifact listing every governed AI system with its classification, materiality and named Business Accountable Executive. The artifact everything else at Layer 4 depends on, because policy, classification and accountability all apply to systems.
**Not to be confused with** the model registry (Layer 3, holds model versions) or the CMDB (Layer 1, holds deployable artifacts). One system may span several models; one model may serve several systems. *Layer 4 §6.*

### AI9GM
The AI-Centric IT Governance Model. A numeronym: **AI** + *CentricIT* (9 letters) + **GM**, following i18n, l10n, a11y and k8s. The nine counts letters, not layers or dimensions. *Normative reference §0.3.*

### Anti-pattern
An observable failure mode named in each layer specification, with a description and a detection test. The detection test is the operative part. *All layer specifications §10.*

### Artifact
A record that must exist as evidence a decision was made or a control operated. Each layer specifies its artifacts with an owner, a review cycle and a required-from value. Seventy-one artifact types exist across the six layers. No organization produces all of them.

### Artifact scoping
The rule that artifacts are required on one of two axes rather than uniformly. Organization-level artifacts are required from a stated maturity level. System-level artifacts are required per instance according to consequence class and materiality. An artifact list read without its scoping column overstates what an organization must produce. *Normative reference §0.1.*

### Authority follows the mechanism *(proposed, not yet normative)*
Decision authority migrates to whichever role holds the operating mechanism through which a decision becomes real, regardless of where the framework allocates it. Where a mechanism attracts authority from another layer, the correction is an entry condition on that mechanism rather than an additional control. *Proposed as a sixth convention. Editor decision pending.*

## B

### Business Accountable Executive (BAE)
The single named executive accountable for the composite decision to deploy and operate a given AI system. Always a person, never a body. Where materiality is low this is the Business Owner; where it is high it is an executive holding appropriate delegated authority. Named by the AI Governance Board.
**Not to be confused with** domain owners, who accept risk within their own domain. The BAE is accountable for the decision to proceed, not for each domain judgment underneath it. *Role Model §1.2, Layer 4 §5.2.*

### Business Owner
The role accountable for the business decision an AI system influences, and for the process the system operates within. Decides whether a capability should use AI at all, and decides work reallocation.
**Not to be confused with** the Model Owner, who is accountable for the model as a technical artifact. They are different people and neither substitutes for the other. *Role Model §1.2.*

## C

### Companion framework
A framework by the same editor with a declared boundary against AI9GM. Currently STRATA Protocol only.

### Composite accountability record
The signed record by which the Business Accountable Executive accepts the overall decision to deploy and operate a system, referencing each domain risk acceptance beneath it. Its absence produces systems where every part was approved and the whole was never decided. *Layer 4 §5.4.*

### Consequence class
The category assigned to an AI system by the severity of what happens when it is wrong. Determines which controls in the mandatory control catalog apply. Determined against four factors: harm magnitude, reversibility, observability by the affected party, and the presence of an effective independent check, all assessed against the worst credible failure rather than the expected one. The mechanism is normative; the class scheme is set by each organization and stated in its control catalog. *Layer 4 §5B.*
**Not to be confused with** materiality, which determines whether formal governance triggers at all. A system can be material and low-consequence, or high-consequence and below the materiality threshold for formal documentation. *Layer 4 §5.2.*

### Consulted (C)
A role whose input is mandatory before a decision is made. Input is required; agreement is not. *Role Model, marks table.*

### Control catalog
The Layer 4 artifact stating which controls are mandatory for each consequence class, mapped to their source instruments. Policy without a control catalog leaves Layer 3 implementing what it judges reasonable. *Layer 4 §5.1, §6.*

## D

### Data as meaning
Layer 3's scope over data: quality, lineage, semantics, classification, mastering and fitness for purpose.
**Not to be confused with** data in motion. *Normative reference §4.*

### Data in motion
Layer 2's scope over data: pipelines, integration, APIs, schemas as contracts, interoperability and distribution. Layer 2 moves data; Layer 3 determines whether it may be relied on. *Normative reference §4.*

### Data Steward
The role accountable for a data domain's fitness for use, and for declaring an interface fit for consumption by an autonomous or AI system. *Role Model §1.2, §2.5.*

### Decides (D)
The single role that makes a decision. One role only, never a committee unless the committee is a named decision-making body. *Role Model, marks table.*

### Decision rights
The allocation of who decides, who must be consulted, who executes and what evidence must survive. AI9GM specifies decision rights per layer rather than controls per layer, on the position that controls are borrowable from ISO and NIST while decision rights are not. *Manifesto, tenet 1.*

### Delegated band
A decision right split at a published threshold. Below the threshold the decision is operational and sits with the executing role; at or above it, the same decision becomes a risk decision and moves to the role holding risk authority. Requires four properties: the measure, the threshold value, the role on each side, and a review cycle. Ten bands exist, all published at Layer 4 §5A. A band with no published threshold is inert. *Normative reference §0.1.*

### Dependency ordering
Layers are numbered by dependency, not importance or value. Weakness low in the stack constrains everything above it; weakness high in the stack leaves everything below directionless. *Normative reference §0.1.*

### Domain risk acceptance
Acceptance of residual risk within a single risk domain by that domain's named owner: CISO for security, DPO for privacy, Head of Risk for enterprise. Time-bounded. *Layer 4 §5.4.*

## E

### Evidence currency
The rule that a record derived from other records is valid only while every record it references is valid. A derived record may state an earlier expiry than its references and never a later one. *Normative reference §0.1.*

### Entry condition
A precondition on an existing mechanism, used to return authority that has migrated to the layer holding that mechanism. The Layer 4 authorization on the Layer 5 production gate, and the traceable strategic outcome on Layer 5 funding, are both entry conditions. The framework's standard correction, in preference to adding a control.

### Evidence retained (E)
The record that must exist after a decision is made. The fourth column of every decision rights table.

### Executes (X)
The role that carries out a decision once made. Separating **D** from **X** is what prevents the role that builds a capability from accepting the risk of its failure.

## F

### Fitness declaration
A Data Steward's statement that a data domain, or an interface, is accurate enough for a decision to rest on it. An interface no steward has assessed is an unassessed model input. Interface fitness records are version-bound: a change to the schema, enumerated values, error set or authentication method invalidates the record. *Layer 3 §5, Layer 2 §5.*

### Focus area
A named subject within a layer. No focus area belongs to more than one layer, under the single-owner rule. *Normative reference §0.1, §3.*

## L

### Layer
Within AI9GM, one of the six governance layers, and nothing else.
**Not to be confused with** STRATA's Stratum 2 derivation layers, which are scoped inside one of its five strata. AI9GM references STRATA by stratum number only. *Normative reference §0.1.*

## M

### Machine consumability
The completeness properties an interface requires when its consumer cannot ask questions: accurate and complete specification, schemas carrying real examples and honest descriptions, documented error conditions, discoverable authentication and explicit relationships between operations. Distinct from documentation quality, because the acceptance test is whether a consumer without judgment can act correctly on the surface alone. *Layer 2 focus area 5.*

### Materiality
The threshold determining whether an AI system requires formal governance. Four independent triggers, any one sufficient: it influences a decision affecting an individual's legal position or access to a service; failure would breach a regulatory or contractual obligation; it acts without human confirmation; annual cost exceeds the CFO's standing operational delegation.
**Not to be confused with** consequence class. Eleven dimensions, any one sufficient: legal and regulatory, individual position, safety, employee, fairness, fundamental rights, privacy, autonomy, financial, operational, reputational. *Layer 4 §5A.*

### Maturity gap approval
Approval of a strategic initiative where the governance maturity it requires is not yet in place, with the gap named in the approval and a remediation plan bound to it. Permitted deliberately: a framework that forbids ambition beyond capability gets ignored rather than followed. *Layer 6 §5.*

### Minimum viable set
The artifacts required of an organization at maturity Level 2 running no material systems: sixteen organization-level types and five system-level types, collapsing to roughly twelve maintained documents. Published separately as the concrete answer to what proportionality means.

### Meta-framework
A framework that sits above the instruments an organization already runs and specifies how they connect, rather than replacing them.

### Model card
The record stating a model version's purpose, training data, limitations and acceptance thresholds. Bound to the version tag, so a new version cannot deploy without one. An expired model card is worse than an absent one, because Layer 4 verifies against it. *Layer 3 §6.*

### Model Owner
The role accountable for a model as a technical artifact: its release to validation, its acceptance thresholds and its drift response within the delegated band. Never authorizes its own model for production.
**Not to be confused with** the Business Owner. *Role Model §1.2.*

## O

### Organization-level artifact
An artifact existing once regardless of how many AI systems run: registers, policies, catalogs, the threshold table, the strategy. Required from a stated maturity level. Forty-seven of the 71.
**Not to be confused with** a system-level artifact.

### Operate versus require
The rule dividing Layers 3 and 4. Layer 3 operates controls and produces evidence; Layer 4 decides which controls are required and verifies the evidence. Two tests resolve any dispute: who is answerable if the control did not run (Layer 3), and who is answerable if it was never required (Layer 4). *Normative reference §0.1.*

## P

### Pilot
A system that has not met any pilot transition trigger. Once any trigger is met it is a production system and requires classification, regardless of what it is called. *Layer 4 §5A, Layer 5 §5.*

### Proportionality
All six layers apply at every organization size. What changes is formality, evidence weight and the number of distinct people holding decision rights. One person holding six roles is a valid implementation. *Normative reference §0.1.*

## S

### Separation of build and acceptance
The role that builds a capability never accepts the risk of that capability failing. The role that sets an acceptance threshold never authorizes production use against it. Applies at every layer, in both directions: Layer 3 must not accept, and Layer 4 must not build. *Normative reference §0.1.*

### Shadow data access
A production model reading directly from a database, bucket or replica rather than through a catalogued interface. Invisible to Layer 2, unassessable by Layer 3. Detected by the Layer 1 data access source reconciliation. *Layer 2 §10.*

### Single-owner rule
No focus area belongs to more than one layer. Cross-layer relationships are expressed as declared inputs and outputs, never as duplication. Applies to documents as well as to focus areas. *Normative reference §0.1.*

### System-level artifact
An artifact existing once per AI system, model, interface or event: model cards, fitness declarations, risk acceptances, authorizations, impact assessments. Required per instance according to consequence class and materiality. Twenty-four of the 71. Drives the real artifact load, because burden follows the number of material systems rather than the number of artifact types.

### STRATA Protocol
Companion framework by the same editor, governing AI-assisted software delivery through five strata: classification, derivation, authority chain, execution loop and artifact trail. AI9GM governs the enterprise; STRATA governs the build. Orthogonal to methodology choice, not an alternative to it. *Normative reference §5.*

### Stratum
One of STRATA Protocol's five divisions. AI9GM references STRATA by stratum number.

## T

### Target maturity
The maturity level per layer that an organization's strategy requires, set at Layer 6. Converts the maturity scale from a description into a roadmap and the assessment from a score into a gap analysis. *Layer 6 §5.*

## V

### Value-chain status
An organization's position under the EU AI Act as provider or deployer. Modifying, fine-tuning or substantially repurposing a third-party model can change it, acquiring the fuller obligation set. Determined by General Counsel at Layer 4, triggered by mandatory consultation on the Layer 3 model release decision. *Layer 4 §5.5, Layer 3 §5.*

---

## The three registers, side by side

The most frequent confusion in the framework, collected in one place.

| Register | Layer | Object held | Answers |
|---|---|---|---|
| CMDB | L1 | Deployable artifacts, including models and datasets as configuration items | What is running, on what, recoverable how |
| Model registry | L3 | Model versions | Which version, trained on what, validated against what |
| AI system register | L4 | Governed AI systems | Which systems exist, classified how, accountable to whom |

One AI system may span several models. One model may serve several systems. A model may exist in the registry and belong to no governed system. A governed system may run without a model of its own, by calling a vendor API.

All three carry the AI system identifier, and the Head of Risk reconciles them quarterly. Internal Audit tests the reconciliation rather than performing it.

---

## Maturity levels

<div class="not-prose">
  <MaturityLevelTable rows={MATURITY_LEVELS} />
</div>

Aligned to CMMI naming because the intended readership already works with it. Scored per layer. **Composite organizational scores are not produced under this specification**, because a single number conceals the imbalance between layers, which is the only finding an assessment generates. *Normative reference §6.*
