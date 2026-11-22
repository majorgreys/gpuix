---
"@gpuix/native": patch
---

In terminal mode the HiDPI scale is now re-derived from the cell size on every resize, not only when the window opens. A pane can open before its terminal knows its pixel size (Rex reports an 8x16 placeholder cell for a pane no client is displaying), so the app used to stay at scale 1, drawn at half size on a Retina screen, until it restarted. `GPUI_TERMINAL_SCALE` still overrides the guess.
