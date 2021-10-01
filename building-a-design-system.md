# Building a Design System

It all starts with a brand.
Don't be just a name. A name is not a brand.
If a name makes a promise and lives up to that promise, THEN it's a brand.

Design System - Pattern Library - Style Guide: each of these are actually different things.

A design system is a living system of guidelines, reusable code and design assets, and tools that helps orangizations deliver consistent, on-brand expreriences at scale and over time.

COGNITIVE LOAD on consumers if we don't have a consistent design system.

Ask yourself: What are you trying to solve?

### Documenting the Design System

- Identify Principles and Goals
- Identify Design and UI Standards
  - Performance
  - Acessibility
  - Technical Considerations
  - SEO
  - Iconography
  - Internationalization / Localization

DOCUMENT AS YOU GO!!!

The overall objective is to make design decisions and stick with them!

"Creativity thrives under intelligent constraints." -- Carmine Gallo Talk Like TED

The measure of a successful design system is how well it is adopted. FLexible - Reliable - Easy to use is a venn diagram.

## Pattern Library

And organized set of related and reusable values, functions, and components, often containing code examples, design guidelines, coding standards, and use cases which are designed

### Basic Patterns

Atoms -> Molecules -> (Needs completed)

Pages -> Layouts -> COmponents -> Elements -> Design Tokens

## Deisgn Tokens

- color
  -animations
  -spacing
  -font sizes
- media queries
- z-indexs
  -shapes and borders
  -shadows

## Naming Conventions

- Kepp color names generic ('primary', 'secondary', 'warning', etc)
- Same with fonts ("base", "accent", "monospace")
- Keep sizes generic ("xs", "sm", "md", "lg", etc)

## Make them Easy to USe

- JSON / SASS / CSS Variables
- Mixins/FUnctions
- Utility Classes
- Document how and when to use utility classes

Anything that need sthemed should be SASS, layout type stuff can be utility classes

### Elements

- CSS Reset
- Sytle your elements using your design tokens

### COmponents

- Reusable
- Configurable
- Replaceable
- Context Agnostic
  - Doesn't care where it is in the site.
- Encapsulated
  - Style doesn't leak our of the component
- Dumb Components

### Layout and Pages

- These are composed of design system elements, but are not typically part of the design system itself.

### Design Tools

- Figma
- Adobe XD
- Sketch

## Some technical Considerations

- Web components and Stencil (A compiler for web components)
- Lightning Design system by salesforce
- Storybook

## Where do I Start?

### 5 Fundamental Questions of UX

- Who are my users?
- What problems are we trying to solve?
- How can we help them solve those problems?
- what do we want them to do?
- how do we incentivize them to do it?

### Starting From Scratch

- Low fidelity markup
- Build User experience first
- If you don't need it, don't build it!

### Starting with an existing Application

-- cssstats.com

### UI Audit

- Identify the key customer journeys (happy path)
- Perform a UI Audit
- Identify Patterns
- Consolidate and create consistency

### Names are Important

- Modal - Toast - Tooltip could all be called popup, but that would not help if someone asked you to create a popup without context.

## Define your Do's and Don't(s)

## Define the configuration (e.g. PropTypes)

# Style Guide is not a Brand Guid

- Style guide might have more specific or more broad options than a brand guide, and may not even match up
- For instance, a brand color may not work well on websites.

### Style Guide

- Brand Decisions
  - Anser 5 UX questions
  - Voice and tone
  - Aestetics
  - Graphics, Images, and Logos
- Design Token Implementation
  - Color
  - Animcations
  - Typography
  - Fonts
  - Font Sizes
  - Medi Queries
  - Spcing
  - Shapes and Borders
  - Shadows
