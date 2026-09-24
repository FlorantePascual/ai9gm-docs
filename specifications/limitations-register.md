# AI9GM Known Limitations Register

*Companion to AI9GM v0.9. Every unresolved item, untested claim, contestable allocation and deferred decision in one place.*

*Compiled 17 August 2026. Editor: Florante Pascual*

---

## Why this document exists

A governance framework that overstates its own maturity has failed its first test. That claim appears in the manifesto and in section 7 of the normative reference, and it only means something if the limitations are written down somewhere specific.

This register is that place. It is intended to be consulted while approaching v1.0, and to be published rather than kept internal. A framework whose limitations are visible is easier to trust than one whose limitations have to be discovered.

**Item IDs are stable.** An ID means what it meant when assigned, including after it closes. Reference them from commit messages, engagement notes and revision decisions.

**IDs are never reused, and a retired ID resolves to a tombstone rather than disappearing.** This register applies the identifier permanence convention at `[AI9GM-v0_9.md](./AI9GM-v0_9.md)` §0.1 to itself. One ID has been retired so far:

| Retired ID | Retired | Reason | Successors |
|---|---|---|---|
| **KL-01** | 17 August 2026 | **Split.** The single item conflated debugging the specification with validating it, and the v1.0 evidence programme resolves only the first. | **KL-01a** author-conducted application. **KL-01b** application by an organization with no author contact. |

Tombstones are excluded from every count in this register.

### Status marks

| Mark | Meaning |
|---|---|
| **Open** | Unresolved. No decision taken. |
| **Deferred** | Decided to defer, with a target version. |
| **Named** | The gap is stated in the specification rather than closed. Deliberate. |
| **Untested** | A requirement exists and no evidence exists that it works. |
| **Contestable** | A decision was taken that a reasonable practitioner would take differently. |
| **Defect** | An internal inconsistency found and not yet fixed. |

---

## A. The evidence deficit

The most significant limitation, and the one that constrains every claim the framework makes.

| ID | Item | Status |
|---|---|---|
| **KL-01a** | **v0.9 has never been applied to a real engagement by its author.** Every revision has come from reasoning. STRATA v1.1 absorbed 33 findings from a first production application, five of which were self-contradictions in its own v1.0 text. Expect a comparable yield. Addressed by the v1.0 evidence programme. | Open |
| **KL-01b** | **v0.9 has never been applied by an organization with no contact with its author.** This is the one that would validate the framework rather than debug it. An author resolves ambiguity from knowledge no reader has, so an author-conducted implementation cannot test whether the specification is sufficient on its own. Not addressed by the evidence programme. | Open |
| **KL-02** | No peer review, no academic evaluation, no independent assessment of the framework by anyone other than its editor. | Open |
| **KL-03** | No measured multi-organization outcomes. The framework's core proposition, that allocating decision rights produces better AI governance than controls alone, is untested. | Open |
| **KL-04** | **Maturity descriptors were written from reasoning, never calibrated.** Nobody has scored an organization against them. The boundaries between levels, particularly the level 2 to level 3 transition that three specifications call the largest, are asserted rather than observed. | Untested |
| **KL-05** | The framework has one author. Its blind spots are one person's blind spots, and no structural mechanism currently exists to surface them. | Open |
| **KL-57** | **Related party concentration.** The editor, the publisher and the sole implementation partner are the same person. Disclosed on `/about/`, in the homepage status panel and on `/roadmap/`. **Disclosed, not mitigated.** Analyzed at `29-Single-Party-Concentration.md`, which finds the concentration currently a net positive for quality and a net negative for credibility, moving in opposite directions over time. | Named |
| **KL-65** | **No editor of record independent of the implementer.** The editor-against-implementer conflict operates silently, because implementation pressure presents as pragmatism. KL-27, the artifact load reaching 71 before anyone noticed it contradicted proportionality, is the visible instance and unlikely to be the only one. One named part-time person with veto over specification changes is the smallest available structural fix. | **Open** |
| **KL-66** | **No continuity or succession position.** An organization adopting AI9GM restructures accountability around it. If the author stops, that organization holds a governance model nobody maintains. This is the provider concentration risk the framework teaches organizations to assess, carried by adopters unmanaged. Needs a license permitting fork and a stated succession position. | **Open** |
| **KL-67** | **Independent stewardship has no date.** Stated as an intention on `/roadmap/` with no deadline. An intention with no date that has to be publicly missed remains an intention. | **Open** |
| **KL-68** | **The complexity conflict is undisclosed.** A consulting practice benefits from a framework being adopted and from implementation being non-trivial. Whether 94 decisions and 71 artifacts reflect genuine complexity or billable complexity cannot be answered credibly from inside. The minimum viable set is the framework's answer and is more convincing when the question is stated first. | **Open** |

**KL-01a is the gating item for debugging the specification. KL-01b is the gating item for believing it.** Category A now holds twelve items, of which five concern the single party concentration analyzed at `29-Single-Party-Concentration.md`. Its conclusion is that a blind implementation, a paid adversarial review and an independent editor of record are worth more than further specification work by the same person. Most of section E below would move one way or the other within a single author-conducted engagement, but only an application by someone with no contact with the author tests whether the specification carries enough on its own.

---

## B. Deliberately deferred to v1.0

| ID | Item | Status |
|---|---|---|
| **KL-06** | **Lifecycle overlay.** Five stages, plan through retire, as a cross-cutting axis over the six layers. The six layers are a static structural model with no temporal axis, so nothing in v0.9 states when a decision gate fires relative to a system's life. Held out of v0.9 to avoid reintroducing the taxonomy confusion the Nine Dimensions caused. | Deferred to v1.0 |
| **KL-07** | **Action surface overlay.** Permitted invocations, value limits, confirmation mechanics and retained records for autonomous systems that act rather than infer. Both authorizations are allocated at Layer 4, and interface classification is required at Layer 2 now. The surface specification itself is deferred. Should derive its pattern from STRATA Stratum 4 rather than invent one. | Deferred to v1.0 |
| **KL-08** | **No conformance regime.** No certification, no accreditation, no assessment scheme, no conformity criteria. Section 7 of the normative reference states this. It is a deliberate position for v0.9, not an omission. | Deferred, no target |

---

## C. Gaps named rather than closed

The framework states these gaps rather than solving them. Naming is defensible; pretending is not.

| ID | Item | Status |
|---|---|---|
| **KL-09** | **Aggregate exposure method is unspecified.** Scope is stated at Layer 4: provider concentration, correlated failure through shared data, cumulative automated decisioning. No method is prescribed, because prescribing one now would mean inventing one. No guidance exists on what a defensible concentration limit looks like. | Named |
| **KL-10** | **Aggregate work reallocation method is unspecified.** Layer 6 accepts a cumulative position with no stated method for computing it. Same shape as KL-09 and the same reasoning. | Named |
| **KL-11** | **Competence assessment for AI literacy is unspecified.** Layer 5 requires competence to be assessed rather than completion recorded, because Article 26(2) requires competence. No method is given for assessing whether a person exercising human oversight can recognize when an output is wrong. | Named |
| **KL-12** | **Cross-layer accountability for a correct decision on wrong information.** An agent acts correctly on an interface description that was wrong. Authored at Layer 2, declared fit at Layer 3, action authorized at Layer 4. The allocation exists in the role model at section 4.6, and it is the only case in the framework where accountability follows an artifact across three layers. Untested by any real incident. | Named, Untested |

---

## D. Contestable allocations

Decisions taken deliberately where a reasonable practitioner would take them differently. Each is reversible.

| ID | Item | Status |
|---|---|---|
| **KL-13** | **Compelled withdrawal.** A domain owner may withdraw a model over the Business Accountable Executive's position. This cuts against the single accountability line. The case for it: a domain owner who cannot stop a system holds accountability without authority. The case against: two people can decide, and in practice the more risk-averse one wins by default, which hollows out the accountable executive. The alternative is that refusal forces AI Risk Committee arbitration rather than immediate withdrawal. | Contestable |
| **KL-14** | **Interface fitness sits with the Data Steward, not Enterprise Architecture.** Architecture owns whether the contract is well-formed; fitness for a decision to rest on is treated as a data judgment. Organizations with strong architecture functions and weak data stewardship will find this allocation impractical. | Contestable |
| **KL-15** | **Master data produces two records per entity.** The Chief Data Officer owns the canonical definition and the CAIO owns AI fitness requirements. The separation is correct in principle and doubles the record count for every entity a production model consumes. | Contestable |
| **KL-16** | **Capacity routing is by purpose, not size.** The CFO owns capacity as an operating resource and the Portfolio Board owns it as an investment. The same amount routes differently depending on what it buys. Expect routing disputes, particularly where an expansion serves both. | Contestable |
| **KL-17** | **Layer 4 is named Control rather than Governance.** Correct, because a Governance layer inside a Governance Model is a collision. It also diverges from the published model on the live site and from every prior AI9GM document. | Contestable |
| **KL-18** | **The Business Accountable Executive is named by the AI Governance Board.** Board naming produces better accountability and slower onboarding. Business-unit naming is faster and produces the pattern where the name is whoever was available. | Contestable |

---

## E. Untested requirements

Requirements AI9GM introduces that no crosswalked instrument contains. Each may work. None has been shown to.

| ID | Item | Status |
|---|---|---|
| **KL-19** | **One named person accountable per AI system.** Every instrument requires defined accountability in general terms; none forces one name against one system. Expect this to be the most resisted requirement in the framework, because it converts a distributed comfort into an individual exposure. | Untested |
| **KL-20** | **Recording a decision not to use AI.** The capability decision register has no precedent in any instrument. Whether organizations will maintain it, rather than populate it once and abandon it, is unknown. | Untested |
| **KL-21** | **Naming your own governance gap in an approval.** The maturity gap approval asks an executive to write down that they are proceeding past a capability the organization lacks. Whether this survives contact with an approval process designed to produce approvals is unknown. | Untested |
| **KL-22** | **Governance readiness as a delivery gate entry condition.** Whether a PMO will decline a production gate for a system that is delivery-ready but lacks an authorization is the single point on which Layer 5 depends. | Untested |
| **KL-23** | **Traceable strategic outcome as a funding entry condition.** Requires a Portfolio Board to decline a good proposal that serves no stated outcome. Layer 6 calls this the hardest transition in the framework. | Untested |

---

## F. Requirements that cannot be verified from outside

Distinct from untested. These may be followed perfectly and produce no external evidence that they were.

| ID | Item | Status |
|---|---|---|
| **KL-24** | The capability decision register can be populated thinly and appear complete. Restraint that was never exercised is indistinguishable from restraint that was, once written down. | Named |
| **KL-25** | Maturity gap approvals depend on self-declaration of the gap. An organization that assesses its own maturity generously produces no gaps to approve. | Named |
| **KL-26** | Proportionate documentation under the Q4 answer means an organization can document almost nothing and claim proportionality. The materiality mechanism bounds this and does not eliminate it. | Named |

---

## G. Structural fragilities

Conditions that will strain the framework as it grows or as it meets a real organization.

| ID | Item | Status |
|---|---|---|
| **KL-27** | The artifact load was not proportionate. **Closed 17 August 2026.** Artifact scoping convention added to §0.1. All 71 artifacts carry a required-from value on one of two axes. The minimum viable set is published: sixteen organization-level and five system-level types at Level 2, collapsing to roughly twelve maintained documents. | Closed |
| **KL-28** | Required artifacts and maturity levels contradicted each other. **Closed 17 August 2026.** Organization-level artifacts now carry a required-from maturity level. Section 6 of each specification is renamed from *Required artifacts* to *Artifacts*. | Closed |
| **KL-29** | **Threshold count is growing.** Seven when Layer 4 was drafted, nine after Layers 5 and 6. No governance exists for adding a threshold, and no owner is named for keeping the table complete as new decisions are specified. | Open |
| **KL-30** | **The AI system identifier is a proposal with no format.** No naming convention, no issuance procedure, no guidance on what happens when a system is split or merged. Three-register reconciliation depends entirely on it. | Open |
| **KL-31** | **Role names may not survive contact.** Eighteen individual roles and five bodies. Renaming one means reworking seven documents. Business Accountable Executive in particular is a construction with no organizational precedent. | Open |
| **KL-32** | **Layer 4 holds 38 of 94 decisions.** Forty percent of the framework sits in one layer. Defensible, since it holds every authorization the others exclude, and a risk that Layer 4 becomes the framework in practice while the other five are read as context. | Open |
| **KL-33** | **Thirty metrics require measurement infrastructure that mostly does not exist.** Five per layer, most requiring data an organization at level 1 or 2 cannot produce. The metrics assume the maturity they are meant to measure. | Open |

**KL-27 and KL-28 are closed.** Both were internal contradictions rather than external unknowns, and both resolved through the same mechanism: scoping artifacts on two axes rather than listing them flat.

One consequence is worth noting. Conformance language is now possible without a conformance regime, because an organization can state which maturity level it targets and which artifacts that level requires. That is not certification, and it is more useful than the previous position, where the artifact list implied an all-or-nothing standard nobody met.

---

## H. Open editor decisions

| ID | Item | Status |
|---|---|---|
| **KL-34** | **Authority follows the mechanism**, proposed as a sixth convention in section 0.1. Decision authority migrates to whichever role holds the operating mechanism through which a decision becomes real. Recommended for adoption. It is the framework's stated method and, unlike most of section 0.1, it is falsifiable. | Open |
| **KL-35** | Assessment design collects **target maturity as well as current**, producing a gap profile rather than a position. Changes the assessment specification. | Open |
| **KL-36** | STRATA terminology. Resolved as Stratum 2 derivation layers, protected on the AI9GM side by the section 0.1 rule. Worth raising on the STRATA side before third parties cite both. | Open, low priority |

---

## I. Known defects awaiting correction

| ID | Item | Status |
|---|---|---|
| **KL-37** | The homepage decision-rights extract was stale. **Closed 17 August 2026.** Both rows corrected against Layer 4 §5. The implementation plan now specifies that this table is generated from Layer 4 data rather than hard-coded, removing the possibility of recurrence. | Closed |
| **KL-38** | **The manifesto predates Layers 4 through 6.** It has not been checked against the finished specifications. The six-layer summary table and the Layer 3 and 4 boundary statement are known correct; the rest is unverified. | Open |
| **KL-39** | **Cross-references between documents use filenames.** `05-Layer-1-Foundation-Specification.md §5` will break when the content becomes web pages. Stable section identifiers are needed before the site build. | Open |
| **KL-40** | **Layer specifications carry no colophon.** No version stamp, editor or revision date on individual specifications, only on the normative reference. | Open |

---

## J. External volatility

Not limitations of the framework. Conditions that will age it.

| ID | Item | Status |
|---|---|---|
| **KL-41** | **EU AI Act timing is unsettled.** The Digital Omnibus, Regulation (EU) 2026/1744, entered into force 27 July 2026 and deferred Annex III to 2 December 2027 and Annex I to 2 August 2028. Further amendment is possible. Every dated statement in the crosswalk and on the site needs a review cycle. | Open |
| **KL-42** | **Clause-level crosswalk references will age.** ISO/IEC 42001, ISO/IEC 27001 and the NIST AI RMF will all revise. Thirteen instruments with clause references is a maintenance commitment, not a one-time artifact. No review cycle is currently stated for the crosswalk. | Open |
| **KL-43** | Sector-specific AI RMF profiles and emerging national regimes are not crosswalked. The crosswalk covers general instruments only. | Named |

## L. Found and closed after v0.9 drafting

| ID | Item | Status |
|---|---|---|
| **KL-49** | **Materiality carried four triggers against ten dimensions practitioners weigh.** Safety, employee impact, reputational impact, and fairness beyond legal position had no trigger. Surfaced while planning the decision notes, which is the pattern to expect: interpreting a decision exposes where it is under-specified. **Closed 17 August 2026.** The mechanism now carries eleven dimensions, any one sufficient. | Closed |
| **KL-50** | **The AI system materiality row was clipped by an editing error** during the Layer 5 amendment and its triggers were orphaned onto the workforce reallocation row. The nine-threshold table published eight, and the Layer 4 maturity descriptor still said seven. **Closed 17 August 2026.** Row repaired, count corrected. Threshold count is now checked at build time. | Closed |
| **KL-51** | Consequence class was a controlling concept that was never defined. **Closed 17 August 2026.** Layer 4 §5B publishes a four-factor determination mechanism as normative. The class scheme is set per organization and stated in the control catalog. No default is published, consistent with the threshold publication policy. An illustrative three-class scheme sits in the L4-CLS-04 note and carries no normative weight. | Closed |
| **KL-52** | A breaking change did not invalidate an interface fitness declaration. **Closed 17 August 2026.** Fitness records are version-bound. The invalidation trigger is narrower than *breaking change* and drawn on what an autonomous consumer can misread rather than on what breaks a build. | Closed |
| **KL-53** | Domain acceptance expiry did not cascade to the composite accountability record. **Closed 17 August 2026.** Resolved as a general convention rather than a patch: *evidence currency* in §0.1 covers all five places in the framework where a derived record can outlive its references. A supporting anti-pattern is added at Layer 4. | Closed |
| **KL-54** | Four decisions had a review cycle and no event trigger. **Closed 17 August 2026.** Triggers published for all four, plus a *decision triggers* convention in §0.1 requiring every decision to state an event or state explicitly that it fires only on cycle. | Closed |
| **KL-56** | **Eleven relationship gaps found by writing all 94 interpretations and 39 decision notes.** Sequencing between paired authorizations, an ordering conflict between naming and determination, three decisions whose triggering event nobody observes, two deferral records with no reconsideration date, an audit acceptance carrying unbounded exposure, a delegated band whose bounds were never required, and two readiness decisions that collapse into one. **Closed 17 August 2026**, all eleven applied to the specifications. | Closed |
| **KL-55** | **The specification has no typed representation of relationships between decisions.** All four of KL-51 through KL-54 were gaps in connections rather than in decisions: a shared concept, two evidence dependencies and four missing triggers. The layer schema handles this at layer level through inputs and outputs; nothing does the equivalent at decision level. Promoting the note relations (upstream, downstream, invalidating, parallel, escalation) from prose to typed data would make them checkable at build time and would have surfaced all four automatically. | **Open** |

---

## K. Site and publication

| ID | Item | Status |
|---|---|---|
| **KL-44** | Brand tokens deferred to a separate session. All color decisions in the mockup are stand-ins. Token specification now written at `28-Design-Token-Specification.md`, awaiting the palette. | Deferred |
| **KL-59** | Inheritance against rebrand was undecided. **Closed 17 August 2026.** Resolved as neither: the site inherits the navy, blue and cyan **relationship** rather than the hex values, because the current site's values were never tested against code, identifiers or dense tables. | Closed |
| **KL-60** | Lotus variable names unverified. **Closed 17 August 2026.** List extracted and committed. The extraction found that Lotus carries a full semantic layer, which reshaped the palette at §4 to four text levels, three border levels and four-part feedback states. Re-run on every theme upgrade. | Closed |
| **KL-61** | Grayscale legibility untested. **Closed 17 August 2026.** Two glyph encodings failed: partial against companion separated by 0.0200 and 0.0061 in effective luminance, because companion is not a coverage level and collides with whatever sits at mid density. Mono letters pass. Assessment bars measure 14.86:1. Retest is a launch gate. | Closed |
| **KL-62** | A monospace face was required and departed from the sans-only identity. **Closed 17 August 2026.** Adopted, scoped to identifiers, code, version stamps, dense table headers and coverage marks. Lotus supports it through `--lotus-font-mono` with no theme modification. | Closed |
| **KL-63** | **Cyan at brand brightness cannot carry text on a light background.** 2.49:1 against a 4.5:1 minimum, and no chroma adjustment fixes it because lightness is the constraint. Two cyans in light, converging in dark. Any substitution must clear the same bar. | Named |
| **KL-64** | **The action and muted-text luminance collision recurred independently in dark mode.** Light theme separated by 0.0016, dark by 0.0012, at values chosen separately. WCAG passes both colors individually in both cases. A luminance separation minimum of 0.04 is now a build gate. The recurrence suggests the failure is a property of blue against cool gray rather than of any one value. | Named |
| **KL-45** | Assessment rebuild: 18 questions, per-layer profile, optional email, and current plus target maturity per KL-35. | Open |
| **KL-46** | Second explainer video, scoped to walk one AI system through six layers and name who decides at each point. | Open |
| **KL-47** | The consolidated decision-rights page, generated from the six specifications rather than written. 94 decisions. | Open |
| **KL-48** | ai9gm.org secured, unimplemented, aspirational. All community and stewardship language stays future-tense until it exists. | Open |
| **KL-69** | **The site now holds personal data.** Contributor accounts begin data protection obligations with the first real account, and AI9GM Layer 3 specifies the controls. A breach here is the framework's own requirements quoted back at it, and it is the cheapest attack a critic has available. Retention, deletion on request and a privacy statement are Phase 7 items, due before DNS. | **Open** |
| **KL-70** | **Authentication, authorization and contributor data sit with one external provider.** Layer 4 §5.4 asks what a single provider's deprecation, pricing change or outage would affect at once. The site publishing that question needs an answer to it. | **Open** |
| **KL-72** | The publications repository requires sync discipline per release. The public repository is generated from the editor's source by a local command and published by the editor at each release. Nothing is written directly in the public repository. The sync is a manual step per release. | **Mitigated** |
| **KL-74** | The Zenodo record is a publication surface. Its title, description and keywords are drafted in the private repository and reviewed against every `BR-HON` requirement before deposit. | **Mitigated** |
| **KL-73** | **CC BY permits a fork the editor cannot control.** Someone may fork the specification, modify it and publish their own version, with attribution and without permission. This is the intended mechanism of KL-66 rather than a defect. Recorded so the trade is explicit rather than discovered later. | **Named** |
| **KL-71** | **The correction queue requires sustained attention after launch from a maintainer with fixed and small capacity.** Anything needing ongoing attention is a liability rather than a feature. The published commitment is best-effort with no service level, which is what the maintainer can hold to. | **Named** |
| **KL-58** | **Reach target set at ten substantive external corrections within twelve months of publication**, citing a specific decision or section, from outside the author's professional network. Traffic is explicitly not the target. Unmet as of publication, and the target itself is untested: nobody knows whether ten is achievable for a framework in this position. | Open |

---

## What would show the framework is wrong

A specification that cannot be falsified is a position rather than a model. Four observations would count against AI9GM as it stands.

**Organizations allocate the decision rights and governance does not improve.** The framework's central proposition is that decision rights matter more than controls. If an organization completes the allocation, maintains the artifacts, and its AI failures continue at the same rate and of the same kind, the proposition is wrong.

**The six-layer boundaries do not hold under use.** If practitioners applying v0.9 consistently find that a focus area belongs in a different layer than assigned, or that the single-owner rule forces artificial splits, the structure is wrong rather than the assignments.

**The operate-versus-require line proves unworkable.** It is the framework's most load-bearing distinction. If organizations cannot staff both sides, or if Layer 4 consistently absorbs Layer 3 execution because the separation is impractical at their scale, the line is drawn in the wrong place or drawn at all in error.

**Nobody will hold single-person accountability.** KL-19 is the requirement most likely to fail in practice. If organizations consistently refuse to name one executive, or name one nominally while decisions continue to be made collectively, the composite accountability model does not describe how organizations can actually work.

---
