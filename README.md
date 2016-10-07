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

```
Part 3 | Chapters 1 to 5 | Alexander Litvinenko

 

Transfer to UCH and treatment there 
3.127  As noted above, Mr Litvinenko was transferred to UCH late at night on 17 November. 
He was an inpatient there for a little less than a week before his death on 23 November. 
3.128  I  heard  oral  evidence  about  Mr  Litvinenko’s  medical  treatment  at  UCH  from 
 
Dr Amit Nathwani, a consultant haematologist at that hospital.135 As with Dr Virchis, I 
also admitted into evidence the relevant medical notes.136 

 

 

 

 

 

 

3.129  In summary: 

 

a.   Following Mr Litvinenko’

 

treatment with Prussian blue and reported feeling much better 
had started 

 

s arrival at UCH, he seemed to be responding well to the 
since the treatment 

b.   Professor John Henry, an internationally renowned toxicologist with an interest in 
s treatment. He died 
rare poisons, became involved in advising on Mr Litvinenko’
in 2007, but statements that he had given to the police were read into the record 

 

c.   Professor Henry stated that he had received a telephone call from Mr Goldfarb 
on  17  November.  They  discussed  Mr   Litvinenko’s  case  and  Mr   Goldfarb  told 
Professor Henry that Mr  Litvinenko had been poisoned by thallium.137 Professor 
Henry visited Mr Litvinen
ko at UCH on 18 November and examined him with the 
agreement of the haematology team. Professor Henry stated that he agreed with 
the diagnosis of thallium poisoning138 and Mr  Litvinenko continued to be treated 
with Prussian blue 

 

 

 

 

 

d.   Despite  the  early  improvement  in  Mr  Litvinen

ko’s  symptoms,  he  began  to 
vomit  blood;  and  Dr  Nathwani  thought  that 
this  might  be  an  adverse  reaction 
to one of the antibiotics with which he had been treated.139 Medical staff were 
also concerned that Mr Litvinenko appeared 
to have an irregular heartbeat, his 
temperature was raised, he continued to vomit and he had abdominal pain.140 An 
(cid:72)(cid:79)(cid:72)(cid:70)(cid:87)(cid:85)(cid:82)(cid:70)(cid:68)(cid:85)(cid:71)(cid:76)(cid:82)(cid:74)(cid:85)(cid:68)(cid:80)(cid:3)(cid:11)(cid:40)(cid:38)(cid:42)(cid:12)(cid:3)(cid:70)(cid:82)(cid:81)(cid:191)(cid:85)(cid:80)(cid:72)(cid:71)(cid:3)(cid:68)(cid:81)(cid:3)(cid:76)(cid:85)(cid:85)(cid:72)(cid:74)(cid:88)(cid:79)(cid:68)(cid:85)(cid:3)(cid:75)(cid:72)(cid:68)(cid:85)(cid:87)(cid:69)(cid:72)(cid:68)(cid:87)(cid:17)141  Dr Nathwani felt 
that 
he and his colleagues were in “uncharted territory” with the suspected thallium 
poisoning. Dr Nathwani 
closely and 
considered the possibility of transferring him to a high dependency or intensive 
care unit (ICU) where his heart rate could be monitored continuously142 

therefore wanted to monitor Mr Litvinenko 

 

 

 

 

e.   On  19  November,  a  bed  became  available  for  Mr  Litvinenko 

on  the  ICU. The 
police expressed concerns as to security with regard to a transfer to the ICU. But 
Dr Nathwani decided that 
Mr  Litvinenko should be moved for his own well being; 
he was transferred to the ICU later that evening143  

 

 

f.   Dr Nathwani assessed Mr Litvinenko’

 

 

concerned  about  Mr  Litvinenko’

 

s condition again on 20 November. He was 
s  bone  marrow  failure  and  raised  temperature 

  
  
  
  
  
  
  
  
  

135 Nathwani 18/93­129 
136 INQ006652 
137 Henry 18/132 
138 Henry 18/137 
139 Nathwani 18/99­100 
140 Nathwani 18/101 
141 Nathwani 18/103 
142 Nathwani 18/103­105 
143 Nathwani 18/107­108 

37 

```

**Here it is processed using Poppler:**
```
Part 3 | Chapters 1 to 5 | Alexander Litvinenko

Transfer to UCH and treatment there 
3.127 As noted above, Mr Litvinenko was transferred to UCH late at night on 17 November. 
 
He was an inpatient there for a little less than a week before his death on 23 November. 
3.128 I  heard  oral  evidence  about  Mr   Litvinenko’s  medical  treatment  at  UCH  from  
135 
 As with Dr Virchis, I 
 
Dr Amit Nathwani, a consultant haematologist at that hospital.
 
136 
also admitted into evidence the relevant medical notes.
3.129 In summary: 
a.   Following Mr Litvinenko’
 
s arrival at UCH, he seemed to be responding well to the 
treatment with Prussian blue and reported feeling much better 
 
since the treatment 
had started 
b.   Professor John Henry, an internationally renowned toxicologist with an interest in 
rare poisons, became involved in advising on Mr Litvinenko’
 
s treatment. He died 
in 2007, but statements that he had given to the police were read into the record 
c.   Professor Henry stated that he had received a telephone call from Mr Goldfarb 
 
on  17  November.  They  discussed  Mr   Litvinenko’s  case  and  Mr   Goldfarb  told 
Professor Henry that Mr   Litvinenko had been poisoned by thallium.137  Professor 
Henry visited Mr Litvinen
 
ko at UCH on 18 November and examined him with the 
agreement of the haematology team. Professor Henry stated that he agreed with 
the diagnosis of thallium poisoning138  and Mr   Litvinenko continued to be treated 
with Prussian blue 
d.   Despite  the  early  improvement  in  Mr   Litvinenko’s  symptoms,  he  began  to 
vomit  blood;   and  Dr   Nathwani  thought  that  this  might  be  an  adverse  reaction 
to  one  of  the  antibiotics  with  which  he  had  been  treated.139  Medical  staff  were 
also concerned that Mr Litvinenko appeared 
to have an irregular heartbeat, his 
 
temperature was raised, he continued to vomit and he had abdominal pain.140 An 
141 
that 
 Dr Nathwani felt 
 
he and his colleagues were in “uncharted territory” with the suspected thallium 
poisoning.  Dr   Nathwani  therefore  wanted  to  monitor  Mr   Litvinenko  closely  and 
considered the possibility of transferring him to a high dependency or intensive 
care unit (ICU) where his heart rate could be monitored continuously142 
e.   On  19  November,  a  bed  became  available  for  Mr   Litvinenko  on  the  ICU.  The 
police expressed concerns as to security with regard to a transfer to the ICU. But 
Dr Nathwani decided that 
 
Mr  Litvinenko should be moved for his own well being; 
he was transferred to the ICU later that evening143  
f.  

Dr Nathwani assessed Mr Litvinenko’
 
 
s condition again on 20 November. He was 
concerned  about  Mr   Litvinenko’s  bone  marrow  failure  and  raised  temperature 

135   

Nathwani 18/93­129 
INQ006652 
137   
Henry 18/132 
138   
Henry 18/137 
139   
Nathwani 18/99­100 
140   
Nathwani 18/101 
141   
Nathwani 18/103 
142   
Nathwani 18/103­105 
143   
Nathwani 18/107­108 
136   

37 
```

**And this is the result of processing that same page using Apache PDFbox:**
```
37 
Part 3 | Chapters 1 to 5 | Alexander Litvinenko
  

  
Transfer to UCH and treatment there 
3.127  As noted above, Mr Litvinenko was transferred to UCH late at night on 17 November. 
He was an inpatient there for a little less than a week before his death on 23 November. 
3.128  I  heard  oral  evidence  about  Mr Litvinenko’s  medical  treatment  at  UCH  from
Dr Amit Nathwani, a consultant haematologist at that hospital.135 As with Dr Virchis, I 
also admitted into evidence the relevant medical notes.136 
3.129  In summary: 
a.  Following Mr Litvinenko’s arrival at UCH, he seemed to be responding well to the 
treatment with Prussian blue and reported feeling much better since the treatment 
had started 
b.  Professor John Henry, an internationally renowned toxicologist with an interest in 
rare poisons, became involved in advising on Mr Litvinenko’s treatment. He died 
in 2007, but statements that he had given to the police were read into the record 
c.  Professor Henry stated that he had received a telephone call from Mr Goldfarb 
on  17  November.  They  discussed Mr  Litvinenko’s  case  and Mr Goldfarb  told 
Professor Henry that Mr Litvinenko had been poisoned by thallium.137 Professor 
Henry visited Mr Litvinenko at UCH on 18 November and examined him with the 
agreement of the haematology team. Professor Henry stated that he agreed with 
the diagnosis of thallium poisoning138 and Mr Litvinenko continued to be treated 
with Prussian blue 
d.  Despite  the  early  improvement  in  Mr  Litvinenko’s  symptoms,  he  began  to 
vomit  blood;  and Dr Nathwani  thought  that  this might  be  an  adverse  reaction 
to one of  the antibiotics with which he had been  treated.139 Medical staff were 
also concerned that Mr Litvinenko appeared to have an irregular heartbeat, his 
temperature was raised, he continued to vomit and he had abdominal pain.140 An 
141  Dr Nathwani felt that 
he and his colleagues were in “uncharted territory” with the suspected thallium 
poisoning. Dr Nathwani  therefore wanted  to monitor Mr Litvinenko closely and 
considered the possibility of transferring him to a high dependency or intensive 
care unit (ICU) where his heart rate could be monitored continuously142 
e.  On 19 November,  a bed became available  for Mr Litvinenko on  the  ICU. The 
police expressed concerns as to security with regard to a transfer to the ICU. But 
Dr Nathwani decided that Mr Litvinenko should be moved for his own well being; 
he was transferred to the ICU later that evening143  
f.  Dr Nathwani assessed Mr Litvinenko’s condition again on 20 November. He was 
concerned  about Mr  Litvinenko’s  bone marrow  failure  and  raised  temperature 
135 Nathwani 18/93­129 
136 INQ006652 
137 Henry 18/132 
138 Henry 18/137 
139 Nathwani 18/99­100 
140 Nathwani 18/101 
141 Nathwani 18/103 
142 Nathwani 18/103­105 
143 Nathwani 18/107­108 
```

As you can see, PDFbox produces a much tidier output, without any of the significant superfluous space that PDFminer produces. Poppler is also quite tidy, but has the problem of putting the paragraph letters on a separate line to the paragraphs.

# Suggesting a new tool

If you have a tool to suggest, please open an issue in the [issue tracker](https://github.com/official-inquiries/tools/issues) for this repository.

If you would like to test the tool, we have a number of test pages in the `/test-pages/` directory from inquiries we would like to process. Including screenshots of the tool being used upon one or more of these in the issue would be very helpful.
