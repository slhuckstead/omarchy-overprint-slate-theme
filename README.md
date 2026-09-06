# Overprint Slate

A Risograph press, simulated, for [Omarchy](https://omarchy.org). Three inks,
real halftone screens at 15/75/45 degrees, subtractive overprint on paper and
screen-blend on dark grounds, paper grain, and deliberate misregistration.

    #0F4C81   #FF5A4D   #FFE800

This is the **slate** ground -- a lifted dark, for a bright room where
the deep ground washes out and paper glares back. Its inks come out
paler than the night theme's, which is the ground rather than a
fault: higher contrast on a lifted ground means lighter. Siblings:
[Overprint](https://github.com/slhuckstead/omarchy-overprint-theme)
and [Overprint Light](https://github.com/slhuckstead/omarchy-overprint-light-theme).

## Install

```bash
omarchy theme install https://github.com/slhuckstead/omarchy-overprint-slate-theme.git
```

## What this is

Nothing here is hand-picked. The palette is *solved*: every ANSI slot is filled
by what this press can physically make -- an ink alone, two overprinted, or all
three -- and then retargeted in OKLab until it clears its contrast floor. The
contrast targets are deliberately non-uniform per hue, because driving every hue
to one ratio flattens lightness below a just-noticeable difference and leaves
hue as the only thing separating two slots, which is exactly what colour-vision
deficiency takes away. Red and green are pushed furthest apart.

Every colour is verified against `selection`, the extreme of the three grounds
that carry text, so it clears against `background` and `lighter_background` too.

The window border is three stops: an ink, what those two inks actually make
where they overlap on this ground, and the other ink. It is the only place in
the theme where an overprint is visible as itself.

`shell.toml` is included, so the bar, launcher, menu, notifications and lock
screen are themed as one surface rather than inheriting a generic fallback.
Interaction states climb through ink rather than through four opacities of the
same grey.

## Wallpapers

6 of them: one per composition family -- 11-register-alt, 3-canon-deep, 4-modulor, 6-duo, 7-spiral, 9-stack -- at 3840x2160. Every
composition is derived from the golden ratio, a diminishing nested series of
large fields with one dominant, and nothing placed by eye.

The generator makes 132 (4 presses x 3 ground levels x 11 compositions). To use
the rest, put them in `~/.config/omarchy/backgrounds/overprint/` -- Omarchy
cycles that directory alongside the theme's own.

## Licence

MIT. See LICENSE.
