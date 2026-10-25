# Polaroid Line Carousel & React/shadcn Setup

This folder contains the React / TypeScript component version of the Hanging Polaroid Image Carousel:
- `components/ui/polaroid-line-carousel.tsx`
- `components/ui/demo.tsx`

## Why `/components/ui`?
In modern React / Next.js ecosystems utilizing `shadcn/ui`, `/components/ui` is the standardized convention for atomic, reusable UI components. Configuring the `components.json` alias to `@/components/ui` enables:
1. Seamless integration with the shadcn CLI (`npx shadcn@latest add ...`).
2. Automatic resolution of path aliases configured in `tsconfig.json`.
3. Clear separation of pure visual UI primitives from feature-specific compound views.

## Setting Up in a React / Next.js / Tailwind Project

1. **Initialize Tailwind & TypeScript** (if starting fresh):
   ```bash
   npx create-next-app@latest my-app --typescript --tailwind --eslint
   cd my-app
   ```

2. **Initialize shadcn/ui**:
   ```bash
   npx shadcn@latest init
   ```
   Select:
   - Style: Default / New York
   - Base color: Slate / Zinc
   - CSS variables: Yes
   - Components alias: `@/components/ui`

3. **Install Lucide Icons (optional)**:
   ```bash
   npm install lucide-react
   ```

4. **Add the Component**:
   Place `polaroid-line-carousel.tsx` into `components/ui/` and import it into your page or feature component.

---

*Note: For the current production Kumaran Elite Travels website, this component has been natively ported to pure, high-performance vanilla JavaScript and CSS directly within `index.html` and `home.css`. This ensures zero bundle overhead, instantaneous loading without Node build steps, and full compatibility with the existing static architecture.*
