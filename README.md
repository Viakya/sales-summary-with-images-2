# CSV Viewer + Images

## Project Overview
This is a minimal, single-file web application (index.html) that:
- Automatically loads `data.csv` from the same directory and displays its contents in a table.
- Displays two images: `photo1.png` and `photo2.png`.
- Provides a manual CSV file picker as a fallback if automatic loading is unavailable (e.g., when not served over HTTP).

The app requires no build step or external dependencies.

## Files
- `index.html` — Main single-page web app. Open this in a browser via a local web server.
- `data.csv` — Sample CSV file that is automatically loaded by the app.
- `photo1.png`, `photo2.png` — Images displayed at the top of the page.

Note: The application expects these files to reside in the same directory.

## Setup
Because modern browsers block `fetch()` from reading local files via the `file://` protocol, please serve the folder with a simple local web server:

- Python 3:
  - macOS/Linux: `python3 -m http.server 8000`
  - Windows (PowerShell): `py -3 -m http.server 8000`
  - Then visit: http://localhost:8000/

- Node.js (using `npx`):
  - `npx serve` (or `npx http-server`)
  - Follow the printed URL (often http://localhost:3000/ or http://127.0.0.1:8080/)

- VS Code:
  - Install the “Live Server” extension and click “Go Live”.

## Usage
1. Place `index.html`, `data.csv`, `photo1.png`, and `photo2.png` in the same directory.
2. Start a local web server in that directory (see Setup).
3. Open `index.html` in your browser (via the local server URL).
4. The page will:
   - Show `photo1.png` and `photo2.png`.
   - Fetch and display `data.csv` in a table.
5. If `data.csv` fails to load automatically, click “Load CSV manually” and choose any `.csv` file from your device.

## License
MIT License

Copyright (c) 2025 Your Name

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.