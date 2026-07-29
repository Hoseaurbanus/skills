# Superpowers + UI/UX Integration: Standard Prompts

> **Complete reference for using Superpowers workflow with integrated UI/UX design capabilities.**

## Table of Contents

1. [Master Prompt](#master-prompt)
2. [Quick Start Prompts](#quick-start-prompts)
3. [Phase-Specific Prompts](#phase-specific-prompts)
4. [Project Type Prompts](#project-type-prompts)
5. [Debugging Prompts](#debugging-prompts)
6. [Audit Prompts](#audit-prompts)
7. [Review Prompts](#review-prompts)
8. [Verification Prompts](#verification-prompts)
9. [Customization Guide](#customization-guide)

---

## Master Prompt

Use this as your default prompt for any software project.

```markdown
I am using the Superpowers workflow with integrated UI/UX design capabilities.

When working on any software project, I follow this process:

## Phase 1: Brainstorming (superpowers:brainstorming)
Before any implementation, I explore:
- User goals and journeys
- UX pain points and opportunities
- Information architecture
- Navigation structure
- Interface requirements
- Visual direction

I ask: "What is the best experience for the user?"
Not only: "What code should be written?"

## Phase 2: Planning (superpowers:writing-plans)
All implementation plans include:
- Frontend architecture (page structure, component hierarchy)
- Design system (colors, typography, spacing)
- Responsive strategy (mobile-first, breakpoints)
- Accessibility requirements (WCAG, keyboard navigation)
- UI/UX resources (shadcn/ui, Radix UI, Lucide Icons)

## Phase 3: Execution (superpowers:executing-plans or superpowers:subagent-driven-development)
While implementing, I maintain:
- Consistent spacing (8px grid)
- Clean layouts with proper whitespace
- Responsive design on all breakpoints
- Accessibility (keyboard, focus indicators, ARIA)
- Loading, error, and empty states
- User feedback for all actions

## Phase 4: Review (superpowers:requesting-code-review)
Code reviews include:
- Engineering review (quality, security, performance)
- UI review (design consistency, UX quality, accessibility)

## Phase 5: Verification (superpowers:verification-before-completion)
Before claiming completion, verify:
- ✓ All tests pass
- ✓ Responsive on mobile, tablet, desktop
- ✓ Keyboard navigation works
- ✓ Focus indicators visible
- ✓ ARIA labels present
- ✓ Loading states exist
- ✓ Error states exist
- ✓ Empty states exist
- ✓ Visual consistency with design system
- ✓ Accessibility check passes

## Default Design Stack
When building React applications:
- React + TypeScript + Tailwind CSS
- shadcn/ui (components)
- Radix UI (accessibility)
- Lucide Icons (icons)
- Framer Motion (animations)

## UI/UX Resources
Reference: skills/ui-ux-design-principles/SKILL.md

## Core Principles
1. UI/UX is a core engineering requirement, not decoration
2. Accessibility is mandatory, not optional
3. Responsive design is required for all screen sizes
4. Visual consistency through design systems
5. User-centered design approach
6. Professional quality standards
```

---

## Quick Start Prompts

### Feature Development

```markdown
Build [FEATURE NAME] using the Superpowers workflow with UI/UX integration.

Requirements:
- [List functional requirements]

UI/UX Requirements:
- Responsive (mobile, tablet, desktop)
- Accessible (WCAG AA)
- Consistent with design system
- Professional appearance

Follow the Superpowers workflow:
1. Brainstorm user experience first
2. Plan with frontend architecture
3. Implement with UI standards
4. Review with UI criteria
5. Verify UI/UX before completion
```

### New Project

```markdown
Start a new project using Superpowers with full UI/UX integration.

Project: [PROJECT NAME]
Purpose: [WHAT IT DOES]
Users: [TARGET AUDIENCE]

Tech Stack:
- [Framework]
- [Styling]
- [Components]

UI/UX Requirements:
- Design system with tokens
- Responsive breakpoints: mobile (375px), tablet (768px), desktop (1280px)
- WCAG AA accessibility
- Professional appearance

Begin with brainstorming phase to define user goals and journeys.
```

### Existing Project Enhancement

```markdown
Enhance [EXISTING FEATURE] using Superpowers with UI/UX integration.

Current State:
- [What exists now]
- [Known issues]

Desired State:
- [What should improve]

UI/UX Improvements:
- Better responsiveness
- Improved accessibility
- Consistent design patterns
- Enhanced user feedback

Follow Superpowers workflow with focus on incremental improvement.
```

---

## Phase-Specific Prompts

### Brainstorming Phase

```markdown
I need to brainstorm [FEATURE/PROJECT] using superpowers:brainstorming.

Before any code, help me explore:
1. User goals - What do users want to accomplish?
2. User journeys - How will they interact with this?
3. Pain points - What problems exist now?
4. Information architecture - How should content be organized?
5. Navigation structure - How will users move around?
6. Interface requirements - What UI elements are needed?
7. Visual direction - What style/approach fits?

Ask me questions one at a time to refine the idea.
Present 2-3 approaches with trade-offs.
Get my approval before moving to planning.
```

### Planning Phase

```markdown
Create an implementation plan using superpowers:writing-plans for [FEATURE].

The design/spec is: [LINK TO SPEC OR DESCRIPTION]

The plan must include:
1. Frontend Architecture
   - Page structure and routing
   - Component hierarchy
   - State management approach

2. Design System
   - Color palette and tokens
   - Typography scale
   - Spacing system (8px grid)
   - Component variants

3. Responsive Strategy
   - Mobile-first approach
   - Breakpoints: 375px, 768px, 1280px
   - Touch targets (44x44px minimum)

4. Accessibility Requirements
   - WCAG AA compliance
   - Keyboard navigation
   - Screen reader support
   - Focus management

5. Interaction Patterns
   - Form validation and feedback
   - Loading states
   - Error handling
   - Success confirmations

6. UI/UX Resources
   - shadcn/ui components
   - Radix UI primitives
   - Lucide Icons

Save plan to: docs/superpowers/plans/YYYY-MM-DD-[feature].md
```

### Execution Phase

```markdown
Execute the implementation plan using superpowers:subagent-driven-development.

Plan location: [LINK TO PLAN]

While implementing, maintain:
- Consistent spacing (8px grid)
- Clean layouts with proper whitespace
- Responsive design on all breakpoints
- Accessibility (keyboard, focus indicators, ARIA)
- Loading states for async operations
- Error states with clear messaging
- Empty states with helpful guidance
- User feedback for all actions

Divide into specialized agents if possible:
- Agent 1: UI/UX Architecture
- Agent 2: Frontend Components
- Agent 3: Backend/API
- Agent 4: Database (if applicable)
- Agent 5: Testing & QA

Include UI/UX criteria in task reviews.
```

### Review Phase

```markdown
Request code review using superpowers:requesting-code-review.

What was implemented: [DESCRIPTION]
Plan/requirements: [LINK]
Base SHA: [BASE]
Head SHA: [HEAD]

Review must include:

Engineering Review:
- Code quality
- Security
- Performance
- Testing

UI/UX Review:
- Design consistency with existing components
- Responsive behavior on all breakpoints
- Accessibility (keyboard, focus, ARIA)
- Loading, error, and empty states
- Visual hierarchy
- Component reuse

Provide severity-based feedback (Critical/Important/Minor).
```

### Verification Phase

```markdown
Verify completion using superpowers:verification-before-completion before claiming success.

I have implemented [FEATURE].

Verify ALL of the10:

Functionality:
- [ ] All tests pass
- [ ] Build succeeds
- [ ] Features work as specified

UI Verification:
- [ ] Responsive on mobile (375px)
- [ ] Responsive on tablet (768px)
- [ ] Responsive on desktop (1280px)
- [ ] Touch targets are 44x44px minimum

Accessibility Verification:
- [ ] Keyboard navigation works
- [ ] Focus indicators visible
- [ ] ARIA labels present
- [ ] Screen reader tested (if possible)
- [ ] Color contrast passes (4.5:1)

UX Verification:
- [ ] Loading states exist
- [ ] Error states exist
- [ ] Empty states exist
- [ ] User feedback for all actions
- [ ] User flows are logical

Visual Consistency:
- [ ] Matches design system
- [ ] Spacing follows 8px grid
- [ ] Colors match tokens
- [ ] Typography is consistent

Run verification commands and show output before claiming completion.
```

---

## Project Type Prompts

### Dashboard Application

```markdown
Build a dashboard application using Superpowers with full UI/UX integration.

Tech Stack:
- React/Next.js
- TypeScript
- Tailwind CSS
- Tremor (charts)
- Origin UI (dashboard components)

Requirements:
- [List features]

UI/UX Requirements:
- Responsive sidebar navigation
- Data visualization with charts
- Tables with sorting/filtering/pagination
- Form handling with validation
- Real-time updates
- Loading skeletons
- Empty states
- Error boundaries

Design System:
- Consistent color palette
- Typography scale
- Spacing tokens (8px grid)
- Component library

Accessibility:
- WCAG AA compliance
- Keyboard navigation
- Screen reader support
- High contrast mode

Follow Superpowers workflow from brainstorming to verification.
```

### E-commerce Application

```markdown
Build an e-commerce application using Superpowers with UI/UX focus.

Tech Stack:
- [Framework]
- [Styling]
- [Payment integration]

Requirements:
- [List features]

UI/UX Requirements:
- Product browsing with filters
- Shopping cart experience
- Checkout flow
- User account management
- Order history
- Responsive product cards
- Image galleries
- Search functionality

Design Principles:
- Clean product presentation
- Trust signals
- Clear CTAs
- Minimal friction checkout
- Mobile-first approach

Accessibility:
- Product images have alt text
- Forms are accessible
- Keyboard navigable
- Screen reader friendly

Follow Superpowers workflow.
```

### SaaS Application

```markdown
Build a SaaS application using Superpowers with professional UI/UX.

Tech Stack:
- [Framework]
- [Styling]
- [Auth provider]

Core Features:
- [List features]

UI/UX Requirements:
- Onboarding flow
- Dashboard with metrics
- Settings management
- Team collaboration
- Billing/subscription
- Notifications
- Search functionality

Design System:
- Professional appearance
- Consistent patterns
- Clear hierarchy
- Efficient workflows

Accessibility:
- WCAG AA compliance
- Keyboard shortcuts
- Screen reader support
- Responsive design

Follow Superpowers workflow.
```

### Mobile-First Application

```markdown
Build a mobile-first application using Superpowers with mobile UI/UX focus.

Tech Stack:
- [Framework]
- [Styling]
- [Mobile considerations]

Requirements:
- [List features]

Mobile UI/UX Requirements:
- Touch-friendly interactions (44x44px targets)
- Swipe gestures
- Pull-to-refresh
- Bottom navigation
- Haptic feedback
- Offline support
- Fast loading
- Minimal typing

Responsive Strategy:
- Mobile: 375px (primary)
- Tablet: 768px
- Desktop: 1280px

Design Principles:
- Thumb-friendly zones
- Clear visual feedback
- Minimal cognitive load
- Progressive disclosure

Accessibility:
- VoiceOver/TalkBack support
- Dynamic type sizes
- High contrast
- Reduce motion

Follow Superpowers workflow with mobile-first approach.
```

---

## Debugging Prompts

### Frontend Bug

```markdown
Debug this frontend issue using superpowers:systematic-debugging with UX investigation.

The issue: [DESCRIBE ISSUE]

Steps to reproduce:
1. [Step 1]
2. [Step 2]
3. [Step 3]

Expected behavior: [WHAT SHOULD HAPPEN]
Actual behavior: [WHAT HAPPENS]

Investigate BOTH:
1. Technical problems:
   - JavaScript errors
   - Component errors
   - API issues
   - State management issues

2. UX problems:
   - Broken user flows
   - Confusing interactions
   - Poor feedback
   - Accessibility issues

Find the root cause, not just the symptom.
```

### Responsive Issue

```markdown
Debug this responsive design issue using superpowers:systematic-debugging.

The issue: [DESCRIBE RESPONSIVE PROBLEM]

Affected breakpoints:
- Mobile (375px): [ISSUE]
- Tablet (768px): [ISSUE]
- Desktop (1280px): [ISSUE]

Investigate:
- CSS media queries
- Flexbox/Grid layout
- Container queries
- Viewport units
- Touch targets

Fix the root cause and ensure consistency across all breakpoints.
```

### Accessibility Issue

```markdown
Debug this accessibility issue using superpowers:systematic-debugging.

The issue: [DESCRIBE ACCESSIBILITY PROBLEM]

WCAG criterion: [CRITERION NUMBER]

Investigate:
- Keyboard navigation
- Focus management
- ARIA labels
- Color contrast
- Screen reader compatibility
- Semantic HTML

Fix the issue and ensure WCAG AA compliance.
```

---

## Audit Prompts

### Full Codebase Audit

```markdown
Run an exhaustive audit on this project using superpowers:exhaustive-audit with full UI/UX evaluation.

Check all 16 categories:

1. Project Identity
2. Tech Stack
3. Directory Structure
4. Entry Points
5. Configuration
6. Core Modules
7. Data Flow
8. External Integrations
9. Dependencies
10. Testing
11. Security
12. Performance
13. Deployment
14. Documentation
15. Pain Points
16. UI/UX Quality

For UI/UX Quality, check:
- Visual consistency across components
- Layout quality and whitespace usage
- Mobile responsiveness on all breakpoints
- Accessibility (keyboard, ARIA, contrast)
- User flow problems
- Navigation issues
- Component duplication
- Design inconsistencies

Provide prioritized recommendations.
Save report to: docs/audits/YYYY-MM-DD-[project]-audit.md
```

### UI/UX Focused Audit

```markdown
Run a UI/UX focused audit on this project.

Evaluate:

Visual Consistency:
- Is there a consistent color system?
- Is typography consistent?
- Are spacing patterns consistent?
- Do components look like they belong?

Layout Quality:
- Are layouts clean and uncluttered?
- Is whitespace used effectively?
- Are elements properly aligned?
- Is visual hierarchy clear?

Mobile Responsiveness:
- Does the app work on mobile?
- Are touch targets large enough?
- Is content readable on small screens?
- Are interactions touch-friendly?

Accessibility:
- Can all features be accessed via keyboard?
- Are focus indicators visible?
- Do colors meet contrast requirements?
- Are forms properly labeled?

User Flows:
- Are user journeys intuitive?
- Can users accomplish goals efficiently?
- Are there any dead ends?
- Is navigation clear?

Provide specific improvement recommendations with file references.
```

### Accessibility Audit

```markdown
Run an accessibility audit on this project.

Test against WCAG 2.1 AA criteria:

Perceivable:
- [ ] Text alternatives for non-text content
- [ ] Captions for multimedia
- [ ] Content adaptable to different presentations
- [ ] Sufficient color contrast

Operable:
- [ ] All functionality available from keyboard
- [ ] Users have enough time to read content
- [ ] Content doesn't cause seizures
- [ ] Users can navigate and find content

Understandable:
- [ ] Text is readable and understandable
- [ ] Pages appear and operate predictably
- [ ] Users are helped to avoid and correct mistakes

Robust:
- [ ] Content compatible with assistive technologies

Provide specific issues with file:line references and fixes.
```

---

## Review Prompts

### UI/UX Code Review

```markdown
Request UI/UX focused code review using superpowers:requesting-code-review.

What was implemented: [DESCRIPTION]
Plan/requirements: [LINK]
Base SHA: [BASE]
Head SHA: [HEAD]

UI/UX Review Checklist:

Design Consistency:
- Components match existing patterns
- Colors follow design system
- Typography is consistent
- Spacing follows 8px grid

Responsive Behavior:
- Works on mobile (375px)
- Works on tablet (768px)
- Works on desktop (1280px)
- Touch targets are adequate

Accessibility:
- Keyboard navigation works
- Focus indicators visible
- ARIA labels present
- Color contrast passes
- Screen reader tested

User Experience:
- Loading states exist
- Error states exist
- Empty states exist
- Feedback for all actions
- Logical user flows

Provide severity-based feedback with specific file:line references.
```

### Component Review

```markdown
Review this component for UI/UX quality.

Component: [COMPONENT NAME]
File: [FILE PATH]

Check:
1. Props API - Is it intuitive?
2. Variants - Are all states handled?
3. Accessibility - Is it keyboard accessible?
4. Responsiveness - Does it work on all sizes?
5. Loading state - Does it have one?
6. Error state - Does it handle errors?
7. Empty state - Does it have one?
8. Animation - Is it purposeful?
9. Documentation - Is it documented?
10. Tests - Are UI tests included?

Provide specific improvement recommendations.
```

---

## Verification Prompts

### Pre-Commit Verification

```markdown
Before I commit, verify this work using superpowers:verification-before-completion.

I have implemented: [DESCRIPTION]

Run and verify:

1. Functionality:
   - [ ] All tests pass: [SHOW COMMAND OUTPUT]
   - [ ] Build succeeds: [SHOW COMMAND OUTPUT]
   - [ ] Linting passes: [SHOW COMMAND OUTPUT]

2. UI Verification:
   - [ ] Responsive on mobile: [TESTED]
   - [ ] Responsive on tablet: [TESTED]
   - [ ] Responsive on desktop: [TESTED]

3. Accessibility:
   - [ ] Keyboard navigation: [TESTED]
   - [ ] Focus indicators: [VERIFIED]
   - [ ] ARIA labels: [VERIFIED]
   - [ ] Color contrast: [PASS/FAIL]

4. UX:
   - [ ] Loading states: [EXISTS]
   - [ ] Error states: [EXISTS]
   - [ ] Empty states: [EXISTS]
   - [ ] User feedback: [EXISTS]

5. Visual Consistency:
   - [ ] Design system: [MATCHES]
   - [ ] Spacing: [8px grid]
   - [ ] Colors: [TOKENS]
   - [ ] Typography: [CONSISTENT]

Show evidence for each verification before I commit.
```

### Pre-PR Verification

```markdown
Before I create a PR, verify completeness using superpowers:verification-before-completion.

Feature: [FEATURE NAME]
Plan: [LINK TO PLAN]

Verify ALL requirements from plan are met:

Requirements Checklist:
- [ ] [Requirement 1]: [STATUS]
- [ ] [Requirement 2]: [STATUS]
- [ ] [Requirement 3]: [STATUS]

UI/UX Checklist:
- [ ] All components follow design system
- [ ] Responsive on all breakpoints
- [ ] Accessible (WCAG AA)
- [ ] Loading/error/empty states
- [ ] User feedback for all actions
- [ ] Professional appearance

Quality Checklist:
- [ ] All tests pass
- [ ] Build succeeds
- [ ] No linting errors
- [ ] Code reviewed
- [ ] Documentation updated

Show evidence for each item before I create PR.
```

---

## Customization Guide

### Modify for Your Project

Replace these placeholders with your project specifics:

| Placeholder | Replace With |
|-------------|--------------|
| `[FEATURE NAME]` | Your feature name |
| `[PROJECT NAME]` | Your project name |
| `[DESCRIPTION]` | What was built |
| `[LINK TO SPEC]` | Path to design spec |
| `[LINK TO PLAN]` | Path to implementation plan |
| `[BASE]` | Git base SHA |
| `[HEAD]` | Git head SHA |
| `[FRAMEWORK]` | React, Vue, Svelte, etc. |
| `[STYLING]` | Tailwind, CSS Modules, etc. |

### Add Custom Requirements

Append project-specific requirements to any prompt:

```markdown
Additional Requirements:
- [Custom requirement 1]
- [Custom requirement 2]
- [Custom requirement 3]
```

### Modify Design Stack

Update the design stack for your needs:

```markdown
Design Stack:
- [Your framework]
- [Your styling solution]
- [Your component library]
- [Your icon library]
- [Your animation library]
```

### Adjust Accessibility Level

Modify accessibility requirements:

```markdown
Accessibility Level:
- WCAG A (minimum)
- WCAG AA (standard) ← default
- WCAG AAA (enhanced)
```

---

## File Location

Save this file to: `docs/superpowers/SUPERPOWERS-UI-UX-PROMPTS.md`

## Usage

1. Copy the appropriate prompt for your task
2. Fill in the placeholders with your specifics
3. Paste into your AI assistant
4. Follow the Superpowers workflow

## Related Files

- `skills/ui-ux-design-principles/SKILL.md` - UI/UX design principles reference
- `skills/emil-design-eng/SKILL.md` - Emil Kowalski design engineering philosophy
- `skills/review-animations/SKILL.md` - Animation code review
- `skills/improve-animations/SKILL.md` - Animation audit and improvement plans
- `skills/find-animation-opportunities/SKILL.md` - Animation opportunity discovery
- `skills/animation-vocabulary/SKILL.md` - Motion terminology reference
- `skills/apple-design/SKILL.md` - Apple design philosophy for web
- `skills/pick-ui-library/SKILL.md` - Curated library recommendations
- `skills/prototype/SKILL.md` - UI variant prototyping
- `skills/*/SKILL.md` - Individual skill documentation
- `docs/superpowers/plans/` - Implementation plans
- `docs/audits/` - Audit reports

---

## Emil Kowalski Design Engineering Integration

Emil Kowalski's skills are layered on top of Superpowers for frontend-specific tasks. They activate ONLY for UI-related work and never override Superpowers engineering decisions.

### When to Use Emil's Skills

| Task | Superpowers Handles | Emil Handles |
|------|---------------------|--------------|
| Build a new feature | Planning, architecture, TDD | Component polish, spacing, typography |
| Review code | Engineering quality, security | Animation craft, motion review |
| Debug a bug | Root cause analysis | UX problem investigation |
| Audit a codebase | Full 16-category audit | Animation-specific audit |
| Design a UI component | Implementation approach | Visual hierarchy, micro-interactions |
| Add animations | When to animate (framework) | How to animate (easing, duration, physics) |
| Choose a library | Engineering fit | Design quality, DX |

### Emil's Workflow Integration Points

**After brainstorming (superpowers:brainstorming):**
- Use `emil-design-eng` to refine UI decisions
- Use `prototype` to explore variant directions

**During implementation (superpowers:executing-plans):**
- Use `pick-ui-library` to select frontend dependencies
- Use `emil-design-eng` for component building principles

**After implementation:**
- Use `review-animations` for animation code review
- Use `find-animation-opportunities` to discover polish moments
- Use `improve-animations` for codebase-wide motion audits

**During review (superpowers:requesting-code-review):**
- Add `review-animations` as a secondary review for UI-heavy diffs

### Priority Rules

1. **Superpowers decides** the engineering approach, architecture, and workflow
2. **Emil refines** the user experience, presentation, and motion
3. **Never let Emil** change architecture, backend, logic, security, or engineering workflow
4. **When both apply**, Superpowers takes precedence; Emil adds polish

### Emil's Skill Invocation

| Skill | Invocation | Auto-trigger? |
|-------|-----------|---------------|
| `emil-design-eng` | `superpowers:emil-design-eng` | Yes (for UI tasks) |
| `review-animations` | `superpowers:review-animations` | No (explicit only) |
| `improve-animations` | `superpowers:improve-animations` | Yes (for motion audits) |
| `find-animation-opportunities` | `superpowers:find-animation-opportunities` | Yes (for UI polish) |
| `animation-vocabulary` | `superpowers:animation-vocabulary` | Yes (for naming effects) |
| `apple-design` | `superpowers:apple-design` | Yes (for gesture/spring UI) |
| `pick-ui-library` | `superpowers:pick-ui-library` | No (explicit only) |
| `prototype` | `superpowers:prototype` | No (explicit only) |

---

**Last Updated:** 2026-07-29
**Version:** 2.0.0 (Emil Kowalski integration added)
