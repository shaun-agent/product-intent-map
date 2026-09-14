# Product Intent Map: What Makes a Good Intent?

[Traditional Chinese guide](README.md)

A practical English companion for founders, clients, and builders. You do not need to design a database or choose an AI model to write a useful intent. Start with the change you want to make, for whom, and how you will know it worked.

## Intent Before Implementation

**Intent is a testable statement about what should become different in the real world after we deliver the work.**

```text
Context + Human Judgment -> Intent -> Engineering -> Delivery
```

- **Context:** the current situation, people, evidence, and constraints.
- **Human judgment:** the purpose, priorities, trade-offs, and responsibility for the decision.
- **Intent:** the intended change, success signals, and boundaries.
- **Engineering:** how to implement, test, and control risk.
- **Delivery:** the usable result, whether software, a report, a workflow, or something else.

An architecture diagram describes a possible implementation. It does not, by itself, establish which problem is worth solving or what counts as success. Existing diagrams, APIs, databases, and compliance requirements are valuable supporting context, not a substitute for intent.

## Start with Three Questions

1. **What changes?** Whose task, behaviour, or decision should become different?
2. **What will we not do?** Name the deliberate exclusions and things that must not break.
3. **How will we know it worked?** Agree the evidence and acceptance criteria before implementation.

"Build an AI chatbot" describes a solution. "Help support coordinators draft accurate answers from approved information, while retaining human approval" starts to describe an intent. It still needs measurable acceptance criteria and a clear scope.

## The Five-Field Intent Card

Keep each answer to one or two sentences. Unknowns are allowed: mark them explicitly and identify the next step needed to resolve them instead of inventing certainty.

| Field | What to explain | Too vague |
|---|---|---|
| Whose problem? | A specific user in a specific situation, and the difficulty they face today. | "Everyone needs better AI." |
| What changes? | An observable change in a task, behaviour, decision, or outcome. | "Make the experience better." |
| Success signals | What evidence would establish success, how it will be checked, and who accepts the result. | "It is launched." |
| Cost of doing nothing | What happens if we leave the situation unchanged, and why it matters now. | "We should keep up with competitors." |
| Boundaries | Inclusions, exclusions, budget, timing, dependencies, and non-negotiable privacy, security, or other constraints. | "Everything, as soon as possible." |

### A Copyable Brief

```text
1. Whose problem?
The initial user is ____. Today, when ____, they struggle to ____.

2. What changes?
After this work, they should be able to ____ instead of ____.

3. Success signals
We will test ____ against ____. We will accept the result when ____.
The person responsible for acceptance is ____.

4. Cost of doing nothing
Without this change, ____. This matters now because ____.

5. Boundaries
The first version includes ____ and explicitly excludes ____.
It must preserve ____. Budget and timing constraints are ____.
Known dependencies and unresolved questions are ____.
```

Attach existing product material, example inputs and outputs, or technical diagrams where they clarify the brief. A rough brief is enough to begin a scoping discussion; a client should not have to solve the architecture first.

## Worked Example: A Support-Reply MVP

This example is fictional. The numbers below are proposed test targets, not measured results or universal standards.

| Field | Example |
|---|---|
| Whose problem? | Support coordinators at one online retailer manually search approved policy documents before drafting answers to routine delivery questions. |
| What changes? | They receive an editable draft with references to the policy passages used, while retaining responsibility for reviewing and sending it. |
| Success signals | On 20 agreed synthetic cases, every policy claim must be supported by an approved source, and unsupported questions must be flagged rather than answered by guessing. Target a 25% reduction in median review-and-edit time against the current process; the support lead reviews the results. |
| Cost of doing nothing | Coordinators continue repeating manual searches, leaving less time for complex cases; the assessment should establish the actual time cost before a wider build. |
| Boundaries | One language, one policy collection, synthetic data, and no automatic sending, refunds, or account changes. Agree the time and cost cap before work; do not connect live customer records in this prototype. |

Passing this prototype test does not prove production readiness or commercial value. Those require a separately scoped evaluation in the intended workflow.

## Boundaries Make an MVP Estimable

The first MVP is a specific set of capabilities and acceptance criteria, not "everything needed until the product feels finished."

- State both what is included and what is deliberately excluded.
- Use a demo to make the intended behaviour concrete, but document constraints a demo cannot show, such as permissions, data handling, and failure behaviour.
- Agree the scope, acceptance criteria, decision owner, and budget before implementation.
- If new information changes the intent, record the change and its effect on scope, cost, and timing before proceeding. Agreement provides a reference for change; it does not prevent learning.

## Two Separate Decisions

**Gate A: Is the intent complete enough to act on?** Anyone can identify missing context or an unresolved acceptance condition. The response is to help resolve it, not use the framework as a reason to dismiss a request. If important unknowns remain, scope an investigation rather than pretend the full build is estimable.

**Gate B: Is this worth doing now?** The accountable decision-maker weighs alternatives, evidence, cost, and opportunity cost. A complete intent can still describe the wrong product. Where practical, use a small, reversible test to learn whether the idea deserves more investment.

User and market evidence can test value; it does not override safety, privacy, or other non-negotiable boundaries.

## From Intent to an Engineering Proposal

Once the intent is clear, the builder should answer five questions:

1. What problem does the proposal solve?
2. Which alternatives were considered, including doing less or doing nothing?
3. How does the proposed approach solve it?
4. What are the limits, risks, and unresolved dependencies?
5. Why is this the best available trade-off under the agreed constraints?

The intent card frames the request; these questions test the proposed response. The card can anchor an AI prompt or a specification, but it does not replace detailed technical contracts, tests, or controls where the work requires them.

**The aim is not more documentation or more meetings. It is enough shared clarity to build, evaluate, and make the next decision without repeatedly guessing what was intended.**

For the fuller framework and its AWS CDK RFC case study, see the [Traditional Chinese guide](README.md) and [case study](case-rfc-bar-raiser.md).
