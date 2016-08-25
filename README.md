Tools for text extraction
===

This is a repository to collect and catalogue any text extraction tools we may want to use on inquiries.

It contains:
* Details of tools already tested, with installation instructions
* A history of our experience with those tools
* Instructions on how to suggest and trial a new tool
* Small, single PDF pages from various inquiries that can be useful for testing new tools

# Tools already tested
* PDFMiner
  * A tool to extract text from normal PDF files  
  * [Instructions for installation](http://www.unixuser.org/~euske/python/pdfminer/)
  * The command to convert a PDF to a text file using this tool is is `pdf2txt.py -o output.txt input.pdf`
* Apache PDFbox
  * A tool to extract text from normal PDF files
  * [Download](http://pdfbox.apache.org/download.cgi)
  * To use PDFbox:
    * Download the `.jar`file 
    * Run the command `java -jar pdfbox-app-2.y.z.jar ExtractText [OPTIONS] <inputfile> <outputfile>` (where `y`and `z`are the version numbers of the file you downloaded)
* Poppler
  * A tool to convert normal PDF files into `.txt` files
  * [Download and installation instructions](https://poppler.freedesktop.org/)
  * Once you have installed Poppler, run the command `pdftotext input.pdf` to output a `.txt` file of the same name in the same directory
* Google Vision
  * This is just a note to say that we tested Google Vision on some scanned documents (PDF files whose pages are scans of paper documents, not parsable text) with poor results.

# Comparison of tools
## PDFMiner vs. Apache PDFbox vs. Poppler
As an example of a comparison, we have tested PDFMiner and Apache PDFbox and Poppler on pages from:
* The Iraq Inquiry
* The Senate PSI Report into the Financial Crisis
* The Litvinenko Inquiry

In each case, Apache PDFbox showed noticeable advantages over PDFMiner (which was our default tool at the time) and some over Poppler.

As an example, **here is an original page from The Litvinenko Inquiry:**

![Original PDF](/screenshots/litvinenko-original.png)


**Now, here is the result of processing that page using PDFMiner:**


![PDFMiner page 1](/screenshots/litvinenko-pdfminer-1.png)
![PDFMiner page 2](/screenshots/litvinenko-pdfminer-2.png)
![PDFMiner page 3](/screenshots/litvinenko-pdfminer-3.png)


**Here it is processed using Poppler:**


![Poppler](/screenshots/litvinenko-poppler.png)


**And this is the result of processing that same page using Apache PDFbox:**


![PDFbox](/screenshots/litvinenko-pdfbox.png)

As you can see, PDFbox produces a much tidier output, without any of the significant superfluous space that PDFminer produces. Poppler is also quite tidy, but has the problem of putting the paragraph letters on a separate line to the paragraphs.

# Suggesting a new tool

If you have a tool to suggest, please open an issue in the [issue tracker](https://github.com/official-inquiries/tools/issues) for this repository.

If you would like to test the tool, we have a number of test pages in the `/test-pages/` directory from inquiries we would like to process. Including screenshots of the tool being used upon one or more of these in the issue would be very helpful.
