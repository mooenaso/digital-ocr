# Digital OCR Evaluation Tool

A comprehensive, browser-based tool designed for evaluating and testing Optical Character Recognition (OCR) systems. This tool allows you to generate highly customizable text samples, simulate real-world document degradation, and load various file formats to test OCR accuracy under different conditions.

It is a **single, self-contained HTML file** with zero backend dependencies. Just open it in any modern web browser.

## Features

### 📝 Advanced Text Generation
- **Custom Sentences:** Type or paste any text to generate test samples.
- **Multi-size Rendering:** Render the same text at multiple font sizes simultaneously (e.g., 8pt, 10pt, 12pt) to test size-dependent OCR accuracy.
- **Grid Generation:** Multiply rows and columns to create dense blocks of text.
- **Typography Controls:** Fine-tune font family, font weight, line spacing, letter spacing, and word spacing.
- **Custom Fonts:** Dynamically load any Google Font by name.

### 🔬 Real-World Degradation Simulation
Test how your OCR engine handles poor-quality scans and photos:
- **Contrast Level:** Adjust the actual text-to-background color contrast (0-100%) to simulate faded ink or low-contrast paper.
- **Blur:** Apply CSS blur to simulate out-of-focus captures.
- **Rotation:** Rotate text from 0 to 360 degrees to test skew tolerance.
- **Noise Overlay:** Add adjustable visual noise (Grain, Scan Lines, or Paper Texture) to simulate poor sensor quality or textured paper.
- **Color Controls:** Custom text and background colors, plus a one-click "Inverse Colors" toggle.

### 📁 File Viewer Mode
A dedicated screen for loading and rendering external files with their native formatting:
- **Supported Formats:** PDF, Markdown (`.md`), Plain Text (`.txt`), HTML, CSV, JSON, and more.
- **PDF Extraction:** Uses PDF.js to extract and render text from PDF documents.
- **Markdown Rendering:** Uses Marked.js to render fully formatted Markdown (headings, tables, code blocks).
- **Drag & Drop:** Simply drop a file into the browser or load from a remote URL.

### 📊 Evaluation Assets & Presets
- **Built-in Presets:** Quick-load configurations for common test scenarios (Small Print, Low Contrast, CJK Test, Confusable Characters, Noisy Scan, Rotated).
- **Custom Presets:** Save your own configurations to local storage.
- **Image Overlays:** Overlay standard evaluation charts (ISO 12233, ColorChecker, Gamma charts) directly onto the workspace.
- **Pixel Density Bar:** Real-time display of your monitor's Device Pixel Ratio (DPR), CSS resolution, physical resolution, and calculated PPI.

### ⚡ General / UX
- **Auto-Update:** The output regenerates instantly as you adjust any slider or input—no "Generate" button needed.
- **Export to PNG:** One-click export of the output area to a high-resolution PNG file.
- **Dark Mode:** Full dark mode support for the UI.
- **URL Sharing:** All settings are encoded in the URL automatically. Share your exact test configuration by simply copying the URL.
- **Keyboard Shortcuts:**
  - `Ctrl+F`: Fold/Unfold controls panel
  - `Ctrl+1` / `Ctrl+2`: Switch between OCR and File Viewer tabs
  - `Ctrl+E`: Export PNG
  - `Ctrl+D`: Toggle Dark Mode
  - `Ctrl+?`: Show shortcuts

## How to Use

1. **Download** the `index_digital_ocr_standalone.html` file.
2. **Open** it in any modern web browser (Chrome, Firefox, Edge, Safari).
3. **Adjust** the settings in the right-hand panel. The text will update automatically.
4. **Export** your test sample using the "Export PNG" button, and feed the resulting image into your OCR engine (Tesseract, EasyOCR, Google Cloud Vision, etc.).

## Use Cases

- **Benchmarking OCR Engines:** Compare how different OCR tools perform on the exact same text under varying levels of blur, noise, and contrast.
- **Testing Edge Cases:** Evaluate OCR performance on confusable characters (0/O, 1/l/I), tight letter spacing, or rotated text.
- **Dataset Generation:** Quickly generate synthetic data for training custom OCR models.

## Dependencies

This tool is entirely self-contained but fetches the following libraries via CDN at runtime:
- [html2canvas](https://html2canvas.hertzen.com/) (for PNG export)
- [PDF.js](https://mozilla.github.io/pdf.js/) (for PDF reading)
- [Marked.js](https://marked.js.org/) (for Markdown rendering)
- Google Fonts API (for custom font loading)

## License

MIT License. Feel free to use, modify, and distribute.
