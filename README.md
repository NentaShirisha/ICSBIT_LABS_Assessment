# GridWatch OT - Dashboard & Attack Path Design

This is my submission for the Frontend + UX Design Challenge (Industrial Cybersecurity Platform).



I built this as a clickable prototype instead of static screens so the interactions (drill-downs,
node selection, filters, path highlighting) could actually be tried out rather than just described.
Open the link above to click through it - the raw files in `project/` are the source but they
won't display properly if you just open them as plain HTML in a browser, since they depend on the
platform they were built in.

## What I made

- **Main.dc.html** - the main dashboard. KPI row at the top (the two red/orange ones are meant to
  draw the eye first since they're the "needs attention now" numbers), then risk & findings, the
  attack path preview card, sensor/platform health, a change timeline, asset breakdown and a small
  topology view. Clicking a KPI expands a drawer under it with the actual assets/findings behind
  that number.
- **AttackPath.dc.html** - the investigation workspace. There are 3 example paths, the highest
  severity one is highlighted by default and the other two are dimmed instead of hidden. Clicking
  any node or edge opens a side panel with the details required in the brief (summary, why it
  matters, evidence, related findings, protocol context, recommended steps). There's a collapsed
  "+34 more assets" node for blast radius so the graph doesn't get overwhelming, and it expands
  when you toggle it. Zoom/fit and severity/confidence filters are also functional.
- **States.dc.html** - a gallery of the different states asked for in the brief (normal, high-risk,
  degraded data, uncertain/low-confidence, empty, large data volume, partial data, action feedback).
- **Tokens.dc.html** - the colours, type scale, buttons/badges and the node/edge legend so the
  design stays consistent if it were extended.
- **Rationale.dc.html** - my write-up covering what I prioritised and why, how the dashboard works
  for both leadership and analysts, how I tried to keep the attack path graph from becoming
  overwhelming, how uncertainty/missing data is shown, how it would scale, and the assumptions I
  made since a lot of the real product details were intentionally left out of the brief.

## Notes on scope

Given the timebox, some things are more "demonstrated" than fully wired - the search box inside the
graph and the mini-map are shown as real UI but aren't functionally connected to anything. Everything
else described above (KPI drill-downs, node/edge selection, path emphasis, blast radius expand,
filters, zoom) is actually working state in the prototype, not just a picture of it. I go into more
detail on this, plus what I'd build next with more time, in the rationale page.

Colours/asset names/CVEs/timestamps are all made up for the purpose of the exercise, and "GridWatch"
is just a placeholder name I used, not a real product name.
