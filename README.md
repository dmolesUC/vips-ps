# Demonstration of [libvips/libvips #2290](https://github.com/libvips/libvips/issues/2290)

| File                | Description                           |
| ---                 | ---                                   |
| villette-040.tiff   | original monochrome TIFF              |
| villette-040-p.tiff | VIPS pyramid TIFF w/JPEG compression  |
| stgall-sm.jpg       | original JPEG                         |
| stgall-sm-p.tif     | VIPS pyramid TIFF w/JPEG compression  |
| stgall-sm-np.tif    | VIPS flat TIFF w/JPEG compresson      |
| stgall-sm-ps.tif    | Photoshop flat TIFF w/JPEG compresson |

VIPS commands used:

- for `villette-040-p.tiff`:

  ```sh
  vips tiffsave villette-040.tiff villette-040-p.tiff --tile --pyramid --compression jpeg --tile-width 256 --tile-height 256
  ```

- for `stgall-sm-p.tif`:

  ```sh
  vips tiffsave stgall-sm.jpg stgall-sm-p.tif --compression jpeg --tile --pyramid --tile-width 256 --tile-height 256
  ```

- for `stgall-sm-np.tif`:

  ```sh
  vips tiffsave stgall-sm.jpg stgall-sm-np.tif --compression jpeg
  ```

Opening in Photoshop 2021 fails with:

> Could not open “villette-040-p.tiff” because an invalid SOS JPEG marker
> (Ss, Se, Ah, or Al) is found.

VIPS version vips-8.10.6-Tue Mar 23 20:52:58 UTC 2021 (macOS 10.15.7, Homebrew)

