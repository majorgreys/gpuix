# About this fork

This is a modified fork of [GPUIX](https://github.com/remorses/gpuix) by
Tommy D. Rossi (remorses) and contributors, licensed under the Apache License 2.0 (see
`LICENSE`). Third-party code that GPUIX itself ports keeps its own licence and
attribution; see `THIRD_PARTY_NOTICES.md`.

Files in this fork that differ from upstream have been changed by Tahir Butt.
The exact changes are the commits on top of upstream `main` (`git log
upstream/main..HEAD`), and each user-facing change has a `.changeset/*.md`
entry. Changes are meant to be offered upstream.

| Branch | Based on | Purpose |
| --- | --- | --- |
| `kitty-backend` | upstream `main` | fixes to the terminal (kitty graphics) backend, `packages/gpui-terminal` |
| `markdown-runs` | `kitty-backend` | styled inline runs in `<text>`, `fontStyle`; zed submodule with the line-wrap fix |

The `markdown-runs` branch points the `zed` submodule at
[majorgreys/zed](https://github.com/majorgreys/zed), branch `gpuix-line-wrap`:
[remorses/zed](https://github.com/remorses/zed) at the commit upstream GPUIX
pins, plus a change to `crates/gpui` (Apache-2.0) by Tahir Butt.
