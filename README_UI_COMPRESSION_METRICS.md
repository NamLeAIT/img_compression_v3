# Panel 2 UI metric update

Panel 2 now shows only the practical compression summary:

- Raw data: actual uploaded image file size (PNG/JPEG/WebP/etc.)
- Compressed data: robust image payload size after Hybrid WebP or Local DCT Compression
- Compression ratio: Raw data / Compressed data

Removed from Panel 2:

- Payload size
- DNA nt before design
- Reduction vs raw pixels
- detailed image payload summary table

This makes Panel 2 focus only on the image-compression step.
DNA length is still shown later in DNA Design.
