# The AI9GM Manifesto

*The AI-Centric IT Governance Model. Specification v0.9 (Draft for Review).*

---

## The core belief

**AI does not replace IT governance. It raises the cost of not having any.**

For three decades, enterprise IT ran on frameworks that earned their authority the hard way. COBIT gave us control objectives. ITIL gave us service discipline. TOGAF gave us architectural rigor. ISO 27001 gave us a defensible security posture. These were not fashions. They were the accumulated scar tissue of organizations that had already made the expensive mistakes.

Then AI arrived, and something specific broke.

Not the frameworks. They remain correct. What broke was the allocation of decision rights underneath them. When a model influences a lending decision, a clinical triage or a maintenance schedule, the question "who decided this?" stops having a clean answer. The model was trained by a data team, deployed by a platform team, procured by a vendor manager, monitored by nobody in particular and relied upon by a business unit that never saw the validation report.

Every one of those groups followed its framework correctly. The failure sits in the seams between them.

AI9GM governs the seams.

---

## Why the name

AI9GM is a numeronym, in the tradition of i18n, l10n, a11y and k8s.

> **AI** + *CentricIT* (9 letters) + **GM**
> **AI**-*Centric IT* **G**overnance **M**odel

If that convention is familiar to you, this framework was written for you.

---

## What we believe

### 1. Governance allocates decision rights. It does not catalog restrictions.

Most AI governance material is a list of things you must not do. That is a category error. Prohibitions are an output of governance, not its substance.

Governance answers five questions, asked of every consequential decision:

- Who decides?
- Who must be consulted before they decide?
- Who executes the decision?
- What evidence must exist that the decision was made?
- Who verifies that evidence later?

An organization that can answer these five questions for its AI estate is governed. An organization with a forty-page AI policy and no answer to them is not, regardless of how the policy reads.

AI9GM therefore specifies decision rights per layer rather than controls per layer. Controls you can borrow from ISO and NIST. Decision rights you have to allocate yourself, and almost nobody has.

### 2. AI cannot be governed in isolation

No AI system stands alone, so no discipline called "AI governance" can stand alone either.

A model is only as available as the infrastructure beneath it. Only as connected as the integration fabric around it. Only as trustworthy as the data feeding it. Only as accountable as the policy above it, only as real as the people delivering it and only as valuable as the strategy directing it.

Govern one of those and you have governed nothing.

That is why AI9GM defines six interdependent layers instead of an AI control set bolted onto an existing estate.

### 3. Integrate. Do not replace.

Nobody is asking you to abandon COBIT, ITIL, ISO or TOGAF. You invested years in them and they are not wrong.

AI9GM is a meta-framework. It sits above the instruments you already run and shows three things per layer: where your existing frameworks already cover it, where they cover it partially and where AI introduces a governance surface that none of them anticipated. Every layer in the specification carries an explicit crosswalk to ISO/IEC 42001, NIST AI RMF, COBIT, ITIL, TOGAF and ISO/IEC 27001.

The proposition is not "replace your governance." It is "connect the governance you already have, then look at what falls between."

### 4. Proportionality is a principle, not a compromise

Governance overhead must match consequence. A retrieval chatbot over public documentation does not warrant the control surface of an automated credit decision.

The same six layers apply to a fifty-person company and a fifty-thousand-person institution. What changes is weight, formality and the number of distinct people holding the decision rights. Sometimes that means six roles. Sometimes it means one person wearing six hats. Both are valid implementations.

A framework that only works at enterprise scale teaches small organizations to defer governance until retrofitting it becomes expensive.

The minimum viable set is the specification's answer to the objection this tenet names. [Read the minimum viable set](./the-model/minimum-viable-set.md).

### 5. State what the framework has not yet earned

Frameworks acquire authority through evidence: implementations, measured outcomes, independent scrutiny and public revision. AI9GM is early. It has not accumulated that evidence.

So we version the specification, publish its changelog, mark what is stable and what is provisional and state plainly what does not exist. A governance framework that overstates its own maturity has failed its first test.

---

## The six layers

The specification defines six interdependent governance layers. Each carries a scope boundary, inputs and outputs, decision rights, required artifacts, metrics, maturity descriptors and a standards crosswalk. The summary:

| # | Layer | Governs | Central question |
|---|-------|---------|------------------|
| 1 | **Foundation** (*The Digital Backbone*) | Infrastructure, platform operations, availability | Can it run? |
| 2 | **Structural** (*The Digital Fabric*) | Applications, integration, architecture, standards | Can it connect? |
| 3 | **Intelligence** (*The Brain & Shield*) | Models, data, security controls in operation | Can it be trusted? |
| 4 | **Control** (*The Control Tower*) | Policy, risk decisions, compliance, assurance, cost | Who is accountable? |
| 5 | **Execution** (*The Leadership Engine*) | Delivery, leadership, talent, change adoption | Can it be built? |
| 6 | **Strategic** (*The Enterprise Compass*) | Alignment, innovation, sustainability | Should it be built? |

Dependency orders the layers, not importance. Weakness low in the stack constrains everything above it. Weakness high in the stack leaves everything below it directionless.

Layers 3 and 4 divide along one line. Layer 3 operates controls and produces evidence. Layer 4 decides which controls are required and verifies that evidence. Layer 3 runs the scanner. Layer 4 decides scanning is mandatory, accepts the residual risk and answers for it.

---

## What AI9GM is not

The distinction matters more than the pitch.

- **Not a standard.** It is a published reference model. No accreditation, no conformity assessment and no legal standing.
- **Not a certification program.** No AI9GM certification exists. Nobody is an AI9GM Certified Anything.
- **Not a compliance shortcut.** Adopting AI9GM does not make you compliant with the EU AI Act, ISO/IEC 42001 or any other instrument. It organizes the work. It does not perform it.
- **Not community-governed yet.** The authors maintain the framework. Independent stewardship is an intention.
- **Not validated by evidence.** No peer-reviewed studies. No measured multi-organization outcomes. This is a structured argument, offered for scrutiny.

Every one of these may change. None has changed yet.

---

## Where it came from

AI9GM was not written as a product. It started as an internal operating model, the master plan for how one technology practice organizes its own AI governance. It was published because a model only its authors can read is a model that never gets corrected.

That origin sets the honest claim: this is a working artifact, used before it was published, rather than a framework assembled to be sold. It also sets the limit. One organization's operating model, generalized, is a hypothesis about other organizations. Treating it as more would repeat exactly the overclaiming this document argues against.

---

## Who this is for

**CIOs** allocating accountability across an AI estate that spans four existing frameworks and fits cleanly into none.

**CTOs and VPs of Engineering** who need governance that adds decision speed instead of approval queues.

**Chief AI Officers** building a function from scratch and needing a defensible structure to build it on.

**Enterprise Architects** mapping where AI changes the reference architecture and where it genuinely does not.

**Risk, compliance and audit leaders** who need AI risk expressed as owned decisions and retained evidence rather than principles.

---

## What to do next

Read the specification. Find the layer where your organization has no named decision-maker. Start there.

Then tell us where the framework is wrong. It improves through contested use, not through agreement.

---

*AI9GM. Specification v0.9 (Draft for Review). Built on decades of IT governance practice, written for the decisions AI has made urgent.*
