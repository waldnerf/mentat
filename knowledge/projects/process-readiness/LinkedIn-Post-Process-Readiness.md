# LinkedIn Post: Process Readiness Score

## Purpose

Publication source for a short LinkedIn post on why companies need to assess process readiness before automating with agentic AI.

Audience: transformation and operations leaders.
Format: short and punchy, roughly 130 to 150 words.
Focus: the why, not the mechanics. Do not lead with scoring methodology.

## Positioning

Deciding to deploy agentic AI on a process means answering five questions in sequence. Each is a gate. Skip one and the cost surfaces later, after budget is committed.

| Domain | Question |
| --- | --- |
| Business value | Is this process worth automating? |
| Process suitability | Does the process naturally lend itself to agentic execution? |
| Readiness | Can agents be implemented today? |
| Implementation complexity | How much engineering is required? |
| Risk and governance | Can we safely automate it? |

Value and suitability describe ambition: this is worth doing and could be done by an agent in principle. Complexity and governance describe the build and the guardrails. Readiness is the reality check between them. It answers the only question that decides whether a pilot ships this year or stalls: can an agent actually run this today, or does the process need groundwork first?

Companies skip readiness because it is the least exciting question. That is exactly why programmes stall. Enthusiasm jumps from "worth automating" straight to "start building", and the blockers, undocumented decisions, missing data owners, systems an agent cannot write to, only appear once the money is spent.

Assessing readiness does three things: it separates ambition from what is deliverable now, it sequences the portfolio so ready processes go first and the rest get a groundwork plan, and it moves the surprises to the front, before commitment, where they are cheap.

## Companion illustration

Tagline: Ready on all four, or not ready at all.

Purpose: pairs with the post to show that readiness is not one question but four dimensions, and that the weakest dimension governs whether an agent can run the process. Order: Process, Technology, Knowledge, Data.

Each dimension summarised as one sentence (rolls up its sub-questions):

- Process: the process is documented, standardised and consistently run, with decisions that reduce to explicit rules, clear approvals, and a defined way of handling exceptions.
- Technology: the systems can be reached and acted on programmatically, are well integrated, allow non-human identities to execute actions, and offer a representative test environment.
- Knowledge: the operational know-how is documented, current, easy for a newcomer to find, and actively owned rather than living in people's heads.
- Data: the data needed to decide is complete and available, consistently defined, drawn from a single trusted source, clearly owned, and retained as queryable history.

Rendered artefact: Illustration-Four-Dimensions.html, and artefacts/linkedin/Process-Readiness-Four-Dimensions.pdf (portrait 4:5, official logo).

Decision (2026-07-24): icons are now a sanctioned part of the brand system (monoline, ink only, never the accent). See knowledge/decisions/2026-07-24-enable-icons.md. The illustration is compliant, no longer a brand override.

Tagline alternatives, if a different emphasis is wanted:

- An agent runs your process only as well as its weakest dimension.
- Readiness is not one question. It is four.
- Four dimensions decide whether an agent can run your process.

## Framework facts (source of truth)

Source: knowledge/projects/process-readiness/Process_Readiness_Score.xlsx

The Process Readiness Score is itself one domain within a wider five-question assessment (business value, process suitability, readiness, implementation complexity, risk and governance). The score below measures the readiness question only, and only remediable pre-work: gaps that can be closed with effort. It does not measure value, suitability, engineering cost, or safe autonomy.

Structure: four dimensions, 18 questions, each rated 1 to 5 against evidence anchors (1 = significant pre-work required, 3 = moderate pre-work, 5 = ready). Two questions are weighted.

Process Readiness (1.1 to 1.5): documentation matches reality; single standard path; key decisions explainable as business rules [weighted, 1.3]; approvals clearly defined and applied; exceptions classified and managed consistently.

Knowledge Readiness (2.1 to 2.4): operational knowledge documented not tacit; policies and rules kept current; a newcomer can find what they need without heavy SME support; policies owned and actively maintained.

Data Readiness (3.1 to 3.5): required data complete and available at decision point; critical terms consistently defined; a single trusted source of truth; clear data ownership and stewardship; complete queryable history.

Technology Readiness (4.1 to 4.4): systems accessible programmatically via APIs; systems integrated with minimal manual hand-off; actions executable by non-human identities such as service accounts [weighted, 4.3]; a representative non-production test environment.

The two weighted items are the structural blockers: 1.3, because decisions that live in individual judgement mean knowledge extraction rather than documentation; and 4.3, because without non-human execution an agent cannot act however good everything else is.

The actionable output is what to fix first before an agent can run the process.

## Post angles

Selected: Angle B (owner decision, 2026-07-24).

### Angle A: The question everyone skips

Before automating a process with agents, companies ask: is it worth it, and can we do it safely? Both are the right questions. Neither is the one that stalls the programme.

The question that stalls it is quieter: can an agent actually run this today?

A process can be high value, well suited to agents, and still not runnable now. The decisions live in one expert's head. No one owns the data. The core system has no way for an agent to write back. None of that shows up in a value case. All of it shows up three months into the build.

That is what a readiness assessment is for. It moves the surprises to the front, before the budget is committed, and tells you which processes are ready now and which need groundwork first.

Ambition picks the target. Readiness decides the timing.

### Angle B: Worth automating is not the same as ready to automate

Most agentic AI shortlists rank processes by value. Value is necessary. It is not sufficient.

"Worth automating" and "ready to automate" are different questions, and confusing them is why pilots slip. A process can clear the value case and still be un-runnable today, because the groundwork was never done.

Readiness is the assessment that sits between deciding a process is worth it and finding out how hard it is to build. It answers one thing: can an agent run this now, or does it need work first?

Do it early and you get a sequenced portfolio: ready processes ship this year, the rest get a named groundwork plan instead of a stalled build.

Skip it and you learn the same thing later, after the money is spent.

Assess readiness before you commit, not after.

### Angle C: Why agentic AI pilots stall

It is rarely the model. It is almost always readiness that was assumed, not assessed.

Deploying agents on a process means answering five questions: is it worth it, does it suit agents, is it ready, how hard is the build, can we do it safely? Four of the five get attention. Readiness, the one in the middle, gets skipped, because it is the least exciting to talk about.

So the programme jumps from "this is worth doing" straight to "let's build it", and the blockers only appear once the money is committed: decisions no one wrote down, data no one owns, systems an agent cannot act in.

Assessing readiness first does not slow you down. It tells you which processes are ready now and which need groundwork, so you spend where it actually ships.
