# Changelog

## [Unreleased]
### Added
- Created `Core Intent Analysis Mechanism` documentation.

### Optimized
- **Homepage Image Performance (2026-01-16):**
  - Replaced `homepage.jpg` (1MB) with compressed `homepage.png` (263KB) - 74% size reduction.
  - Added `<link rel="preload">` for hero image to improve LCP (Largest Contentful Paint).
  - Added `fetchpriority="high"`, `decoding="async"`, and explicit `width/height` attributes for better rendering performance.

## [1.5.6] - 2026-01-16
### Changed
- **Website UI/UX Redesign:**
  - Replaced Logo and Homepage assets with updated versions (`@logo.png`, `@homepage.jpg`).
  - Redesigned "Add to Chrome" and "Install" buttons to be more emphasized and premium.
  - Replaced generic icons with official SVG icons for Chrome and Edge.
  - Optimized "Join Community" overlay style and fixed z-index/clipping issues.
- **Content & Localization:**
  - Updated "Pain Points" and "Solutions" text to align with the latest product summary (Chaos vs Flow).
  - Synchronized localization for all installation guidance text (previously hardcoded).
  - Added multi-language support for contact info and footer.
### Fixed
- **UI:**
  - Fixed "Join Community" overlay being clipped by z-index issues.
  - Fixed Homepage Image not loading (removed broken WebP source).
  - Standardized sizes of all three Hero buttons (`px-6 py-3`).
- **Localization:**
  - Fixed "Mixed Language" issue by adding localization to Navbar, Version Badge, and Footer.
