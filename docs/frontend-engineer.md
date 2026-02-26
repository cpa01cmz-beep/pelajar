# Frontend Engineer Domain

## Overview
Frontend-engineer specialist handles all client-side code, UI/UX implementation, and browser-based functionality for the Santri/Pelajar application.

## Tech Stack Recommendations
- **Framework**: Next.js (React-based, serverless-friendly)
- **Styling**: Tailwind CSS
- **State Management**: React Context / Zustand
- **Build Tool**: Vercel (deployment target)
- **Language**: TypeScript

## Core Responsibilities

### 1. UI/UX Implementation
- Pixel-perfect implementation from designs
- Responsive design across all breakpoints
- Accessibility (WCAG 2.1 AA compliance)
- Performance optimization (Core Web Vitals)

### 2. Component Architecture
- Reusable component library
- Atomic design principles
- Proper component composition
- Type-safe props and state

### 3. Code Quality
- Strict TypeScript usage
- ESLint + Prettier configuration
- Zero console warnings
- Proper error boundaries

### 4. Performance
- Code splitting / lazy loading
- Image optimization
- Bundle size monitoring
- SSR/SSG optimization where appropriate

## Best Practices

### Component Structure
```
src/
├── components/
│   ├── ui/          # Base UI components
│   ├── features/    # Feature-specific components
│   └── layouts/     # Layout components
├── hooks/           # Custom React hooks
├── lib/             # Utilities
├── pages/           # Next.js pages
└── styles/          # Global styles
```

### Naming Conventions
- Components: PascalCase (e.g., `UserProfile.tsx`)
- Hooks: camelCase with `use` prefix (e.g., `useAuth.ts`)
- Utils: camelCase (e.g., `formatDate.ts`)
- Types: PascalCase (e.g., `UserType.ts`)

### Git Workflow
- Feature branches: `feat/frontend/<description>`
- Bug fixes: `fix/frontend/<description>`
- PR labels: `frontend-engineer`

## Common Issues to Watch

### Security
- XSS vulnerabilities in user-generated content
- Sensitive data in client-side code
- Improper CORS configuration

### Performance
- Large bundle sizes
- Unnecessary re-renders
- Missing memoization
- Blocking main thread

### Accessibility
- Missing alt text
- Poor color contrast
- Missing ARIA labels
- Keyboard navigation issues

## Definition of Done
- [ ] Code follows project conventions
- [ ] TypeScript strict mode passes
- [ ] No lint errors/warnings
- [ ] Responsive on mobile/tablet/desktop
- [ ] Accessibility check passes
- [ ] Tests added for critical paths
- [ ] PR linked to issue (if applicable)

## Collaboration
- Coordinate with UI-UX for design implementation
- Coordinate with Backend for API integration
- Coordinate with QA for testing requirements
