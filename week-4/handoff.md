# Stride — Developer Handoff
## Scope
Browser-local fitness prototype with 16 designed screens. No real account, health integration or server. Demo values are illustrative.

## Inventory
01 Welcome; 02 Track your way; 03 Stay in control; 04 Goal setup; 05 Today; 06 Choose activity; 07 Log activity; 08 Review; 09 Saved; 10 Progress; 11 History; 12 Activity detail; 13 Edit activity; 14 Profile; 15 Preferences; 16 Reminders.

## Tokens and typography
See tokens.json. CSS custom properties mirror colours. System sans fallback; no licensed font files required. Body 16/24 px, titles 28/36, headings 20/28, labels 14/20. 4 px spacing grid. Horizontal phone padding 24 px; control minimum height 48 px; focus outline 3 px.

## Components and states
- Button: primary, secondary, disabled, hover and keyboard focus.
- Input: visible label, default, focus and invalid with text error.
- Card: metric, activity and informational.
- Navigation: Today, Progress, Profile; selected item is labeled and underlined.
- Progress bar: accessible name and numeric value.
- Dialog/message: save confirmation uses status text and explicit next action.
- Chart: values and units remain available as text.
- Switch/checkbox: visible label and checked state.
- Empty history: message + Log activity action.
All implemented as reusable HTML/CSS patterns in prototype.html. Gallery panels are visual specimens, not independent running forms.

## Main flows
Welcome → Track your way → Stay in control → Goal → Today.
Today → Choose activity → Log → Review → Saved → Progress.
History → Detail → Edit → Review → Saved.
Profile → Preferences → Reminders → Profile.
Back controls return to the appropriate step. Validation does not erase inputs.

## Data contract for future implementation
Activity {id:string, type:walk|run|strength|cycle, durationMinutes:number>0, distanceKm?:number>=0, date:YYYY-MM-DD}. Weekly goal: integer 1–7. Reminder: enabled:boolean, time:HH:mm. Account fields are sample content.
Review uses entered values; successful save updates session data. Entries are not persisted after reload. This is disclosed in the UI. Future backend needs authentication, authorized access, timezone rules, duplicate prevention and secure storage.

## Interaction & responsive behavior
180–250 ms opacity/translate transition. prefers-reduced-motion removes animation. At <760 px portfolio and gallery become one column; app phone scales within the viewport. Keyboard activation uses native buttons. Focus moves to screen heading after navigation. Error fields receive focus. Status messages use aria-live.

## Accessibility
Normal text ≥4.5:1; essential control boundaries ≥3:1. #115E59 on white is 7.58:1; white on #115E59 7.58:1; #172033 on white 16.27:1; #475569 on white 7.58:1; #64748B on white 4.76:1. Colour is accompanied by text, selected indicators and values. Full WCAG conformance requires implementation testing.

## Assets
assets/logo.svg: logo lockup, viewBox 240 × 64.
assets/activity.svg, goal.svg, success.svg: 64 × 64 SVG icons.
Vector assets are original editable exports and scale without loss. Decorative illustrations use empty alt; meaningful icons must have adjacent text or accessible names. Use currentColor variants if needed; preserve contrast.

## Acceptance checklist
Validate positive duration and nonnegative distance; review entered values; edit retains values; save displays confirmation; weekly target changes update Today; reminder controls show current state; test keyboard navigation and reduced motion; check at 390/768/1440 widths. No browser execution was available in this workspace; syntax and structure checks only.
