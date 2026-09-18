# GridWatch OT — Frontend + UX Design Challenge

Submission for: **Frontend + UX Design Challenge — Industrial Cybersecurity Platform**
(`Frontend_UX_Design_Challenge_OT_Security.pdf`, in the parent folder)

## View the prototype

Live, clickable prototype: **https://claude.ai/artifact/UePVuuL5Zy1duYojbDTpMD**

The prototype is a private link. If you need to share it with someone else, open it and use the
page's own **Share** menu — this repo copy does not change that.

> The `.dc.html` files in `project/` are the raw source of that prototype. They depend on a
> runtime (`support.js`) and a design-canvas engine injected by the artifact platform when the
> page is opened there — opening them as plain local HTML files will **not** render the styled,
> interactive experience. They're kept here as the source of record alongside the brief, not as
> a standalone app. Use the link above to actually view and click through the design.

## What's included

| Screen | File | Covers |
|---|---|---|
| A. Main Dashboard | `project/Main.dc.html` | Posture KPI strip with real drill-down drawers, filter bar (time range, severity, site/zone), risk & findings, attack-path preview, platform/sensor health, recent change timeline, asset visibility, network/topology insight |
| B. Attack Path Map | `project/AttackPath.dc.html` | Interactive graph workspace: ranked paths, click-to-select nodes/edges, investigation side panel, blast-radius expand, single-path vs. all-paths toggle, severity/confidence filtering, zoom/fit controls, always-visible legend |
| C. States Gallery | `project/States.dc.html` | The 8 required functional states (Normal, High-risk, Degraded, Unknown/Uncertain, Empty, Large volume, Partial data, Action feedback) |
| D. Components & Tokens | `project/Tokens.dc.html` | Colour tokens (brand + severity), typography scale, buttons, badges, spacing/radius scale, graph node/edge semantics |
| E. Design Rationale | `project/Rationale.dc.html` | Written rationale — required by brief §8.1 |
| — | `project/canvas.json` | Canvas layout index (artboard positions/sizes) for the design-canvas platform |
| — | `shared-styles.css` | Shared stylesheet (design tokens + component classes) used by every screen |

## Design summary

- **Palette:** required Orange / Black / White base, plus a severity ramp (Critical/High/Medium/Low)
  and status colours (Good, Unknown) — every status is paired with an icon and/or text label, never
  colour alone.
- **Typography:** IBM Plex Sans for UI text, IBM Plex Mono for identifiers, IPs, CVEs and other data
  values.
- **Visual system:** light neutral surface for the dense dashboard content; dark chrome + dark
  investigation canvas for the Attack Path Map, which is the common enterprise-security convention
  for long graph-reading sessions and improves edge/line legibility.
- **Interaction depth:** KPI drill-downs, filter chips, and the attack-path graph (node/edge
  selection, path emphasis, blast-radius expand, zoom) are wired to real component state — this is a
  working interactive prototype, not static comps. Scope limits (mini-map viewport sync, live text
  search in the graph) are called out explicitly in the Design Rationale screen.

## Assumptions

See the **Design Rationale** screen (`project/Rationale.dc.html`, section 6) for the full list —
in short: all names/counts/CVEs/timestamps are illustrative, "GridWatch" is a placeholder product
name, and the design is desktop-first at 1440px per the brief's explicit allowance.
