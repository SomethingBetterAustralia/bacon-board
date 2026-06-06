# Target architecture

Not yet decided — to be defined by the contributing devs, open to community consultation.

For reference, the Something Better Australia **website** repo uses Vite + React + TypeScript + Tailwind v4 (shadcn-style components) on the frontend with an Express + TypeScript backend. This project is looking for **complementary** stacks rather than assuming the same one — proposals welcome.

When the shape of the project is settled, document it here:

## Shape

- Packages / top-level layout
- How the pieces talk to each other (APIs, shared types, etc.)
- Ports / environment configuration

## Layering

- Where each kind of module belongs as the codebase grows

## Stage of life

Early. Mocks are first-class — when an external dependency isn't ready yet, mock it with a `MOCK:` marker and move on. Backwards-compat shims are not allowed; when a contract changes, update all call sites in the same change.
