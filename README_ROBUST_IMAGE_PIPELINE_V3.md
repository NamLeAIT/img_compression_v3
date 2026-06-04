# Robust Image DNA Storage Pipeline v3

This version implements the new image-first pipeline:

1. Upload image
2. Show uploaded file information
3. Convert image to raw pixel representation
4. Show raw pixel data and raw pixel binary
5. Image Compression:
   - No compression
   - Hybrid WebP
   - Local DCT Compression
6. DNA Design:
   - SM
   - R∞
   - R2
   - R1
   - R0
   - Protected Design
   - Reed-Solomon
7. Strand Design / sequencing simulation / strand rebuild
8. Image Reconstruction
9. Validation

## Panel 1

Shows:
- uploaded file type
- uploaded file extension
- uploaded file size
- image size
- channels
- raw pixel data
- raw pixel binary preview

## Panel 2

Compression choices:
- No compression: raw pixel bytes are sent directly to DNA Design
- Hybrid WebP: base layer + WebP tile enhancement + CRC32
- Local DCT Compression: local YCbCr/DCT packets + CRC8

Compression level:
- High quality
- Balanced
- High compression
- Custom

Panel 2 metrics:
- Raw pixel data
- Compressed payload
- Compression ratio

## Panel 6

Validation shows:
- Before DNA error
- After DNA decoding
- comparison table with compression, DNA design, payload match, and image metrics
