# pdfeditable
Convert a scanned pdf to an editable document: word, txt, html etc.

## Techniques & Workflow

Just a sketch, it might be using follow techniques:
- `Tesseract`, for OCR extracting words.
- `Baidu OCR API`, for easier & more accurate extracting.
- `pdfimages`, extract scanned page as image.
- `ImageMagick`, convert pdf page to image.
- `pdftk`, for basic PDF operations.
- `ReportLab & RML`, for generating PDF with texts & coordinates.

Workflow:
- Split PDF to multiple 1-page PDFs (`pdftk`) -> 
- Extract or convert each PDF page to a image file (`pdfimages` or `ImageMagick`) ->
- OCR each image to get texts and positions (`Tesseract` or `Baidu OCR API`) ->
- Generate editable document from texts & positions (`ReportLab`)

