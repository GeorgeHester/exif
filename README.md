Test data: https://code.google.com/archive/p/imagetestsuite/downloads

Supported File Formats

| Supported | Name      | Extensions                                       | Information | Exif |
| --------- | --------- | ------------------------------------------------ | ----------- | ---- |
| []        | JPEG      | .jpg .jpeg .jpe .jif .jfif .jfi                  | ----------- |      |
| []        | JPEG 2000 | .jp2 .j2k .jpf .jpm .jpg2 .j2c .jpc .jpx .mj2    | ----------- |      |
| []        | JPEG XL   | .jxl                                             | ----------- |      |
| []        | PNG       | .png                                             | ----------- |      |
| []        | WebP      | .webp                                            | ----------- |      |
| []        | HEIF      | .heif .heifs .heic .heics .avci .avcs .avif .hif | ----------- |      |
| []        | AVIF      | .avif                                            | ----------- |      |
| []        | TIFF      | .tiff .tif                                       | ----------- |      |
| []        | BMP       | .bmp .dib                                        | ----------- |      |

### EXIF

EXIF makes use of APPn headers, the two supported are APP1 and APP2 or COM, any other APPn is not part of EXIF.

### JPEG (with EXIF)

File Start:

- FF D8 (JPEG)
- FF E1 58 45 45 78 69 66 (JPEG EXIF)
- 00 00 (NULL Bytes)

TIFF Header

- 4D 4D (Big Endian) || 49 49 (Little Endian)
- 00 2A
- XX XX XX XX (Offset of IFD) [If immediately after the TIFF header this value is 00 00 00 08, for 8 bytes from file or EXIF start]
