# UI/UX Integration Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Integrate professional UI/UX design capabilities into all existing Superpowers skills, treating UI/UX as a core engineering requirement rather than decoration.

**Architecture:** Enhance each skill with UI/UX considerations by adding new sections, checklists, and guidelines. Create a shared UI/UX design principles reference document. Maintain existing skill structure and follow writing-skills guidelines.

**Tech Stack:** Markdown documentation, Superpowers skill system

## Global Constraints

- Do NOT create new skills - extend existing ones
- Maintain existing YAML frontmatter structure
- Preserve existing skill workflows and Iron Laws
- Follow writing-skills guidelines for documentation
- Use consistent UI/UX terminology across all skills
- Reference shared UI/UX principles document where needed

---

## Task 1: Create UI/UX Design Principles Reference Document

**Files:**
- Create: `C:\Users\User1\.config\opencode\skills\ui-ux-design-principles\SKILL.md`

**Interfaces:**
- Consumes: None (standalone reference)
- Produces: Shared UI/UX principles referenced by all enhanced skills

- [ ] **Step 1: Create UI/UX design principles directory**

```bash
mkdir -p "C:\Users\User1\.config\opencode\skills\ui-ux-design-principles"
```

- [ ] **Step 2: Create SKILL.md with comprehensive UI/UX principles**

```markdown
---
name: ui-ux-design-principles
description: Reference document for UI/UX design principles used across all Superpowers skills. Not a workflow skill - provides design system, component architecture, and accessibility standards.
---

# UI/UX Design Principles

## Overview

This is a reference document for UI/UX design principles applied across all Superpowers skills. It defines the design system, component architecture, accessibility standards, and modern UI patterns.

## Design Systems

### Reusable Components
- Build component libraries, not one-off implementations
- Use design tokens for consistent spacing, colors, typography
- Create composable primitives (Button, Input, Card, Modal)
- Implement compound components for complex patterns

### Consistent Tokens
```css
/* Spacing scale */
--space-1: 0.25rem;
--space-2: 0.5rem;
--space-3: 0.75rem;
--space-4: 1rem;
--space-6: 1.5rem;
--space-8: 2rem;

/* Color system */
--primary: oklch(0.65 0.19 265);
--secondary: oklch(0.65 0.19 265);
--background: oklch(1 0 0);
--foreground: oklch(0.15 0 0);
--muted: oklch(0.95 0 0);
--accent: oklch(0.65 0.19 265);

/* Typography scale */
--text-xs: 0.75rem;
--text-sm: 0.875rem;
--text-base: 1rem;
--text-lg: 1.125rem;
--text-xl: 1.25rem;
--text-2xl: 1.5rem;
```

### Clear Hierarchy
- Visual hierarchy through size, weight, color, and spacing
- Consistent heading levels (H1-H6)
- Proper content grouping and sectioning
- Scannable layouts with clear focal points

## Modern UI Patterns

### Clean Layouts
- Grid-based layouts with consistent gutters
- Responsive breakpoints (mobile, tablet, desktop)
- Proper whitespace usage
- Visual breathing room

### Minimal Clutter
- Progressive disclosure - show only what's needed
- Reduce cognitive load
- Clear visual hierarchy
- Purposeful animations

### Professional Spacing
- 8px grid system
- Consistent margins and padding
- Visual rhythm and balance
- Proper alignment

### Subtle Animations
- Purpose-driven animations (not decorative)
- Smooth transitions (200-300ms)
- Easing curves for natural motion
- Reduced motion support

## Accessibility (WCAG)

### Keyboard Support
- All interactive elements focusable
- Visible focus indicators
- Logical tab order
- Keyboard shortcuts for common actions

### Proper Contrast
- 4.5:1 minimum for normal text
- 3:1 minimum for large text
- 3:1 for UI components
- Test with color blindness simulators

### Semantic HTML
- Proper heading hierarchy
- ARIA labels where needed
- Form labels and descriptions
- Error messages associated with fields

### Screen Reader Support
- Alt text for images
- ARIA live regions for dynamic content
- Skip navigation links
- Proper form announcements

## Responsive Design

### Mobile First
- Design for smallest screen first
- Progressive enhancement
- Touch-friendly targets (44x44px minimum)
- Viewport meta tag

### Tablet Optimized
- Adapted layouts for medium screens
- Touch and pointer support
- Optimized navigation patterns

### Desktop Optimized
- Full feature set available
- Keyboard shortcuts
- Multi-column layouts
- Hover states

## Component Architecture

### shadcn/ui Pattern
```tsx
// Composable primitives
<Button variant="outline" size="icon">
  <Icon />
</Button>

// Compound components
<Dialog>
  <DialogTrigger>Open</DialogTrigger>
  <DialogContent>
    <DialogHeader>
      <DialogTitle>Title</DialogTitle>
      <DialogDescription>Description</DialogDescription>
    </DialogHeader>
  </DialogContent>
</Dialog>
```

### Radix UI Primitives
- Unstyled, accessible components
- Customizable via styling solutions
- Keyboard navigation built-in
- Focus management handled

### Lucide Icons
- Consistent icon system
- SVG-based for scalability
- Tree-shakeable imports
- Consistent stroke width

## Default Design Stack

### Core
- React / Vue / Svelte
- TypeScript
- Tailwind CSS

### Components
- shadcn/ui (recommended)
- Radix UI (accessibility)
- Lucide Icons (icons)

### Animations
- Framer Motion (React)
- Magic UI (premium effects)
- CSS transitions (simple)

### Dashboards
- Tremor (data visualization)
- Origin UI (dashboard components)

## Quality Standards

### Visual Consistency
- Consistent color usage
- Typography system
- Spacing system
- Component variants

### Professional Appearance
- No placeholder content
- Real data examples
- Polished interactions
- Attention to detail

### Performance
- Optimized assets
- Lazy loading
- Minimal re-renders
- Efficient animations

## Integration Points

This document is referenced by:
- **brainstorming** - User experience considerations
- **writing-plans** - Frontend architecture planning
- **executing-plans** - UI implementation standards
- **exhaustive-audit** - UI/UX audit criteria
- **systematic-debugging** - UX problem investigation
- **test-driven-development** - UI testing patterns
- **subagent-driven-development** - UI/UX agent roles
- **requesting-code-review** - UI review criteria
- **verification-before-completion** - UI/UX verification
```

- [ ] **Step 3: Verify file creation**

```bash
ls -la "C:\Users\User1\.config\opencode\skills\ui-ux-design-principles"
```

Expected: SKILL.md file exists

- [ ] **Step 4: Commit**

```bash
git add skills/ui-ux-design-principles/SKILL.md
git commit -m "feat: add UI/UX design principles reference document"
```

---

## Task 2: Enhance Brainstorming Skill with UI/UX Considerations

**Files:**
- Modify: `C:\Users\User1\.config\opencode\skills\brainstorming\SKILL.md`

**Interfaces:**
- Consumes: ui-ux-design-principles (reference)
- Produces: Enhanced brainstorming with UI/UX focus

- [ ] **Step 1: Add UI/UX section to checklist (after line 26)**

Insert after "Ask clarifying questions" step:

```markdown
4. **Analyze user experience** — user goals, journeys, pain points, information architecture
```

- [ ] **Step 2: Add UI/UX questions section (after line 73)**

Insert after "Focus on understanding: purpose, constraints, success criteria":

```markdown
**UI/UX exploration:**

- What are the user's primary goals?
- What is the ideal user journey?
- What are the pain points in the current experience?
- How should information be organized?
- What navigation structure works best?
- What interface requirements exist?
- What visual direction is preferred?

Ask: "What is the best experience for the user?"
Not only: "What code should be written?"
```

- [ ] **Step 3: Add UI/UX to design section (after line 86)**

Insert after "Cover: architecture, components, data flow, error handling, testing":

```markdown
- Include: user experience, interface design, accessibility, responsive strategy
```

- [ ] **Step 4: Update visual companion section (line 146)**

Replace the visual companion section with enhanced UI/UX focus:

```markdown
**Offering the companion (just-in-time):** Do NOT offer it upfront. Wait until a question would genuinely be clearer shown than told — a real mockup / layout / diagram question, not merely a UI *topic*. The first time that happens, offer it then, as its own message:

> "This next part might be easier if I show you — I can put together mockups, diagrams, and comparisons in a browser tab as we go. It's still new and can be token-intensive. Want me to? I'll open it for you."

**This offer MUST be its own message.** Only the offer — no clarifying question, summary, or other content. Wait for the user's response. If they accept, start the server with `--open` so their browser opens to the first screen automatically. If they decline, continue text-only and don't offer again unless they raise it.

**Per-question decision:** Even after the user accepts, decide FOR EACH QUESTION whether to use the browser or the terminal. The test: **would the user understand this better by seeing it than reading it?**

- **Use the browser** for content that IS visual — mockups, wireframes, layout comparisons, architecture diagrams, side-by-side visual designs
- **Use the terminal** for content that is text — requirements questions, conceptual choices, tradeoff lists, A/B/C/D text options, scope decisions

A question about a UI topic is not automatically a visual question. "What does personality mean in this context?" is a conceptual question — use the terminal. "Which wizard layout works better?" is a visual question — use the browser.

If they agree to the companion, read the detailed guide before proceeding:
`skills/brainstorming/visual-companion.md`
```

- [ ] **Step 5: Add UI/UX to key principles (after line 140)**

Insert after "Be flexible - Go back and clarify when something doesn't make sense":

```markdown
- **User-centered design** - Always ask "What is the best experience for the user?"
- **Accessibility first** - Consider accessibility from the start, not as an afterthought
- **Responsive by default** - Design for all screen sizes
```

- [ ] **Step 6: Verify changes**

```bash
grep -n "UI/UX\|user experience\|accessibility\|responsive" skills/brainstorming/SKILL.md
```

Expected: Multiple matches showing UI/UX integration

- [ ] **Step 7: Commit**

```bash
git add skills/brainstorming/SKILL.md
git commit -m "feat: enhance brainstorming with UI/UX considerations"
```

---

## Task 3: Enhance Writing-Plans Skill with Frontend Architecture

**Files:**
- Modify: `C:\Users\User1\.config\opencode\skills\writing-plans\SKILL.md`

**Interfaces:**
- Consumes: ui-ux-design-principles (reference)
- Produces: Enhanced planning with frontend architecture

- [ ] **Step 1: Add frontend architecture section (after line 34)**

Insert after "This structure informs the task decomposition. Each task should produce self-contained changes that make sense independently.":

```markdown
## Frontend Architecture

When planning frontend or full-stack projects, include:

**Page structure:**
- Page hierarchy and routing
- Layout components (header, sidebar, footer)
- Content areas and sections
- Modal and overlay patterns

**Component hierarchy:**
- Atomic design principles (atoms, molecules, organisms)
- Shared vs page-specific components
- Component composition patterns
- State management approach

**Design system:**
- Color palette and tokens
- Typography scale
- Spacing system
- Component variants and states

**Responsive strategy:**
- Breakpoints and media queries
- Mobile-first approach
- Touch targets and interactions
- Layout adaptations

**Accessibility requirements:**
- WCAG compliance level
- Keyboard navigation
- Screen reader support
- Focus management

**Interaction patterns:**
- Form validation and feedback
- Loading states and skeletons
- Error handling and recovery
- Success confirmations

**Animation strategy:**
- Purpose-driven animations
- Performance considerations
- Reduced motion support
- Transition timing
```

- [ ] **Step 2: Add UI resources section (after line 142)**

Insert after "## Remember" section:

```markdown
## UI/UX Resources

When building React applications, reference these resources:

**Component Libraries:**
- shadcn/ui: https://github.com/shadcn-ui/ui
- Radix UI: https://github.com/radix-ui/primitives
- Lucide Icons: https://github.com/lucide-icons/lucide

**Premium Effects:**
- Magic UI: https://github.com/magicuidesign/magicui
- Aceternity UI: https://github.com/aceternity/ui

**Dashboards:**
- Origin UI: https://github.com/origin-space/originui
- Tremor: https://github.com/tremorlabs/tremor

**Accessibility:**
- Radix UI: https://github.com/radix-ui/primitives
- WCAG Guidelines: https://www.w3.org/WAI/WCAG21/quickref/
```

- [ ] **Step 3: Update plan header template (after line 77)**

Insert after "## Global Constraints" section in the header template:

```markdown
**Design System:** [UI component library, design tokens, accessibility level]

**Responsive Strategy:** [Mobile-first breakpoints, touch targets, layout approach]
```

- [ ] **Step 4: Add UI/UX to self-review (after line 153)**

Insert after "3. Type consistency" section:

```markdown
**4. UI/UX coverage:** Does the plan include frontend architecture, component hierarchy, design system, responsive strategy, and accessibility requirements? List any gaps.
```

- [ ] **Step 5: Verify changes**

```bash
grep -n "frontend architecture\|component hierarchy\|design system\|responsive\|accessibility" skills/writing-plans/SKILL.md
```

Expected: Multiple matches showing frontend architecture integration

- [ ] **Step 6: Commit**

```bash
git add skills/writing-plans/SKILL.md
git commit -m "feat: enhance writing-plans with frontend architecture"
```

---

## Task 4: Enhance Executing-Plans Skill with UI Standards

**Files:**
- Modify: `C:\Users\User1\.config\opencode\skills\executing-plans\SKILL.md`

**Interfaces:**
- Consumes: ui-ux-design-principles (reference)
- Produces: Enhanced execution with UI standards

- [ ] **Step 1: Add UI standards section (after line 30)**

Insert after "4. Mark as completed":

```markdown
**UI/UX Quality Checks:**
- Consistent spacing (8px grid)
- Clean layouts with proper whitespace
- Responsive design working on all breakpoints
- Accessibility: keyboard navigation, focus indicators, ARIA labels
- Loading states for async operations
- Error states with clear messaging
- Empty states with helpful guidance
- User feedback for all actions
```

- [ ] **Step 2: Add UI/UX to "Remember" section (after line 62)**

Insert after "Never start implementation on main/master branch without explicit user consent":

```markdown
- Follow UI/UX design principles from ui-ux-design-principles skill
- Maintain visual consistency across components
- Test responsive behavior on multiple screen sizes
- Verify accessibility with keyboard and screen reader
```

- [ ] **Step 3: Verify changes**

```bash
grep -n "UI/UX\|responsive\|accessibility\|consistent spacing" skills/executing-plans/SKILL.md
```

Expected: Multiple matches showing UI standards integration

- [ ] **Step 4: Commit**

```bash
git add skills/executing-plans/SKILL.md
git commit -m "feat: enhance executing-plans with UI standards"
```

---

## Task 5: Enhance Exhaustive-Audit Skill with UI/UX Audit

**Files:**
- Modify: `C:\Users\User1\.config\opencode\skills\exhaustive-audit\SKILL.md`

**Interfaces:**
- Consumes: ui-ux-design-principles (reference)
- Produces: Enhanced audit with UI/UX criteria

- [ ] **Step 1: Add UI/UX audit category (after line 152)**

Insert after "### 15. Pain Points" section:

```markdown
### 16. UI/UX Quality

**Visual Consistency:**
- Is there a consistent color system?
- Is typography consistent across pages?
- Are spacing and layout patterns consistent?
- Do components look like they belong to the same system?

**Layout Quality:**
- Are layouts clean and uncluttered?
- Is whitespace used effectively?
- Are elements properly aligned?
- Is visual hierarchy clear?

**Mobile Responsiveness:**
- Does the app work on mobile devices?
- Are touch targets large enough (44x44px)?
- Is content readable on small screens?
- Are interactions touch-friendly?

**Accessibility:**
- Can all features be accessed via keyboard?
- Are focus indicators visible?
- Do colors meet contrast requirements?
- Are forms properly labeled?

**User Flow Problems:**
- Are user journeys intuitive?
- Can users accomplish goals efficiently?
- Are there any dead ends or confusing paths?
- Is navigation clear and consistent?

**Navigation Problems:**
- Can users find what they're looking for?
- Is the navigation structure logical?
- Are there too many navigation levels?
- Is search functionality effective?

**Component Duplication:**
- Are similar components used consistently?
- Is there unnecessary component duplication?
- Can components be consolidated?
- Are design patterns applied consistently?

**Design Inconsistencies:**
- Do similar elements look different?
- Are there conflicting visual patterns?
- Is there a clear design language?
- Are there any visual surprises?
```

- [ ] **Step 2: Update investigation checklist count (line 35)**

Replace "You MUST complete all 15 categories" with:

```markdown
You MUST complete all 16 categories before presenting any summary. Skipping a category because it "seems obvious" or "not important" is a violation.
```

- [ ] **Step 3: Update output format (line 175)**

Replace "After all 15 categories" with:

```markdown
After all 16 categories
```

- [ ] **Step 4: Add UI/UX to anti-rationalization guards (after line 210)**

Insert after "I already know this codebase" row:

```markdown
| "UI/UX is just cosmetic" | UI/UX is a core engineering requirement. Check it. |
| "Accessibility is optional" | Accessibility is mandatory. Check it. |
| "Mobile can wait" | Mobile responsiveness is required. Check it. |
```

- [ ] **Step 5: Update scope rules (after line 221)**

Insert after "Check ALL scripts in package.json":

```markdown
- Check ALL UI/UX categories (visual consistency, layout, responsiveness, accessibility, user flows, navigation, component duplication, design inconsistencies)
```

- [ ] **Step 6: Verify changes**

```bash
grep -n "UI/UX\|accessibility\|responsive\|visual consistency" skills/exhaustive-audit/SKILL.md
```

Expected: Multiple matches showing UI/UX audit integration

- [ ] **Step 7: Commit**

```bash
git add skills/exhaustive-audit/SKILL.md
git commit -m "feat: enhance exhaustive-audit with UI/UX audit"
```

---

## Task 6: Enhance Systematic-Debugging Skill with UX Debugging

**Files:**
- Modify: `C:\Users\User1\.config\opencode\skills\systematic-debugging\SKILL.md`

**Interfaces:**
- Consumes: ui-ux-design-principles (reference)
- Produces: Enhanced debugging with UX investigation

- [ ] **Step 1: Add UX problems to "When to Use" (after line 39)**

Insert after "Integration issues":

```markdown
- User experience problems
- Confusing interactions
- Poor feedback
- Slow experiences
```

- [ ] **Step 2: Add UX investigation to Phase 1 (after line 109)**

Insert after "### Phase 2: Pattern Analysis" section:

```markdown
**UX Problem Investigation:**

When debugging frontend issues, investigate BOTH technical AND UX problems:

**Technical problems:**
- JavaScript errors
- Component errors
- API issues
- State management issues

**UX problems:**
- Broken user flows
- Confusing interactions
- Poor feedback
- Slow experiences
- Accessibility issues
- Responsive design problems

**UX debugging steps:**
1. Identify the user flow that's broken
2. Trace the interaction path
3. Find where the UX breaks down
4. Determine if it's a technical or design issue
5. Fix the root cause, not the symptom
```

- [ ] **Step 3: Add UX to Red Flags (after line 228)**

Insert after "Each fix reveals new problem in different place":

```markdown
- "UX doesn't matter, just fix the code"
- "Users can figure it out"
- "It's just a cosmetic issue"
```

- [ ] **Step 4: Add UX to Common Rationalizations (after line 256)**

Insert after "One more fix attempt (after 2+ failures)" row:

```markdown
| "UX is just cosmetic" | UX is a core engineering requirement. Broken UX = broken software. |
| "Users can figure it out" | If users can't figure it out, it's broken. Fix it. |
| "It's just a visual issue" | Visual issues affect usability. Fix them. |
```

- [ ] **Step 5: Add UX to Quick Reference (after line 265)**

Insert after the table:

```markdown
**UX Investigation:**
- Identify broken user flow
- Trace interaction path
- Find where UX breaks down
- Determine technical vs design issue
- Fix root cause
```

- [ ] **Step 6: Verify changes**

```bash
grep -n "UX\|user experience\|confusing interactions\|poor feedback" skills/systematic-debugging/SKILL.md
```

Expected: Multiple matches showing UX debugging integration

- [ ] **Step 7: Commit**

```bash
git add skills/systematic-debugging/SKILL.md
git commit -m "feat: enhance systematic-debugging with UX debugging"
```

---

## Task 7: Enhance Test-Driven-Development Skill with UI Testing

**Files:**
- Modify: `C:\Users\User1\.config\opencode\skills\test-driven-development\SKILL.md`

**Interfaces:**
- Consumes: ui-ux-design-principles (reference)
- Produces: Enhanced TDD with UI testing

- [ ] **Step 1: Add UI testing to "When to Use" (after line 28)**

Insert after "Configuration files":

```markdown
- User interface components
- User interactions
- Responsive behavior
- Accessibility compliance
```

- [ ] **Step 2: Add UI testing section (after line 371)**

Insert at end of file:

```markdown
## UI Testing Considerations

When testing frontend components, include:

**User Interactions:**
```typescript
test('button click triggers form submission', async () => {
  render(<LoginForm onSubmit={mockSubmit} />);
  fireEvent.click(screen.getByRole('button', { name: /submit/i }));
  expect(mockSubmit).toHaveBeenCalledWith(expect.any(Object));
});
```

**Forms:**
```typescript
test('validates required fields', async () => {
  render(<ContactForm />);
  fireEvent.click(screen.getByRole('button', { name: /submit/i }));
  expect(screen.getByText(/name is required/i)).toBeInTheDocument();
  expect(screen.getByText(/email is required/i)).toBeInTheDocument();
});
```

**Navigation:**
```typescript
test('navigation links work correctly', async () => {
  render(<App />, { wrapper: BrowserRouter });
  fireEvent.click(screen.getByRole('link', { name: /about/i }));
  expect(screen.getByText(/about page/i)).toBeInTheDocument();
});
```

**Responsive Behavior:**
```typescript
test('layout adapts to mobile viewport', async () => {
  global.innerWidth = 375;
  global.dispatchEvent(new Event('resize'));
  render(<Dashboard />);
  expect(screen.getByTestId('mobile-nav')).toBeInTheDocument();
  expect(screen.queryByTestId('desktop-nav')).not.toBeInTheDocument();
});
```

**Accessibility:**
```typescript
test('form is accessible', async () => {
  const { container } = render(<ContactForm />);
  const results = await axe(container);
  expect(results.violations).toHaveLength(0);
});
```

**Component States:**
```typescript
test('shows loading state while fetching', async () => {
  render(<UserProfile userId="123" />);
  expect(screen.getByText(/loading/i)).toBeInTheDocument();
  await waitFor(() => {
    expect(screen.getByText(/user name/i)).toBeInTheDocument();
  });
});
```

## UI Testing Checklist

Before marking frontend work complete:

- [ ] User interactions tested
- [ ] Form validation tested
- [ ] Navigation tested
- [ ] Responsive behavior tested
- [ ] Accessibility tested (keyboard, screen reader)
- [ ] Loading states tested
- [ ] Error states tested
- [ ] Empty states tested
```

- [ ] **Step 3: Verify changes**

```bash
grep -n "UI testing\|user interactions\|responsive\|accessibility" skills/test-driven-development/SKILL.md
```

Expected: Multiple matches showing UI testing integration

- [ ] **Step 4: Commit**

```bash
git add skills/test-driven-development/SKILL.md
git commit -m "feat: enhance test-driven-development with UI testing"
```

---

## Task 8: Enhance Subagent-Driven-Development Skill with UI/UX Agent

**Files:**
- Modify: `C:\Users\User1\.config\opencode\skills\subagent-driven-development\SKILL.md`

**Interfaces:**
- Consumes: ui-ux-design-principles (reference)
- Produces: Enhanced SDD with UI/UX agent roles

- [ ] **Step 1: Add UI/UX agent to process diagram (after line 83)**

Insert after the process diagram:

```markdown
**UI/UX Agent Division:**

When possible, divide large frontend projects into specialized agents:

- **Agent 1: UI/UX Architecture** - Page structure, component hierarchy, design system, responsive strategy
- **Agent 2: Frontend Components** - Component implementation, styling, interactions
- **Agent 3: Backend/API** - Data fetching, state management, business logic
- **Agent 4: Database** - Schema, migrations, queries (if applicable)
- **Agent 5: Testing & QA** - Unit tests, integration tests, accessibility tests
```

- [ ] **Step 2: Add UI/UX to reviewer prompt (after line 270)**

Insert after "Final whole-branch review: use superpowers:requesting-code-review's code-reviewer.md":

```markdown
- **UI/UX Review:** Include UI/UX criteria in task reviews:
  - Design consistency
  - UX quality
  - Accessibility
  - Responsive behavior
  - Component reuse
```

- [ ] **Step 3: Add UI/UX to Red Flags (after line 389)**

Insert after "Re-dispatch a task the progress ledger already marks complete":

```markdown
- Skip UI/UX review on frontend tasks
- Ignore accessibility issues
- Dismiss responsive design problems as "cosmetic"
```

- [ ] **Step 4: Verify changes**

```bash
grep -n "UI/UX\|accessibility\|responsive\|design consistency" skills/subagent-driven-development/SKILL.md
```

Expected: Multiple matches showing UI/UX agent integration

- [ ] **Step 5: Commit**

```bash
git add skills/subagent-driven-development/SKILL.md
git commit -m "feat: enhance subagent-driven-development with UI/UX agent"
```

---

## Task 9: Enhance Requesting-Code-Review Skill with UI Review

**Files:**
- Modify: `C:\Users\User1\.config\opencode\skills\requesting-code-review\SKILL.md`
- Modify: `C:\Users\User1\.config\opencode\skills\requesting-code-review\code-reviewer.md`

**Interfaces:**
- Consumes: ui-ux-design-principles (reference)
- Produces: Enhanced code review with UI criteria

- [ ] **Step 1: Add UI review to "When to Request Review" (after line 22)**

Insert after "After fixing complex bug":

```markdown
- After implementing UI components
- After responsive design changes
- After accessibility improvements
```

- [ ] **Step 2: Add UI review section to code-reviewer.md (after line 67)**

Insert after "**Production readiness:**" section:

```markdown
    **UI/UX quality:**
    - Design consistency with existing components?
    - Responsive behavior on all breakpoints?
    - Accessibility: keyboard navigation, focus indicators, ARIA labels?
    - Loading, error, and empty states handled?
    - Visual hierarchy clear and intuitive?
    - Component reuse over duplication?
    - Animations purposeful and performant?
```

- [ ] **Step 3: Add UI/UX to output format (after line 101)**

Insert after "### Recommendations" section:

```markdown
    ### UI/UX Assessment

    **Design Consistency:** [Consistent | Inconsistent | Needs Improvement]

    **Accessibility:** [Compliant | Partially Compliant | Non-Compliant]

    **Responsive Behavior:** [Works on all devices | Issues on specific devices]

    **Recommendations:**
    - [UI/UX specific improvements]
```

- [ ] **Step 4: Add UI/UX to Critical Rules (after line 125)**

Insert after "**DON'T:**" section:

```markdown
    **UI/UX REVIEW:**
    - Check design consistency with existing components
    - Verify responsive behavior on mobile, tablet, desktop
    - Test keyboard navigation and focus indicators
    - Verify accessibility with screen reader (if possible)
    - Check loading, error, and empty states
    - Verify visual hierarchy and layout
```

- [ ] **Step 5: Verify changes**

```bash
grep -n "UI/UX\|design consistency\|accessibility\|responsive" skills/requesting-code-review/SKILL.md skills/requesting-code-review/code-reviewer.md
```

Expected: Multiple matches showing UI review integration

- [ ] **Step 6: Commit**

```bash
git add skills/requesting-code-review/SKILL.md skills/requesting-code-review/code-reviewer.md
git commit -m "feat: enhance requesting-code-review with UI review"
```

---

## Task 10: Enhance Verification-Before-Completion Skill with UI/UX Verification

**Files:**
- Modify: `C:\Users\User1\.config\opencode\skills\verification-before-completion\SKILL.md`

**Interfaces:**
- Consumes: ui-ux-design-principles (reference)
- Produces: Enhanced verification with UI/UX checks

- [ ] **Step 1: Add UI/UX verification to Common Failures (after line 50)**

Insert after "Requirements met" row:

```markdown
| UI responsive | Test on mobile, tablet, desktop | Only tested on one screen size |
| UI accessible | Keyboard + screen reader test | Visual inspection only |
| UI consistent | Compare with design system | Component looks different |
| UX intuitive | User flow test | Developer assumes it's obvious |
```

- [ ] **Step 2: Add UI/UX verification section (after line 106)**

Insert at end of file:

```markdown
## UI/UX Verification

Before claiming frontend work is complete, verify:

**Functionality:**
```bash
# Run all tests
npm test
# Expected: All tests pass
```

**UI Verification:**
```bash
# Check responsive design
# Test on mobile (375px), tablet (768px), desktop (1280px)
# Verify touch targets are 44x44px minimum
# Check color contrast ratios
```

**UX Verification:**
```bash
# Test user flow end-to-end
# Verify all interactions provide feedback
# Check loading states exist
# Verify error states exist
# Check empty states exist
```

**Accessibility Verification:**
```bash
# Test keyboard navigation
# Verify focus indicators visible
# Check ARIA labels present
# Test with screen reader (if available)
# Run axe accessibility check
```

**Visual Consistency:**
```bash
# Compare with design system
# Check spacing (8px grid)
# Verify colors match tokens
# Check typography scale
```

## UI/UX Verification Checklist

Before claiming frontend work complete:

- [ ] All tests pass
- [ ] Responsive on mobile, tablet, desktop
- [ ] Keyboard navigation works
- [ ] Focus indicators visible
- [ ] ARIA labels present
- [ ] Loading states exist
- [ ] Error states exist
- [ ] Empty states exist
- [ ] Visual consistency with design system
- [ ] Accessibility check passes (axe)

Can't check all boxes? You haven't verified UI/UX. Don't claim completion.
```

- [ ] **Step 3: Verify changes**

```bash
grep -n "UI/UX\|responsive\|accessibility\|visual consistency" skills/verification-before-completion/SKILL.md
```

Expected: Multiple matches showing UI/UX verification integration

- [ ] **Step 4: Commit**

```bash
git add skills/verification-before-completion/SKILL.md
git commit -m "feat: enhance verification-before-completion with UI/UX verification"
```

---

## Task 11: Final Verification and Documentation

**Files:**
- Verify all skill modifications
- Update any cross-references
- Test skill discovery

**Interfaces:**
- Consumes: All modified skills
- Produces: Verified integration

- [ ] **Step 1: Verify all skills have UI/UX content**

```bash
for skill in brainstorming writing-plans executing-plans exhaustive-audit systematic-debugging test-driven-development subagent-driven-development requesting-code-review verification-before-completion; do
  echo "=== $skill ==="
  grep -c "UI/UX\|user experience\|accessibility\|responsive" "skills/$skill/SKILL.md"
done
```

Expected: Each skill shows at least 1 match

- [ ] **Step 2: Verify UI/UX principles reference exists**

```bash
ls -la skills/ui-ux-design-principles/SKILL.md
```

Expected: File exists

- [ ] **Step 3: Test skill discovery**

```bash
grep -l "UI/UX" skills/*/SKILL.md
```

Expected: All enhanced skills listed

- [ ] **Step 4: Update any README or documentation (if exists)**

```bash
# Check for README files that might need updating
ls -la skills/README.md docs/README.md 2>/dev/null || echo "No README found"
```

- [ ] **Step 5: Final commit**

```bash
git add -A
git commit -m "feat: complete UI/UX integration across Superpowers skills"
```

---

## Summary

This plan enhances 9 existing skills with UI/UX capabilities:

1. **brainstorming** - User goals, journeys, UX problems, information architecture
2. **writing-plans** - Frontend architecture, component hierarchy, design system, responsive strategy
3. **executing-plans** - Professional UI standards, consistent spacing, responsive design
4. **exhaustive-audit** - UI/UX audit checklist (16th category)
5. **systematic-debugging** - UX problem investigation alongside technical debugging
6. **test-driven-development** - UI testing patterns for interactions, forms, navigation
7. **subagent-driven-development** - UI/UX agent roles for large projects
8. **requesting-code-review** - UI review criteria in code review
9. **verification-before-completion** - UI/UX verification before claiming completion

Additionally, creates a shared **ui-ux-design-principles** reference document.

**Key Principles Applied:**
- UI/UX is a core engineering requirement, not decoration
- Accessibility is mandatory, not optional
- Responsive design is required for all screen sizes
- Visual consistency through design systems
- User-centered design approach
- Professional quality standards
