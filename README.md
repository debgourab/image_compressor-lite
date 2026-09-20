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

