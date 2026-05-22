# Changelog

## 2026-05-23 — Design overhaul + UI fixes

### Changed
- **Complete visual redesign**: light theme with warm gold palette
  - Hero section: multi-color gradient background (gold/blue/pink)
  - Gold gradient text for main title
  - Subtle dot-grid background texture
  - Softer card shadows and borders
- **Navigation bar**: fixed `overflow-x:auto` → `overflow:visible`
  - Previously clipped the "名單" dropdown menu
  - Added `position:relative` on `.nav-teams` for correct dropdown anchoring
  - Mobile: `overflow-x:auto` only on small screens (≤640px) for horizontal scroll
- **Group cards**: removed `overflow:hidden` so hover effects and potential overlays aren't clipped
- **Typography**: section titles with gold bottom border accent
- **Filter tabs**: pill-style active/inactive states for group filter on fixtures page
- **Dropdown**: wider (260px), better shadow, scrollable with `max-height:60vh`

### Fixed
- **Nav dropdown cut off**: `.nav` had `overflow-x:auto` which clipped absolutely positioned children
- **Duplicate CSS rule**: removed duplicate `.nav-teams{position:relative}` line
- **Group card overflow**: removed `overflow:hidden` on `.g-card` to allow hover transforms and future squad overlays

### Data
- 48 teams across 12 groups (A–L)
- 72 group-stage fixtures with dates, venues
- 9 complete squads with player details (Brazil, France, Portugal, Croatia, Germany, Japan, South Korea, Switzerland, Belgium)
- Japanese and Korean player names in native kanji/hangul
- 16 venues across 3 host nations
