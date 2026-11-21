# Improve 3D performance and scrolling

## Goal
Keep the portfolio’s AI/ML visual identity while making page loading and scrolling feel lighter and more immediate.

## Changes
- Reduce decorative objects and rendering cost in the existing 3D scene, and pause its continuous rendering when the hero is off-screen.
- Remove scroll snapping and retain natural browser scrolling; lighten the full-screen code animation and pause it when the page is hidden.
- Verify desktop and mobile preview behavior, plus current build and runtime logs.

## Technical details
- Keep the existing React Three Fiber scene and theme colors; use visibility-aware rendering, fewer animated meshes, and conservative canvas quality settings.
- Remove CSS section snap rules and any scene-only scroll easing that makes movement lag behind the page.
- Visitor speed data currently has one reading per metric, so it is too limited to determine real-world regressions; use preview checks for this iteration.