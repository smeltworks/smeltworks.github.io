# Brand assets

Approved 2026-10-18. The SVGs are the sources; the PNGs are renders of them.

| File | Use |
| --- | --- |
| `smeltworks.svg` | smeltworks icon: a crucible of molten metal on an iron tile. Also the site's `favicon.svg`. |
| `smeltworks-square.svg`, `smeltworks-avatar-512.png` | Square-cornered variant for places that apply their own mask: the GitHub org avatar, `apple-touch-icon.png`. |
| `smeltworks-{16,32,128,512}.png` | Rendered sizes of the rounded icon. |
| `cnx.svg` | cnx icon: a copper C and the `<-` assignment arrow on the same iron tile. The C is outlined from Arial Black, so no font is needed. |
| `cnx-{16,32,128,256,512}.png` | Rendered sizes. `cnx-256.png` is the VS Code Marketplace icon (sharp on high-density screens). |

## Palette

| Token | Value |
| --- | --- |
| Iron tile | `#2e2722` → `#110e0c` (diagonal gradient) |
| Crucible iron | `#4a423a` → `#1f1a16`, rim `#5a5047` |
| Molten | `#fff3b8` → `#ffb347` → `#e8590c` (radial) |
| Copper (the C) | `#f0b77a` → `#c27a38` |
| Arrow | `#ffb347` |
| Wordmark copper | `#a8592a` on light, `#d98a4e` on dark |

## Regenerating the PNGs

```sh
for s in 16 32 128 256 512; do
  inkscape brand/smeltworks.svg -w $s -h $s -o brand/smeltworks-$s.png
  inkscape brand/cnx.svg -w $s -h $s -o brand/cnx-$s.png
done
inkscape brand/smeltworks-square.svg -w 512 -h 512 -o brand/smeltworks-avatar-512.png
inkscape brand/smeltworks-square.svg -w 180 -h 180 -o apple-touch-icon.png
```
