# Robust Image DNA Storage Pipeline v4

This version fixes the pixel-representation layer.

## Main updates

1. Pixel representation selection:
   - Black-white (1 bit/pixel)
   - Grayscale (8 bits/pixel)
   - RGB (24 bits/pixel)

2. Black-white is now true packed-bit storage:
   - 28 x 28 = 784 bits = 98 bytes
   - It is no longer stored as 1 byte per pixel.

3. Panel 1 now shows:
   - Uploaded file information
   - Pixel representation
   - Image size
   - Pixel depth
   - Raw pixel data
   - Selected pixel image preview
   - Raw pixel binary preview

4. Panel 2 now has:
   - No compression
   - Hybrid WebP
   - Local DCT Compression

5. Wording is method-aware:
   - No compression uses Payload data / Payload ratio.
   - Hybrid WebP and Local DCT use Compressed payload / Compression ratio.

6. Validation uses:
   - Before DNA error
   - After DNA decoding

## Smoke tests passed

For a 28 x 28 test image:
- Black-white raw data = 98 B
- Grayscale raw data = 784 B
- RGB raw data = 2352 B

All passed through:
- payload generation
- Simple Mapping DNA Design
- DNA decoding
- image reconstruction
