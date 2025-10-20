Cassecroute OCR is a tool for processing scanned PDF files using [PdfSandwich](http://www.tobias-elze.de/pdfsandwich/). It provides a simple web interface to start a scan, monitor progress, and download the cleaned file.

Its main use is handling large, heavy files for reading on small devices such as e-readers. Removing images from PDF files (backgrounds, illustrations) and pre-processing character recognition greatly speeds up page loading across a wide range of e-reader models.

The PdfSandwich processing is straightforward:

    When a file is placed in /data/input, it is detected and the process is started by autoocr.
    The scanned PDF is processed with OCR to detect text elements and transcribe them as text. This scan is performed using the Tesseract OCR project.
    A PDF file is generated for each page, placing the text approximately where it appeared in the original document. These page PDFs are then merged.
    Most illustrations disappear. However, some diagrams may be preserved after processing.
    You can find the processed result in /data/output. It will also be downloadable directly via the interface.
