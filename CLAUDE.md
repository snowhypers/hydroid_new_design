# Project Context

Stack: Static HTML / Tailwind CDN / vanilla JavaScript
Architecture: Single-file mobile app prototype
Entry: `hydroid.html` opened directly in browser or via Live Server
Tests: None configured
Lint: None configured

## Structure
`hydroid.html` - complete Hydroid smart bottle app UI, styling, markup, and scripts.
`image.png` - Hydroid product/feature banner used by the Discover tab.
`.vscode/settings.json` - Live Server configured on port 5501.
`.ijfw/` - IJFW local metadata.

## Patterns
Tailwind utility classes are used inline through the CDN config in `hydroid.html`.
UI is organized as four tab views: home, history, discover, profile.
Bottom navigation calls `switchTab()` and toggles view/header visibility.
History analytics use `chartDatasets` plus `updateChart()` to mutate SVG paths and labels.
Hydroid Coach is a local scripted chat modal with canned keyword responses.
Profile rows use `toggleSection()` to expand and collapse hidden detail panels.

## Key Files
`hydroid.html` - app shell, all screens, modal, chart state, and interaction handlers.
`image.png` - real product artwork displayed in Discover with an inline fallback.

## Notes
External runtime dependencies are loaded from Tailwind CDN, Google Fonts, Font Awesome, and ui-avatars.
Current `hydroid.html` ends with duplicate closing `</body>` and `</html>` tags.
