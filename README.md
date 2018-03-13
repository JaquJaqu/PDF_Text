# PDF_Text
# Data Collection: Tables from Academic Papers (PDF Form)

## Explanation of Notebook

This notebook was a project for my internship with Earth Economics. I was asked to gather data about wild rice harvesting throughout the Native American tribes of Minnesota. Everything I found was in the form a report (PDF), either from the Minnesota Department of Natural Resources (MNDNR) or from one of the tribal agencies. The PDF below, had enough data that it made more sense to transfer it to text in Python and use regular expressions to separate it accordingly.

*The table I am turning into a csv starts on page 57 (numbered 54 on the page), which since the page iterator starts at 0, will be started at 56.*

## Explanation of Process

So the basic structure in order for data to be read as a csv is that each row must be separated by a newline character, each column in each row separated by a comma. In addition, there needs to be a text delimiter so that a chunk of text can be taken together no matter what characters are in the string. 

It is visible in the PDF above that it *looks* like it is already in proper csv format, but a PDF has the text printed on it, so it doesn't have any systematic structure to it, when it is converted to text.

The first step in this notebook will be to use the PyPDF2 library to read the desired pages of the PDF into text format. After that, it will be a matter of understanding the text output in this particular example and designing substitutions using python's reguar expressions library (re) to rearrange the unstructured text into a csv format.

Additionally, throughout this notebook, I will explain the idea behind the different methods I am using in the regular expressions library to make the approprite substitutions. A great website that I used to test regular expression methods is <a href = 'https://regex101.com/', target = '_blank'>Regex101</a>
