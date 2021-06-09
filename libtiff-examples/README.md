# Demonstration of [libtiff/libtiff #266](https://gitlab.com/libtiff/libtiff/-/issues/266)

| File                        | Description                                 |
| ---                         | ---                                         |
| `stgall-sm-ps-zip.tif`      | Original TIFF (Photoshop, ZIP compression)  |
| `stgall-sm-tiffcp-jpeg.tif` | Converted TIFF (`tiffcp`, JPEG compression) |

Command to reproduce:

```sh
tiffcp -r 128 -c jpeg stgall-sm-ps-zip.tif stgall-sm-tiffcp-jpeg.tif
```

