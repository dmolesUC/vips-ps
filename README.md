# Demonstration of VIPS/Photoshop issue

| File                | Description               |
| ---                 | ---                       |
| villette-040.tiff   | original                  |
| villette-040-p.tiff | pyramid created with vips |

VIPS command used:

```sh
vips tiffsave villette-040.tiff villette-040-p.tiff --tile --pyramid --compression jpeg --tile-width 256 --tile-height 256
```

Opening in Photoshop 2021 fails with:

> Could not open “villette-040-p.tiff” because an invalid SOS JPEG marker
> (Ss, Se, Ah, or Al) is found.

VIPS version vips-8.10.6-Tue Mar 23 20:52:58 UTC 2021 (macOS 10.15.7, Homebrew)

