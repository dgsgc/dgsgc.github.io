# Shared design

One look for every tool: [suite.css](suite.css) is the master copy of the colours, font, corners,
buttons, labels and title style. Each tool copies it into its own stylesheet (they all have to
work without the internet), so change it here first and then copy it on.

- **Dark** everywhere; the planner also has the light version when the computer is in light mode.
  The monitor's screens stay dark, with their red Night mode.
- **Each tool has its own green:** the monitor `#4fb06d`, the planner teal `#3bb3a1`. It's used for
  the tool's icon, its title, its main buttons and focus rings. Everything else is neutral.
- **Guiding levels** (OK, warn, alert, RA, Dec) are the same on the web page, the morning report
  and the ESP32 display.
- **Font:** the computer's own. 15 px on app screens, 17 px on web pages.
- **Corners:** 12 px for cards, 8 px for buttons and fields, round for chips.
- **Buttons:** `.btn.main` (filled, the tool's colour), `.btn` (dark with an outline), `.btn.quiet`.
- **Labels:** small capitals (`.label`) for card and section headings.
- **Title icons:** simple line icons in the tool's colour, next to its name.

## Icons

Astro Rig Monitor, a crosshair:

```html
<svg viewBox="0 0 32 32" aria-hidden="true"><circle cx="16" cy="16" r="11" fill="none" stroke="currentColor" stroke-width="3"/><path d="M16 2v8M16 22v8M2 16h8M22 16h8" stroke="currentColor" stroke-width="3"/></svg>
```

ASIAIR Mosaic Planner, two overlapping frames:

```html
<svg viewBox="0 0 32 32" aria-hidden="true"><rect x="4" y="6" width="14" height="11" rx="1.5" fill="none" stroke="currentColor" stroke-width="2.6"/><rect x="14" y="15" width="14" height="11" rx="1.5" fill="none" stroke="currentColor" stroke-width="2.6"/></svg>
```

Set `color` to the tool's colour (`color: var(--accent)`). The Mac app icons stay as they are.
