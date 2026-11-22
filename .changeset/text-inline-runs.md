---
"@gpuix/native": minor
"@gpuix/solid": minor
"@gpuix/react": minor
---

A `<text>` whose children are all `<text>` nodes now paints as one wrapped paragraph, with each child as a styled run, when at least one child has a `style` or an `href`. Children can change the font family, weight, italic, colour, background and underline, so mixed inline formatting such as `<text>plain <text style={{ fontWeight: 700 }}>bold</text> and <text href="https://example.com">a link</text></text>` wraps and selects as one line of text instead of separate boxes. A run can't change the font size, because GPUI text runs share the paragraph's size. Link runs are underlined and fire `onLinkClick` on the parent `<text>`.

New style property `fontStyle: "normal" | "italic"` selects the family's italic face, on any element and on runs.

Text no longer wraps with a trailing `+` or a superscript digit alone at the start of a line (`4,000+`, `C++`, `note¹`). This comes from a GPUI fix in the zed submodule.
