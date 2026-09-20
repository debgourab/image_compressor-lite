# Image Compressor

A simple browser-based image compressor built with HTML, CSS, and JavaScript. Select multiple images, compress them using the Canvas API, and download the results together in a ZIP archive.

## Features

- Drag and drop images or use the file browser.
- Select multiple images in one batch.
- Encode JPEG and WebP images with a quality setting of `0.7`.
- Convert other browser-decodable image formats to JPEG.
- Preserve the original image dimensions.
- Display compression progress and ZIP creation status.
- Download results inside a `compressed_images` folder in `compressed_images.zip`.
- Process images locally in the browser; the application does not upload them to a server.

## Technologies

| Technology | Purpose |
| --- | --- |
| HTML5 | Page structure and file selection |
| CSS3 | Layout, colors, and drag feedback |
| JavaScript | File handling, compression, and downloads |
| Canvas API | Image rendering and encoding |
| FileReader API | Reading selected images |
| JSZip 3.10.1 | Building the ZIP archive |

JSZip is loaded from the CDN already included in the original code. No framework, backend, package installation, or build step is required.

## Project Files

| File | Purpose |
| --- | --- |
| `index.html` | Application markup and script/style links |
| `style.css` | Original visual styling |
| `script.js` | Original compression and download logic |
| `README.md` | Setup instructions and project documentation |

## Repository

[Image Compressor Lite on GitHub](https://github.com/debgourab/image_compressor-lite)

Clone the project:

```bash
git clone https://github.com/debgourab/image_compressor-lite.git
cd image_compressor-lite
```

## Run Locally

1. Extract the project ZIP.
2. Open the `image-compressor` folder.
3. Double-click `index.html` to open it in your browser.
4. Keep an internet connection available so the JSZip CDN script can load.

You can also open the folder in VS Code and use Live Server if you already have that extension installed.

## How to Use

1. Click **click to browse**, or drag images into the dashed area.
2. Select one or more images. Each new selection replaces the previous batch.
3. Click **Compress & Download ZIP**.
4. Wait for compression and ZIP creation to finish.
5. Open the downloaded ZIP to access your images.

## How Compression Works

The application reads each image with FileReader, draws it onto a canvas at its original dimensions, and calls `canvas.toBlob()` with a quality value of `0.7`. JPEG and WebP inputs retain their requested output format; other decodable inputs are converted to JPEG. JSZip bundles the resulting blobs into one download.

The quality value is an encoder setting, not a promise of 70% file-size reduction. Some output files may be larger than their originals.

## Original-Code Notes

The supplied styling and JavaScript logic have been preserved. Packaging only adds the HTML document structure, separates CSS and JavaScript into linked files, and removes the pasted `..` separators outside the code.

Because the original implementation is unchanged:

- Format labels and the file picker do not guarantee browser decoding support. TIFF and some other inputs may not decode in the user's browser.
- Unsupported or damaged images can leave compression waiting because image-reading and decoding error handlers are not implemented.
- Conversion to JPEG removes transparency, and animated inputs become a still image.
- Files that produce the same output filename can overwrite one another inside the ZIP. Use distinct base filenames.
- Very large batches or high-resolution images may use substantial browser memory.
- The success message means a download was triggered; the application cannot confirm that the browser saved it.

