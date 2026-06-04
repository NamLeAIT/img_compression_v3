# Robust Image DNA Storage Pipeline v6

This version updates the evaluation flow to focus on image reconstruction from selectable DNA sources.

## Main updates

### Panel 2 — Image Compression

Panel 2 now adds compression-stage image quality metrics:

- Image size
- Pixel representation
- Raw pixel data
- Payload data / Compressed payload
- Payload ratio / Compression ratio
- PSNR / SSIM when available

The comparison is:
- Selected pixel image vs Payload preview for No compression
- Selected pixel image vs Before DNA error for compressed methods

This separates compression loss from DNA/error loss.

### Panel 4 — Strand Design and DNA Error Simulation

The main flow now focuses on prepared-strand-level DNA errors.

- Strand Design stays visible.
- DNA Error Simulation stays visible and can generate:
  - advanced_error_rows
  - noisy_dna
  - dna_error_stats

Sequencing read errors are moved into:

- Advanced sequencing simulation

This section is collapsed by default and optional.

### Panel 5 — Image Reconstruction

Image Reconstruction now supports three reconstruction sources:

1. Original encoded data
2. Noisy encoded data
3. Sequencing rebuilt data

This means sequencing simulation is no longer required for image reconstruction.

### Panel 6 — Validation

Validation now records:

- Reconstruction source
- DNA error settings when using Noisy encoded data
- Payload exact match
- Valid/invalid image units
- Before DNA error vs After DNA decoding image metrics
- Original vs decoded image metrics

## Preserved

- 5 image compression methods:
  - No compression
  - Robust Low-Resolution
  - Base + Local Detail
  - Base + WebP Detail
  - Local Block Coding

- Pixel representations:
  - Black-white (1 bit/pixel)
  - Grayscale (8 bits/pixel)
  - RGB (24 bits/pixel)

- DNA Design methods:
  - SM
  - R∞
  - R2
  - R1
  - R0
  - Protected Design
  - Reed-Solomon
