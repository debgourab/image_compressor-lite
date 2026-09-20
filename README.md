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

