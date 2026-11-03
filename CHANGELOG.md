# Changelog

All notable changes to this theme. The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [1.1.1] - 2026-11-02

### Added

- The theme defines the chart colour tokens the Stats plugin reads.

## [1.1.0] - 2026-11-02

### Changed

- The base text size is 16px, up from 14px. It is the token `--theme-font-size`.
- List text is 14px, up from 11.4px. The sidebar is 14px, up from 12.3px. Fields and buttons are 15px, up from 13.3px.
- Labels, chips, headings, the header and the action buttons grew in the same proportion.
- `--theme-font` starts with Noto Sans and `--theme-font-monospace` with Noto Sans Mono, before the system fonts.
- Chips in the issue list, the action buttons and the label column of the issue page grow with the text.
- In a tight issue list, a date and its time stack on two lines, and cells have 10px of padding at each side, down from 12px.
- The right-hand sidebar is 216px wide, down from 232px, so the issue list fits beside it at 1280px.
- From 900px to 1179px the project switcher is 176px wide and the search field 100px, so the switcher's text fits.

### Added

- The theme ships Noto Sans for text and Noto Sans Mono for code, as woff2 files in `opal/fonts/`, so nothing is loaded from another site.
- The font files are under the SIL Open Font License 1.1, and the licence texts are in `opal/fonts/`.

## [1.0.1] - 2026-11-02

### Fixed

- Overdue due dates in issue lists keep enough contrast on striped and hovered rows.
- On a phone, the administration links no longer show through the slide-out menu.

## [1.0.0] - 2026-11-02

### Added

- The theme: an off-white page with white panels, a blue-teal primary, and a lilac and peach wash on the header, the focus rings
  and the primary button. Every colour, corner, font and a few sizes are tokens in `opal/stylesheets/tokens.css`, with
  names that start with `--theme-` and are the same in every Rubylode theme.
- A two-row header: the mark, the global links, the search, the project switcher and the avatar on top; the project name, the tabs
  and the "+" menu below. The Rubylode New issue button plugin's button sits beside the search.
- Tables get a header band, row hairlines, column lines, stripes and a teal hover, on every list and wiki table.
- Status chips with a dot and priority chips with a five-bar meter in the issue list and on the issue page. A status dot beside
  group names in lists grouped by status.
- The issue page: a card with an edge in the status colour, parent strips, a segmented previous / next control, an attribute panel,
  framed subtasks and related issues, and a card per note.
- Card panels for the sidebar, the filters, My page, the project overview, the projects list, activity and the roadmap.
- Tinted action buttons, and a primary gradient for the main action.
- Styles for flash messages, tabs, the right-click menu, dropdowns, pagination, the editor, the calendar, the Gantt chart,
  administration and the phone slide-out menu.
- The Rubylode plugins' blocks (Projects, Home, To-do, Uptime Kuma, GlitchTip, Windmill, Beszel, Stats) take the theme's colours
  through their custom properties, set in one section of the theme. The Stats overview tiles get the theme's red and green.
- Dark mode, from the system setting, in one file.
- The Opal mark and a favicon.
- A small script, `javascripts/theme.js`, which only reads the page. The theme works without it.
- A demo Redmine that mounts the Rubylode plugins it finds next to the repository, and points the status plugins at an
  address where nothing answers, so their pages show the "unavailable" state.
- A page check of 29 pages: 116 runs in light and dark, at desktop and phone width, with no console errors, no failed requests,
  no sideways scrolling and text at WCAG AA contrast. Measured contrast ratios are in `docs/accessibility.md`.
- Gitea workflows that run manual checks only on `main`, check that a release tag is on `main` and keep the release token out of
  the job that runs the repository's code.
- Tested on Redmine 7.0.2.
