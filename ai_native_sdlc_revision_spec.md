# AI-Native SDLC HTML Revision Specification

## Purpose

This specification defines how to revise the current HTML artifact into a sharper, more interactive, high-level internal blueprint for an AI-native SDLC. The target audience is internal product teams. The goal is to preserve the ambition and clarity of the current artifact while making it more useful as a north star proposal and first-draft blueprint.

This revision should remain conceptual, not operationally deep. It should feel credible, structured, and directional without turning into a technical implementation manual.

## 1. Revision Goals

The updated HTML should do five things better than the current version:

1. Present the SDLC as a coordinated system, not just a sequence of attractive phase cards.
2. Make the role of the spec more explicit and structurally central.
3. Clarify how humans participate without reducing the model back to traditional manual SDLC.
4. Reduce the unintended impression that the model is strictly linear.
5. Add lightweight simulated interactivity so users can inspect representative agent outputs.

## 2. Core Strategic Changes

### 2.1 Reframe the artifact from "pipeline" to "operating model"

The current page visually reads as a step-by-step linear process, even though the copy says the lifecycle is continuous and looping. The revised page should position the 12 phases as one expression of a broader operating model.

#### Required copy change
- Replace repeated framing around "linear pipeline" with language such as:
  - "AI-Native SDLC Operating Model"
  - "12-phase operating model"
  - "continuous lifecycle system"
  - "non-linear, spec-driven product evolution"

#### Required UI change
- Rename the main pipeline label from:
  - `The 12-Phase Pipeline`
- To something like:
  - `The 12-Phase Operating Model`
  - or `The 12-Phase Lifecycle System`

#### Footer update
- Replace `Linear Pipeline View` with `Operating Model View` or `Lifecycle View`.

### 2.2 Introduce an explicit system layer above the phases

Right now the page jumps straight from the hero into principles and then the 12 phases. It needs a conceptual layer in between that explains the SDLC as a system.

#### Add a new section directly below Philosophy and above the phase list

### Section title
`How the System Works`

### Purpose
Explain the four persistent constructs that operate across every phase.

### Add four system cards:

#### Card 1: Spec Layer
Short description:
The spec is the system contract. It translates intent into structured requirements, acceptance logic, and change history.

#### Card 2: Agent Layer
Short description:
Specialized agents perform bounded work in each phase, but they do not operate independently. They act within shared context and shared constraints.

#### Card 3: Human Governance Layer
Short description:
Humans do not manually execute every task. They steer priorities, approve high-risk transitions, and intervene when confidence or alignment drops.

#### Card 4: Feedback Layer
Short description:
Signals from testing, release, usage, support, and production continuously re-enter the lifecycle and reshape future work.

### Layout guidance
- Use a 2x2 responsive card grid.
- Visually distinct from the phase cards.
- Should feel like a framing layer, not another detailed section.

### 2.3 Make non-linearity explicit in both content and interface

The current page says the lifecycle is a loop, but the interface still strongly implies a one-way flow.

#### Required changes

##### Change connector language and meaning
- Keep visual connectors if desired, but soften their implication.
- Add a sub-caption near the phase section stating:
  - `Phases are shown in a readable sequence, but execution is iterative, branching, and feedback-driven.`

##### Add loopback visualization
- Add a subtle visual return path from Phase 12 back to Phase 1.
- This can be a curved connector, loop icon, or closing statement block after Phase 12.

##### Add cross-phase signal indicators
For selected phases, include small badges or annotations such as:
- `feeds Phase 3`
- `can trigger re-entry to Phase 1`
- `may reopen Phase 5 or 7`

This should be done sparingly, not on every card.

##### Recommended phase relationships to show
- Phase 12 feeds Phase 1
- Phase 7 can send work back to Phase 3 and Phase 5
- Phase 8 can send work back to Phase 4 and Phase 5
- Phase 9 can reopen Phase 2 or Phase 5

## 3. Content Improvements by Narrative Level

### 3.1 Improve the hero section

The current hero is elegant, but it is heavy on rhetoric and light on framing.

#### Replace subtitle with sharper copy
Current subtitle is strong but slightly manifesto-like. Revise to something closer to:

`A high-level blueprint for a spec-driven, agent-powered software lifecycle where humans govern direction, quality, and risk while AI accelerates structured execution.`

#### Add a short secondary meta line under the subtitle
Example:

`Designed as a north star proposal for internal product teams exploring how software delivery changes when specs, agents, and feedback systems become first-class.`

#### Add a lightweight CTA row below hero
Buttons or chips:
- `Explore the 12 phases`
- `See simulated outputs`
- `View operating principles`

These should scroll to sections on the page.

### 3.2 Sharpen the philosophy bar

The philosophy bar is good, but it should emphasize the actual differentiators.

#### Recommended revised philosophy pillars
Replace or refine current labels to:
- `Spec-Centered`
- `Agent-Orchestrated`
- `Human-Governed`
- `Continuously Evolving`

#### Guidance
Each description should be one sentence, more precise, less slogan-like.

Example for Human-Governed:
`Humans set intent, approve critical transitions, and resolve ambiguity or risk that should not be automated.`

### 3.3 Add a section that explains "What changes vs traditional SDLC"

This is currently implied but not made explicit. Internal product teams will benefit from a comparison lens.

#### Add a new section after `How the System Works` and before the phase list

### Title
`What Changes in an AI-Native SDLC`

### Format
A 2-column comparison grid.

#### Left column
`Traditional SDLC`

#### Right column
`AI-Native SDLC`

### Suggested comparison rows
- Requirements are written for people vs specs are structured for humans and machines
- Teams manually coordinate handoffs vs agents execute bounded handoffs with traceable outputs
- Testing follows implementation vs tests are derived from specification intent
- Documentation lags shipped code vs docs are continuously regenerated from system artifacts
- Release is an endpoint vs release is one state in a continuous feedback loop

Keep this concise. This section should orient readers fast.

## 4. Phase Card Content Improvements

The current phase cards are strong, but they are inconsistent in usefulness. The revised cards should become slightly more structured and slightly less verbose.

### 4.1 Standardize the internal structure of every phase

Every expanded phase should follow the same content hierarchy in this exact order:

1. Phase description
2. Why this phase matters
3. Simulated agent outputs
4. Agents involved
5. Inputs / Outputs / Human gate
6. Phase relationships

### 4.2 Add a new subsection to each phase: `Why this phase matters`

This should be a short 1 to 2 sentence explanation that answers:
- Why this phase exists in an AI-native model
- What failure it prevents

Example for Phase 3:
`This phase prevents AI-generated implementation from becoming loosely interpreted intent. It creates the shared contract that makes downstream generation, review, and validation traceable.`

### 4.3 Rename `Quality Gate` to `Human Gate`

Reason:
The current label sounds like quality is only checked at the gate. In reality the human step is about governance, judgment, and intervention.

#### New box labels for every phase
- `Inputs`
- `Outputs`
- `Human Gate`

### 4.4 Refine gate language

Gate criteria should avoid sounding overly rigid or pseudo-precise unless they genuinely add clarity.

Examples:
- Replace `Problem validated with ≥3 data sources`
- With `Problem supported by multiple evidence sources`

- Replace `Readability score ≥ target`
- With `Audience-appropriate and free of stale references`

### 4.5 Add a `Phase relationships` row or micro-strip

At the bottom of each expanded phase, add a small text strip such as:
- `Typically follows: Phase 2`
- `Commonly informs: Phase 5, Phase 7`
- `Can be re-entered from: Phase 9, Phase 12`

This is a key change to reduce the false impression of strict linearity.

## 5. Simulated Pipeline Interactivity

This is the most important UX enhancement requested.

### 5.1 Add simulated outputs to every phase

Each phase should include an expandable or tabbed subsection titled:
`Simulated Agent Outputs`

This should not be real data. It should be representative artifacts that make the lifecycle feel tangible.

### 5.2 Interaction model

For each phase, include 2 to 4 output tabs/chips/buttons.
When clicked, a preview panel should display a representative artifact for that phase.

#### Example interaction structure per phase
- Output chip 1: `Problem Brief`
- Output chip 2: `Opportunity Score`
- Output chip 3: `Signal Summary`

Clicking each chip updates the preview panel below.

### 5.3 Design guidance for preview panel

The preview panel should look like a lightweight artifact viewer.
It can be styled as:
- a code/spec pane
- a memo card
- a checklist
- a mini dashboard
- a diff viewer

Do not overcomplicate it. This is simulation, not a real product.

### 5.4 Simulated outputs by phase

#### Phase 1: Ideation & Problem Discovery
Suggested outputs:
- Problem Brief
- Signal Cluster Summary
- Opportunity Scorecard

#### Phase 2: Product Requirements
Suggested outputs:
- PRD Summary
- User Journey Snapshot
- Requirement Checklist

#### Phase 3: Technical Specification
Suggested outputs:
- API Contract Snippet
- Acceptance Criteria Assertions
- Spec Delta Example

#### Phase 4: Architecture & System Design
Suggested outputs:
- ADR Summary
- System Topology Summary
- Tradeoff Matrix

#### Phase 5: Implementation
Suggested outputs:
- Generated Module Outline
- API Endpoint Skeleton
- UI Component Contract

#### Phase 6: Code Review & Quality
Suggested outputs:
- Review Findings
- Drift Report
- Suggested Fixes

#### Phase 7: Testing & Validation
Suggested outputs:
- Test Matrix
- Adversarial Test Cases
- Perf Budget Report

#### Phase 8: Security & Compliance
Suggested outputs:
- Threat Summary
- Vulnerability Snapshot
- Compliance Evidence Checklist

#### Phase 9: Demo & Staging
Suggested outputs:
- Staging Summary
- Demo Walkthrough Script
- UAT Notes

#### Phase 10: Documentation
Suggested outputs:
- User Guide Excerpt
- API Reference Preview
- Change Log for Docs

#### Phase 11: Release & Rollout
Suggested outputs:
- Release Summary
- Flag Rollout Plan
- Rollback Conditions

#### Phase 12: Monitoring, Feedback & Evolution
Suggested outputs:
- Health Snapshot
- Adoption Summary
- Improvement Proposal

### 5.5 Content style for simulated outputs

Simulated outputs should be:
- concise
- believable
- formatted consistently
- clearly synthetic

Add a tiny label like:
`Illustrative output`

This avoids implying that these are live system artifacts.

## 6. Add One New Summary Section at the End

The current `Living Product` section is good, but it needs one more closing summary section that ties everything together.

### Add new section below `Living Product`

### Title
`What This Blueprint Is and Is Not`

### Purpose
Prevent misinterpretation.

### Two-column card layout

#### Left card: `What it is`
Include bullets like:
- A north star model for AI-native software delivery
- A conceptual blueprint for product and engineering discussions
- A way to think about specs, agents, humans, and feedback as one system

#### Right card: `What it is not`
Include bullets like:
- Not a locked implementation architecture
- Not a mandate for zero-human development
- Not a claim that every phase must be fully automated
- Not a replacement for product judgment or engineering leadership

This section will materially improve credibility.

## 7. Copy Editing and Tone Adjustments

The current document is stylish but occasionally overstates. Because this is for internal product teams, the revised copy should remain ambitious while becoming more disciplined.

### 7.1 Reduce overly theatrical phrasing

Examples of phrases to soften:
- `radical`
- `own every phase end-to-end`
- `self-healing and self-evolving`
- `not a copilot bolted onto waterfall`

These are memorable, but for internal blueprint use they can undermine precision.

### Replace with language like:
- `structured`
- `agent-led within bounded responsibilities`
- `continuously improving`
- `designed natively for agent participation rather than post-hoc assistance`

### 7.2 Keep the tone visionary but grounded

Preferred style:
- confident
- clear
- high-signal
- internally credible

Avoid:
- startup manifesto voice
- sci-fi framing
- marketing exaggeration

## 8. HTML Structure Changes Required

### 8.1 Add new top-level sections in this order

1. Hero
2. Philosophy
3. How the System Works
4. What Changes in an AI-Native SDLC
5. 12-Phase Operating Model
6. Living Product Model
7. What This Blueprint Is and Is Not
8. Footer

### 8.2 Update section naming in HTML

#### Rename these classes only if you want semantic cleanup
Not required, but recommended:
- `.pipeline-container` can remain, but `.lifecycle-container` would be clearer
- `.pipeline-label` should become `.lifecycle-label` if refactoring

#### Add new reusable component classes
Recommended new classes:
- `.system-grid`
- `.system-card`
- `.comparison-grid`
- `.comparison-card`
- `.phase-meta`
- `.phase-why`
- `.phase-relationships`
- `.sim-output-section`
- `.sim-output-tabs`
- `.sim-output-tab`
- `.sim-output-panel`
- `.disclaimer-grid`
- `.disclaimer-card`

## 9. JavaScript Enhancements Required

### 9.1 Preserve current expand/collapse behavior for phases
This interaction works well and should remain.

### 9.2 Add simulated output switching logic

Each phase should support local tab switching inside the expanded card.

#### Functional behavior
- Clicking a simulated output tab updates the output preview panel
- Each phase manages its own active simulated output state
- Default the first simulated output to active when a phase opens

#### Implementation guidance
Use lightweight vanilla JavaScript. No libraries needed.

Suggested behavior:
- Add `data-output-target` attributes to output tabs
- Add `data-output-panel` containers per phase
- On click, remove `.active` from sibling tabs and panels, then activate selected one

### 9.3 Improve accessibility for interactions

Current issues:
- Phase headers are clickable divs, not accessible controls

#### Required improvement
Convert phase headers into buttons or add:
- `role="button"`
- `tabindex="0"`
- keyboard interaction for Enter and Space
- `aria-expanded`
- `aria-controls`

#### For simulated output tabs
Use button elements with proper active states and labels.

### 9.4 Theme toggle improvements

Recommended enhancements:
- Persist theme in `localStorage`
- Add accessible label updates
- Preserve user choice on reload

## 10. CSS / Visual Design Changes Required

### 10.1 Maintain current aesthetic direction
Keep:
- dark, premium, editorial look
- serif headline contrast
- monospace metadata accents
- restrained gradients

### 10.2 Improve scanability
The page is visually strong but dense.

#### Required spacing changes
- Increase spacing between major sections
- Slightly tighten body copy in phase descriptions
- Increase visual separation between description, agents, simulated outputs, and IO strip

### 10.3 Add styling for simulated artifact panels
Suggested styles:
- slightly inset panel background
- subtle border glow on active state
- monospace or mixed mono/body typography depending on artifact type
- optional header bar with file-like label such as `problem_brief.md` or `spec_delta.json`

### 10.4 Add visual cue for non-linearity
Possible treatments:
- loopback arrow accent after Phase 12
- relationship badges on phase cards
- subtle system map iconography in the `How the System Works` section

### 10.5 Address light theme issues
There is at least one likely typo in current CSS:
- `--text-muted: #6666880;`

This appears malformed and should be corrected.

Use a valid light theme muted color such as:
- `#666688`

Also review contrast in light theme for:
- text-muted
- text-dim
- borders
- accent glow

## 11. Specific Content Recommendations by Phase

This section defines how to sharpen each phase while staying conceptual.

### Phase 1
Add emphasis on signal interpretation, not just signal collection.
Refine output language to show this phase creates prioritizable opportunity framing, not just idea generation.

### Phase 2
Clarify that PRDs are human-readable and machine-usable, not just comprehensive.
Mention that good requirements reduce ambiguity before spec formalization.

### Phase 3
Make this the central anchor of the whole page.
Visually emphasize it as the keystone phase.
This is the best candidate for default expansion or highlighted styling.

### Phase 4
Clarify that architecture here is still conceptual and decision-oriented, not low-level implementation design.
Focus on tradeoffs and fit with existing systems.

### Phase 5
Reduce emphasis on "AI writes production code" as the headline promise.
Shift to `agents generate implementation aligned to the spec and codebase context`.
This sounds more credible and less hype-heavy.

### Phase 6
Clarify that review is not just defect detection, but alignment checking.
Review should feel like semantic governance, not automated nitpicking.

### Phase 7
Sharpen the idea that validation is spec-derived.
Avoid making the coverage percentages look arbitrary unless you plan to defend them.

### Phase 8
Keep the AI-specific risks, but phrase them in a way that does not make the page suddenly much more technical than the rest.

### Phase 9
This phase is a good differentiator. Keep it, but emphasize communication and shared understanding, not only demo generation.

### Phase 10
Clarify that documentation becomes another generated artifact in the system, not an afterthought.

### Phase 11
Stress controlled rollout, observability, and communication.
This phase should feel like managed release governance.

### Phase 12
Avoid language that sounds like autonomous self-management.
Use `continuous feedback and adaptation` instead of `self-healing` unless you explicitly want stronger futurist framing.

## 12. Recommended New Microcopy

Use or adapt the following.

### Main phase section caption
`Shown in a readable sequence. Operated as a continuous, feedback-driven system.`

### Simulated output section label
`Illustrative outputs`

### Phase relationship label
`Common phase relationships`

### Human gate helper text
`Where human judgment, approval, or intervention is most important.`

### Living Product subtitle revision
`How the operating model supports continuous product change across iterations, enhancements, and replacements.`

## 13. Minimal Data Model for Simulated Outputs

To keep the HTML maintainable, simulated outputs should be stored as structured data rather than hardcoded in many places.

### Recommended structure
For each phase, define an array of output objects with:
- `id`
- `label`
- `title`
- `format`
- `content`

Example conceptual shape:

```js
const simulatedOutputs = {
  phase1: [
    {
      id: 'problem-brief',
      label: 'Problem Brief',
      title: 'problem_brief.md',
      format: 'markdown',
      content: '...'
    }
  ]
}
```

This allows the HTML to scale cleanly.

## 14. Priority Order for Implementation

If this revision is done in stages, use this order.

### Priority 1
- Reframe from pipeline to operating model
- Add `How the System Works`
- Add non-linearity explanation
- Add simulated outputs for all phases
- Improve phase structure consistency

### Priority 2
- Add `What Changes in an AI-Native SDLC`
- Add `What This Blueprint Is and Is Not`
- Improve accessibility and semantic HTML
- Persist theme choice

### Priority 3
- Add loopback visualization
- Add phase relationship cues
- Refine light theme and spacing polish

## 15. Definition of Done

The revised HTML is complete when:

1. The page no longer reads as only a linear pipeline.
2. The page explains the system layer above the phases.
3. Every phase includes simulated outputs.
4. The spec is visibly established as the central operating contract.
5. Human governance is explicit and credible.
6. The artifact feels sharper and more internally useful without becoming operationally dense.
7. The page remains visually premium and easy to navigate.

## 16. Final Editorial Direction

The revised artifact should feel like this:

- a north star
- a structured internal proposal
- a conceptual blueprint
- a conversation tool for product and engineering

It should not feel like:

- a marketing landing page
- a detailed implementation architecture
- a rigid step-by-step methodology
- a claim that software delivery can or should become fully autonomous

## 17. Optional Final Enhancement

If you want one additional high-value touch, add a small fixed mini-map or section navigator on desktop with anchors to:
- Principles
- System Model
- Comparison
- Phases
- Living Product
- Blueprint Boundaries

This would significantly improve usability for longer internal review sessions.
