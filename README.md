# omarchy-fonts

The font and icon set Omarchy's shell, terminal and editors are designed
against, as a charly layer.

The `omarchy-fonts` candy installs the faces Omarchy's own configuration names:
the JetBrains Mono Nerd variant its terminal and Quickshell bar render with, the
iA Writer family its editor themes reference, Noto for CJK and emoji coverage,
and the Yaru icon theme and GTK theme engine its GTK applications resolve
against. Without them the desktop still starts, but it renders with fallback
faces and missing glyph boxes wherever a Nerd Font symbol is used — which is most
of the bar.

## What it provides

| Property | Value |
|---|---|
| Layer / candy | `omarchy-fonts` |
| Requires | `layer-omarchy-base` (the foundation layer) |
| Fonts | `ttf-jetbrains-mono-nerd-basic`, `ttf-ia-writer`, `ttfx`, `woff2-font-awesome`, `noto-fonts`, `noto-fonts-cjk`, `noto-fonts-emoji` |
| Icons / themes | `yaru-icon-theme`, `gnome-themes-extra` |
| Service / port | none |

## How to use it

Compose the layer by pinning the member candy's sub-path in a desktop box's
`candy:` list:

```yaml
my-omarchy-desktop:
  candy:
    # the named box's value is the box BODY; `base:` and the `candy:` list are its keys
    base: omarchy
    candy:
      - '@github.com/opencharly/layer-omarchy-base/candy/omarchy-base:v2026.242.0701'
      - '@github.com/opencharly/layer-omarchy-fonts/candy/omarchy-fonts:v2026.242.0557'
```

## Layout

- `charly.yml` — repo shape: the `discover:` rule that finds the member candy.
- `candy/omarchy-fonts/charly.yml` — the candy entity (the `distro:` package arm
  and the `plan:` `check:` assertions).
- `.github/workflows/tag-on-merge.yml` — CalVer tag + `CHANGELOG/` on merge.
- `README.md` — this user overview.

## Related

- Closest family skill: `/charly-distros:omarchy-base` — the nearest owning procedure; this
  repo carries no `skill:` entity of its own.
- Foundation: `/charly-distros:omarchy-base`.
- Sibling desktop fonts: `/charly-selkies:desktop-fonts` — the sway/labwc desktop
  font set, distinct from Omarchy's.
- [`opencharly/opencharly](https://github.com/opencharly/opencharly) — the umbrella.
