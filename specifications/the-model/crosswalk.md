# Consolidated crosswalk

import CrosswalkSection from '../../components/publication/CrosswalkSection.astro';

*AI9GM v0.9. Thirteen instruments across six layers.*

---

## How to read this

AI9GM replaces nothing in this document. Each instrument below governs something real, and most organizations already run several. The crosswalk states which layer of AI9GM each instrument covers, how completely, and where a layer has no instrument behind it at all.

| Mark | Meaning |
|---|---|
| **Full** | The instrument substantially covers this layer's subject matter. Adopting AI9GM here means allocating decision rights over practice the instrument already defines. |
| **Partial** | The instrument addresses part of the layer, or addresses it at a level of generality that does not reach practice. |
| **None** | The instrument does not address this layer. Not a criticism of the instrument. |
| **Companion** | Not an external instrument. A framework by the same editor with a declared boundary. |

**Coverage is not compliance.** A Full mark means an instrument covers the subject. It does not mean an organization running that instrument has satisfied the layer, and it does not mean AI9GM's decision rights are already allocated.

---

## The matrix

<CrosswalkSection />

**Read the columns, not the rows.** The useful question is not how much of AI9GM an instrument covers. It is which instruments stand behind a given layer, and whether any of them reach the decisions that layer holds.

Two observations follow from the matrix itself.

**COBIT is the only instrument with substantial coverage across all six layers.** An organization already running COBIT has the widest existing foundation to allocate against, and the smallest gap to close. It also has the highest risk of assuming coverage where COBIT stops at control objectives and AI9GM continues into decision rights.

**Layer 3 and Layer 4 are covered by different instruments, which is why the seam between them is a seam.** ISO 27001 and NIST MEASURE sit at Layer 3. ISO 42001, ISO 38500 and NIST GOVERN sit at Layer 4. An organization running both sets can satisfy each fully and still have nobody who decides which controls are mandatory. That is the operate-versus-require gap, and the matrix shows why it appears: the instruments on either side were never designed to meet.

---

## Instrument detail

### COBIT 2019

### ITIL 4

### TOGAF 10

### ISO/IEC 27001:2022

### ISO/IEC 42001

### NIST AI RMF

The four RMF functions distribute cleanly across AI9GM: MAP to Layer 2, MEASURE to Layer 3, GOVERN to Layer 4, MANAGE across Layers 1, 3 and 5. That distribution is itself evidence for the layer boundaries, since the RMF's functions were drawn independently.

### EU AI Act

**Timing note, current at 17 August 2026.** The Digital Omnibus on AI, Regulation (EU) 2026/1744, entered into force on 27 July 2026 and deferred Annex III high-risk obligations to 2 December 2027 and Annex I to 2 August 2028. Article 5 prohibitions and general-purpose AI provider obligations are unaffected. **Article 4 AI literacy has applied since February 2025 and is independent of the deferrals**, which makes Layer 5 the layer with the nearest live obligation rather than Layer 4.

### ISO/IEC 38500

### ISO/IEC 23894

### ISO 31000

### PMI portfolio and program standards

### Greenhouse Gas Protocol and CSRD

### STRATA Protocol (companion)

---

## What no instrument covers

Ten gaps, found by writing the layer specifications against the instruments above. This section is the framework's contribution statement, and every claim in it is checkable against the crosswalk.

| # | Gap | Layer | AI9GM position |
|---|---|---|---|
| 1 | Capacity planning for accelerated compute, and model artifacts as recoverable assets | L1 | Specified as Layer 1 practice. Disaster recovery covering data but not model weights is the observable failure. |
| 2 | Interface completeness requirements where the consumer cannot ask questions | L2 | Machine consumability, Layer 2 focus area 5. TOGAF predates the condition. ISO 27001 addresses whether an interface is secure, not whether it is intelligible. |
| 3 | Who determines that a modification to a third-party model changes value-chain status | L2, L3, L4 | Allocated to General Counsel at Layer 4, triggered by mandatory consultation on the Layer 3 release decision. Article 25 creates the obligation and names no owner. |
| 4 | The line between operating a control and requiring it | L3, L4 | The operate-versus-require convention. Every instrument specifies controls and assumes the two responsibilities are allocated somewhere. |
| 5 | Governance of autonomous action rather than inference | L2, L3, L4 | Partially addressed. Both authorizations are allocated at Layer 4. The action surface specification is deferred to the v1.0 overlay. |
| 6 | A single named person accountable for the composite decision to deploy and operate | L4 | Business Accountable Executive. Instruments require defined accountability in general terms. None forces one name against one system. |
| 7 | Aggregate exposure across an AI estate | L4, L6 | Aggregate exposure assessment. Every instrument assesses systems individually, so concentration, correlated failure and cumulative decisioning are invisible. |
| 8 | Governance readiness as a delivery gate condition | L5 | The Layer 4 authorization as a mandatory gate entry condition. COBIT, PMI and ITIL all gate on delivery criteria. |
| 9 | Who decides that work moves from a person to an AI system | L5, L6 | Business Owner decides, Head of Talent consulted without exception, aggregate position at Layer 6. Instruments address training people to work with AI, not reallocating their work. |
| 10 | Recording a decision **not** to use AI, and governance capability as a precondition of ambition | L6 | Capability decision register and the maturity gap approval. Every framework governs the AI an organization has, none the AI it declined. |

Gaps 4, 6, 7 and 8 are the substantive ones. Each names a decision that gets made in every organization running AI and is allocated in none of the instruments above.

---

## Inconsistencies corrected during the merge

Consolidating six independently written crosswalks surfaced four defects. Recorded because a crosswalk that hides its own corrections is not worth trusting.

**ISO/IEC 23894 appeared at Layer 3 only.** The Layer 3 entry stated that risk decisions sit at Layer 4, while Layer 4's crosswalk omitted the instrument entirely. 23894 now appears at both, marked Partial, with the treatment-versus-decision split stated.

**Greenhouse Gas Protocol appeared at Layer 6 only.** Layer 6 sets sustainability targets and Layer 1 measures the energy those targets are tracked against. The instrument now appears at both.

**PMI appeared at Layer 5 only.** Portfolio strategic alignment reaches Layer 6. Added as Partial.

**STRATA was absent rather than marked None at Layers 1, 3 and 6.** Absence and a deliberate None read identically in a per-layer table and differently in a matrix. Now explicit.

One tension was examined and left standing. EU AI Act Article 15 appears at Layer 1 and Layer 3. Layer 1 notes that accuracy and cybersecurity requirements depend on Layer 1 capability but are determined at Layer 4; Layer 3 lists Article 15 as covered. Both are correct and the article genuinely spans them. Marking it once would misrepresent an obligation that reaches three layers.

---

## How to use this crosswalk in an adoption

Run it in three passes.

**First, find your instruments in the matrix and read down their columns.** Whatever is marked Full is practice you already have. AI9GM adds decision rights over it rather than replacing it.

**Second, read across the layer rows for anything marked Partial or None.** Those are layers where no instrument stands behind your practice, and where AI9GM's specification is doing original work rather than allocating existing work.

**Third, read section 4.** Those ten gaps are unaddressed regardless of how many instruments you run. Adopting every framework in this document does not close them.
