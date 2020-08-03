# addpagenum.py

# About
This is a simple Python script to add page numbers to a PDF file.

# Prerequisites
Python 3.6 or later - It uses f-strings.
pip-install:

    pip install reportlab
    pip install pdfrw

# Usage

    python addpagenum.py <pdf filename>

A new PDFfile w/ page numbers, filename_pgn.pdf will be created.

ReportLab's default page size is A4.  If you'd like to change it to, for example, letter, you'll need to modify a little:

    canvas = Canvas(output_file, pagesize=letter)

You can also change these:

    footer_text = f"{page_num}/{len(pages)}"
    canvas.setFont('Times-Roman', 14)
    canvas.drawString(290, 10, footer_text)

Note that x=290, y=10 are from bottom-left corner of a page.


# Acknowledgement
I borrowed most of the ideas from this stackoverflow Q&As.

https://stackoverflow.com/questions/28281108/reportlab-how-to-add-a-footer-to-a-pdf-file

