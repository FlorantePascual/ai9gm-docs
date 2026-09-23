# Thresholds

Every delegated band in the framework is published here.

10 thresholds: 7 mechanisms and 3 defaults.

A band absent from this table is inert, and any decision right depending on it cannot be exercised.

## Mechanisms

### THR-01. Architecture exception risk band

An exception routes to the Head of Risk where it removes, defers or weakens a control that the mandatory control catalog marks required for the affected system's consequence class. All other exceptions sit with Enterprise Architecture. The band is defined by the catalog, not by a number, so it moves automatically when the catalog changes.

| Decision | Decides |
| --- | --- |
| L2-06 | Head of Enterprise Architecture |
| L2-07 | Head of Risk |

### THR-02. Model drift response band

Within band: drift inside the thresholds recorded on the model card at authorization. At or beyond: any drift breaching a recorded threshold, or any drift at all on a system at or above materiality.

| Decision | Decides |
| --- | --- |
| L3-10 | Model Owner |
| L3-11 | Business Accountable Executive |

### THR-03. Risk domain acceptance limits

Each domain owner accepts within the limits stated for that domain in the risk appetite statement. Anything above routes to the AI Governance Board. Limits are expressed in the domain's own units rather than converted to a common scale.

| Decision | Decides |
| --- | --- |
| L4-RSK-02 | Domain owner: CISO for security, DPO for privacy, Head of Risk for enterprise |
| L4-RSK-04 | AI Governance Board |

### THR-10. Policy exception risk band

Within band: a departure from AI policy that does not weaken a control the mandatory control catalog marks required for the affected system's consequence class. The Head of Risk grants the exception, time-bounded with a named remediation owner. At or above the band: where the departure reaches such a control, the exception routes to the AI Governance Board for board-recorded acceptance with a review date.

| Decision | Decides |
| --- | --- |
| L4-POL-04 | Head of Risk |
| L4-POL-05 | AI Governance Board |

### THR-04. Pilot transition to production

A pilot is a production system where any one of the following holds: it serves users outside the team that built it; its output influences a decision that is acted upon; it processes production data containing personal or regulated information; it has operated beyond the duration stated in its pilot registration. The fourth trigger makes the others enforceable, because a pilot registered with no end date is a production system that has not been classified.

| Decision | Decides |
| --- | --- |
| L5-06 | Business Accountable Executive |

### THR-05. Workforce reallocation materiality

Reallocation of work from people to AI systems requires an aggregate position at Layer 6 where any one of the following holds: it affects a defined role rather than discrete tasks within it; it affects more than a stated proportion of headcount in a function; it removes a step that was the only human review in a process; it triggers a consultation or notification obligation.

| Decision | Decides |
| --- | --- |
| L5-12 | Business Owner |
| L6-05 | CEO or equivalent |

### THR-06. AI system materiality

A system is material where any one of the dimensions below applies. Dimensions are not ranked and any single trigger is sufficient. Legal and regulatory: failure would breach a regulatory obligation or a contractual commitment. Individual position: it influences a decision affecting a person's legal position, access to a service, or the terms on which a service is offered. Safety: failure could cause physical harm, or the system informs a decision bearing on physical safety. Employee: it informs hiring, evaluation, allocation, discipline or termination, or it reallocates work at or above the workforce reallocation threshold. Fairness: its outputs could differ systematically across a protected characteristic, whether or not legal position is affected. Fundamental rights: it bears on a right for which a fundamental rights impact assessment would be required. Privacy: it processes special category data, or personal data at a scale or in a combination the data subject would not expect. Autonomy: it takes action without human confirmation. Financial: annual cost exceeds the CFO's standing operational delegation, or one automated decision can commit value above the agent transaction limit. Operational: failure would interrupt a process the organization cannot perform manually at required volume. Reputational: failure would be externally visible in a way a reasonable executive would escalate.

| Decision | Decides |
| --- | --- |
| L4-CLS-03 | Business Owner |
| L4-CLS-04 | AI Risk Committee |
| L4-CLS-05 | Business Accountable Executive |
| L5-04 | PMO Lead |
| L5-05 | PMO Lead |

## Defaults

### THR-07. Capacity expansion delegated band

The CFO decides within the approved annual envelope where the expansion is under 25 percent of currently provisioned capacity for that workload class. Above either bound, escalate.

### THR-08. Operating resource versus investment

Expansion serving growth in existing demand is an operating resource and sits with the CFO. Expansion enabling a capability not currently in production is an investment and sits with the Portfolio Board.

### THR-09. Agent transaction and aggregate limits

Inherit the organization's existing financial delegation limits. Add an AI-specific per-transaction limit at 10 percent of the human delegation for the equivalent role, and a daily aggregate limit at five times the per-transaction limit. High-impact or irreversible actions default to human confirmation regardless of monetary value. Value is a poor proxy for consequence: deleting a records archive, submitting a regulatory filing or terminating an account may carry no transaction value at all.

## Consequence classification

Materiality is the gate. Consequence class is the depth behind it, and it selects the control set a system carries from the mandatory control catalog. This is not a delegated band and does not appear in section 5A. A delegated band splits one decision between two roles at a threshold. Consequence class grades a system within the material range.

Consequence class is determined by four factors, assessed against the worst credible failure rather than the expected one. A system that fails rarely and severely is high consequence. Reliability belongs to the risk acceptance decisions, not here.

### Harm magnitude

How serious the harm is when the system is wrong. Assessed against the eleven materiality dimensions, as severity rather than as a gate.

### Reversibility

Whether the outcome can be undone, and at what cost to the affected party rather than to the organization.

### Observability

Whether the person affected can tell the system was wrong. An error invisible to the affected party removes the correction path, which raises consequence independently of magnitude.

### Independent check

Whether anything else would catch the error before it takes effect. A person reviewing several hundred outputs a day is not a check, and volume is the test rather than the presence of a review step.

Three of these four already operate elsewhere in the framework. Irreversibility overrides monetary value in the agent transaction limits at section 5A. Observability is the basis of the invisible model anti-pattern at Layer 3. Independent check is the operate-versus-require line itself. Section 5B states them once so they are applied consistently.

The mechanism above is normative. The class scheme is not. An organization determines its own classes against the four factors and states the scheme in its mandatory control catalog, per L4-POL-03. An illustrative three-class scheme is published in the L4-CLS-04 decision note. It is an illustration and carries no normative weight. An organization running a wide estate will want four or five classes; one running three systems will want two.

A published default gets adopted without reasoning, and a consequence scheme adopted without reasoning produces a control catalog that matches somebody else's estate. This follows the threshold publication policy at section 5A: risk-related determinations are published as mechanisms, not as values.
