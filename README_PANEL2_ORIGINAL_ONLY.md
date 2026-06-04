# Panel 2 update: Original file pipeline only

This update changes Panel 2 (Compression):

- Removed Image data source options:
  - Original file bytes
  - RGB pixels
  - Grayscale pixels
  - Binary image pixels
- The pipeline now always uses the uploaded original file bytes.
- Compression mode still benchmarks all valid compressors.
- After compression, the selected compressed output is previewed when supported.
- Image outputs after compression can now be previewed directly in Panel 2.

The removed image-pixel branches are no longer used in the UI.
