# Robust Image DNA Storage Pipeline

This version changes the project direction from generic file compression to image-aware robust DNA storage.

## New pipeline

1. Input Image
2. Image Compression
   - Hybrid WebP
   - Local DCT Compression
3. DNA Design
   - SM
   - R∞
   - R2
   - R1
   - R0
   - Protected Design
   - Reed-Solomon
4. Strand Design / sequencing simulation / strand rebuild
5. Image Reconstruction
6. Validation and image comparison

## What changed

- The old generic compressor candidates are no longer used in Panel 2.
- Panel 2 now creates an image payload using robust image-specific compression.
- Panel 3 still applies DNA design/ECC to that payload.
- Panel 5 reconstructs an image from the decoded payload instead of validating the payload as a generic file.
- Hybrid WebP uses base layer + WebP tiles + CRC32 fallback.
- Local DCT Compression uses YCbCr local DCT packets + CRC8 local validation.

## Method names in UI

- Hybrid WebP
- Local DCT Compression

## Important

This app version is image-focused. It is designed for graceful degradation under DNA errors rather than exact generic file recovery.
