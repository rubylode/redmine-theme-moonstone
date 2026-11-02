# Changelog

All notable changes to this theme. The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [1.0.0] - 2026-11-02

### Added

- Opal: a milky, cool off-white page with white panels, a soft blue-teal primary, and a faint lilac and peach shimmer on the
  header, the focus rings and the primary button. Every colour is a token in `opal/stylesheets/opal-tokens.css`.
- A compact two-row header: the mark, the global links, the search and the project switcher as rounded fields, and the avatar
  on top; the project name, the tabs and the "+" menu below. The New issue button of the Rubylode plugin sits beside the search.
- Tidy tables: a header band, row hairlines, column lines, stripes and a teal hover, on every list and wiki table.
- Status chips with a dot and priority chips with a five-bar meter in the issue list and on the issue page; a status dot beside
  group names in lists grouped by status.
- The issue page: a card with an edge in the status colour, parent strips, a segmented previous / next control, an attribute panel,
  framed subtasks and related issues, a card per note.
- Card panels for the sidebar, the filters, My page, the project overview, the projects list, activity and the roadmap; tinted
  action buttons and a primary gradient for the main action; styled flash messages, tabs, the right-click menu, dropdowns,
  pagination, the editor, the calendar, the Gantt chart, administration and the phone slide-out menu.
- The Rubylode plugins' blocks (Projects, Home, To-do, Uptime Kuma, GlitchTip, Windmill, Beszel, Stats) follow the theme
  through their custom properties, in one section of the theme.
- Dark mode from the system setting, in one file.
- The Opal mark and a favicon.
- One small script, `javascripts/theme.js`, which only reads the page; the theme works without it.
- The demo Redmine mounts the Rubylode plugins it finds next to the repository; the page check covers 24 pages, all gated:
  96 runs in light and dark, at desktop and phone width, with no console errors, no failed requests, no sideways scrolling and
  text at WCAG AA contrast. Measured contrast ratios are in `docs/accessibility.md`.
- Gitea workflows that run manual checks only on `main`, check that a release tag is on `main`, and keep the release token out of
  the job that runs the repository's code.
- Tested on Redmine 7.0.2.
