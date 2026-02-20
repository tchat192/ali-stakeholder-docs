# Nic Touch-Base: Figma-to-Code Workflow
## December 3, 2025 | 5-minute prep guide

---

## 🎯 MEETING GOAL
Align on what I need from Nic to efficiently translate Figma designs to code going forward.

---

## PART 1: WHAT WE HAVE (Current State)

### Design Tokens Extracted ✅
- **218 tokens** pulled from "Ali Assessment V2" Figma file
- Stored in: `docs/design-tokens.json`
- Includes: colors, spacing, typography, animations, shadows, border-radius

**Sample tokens:**
| Category | Example | Value |
|----------|---------|-------|
| Brand Purple | `--brand-purple` | `#8b5cf6` |
| Spacing MD | `--spacing-md` | `16px` |
| Font Base | `--font-size-base` | `16px` |
| Duration Base | `--duration-base` | `300ms` |

### Fonts Currently in App
| Font | Status | Location |
|------|--------|----------|
| **Satoshi** | ✅ Installed (all weights) | `public/fonts/` |
| **Metro Sans** | ⚠️ In docs only, NOT in app | `docs/fonts/` |
| **Moret** | ⚠️ In docs only (Product Brief) | `docs/fonts/` |

### Figma MCP Integration ✅
**How it works:** I can point Claude at any Figma frame and it:
1. Extracts the design context (structure, colors, spacing)
2. Pulls variable definitions (design tokens)
3. Takes screenshots for visual reference
4. Generates React/CSS code suggestions

**What I need from Nic:** The Figma file URL or node IDs for specific frames

---

## PART 2: SCREENS WE HAVE (App Structure)

| Screen | File | Design Status |
|--------|------|---------------|
| **Chat Page** | `src/chatbot/ChatPageSimple.tsx` | ⚠️ Need design review |
| **Assessment** | `src/assessment/AssessmentPage.tsx` | ⚠️ Need design specs |
| **Results Page** | `src/assessment/ResultsPage.tsx` | ⚠️ Need design specs |
| **Landing Page** | `src/landing-page/LandingPage.tsx` | ⚠️ Need design specs |
| **NavBar** | `src/client/components/NavBar/NavBar.tsx` | ✅ Recently updated |
| **Login/Signup** | `src/auth/` | ⚠️ Need design specs |
| **Dashboard** | `src/dashboard/Dashboard.tsx` | ⚠️ Need design specs |

---

## PART 3: WHAT I NEED FROM NIC

### 1. Figma File Access
**Question:** "Can you share the Figma file URL so I can use the Figma MCP to pull designs directly?"

The format I need:
```
https://figma.com/design/[FILE_KEY]/[FILE_NAME]?node-id=[NODE_ID]
```

### 2. Priority Screens to Design
**Which screens are highest priority for design completion?**
- [ ] Chat interface (main product experience)
- [ ] Assessment flow (70-question Silhouette)
- [ ] Results page (personality reveal)
- [ ] Landing page (first impression)

### 3. Font Files Needed
**Question:** "What fonts should the app use? I have Satoshi installed but see Metro Sans and Moret in some designs."

**Preferred format:** `.woff2` (best compression + browser support)

If custom fonts needed:
- [ ] Export as `.woff2` + `.woff` fallback
- [ ] Include all weights we'll use (Regular, Medium, Bold at minimum)
- [ ] Provide font-family CSS recommendations

### 4. Component Specifications
For each major component, I need:
- [ ] Exact colors (hex or Figma variable names)
- [ ] Spacing values (px or use design tokens)
- [ ] Typography (font, size, weight, line-height)
- [ ] States (default, hover, active, disabled)
- [ ] Responsive breakpoints (if different from desktop)

### 5. Asset Exports
**Question:** "Are there any icons, illustrations, or images I should export from Figma?"

Preferred formats:
- Icons: **SVG** (scalable, can be colored via CSS)
- Images: **PNG** or **WebP** (with 2x for retina)
- Logos: **SVG**

---

## PART 4: HOW WE'LL WORK TOGETHER

### My Workflow (with Figma MCP)
1. Nic designs in Figma → marks frame ready
2. Nic shares Figma URL or node ID
3. I use Figma MCP to extract:
   - Design context (structure)
   - Variables (tokens)
   - Screenshot (reference)
4. I implement in React + Tailwind/CSS
5. I share screenshot or staging link for review
6. Nic provides feedback → iterate

### Handoff Checklist Per Screen
When a screen is "ready for dev":
- [ ] All components in Figma use design system variables
- [ ] States are designed (hover, active, disabled, error, loading)
- [ ] Responsive variations marked (if applicable)
- [ ] Figma URL/node-id shared with me
- [ ] Any custom assets exported

---

## QUICK REFERENCE

### Figma MCP Commands I Can Use
```
- get_design_context → Extracts structure + code suggestions
- get_variable_defs → Pulls design tokens
- get_screenshot → Visual reference
- get_metadata → Node structure overview
```

### Current Design Token Categories
- Colors: Brand (purple, green, gray, gold), Animation, Opacity
- Spacing: xs(4px) → 5xl(128px)
- Border Radius: sm(4px) → full(9999px)
- Typography: Size, Weight, Line Height
- Animation: Durations, Easings
- Shadows: sm, md, lg, xl, focus variants

---

## ACTION ITEMS TO CAPTURE

After meeting, confirm:
1. [ ] Figma file URL shared
2. [ ] Priority screens identified
3. [ ] Font decision made (Satoshi only? + Metro Sans? + Moret?)
4. [ ] First screen to implement together
5. [ ] Communication channel for async feedback (Slack? Figma comments?)

---

*Meeting prep generated Dec 3, 2025*
