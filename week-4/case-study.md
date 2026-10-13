# Stride — Small steps, real progress
**UX case study · Week 4 · Mirza Mohteshim · 13 October 2026**

## Overview
Stride explores a real problem: people with limited time may find fitness tracking too demanding to maintain. The concept prioritizes manual activity logging, flexible weekly goals and clear feedback. Deliverables include 16 high-fidelity screen designs, key-flow prototyping, a token-based design system, original SVG exports and developer specs.

Role: UX/UI concept design and documentation. Tools: HTML, CSS, JavaScript, SVG, Figma for the earlier research concept. This is an assignment concept, not a launched product.

## Research method and honesty
Desk research used two published qualitative studies and official competitor documentation. No interviews, surveys or usability sessions were conducted. Personas, empathy statements, journey emotions and product opportunity claims are hypotheses. No measured retention, completion or health outcomes are claimed.

R1 reports that guidance, lower cognitive load and self-monitoring can support engagement, while reminder preferences vary. R2 describes tracking burden, negative feelings from progress feedback and privacy concerns. These findings informed a small number of required fields, opt-in reminders and neutral weekly feedback; they do not prove our design is effective.

[R1 — Health-app engagement, 2021](https://mhealth.jmir.org/2021/12/e29098)
[R2 — Health behavior change apps, 2013](https://www.jmir.org/2013/4/e86/)
Limitations: broader health-app contexts, older studies and no sample from our intended audience.

## Problem statement
How might we help adults record everyday activity quickly, choose a goal that fits their week and understand progress without making missed days feel like failure?

## Personas — fictional hypotheses
### Aanya, 24 — busy beginner
Context: student or early-career worker; smartphone only. Goal: stay active with short walks or workouts. Behavior: activity fits into breaks; logging may be forgotten later. Pain: long setup, overloaded metrics and rigid targets. Need: a manageable goal and one obvious next step.
Empathy: says “I only have 20 minutes”; thinks “Does a short walk count?”; does short sessions between commitments; feels hopeful but easily overwhelmed. These are imagined statements, not interview quotes.

### Rohan, 32 — regular exerciser
Context: software professional; exercises three times per week. Goal: record sessions accurately and compare consistency. Behavior: repeats routines and reviews weekly totals. Pain: repetitive entry and unclear metrics. Need: editable details, history and understandable units.
Empathy: says “Let me reuse my last workout”; thinks “Is this record accurate?”; checks past activity; feels motivated by understandable progress. These are imagined statements.

## Hypothesis journey map
| Stage | Action / thought | Emotion | Friction | Design response |
|---|---|---|---|---|
| Start | Choose a goal / Can I fit this in? | Hopeful | Long setup | Three short onboarding screens |
| Check Today | Decide what to record | Uncertain | Dashboard overload | One dominant Log activity action |
| Log | Enter activity and minutes | Impatient | Too many fields | Only duration required after type selection |
| Review | Check and save details | Reassured | Accidental errors | Editable review before save |
| Reflect | Review weekly consistency | Encouraged | Punitive streak pressure | Flexible weekly totals, no failure language |

## Competitive analysis
| Product | Documented emphasis | Relevance to Stride |
|---|---|---|
| Strava | Activity tracking, sharing, routes and training analysis | Benchmark clear activity history; Stride focuses on simple manual entry |
| MyFitnessPal | Today tab supports meals, water, exercise and weight logging | Benchmark accessible logging entry; Stride narrows initial scope to activity |
| Stride concept | Manual sessions, flexible goals and private-first presentation | Proposed positioning; not proof of a market gap |

[C1 — Strava official site](https://www.strava.com/)
[C2 — MyFitnessPal Today tab](https://support.myfitnesspal.com/hc/en-us/articles/39985611667341-Your-Today-tab)
Review uses documented features, not timed competitor tests. Feature availability can vary.

## Information architecture and wireframes
Three primary destinations: Today, Progress and Profile. Activity entry is a focused flow rather than a fourth crowded tab. Week 1 low-fidelity work established Goal → Today → Log → Review → Progress.
[Earlier Figma concept](https://www.figma.com/design/SIDuYnnVOpus2hlWFQh4mi)

The new screen gallery includes a grayscale wireframe treatment for structural review. It is a representation of the final layout, not evidence of an additional user-tested iteration.

## Design system
Colours: dark teal primary #115E59, ink #172033, muted #475569, white surface and pale slate canvas. Lime #D9F99D accents supportive feedback. Typography uses system sans with 28/36 titles and 16/24 body text. Spacing uses a 4 px grid.

Components: buttons, labeled inputs, selects, cards, activity rows, bottom navigation, progress bars, chart bars, checkboxes and status feedback. Default, hover, focus, selected, disabled and error states are specified in the handoff. Shared CSS patterns and design tokens keep implementation consistent.

## High-fidelity screen inventory
1. Welcome
2. Track your way
3. Stay in control
4. Weekly goal
5. Today dashboard
6. Activity selection
7. Activity logging
8. Review activity
9. Saved confirmation
10. Weekly progress
11. Activity history
12. Activity detail
13. Edit activity
14. Profile
15. Preferences
16. Reminders

## Prototype flows
Onboard → set goal → Today.
Today → choose activity → enter details → review → save → progress.
History → activity detail → edit → review → save.
Profile → preferences → reminders → save.
Entered values appear in review and details. Goals and reminders update the in-memory demo. Data resets on reload; no actual notifications or account are connected.

## UX copy
Welcome: “Small steps. Real progress.” / “Make room for movement, one session at a time.”
Track: “Track your way” / “Log a walk, run or workout in moments. No wearable needed.”
Control: “You’re in control” / “Choose a goal that fits your week. Reminders are optional, and your activity stays private.”
The tone favors encouragement over guilt and avoids health outcome promises.

## Accessibility and handoff
Minimum control height 48 px; visible keyboard focus; labeled fields; text values alongside charts; reduced-motion preference supported. Primary teal/white contrast is 7.58:1. Specs include data shape, validation, error handling, assets and implementation acceptance checks. Static designs and syntax checks do not establish complete WCAG conformance.

## Validation plan and outcomes
No usability results exist. Next: interview 6–8 intended users, then test five participants on goal setting, a 20-minute walk log, editing and finding weekly totals. Measure unaided completion, entry time, mistakes and perceived clarity. Proposed targets: 4/5 complete core tasks unaided, with typical logging under 60 seconds. These are targets, not observed results.

Completed output: coherent research-informed concept, sixteen screen designs, interactive demo and handoff package. Open questions: whether the session-based goal suits intended users, how repeat logging should work, and whether reminders help or irritate. Validate those before building a production app.
