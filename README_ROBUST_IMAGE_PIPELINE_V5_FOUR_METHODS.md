# Robust Image DNA Storage Pipeline v5

This version adds the four presentation-friendly no-ECC image compression methods
from `dna_four_methods.py` into the latest app.

## Final Panel 2 compression methods

1. No compression
   - Uses selected raw pixel data directly.
   - Black-white is packed as 1 bit/pixel.

2. Robust Low-Resolution
   - Stores only a small quantized image.
   - Very robust, but blurry.

3. Base + Local Detail
   - Main proposed method.
   - Robust base image + lightweight local detail.
   - If detail is damaged, the region falls back to the base.

4. Base + WebP Detail
   - Robust base image + WebP detail tiles.
   - Keeps advanced settings:
     WebP quality, tile size, base downsample, base bits.

5. Local Block Coding
   - Local block/DCT-style coding.
   - Keeps advanced settings:
     Y q scale, C q scale, Y packet bits, C packet bits.

## Preserved from v4

- Pixel representation:
  - Black-white (1 bit/pixel)
  - Grayscale (8 bits/pixel)
  - RGB (24 bits/pixel)

- DNA Design:
  - SM
  - R∞
  - R2
  - R1
  - R0
  - Protected Design
  - Reed-Solomon

- Strand Design / sequencing simulation / rebuild / image reconstruction.

## Smoke tests

For a 28 x 28 test image using Black-white:
- Raw pixel data = 784 bits = 98 bytes

All 5 methods passed:
- payload generation
- Simple Mapping DNA Design
- DNA decoding
- image reconstruction
