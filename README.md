# CocoPDF

**Free online PDF tools. No account, no watermarks, nothing to install.**

[cocopdf.com](https://cocopdf.com)

> This repository is documentation only. The application source is not published here.

CocoPDF is a set of 26 PDF tools that run in the browser: merging, splitting, compressing,
converting to and from the Office formats, OCR, and repairing files that will not open.
Every tool is free, there is no paid tier holding anything back, and there is no signup
in front of any result.

| | |
|---|---|
| Cost | Free, with no paid plan and no feature held back |
| Account | Not required, on any tool |
| Watermarks | None, on any output file |
| File size | 50 MB maximum per upload |
| Retention | Upload and result both deleted within one hour |
| Install | Nothing to install, it runs in the browser |

---

## Tools

### Organize

| Tool | What it does |
|---|---|
| [Merge PDF](https://cocopdf.com/tools/merge-pdf) | Combine several PDFs into one file, in whatever order you arrange them |
| [Split PDF](https://cocopdf.com/tools/split-pdf) | Break a single PDF into separate documents by page range |
| [Remove Pages](https://cocopdf.com/tools/remove-pages) | Delete the pages you do not want and download what is left |
| [Extract Pages](https://cocopdf.com/tools/extract-pages) | Pull a range of pages out into a document of its own |
| [Organize Pages](https://cocopdf.com/tools/organize-pages) | Reorder pages into the sequence you actually wanted |

### Convert to PDF

| Tool | What it does |
|---|---|
| [Word to PDF](https://cocopdf.com/tools/word-to-pdf) | DOC and DOCX through a real office engine rather than a browser approximation |
| [Excel to PDF](https://cocopdf.com/tools/excel-to-pdf) | Spreadsheets to PDF with the sheet layout intact |
| [PowerPoint to PDF](https://cocopdf.com/tools/powerpoint-to-pdf) | Slide decks flattened to a paginated document |
| [Image to PDF](https://cocopdf.com/tools/image-to-pdf) | JPG and PNG files assembled into one document |
| [HTML to PDF](https://cocopdf.com/tools/html-to-pdf) | Render a web page or an HTML file to PDF |
| [PDF Scanner](https://cocopdf.com/tools/scan-to-pdf) | Use a phone camera or webcam as a scanner, with edge detection and perspective correction |

### Convert from PDF

| Tool | What it does |
|---|---|
| [PDF to Word](https://cocopdf.com/tools/pdf-to-word) | Produces an editable DOCX, not a document full of page images |
| [PDF to Excel](https://cocopdf.com/tools/pdf-to-excel) | Recover table data back into a spreadsheet |
| [PDF to PowerPoint](https://cocopdf.com/tools/pdf-to-powerpoint) | Turn pages back into slides you can edit |
| [PDF to JPG](https://cocopdf.com/tools/pdf-to-jpg) | Export every page as a JPG image |
| [PDF to PNG](https://cocopdf.com/tools/pdf-to-png) | Export pages as PNG when you need lossless output |

### Edit

| Tool | What it does |
|---|---|
| [Rotate PDF](https://cocopdf.com/tools/rotate-pdf) | Writes the rotation into the file, so it holds everywhere instead of just in your viewer |
| [Crop PDF](https://cocopdf.com/tools/crop-pdf) | Trim margins, or clear a running header off every page at once |
| [Watermark PDF](https://cocopdf.com/tools/watermark-pdf) | Stamp text or an image across the pages |
| [Page Numbers PDF](https://cocopdf.com/tools/page-numbers-pdf) | Add page numbers to a document that arrived without them |

### Optimize

| Tool | What it does |
|---|---|
| [Compress PDF](https://cocopdf.com/tools/compress-pdf) | Bring a file under an email or upload limit |
| [Repair PDF](https://cocopdf.com/tools/repair-pdf) | Rebuild a damaged file and recover whatever is still readable inside it |
| [OCR PDF](https://cocopdf.com/tools/ocr-pdf) | Run text recognition over a scan so the words become selectable and searchable |

### Secure

| Tool | What it does |
|---|---|
| [Protect PDF](https://cocopdf.com/tools/protect-pdf) | Add a password so the document cannot be opened without it |
| [Unlock PDF](https://cocopdf.com/tools/unlock-pdf) | Remove a password you already know from a file that is yours |
| [Sign PDF](https://cocopdf.com/tools/sign-pdf) | Put a signature on a document without printing and rescanning it |

---

## How it is built

The front end is Next.js and the API is Express, with nginx in front and Redis behind, all
running in Docker containers on a single server.

The conversions themselves are not done in JavaScript. Office documents go through
LibreOffice, compression and PDF repair run on Ghostscript, image work uses ImageMagick,
and OCR is Tesseract. Those are the same engines a desktop tool would reach for, which is
why a Word file with an awkward layout tends to survive the trip rather than coming out
approximately right.

---

## Writing

Longer pieces on why documents misbehave, which are often more useful than the tool itself
once you know what actually went wrong.

- [PDF Repair: Causes and Fixes for Corrupt PDF Files](https://cocopdf.com/blog/repair-corrupted-pdf)
- [Why Your PDF Keeps Reverting to Sideways](https://cocopdf.com/blog/rotate-pdf-permanently-guide)
- [Why Word to PDF Conversion Sometimes Breaks Formatting](https://cocopdf.com/blog/word-to-pdf-formatting-guide)
- [How to Crop PDF Margins and Remove Headers and Footers](https://cocopdf.com/blog/crop-pdf-margins-guide)
- [How to Scan Documents to PDF With Just Your Phone](https://cocopdf.com/blog/scan-to-pdf-guide)
- [OCR Explained: How to Make Scanned PDFs Searchable](https://cocopdf.com/blog/ocr-scanned-pdf-guide)
- [How to Compress a PDF Without Losing Quality](https://cocopdf.com/blog/compress-pdf-quality-guide)
- [How to Merge PDF Files Into One, the Right Way](https://cocopdf.com/blog/merge-pdf-guide)
- [How to Split a PDF File Into Separate Documents](https://cocopdf.com/blog/split-pdf-guide)
- [PDF to JPG or PDF to PNG: Which Should You Use?](https://cocopdf.com/blog/pdf-to-jpg-vs-png-guide)
- [PDF vs DOCX: When to Convert and When Not To](https://cocopdf.com/blog/pdf-vs-docx-when-to-convert)
- [PDF Password Protection: What It Actually Does](https://cocopdf.com/blog/protect-pdf-password-guide)
- [How PDF Password Removal Actually Works](https://cocopdf.com/blog/unlock-pdf-password-removal-guide)
- [Electronic Signatures: What Signing a PDF Means](https://cocopdf.com/blog/sign-pdf-electronic-signatures-explained)

---

## Links

[Website](https://cocopdf.com) ·
[About](https://cocopdf.com/about) ·
[Contact](https://cocopdf.com/contact) ·
[Privacy](https://cocopdf.com/privacy) ·
[Terms](https://cocopdf.com/terms)

Built and run by Oussama EL.
