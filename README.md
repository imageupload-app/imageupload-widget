# Image Uploader

A lightweight embeddable image uploader widget powered by [imageupload.app](https://imageupload.app).

Built with [Wely](https://litepacks.github.io/welyjs/).

## Installation

```bash
npm install image-uploader-widget
```

```javascript
import 'image-uploader-widget'
// Component auto-registers; use <image-uploader> in HTML
```

## CDN Usage

```html
<script src="https://cdn.jsdelivr.net/npm/image-uploader-widget/dist/wely.bundle.umd.js"></script>
<image-uploader></image-uploader>
```

## Embedding Example

```html
<image-uploader
  max-size="10"
  theme="light"
  token="your-api-token"
></image-uploader>
```

### Attributes

| Attribute   | Type   | Default                           | Description                    |
| ----------- | ------ | --------------------------------- | ------------------------------ |
| `max-size`  | number | 5                                 | Max file size in MB            |
| `theme`     | string | "light"                              | "light" or "dark"              |
| `endpoint`  | string | https://imageupload.app/api/1/upload | Upload API URL                 |
| `token`     | string | -                                    | API auth token (Bearer header) |

## API Response Example

```json
{
  "status": 200,
  "success": true,
  "data": {
    "id": "373177ed0d13059db5b0",
    "url": "https://i.imageupload.app/373177ed0d13059db5b0.png",
    "display_url": "https://i.imageupload.app/373177ed0d13059db5b0.png",
    "url_viewer": "https://imageupload.app/i/373177ed0d13059db5b0"
  }
}
```

The widget uses `data.url` or `data.display_url` for the image link.

## Features

- Drag and drop upload area
- Click to select file
- Image preview after upload
- Upload progress bar
- Copy image link button
- Open image button
- Image size validation (max 5)
- Accepted formats: jpg, jpeg, png, webp, gif
- Dark mode support
- Event system (`uploaded`, `error`, `progress`)

## Events

```javascript
const uploader = document.querySelector('image-uploader');

uploader.addEventListener('uploaded', (e) => {
  console.log('Image URL:', e.detail);
});

uploader.addEventListener('error', (e) => {
  console.log('Error:', e.detail);
});

uploader.addEventListener('progress', (e) => {
  console.log('Progress:', e.detail, '%');
});
```

## Free Image Hosting

This uploader is powered by [imageupload.app](https://imageupload.app/en).

Upload images instantly for free: **https://imageupload.app/en**

## Live Demo

```bash
wely dev
```

## Keywords

image uploader, free image hosting, upload images online, share images, image hosting widget
