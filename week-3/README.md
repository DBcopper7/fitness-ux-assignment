# Week 3 — Design Systems & Prototyping

## Deliverables
1. [Editable Figma design system and dashboard layouts](https://www.figma.com/design/ZAYotFEHd7PhhdMMy9dIuO)
2. [Interactive HTML prototype](./prototype.html) — download the file using GitHub's **Download raw file** control, then open it in Chrome, Edge or Firefox. It needs no installation or server.

**Figma's Starter MCP limit prevented the interaction connections from being saved. Figma contains editable design artifacts; the HTML file supplies the working interactive prototype.**

## Component library
- Buttons: Default, Hover, Focus, Disabled, Secondary
- Inputs: Default, Focus, Error, Disabled
- Metric cards, project forms, project tables, labelled bar charts, navigation and modals
- Native linked Figma instances, reusable text styles and semantic colour variables aliased to primitives

## Five-screen prototype
Overview → Projects → Project detail → Analytics → Settings → Overview.
This loop has six screen changes. The Projects screen also opens a New project modal with Cancel, required-field validation and Create actions.

Screen entrance: 250 ms fade and upward motion. Modal entrance: 200 ms. System reduced-motion preferences and the demo's Reduce motion preference disable animations. Standard HTML dialog provides modal semantics, Escape dismissal and focus containment. Actions and fields have visible keyboard focus. Demo state is in memory only.

## Responsive layouts
| Width | Layout |
|---|---|
| Desktop ≥1024 px | Sidebar, 3 KPI columns, full project table |
| Tablet 768–1023 px | Horizontal navigation, 2 KPI columns |
| Mobile <768 px | Collapsible menu, single-column metrics, project cards replacing the table |

Figma includes 390, 768 and 1200 px layout specimens. HTML implements the breakpoints.

## Style guide
Inter/system sans. Title 28/36 px, heading 20/28, body 16/24, label 14/20, caption 12/18. Spacing: 4, 8, 12, 16, 24, 32, 48 px. Radius 12 px. Buttons have a minimum 48 px height.
Primary #1D4ED8; text #172033; secondary text #475569; surface #FFFFFF; canvas #F1F5F9; control border #64748B; error #B91C1C; success #166534.

## Heuristic evaluation: Todoist
Documentation-based expert review conducted 13 October 2026. Scope: task capture, date parsing and filters. No logged-in user test. Severity is an expert estimate: 0 strength, 1 cosmetic, 2 minor, 3 major, 4 blocker.

| Heuristic | Evidence | Assessment | Recommendation | Severity |
|---|---|---|---|---|
| Match with real world | Conversational date parsing [S1] | Familiar language may reduce entry effort | Retain parsed-date feedback | 0 |
| User control | Date recognition can be disabled [S1] | Automation can be overridden | Keep preference discoverable | 0 |
| Recognition over recall | Filters use query syntax [S2] | Novices may need to recall syntax | Visual filter chips and preview | 2 |
| Consistency | No-priority syntax differs in filters and Quick Add [S2] | Context switching may cause errors | Context-sensitive syntax help | 2 |
| Visibility | Completed tasks excluded from filters [S2] | Empty results may confuse users | Active-only label and history link | 2 |
| Efficiency | Quick Add supports task attributes [S1] | Efficient single-panel entry | Optional novice hints | 0 |

[S1: Todoist glossary](https://www.todoist.com/help/todoist/get-started/todoist-glossary-cA60laWMH)
[S2: Introduction to filters](https://www.todoist.com/help/todoist/features/introduction-to-filters-V98wIH)

These are interpretations of documented behavior, not observed usability failures. Verify proposed issues in current product sessions before prioritizing fixes. Offline behavior, error recovery and full accessibility conformance were not evaluated.

## Verification and limits
JavaScript syntax check passed; five route views, responsive breakpoints, modal controls and reduced-motion rules are present. Automated browser testing could not run because the runtime has no Chromium executable. Open the HTML file to review the clickable flow. Static Figma mockups do not establish full accessibility conformance. Data is illustrative and no backend is implemented.
