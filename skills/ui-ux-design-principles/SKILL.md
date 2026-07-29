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

## Emil Kowalski Design Engineering Skills

For deep animation and motion work, use Emil Kowalski's specialized skills:

| Skill | Purpose | When to Use |
|-------|---------|-------------|
| `emil-design-eng` | Core design engineering philosophy | Building UI components, reviewing UI code |
| `review-animations` | Strict animation code review | After implementing animations |
| `improve-animations` | Codebase-wide animation audit | When animations feel off across a project |
| `find-animation-opportunities` | Discover animation moments | When UI feels static or jarring |
| `animation-vocabulary` | Name motion effects | When you need the right term for an effect |
| `apple-design` | Apple's design philosophy | Building gesture-driven, spring-based UI |
| `pick-ui-library` | Curated library picks | Choosing frontend dependencies |
| `prototype` | Build UI variant explorations | Exploring design directions |

**Key distinction:** This document (`ui-ux-design-principles`) provides general UI/UX standards. Emil's skills provide specialized, craft-level guidance on animation, motion, and design engineering details. Use both together for comprehensive frontend quality.
