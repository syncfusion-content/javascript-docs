# Contents

* [General guidelines](#General guidelines)

# Documentation Guidelines

This section contains guidelines on naming files, sections, documents and other document elements.

## File naming Convention:
* All files should have a .md extension.
* Separate words in file names with hyphens (i.e. -.)
* For most documents, file names should have a brief one or two word name that describes the material covered in the document. 
* The full title of the document should be in the file name. 
* Phrase title and description so users can determine what questions the text will answer, and material that will be addressed, without needing them to read the content. This shortens the amount of time that people spend looking for answers, and improvise search/scanning, and possibly “SEO.”
* Prefer titles and headers in the form of “Using foo” over “How to Foo.”

For ex, In the top section of each MD file,

**Title :** Getting started with Chart widget for Syncfusion Essential JS 

**Description :** How to create a chart, add series, enable tooltip and other functionalities.


## Markdown Syntax Guideline
* Follow the syntax mentioned in this [link](http://kramdown.gettalong.org/syntax.html) for most of the elements. There are some elements which need special styling or additional settings to do. Those have been described in the below topics.

## General
* Do not bold the words unnecessarily.
* Use [inline code style](http://kramdown.gettalong.org/quickref.html#inline-code) wherever it is possible to highlight the keywords, variables or one line code snippets which comes within the paragraph.
* Todo -> How to highlight the keyboard shortcuts like this? [Stackoverflow](http://meta.stackexchange.com/questions/26207/how-can-i-format-as-keyboard-keys)

### Cross-reference
* Todo -> How to link the content within the page?
* Todo -> How to link to the other page in the documentation?

### Table
* Todo -> How to create a table and whatelse need to be instructed the content contributor
* Todo -> can we give code snippet within the table? if possible, how?
* Do not provide table captions.
* Provide TH tag for table headers.

### Image
* Make sure image is not resized or blurred.
* Todo -> how to include the image?
* Caption is not necessary to provide for all images except for the case where we will have displayed more than one image.
* Todo -> If we need to include the caption, how?
* Todo -> What is the minimum & maximum size?
* If you are including the image to show an output of a code block, make sure the exact output can see the user also when he executes the same code snippet.

### Code Blocks
* Align the code snippets using following free formatters:
	[JS](http://jsbeautifier.org/) ,
	[HTML](http://www.freeformatter.com/html-formatter.html)
* Remove extra lines added within the code block.
* Todo -> How to include the code block and what needs to be followed?
* Todo -> How to use JSRender template syntax in the code block?
* Make sure the given code block runs without any issues.

### Bullet style
* Todo -> How to provide numbering bullet style?
* Do not provide a line gap between the bullet points.

### Notes style
* Todo -> How to provide Important style
* Todo -> How to provide warning style
* Todo -> How to provide other topics which we would like to highlight. For ex, Notes or Tips.

### See also
* Todo -> How to add see also section? What is the syntax?

### JS Playground integration
* Todo -> How to link the JS Playground link on top of the each code blocks?

## API Reference Guideline

### Version information
* Todo -> how to specify when the property is added.
* Todo -> how to specify when the property is depricated.
* Todo -> how to specify when the property is changed.

### Naming Standards
* Use the JS API naming standards mentioned in the following page - [API Naming Standards](https://syncfusion.atlassian.net/wiki/display/JS/API+Naming+Standards)



## Style Guide

### General guidelines
* Remember that no documentation is better than poor quality documentation.
* Also, remember that "Less is more" when it comes to technical documentation.
* Imagine that  every word takes up unnecessary space so constantly look for words that can be removed. Please note that this is different from not writing anything at all. We still need to convey the maximum possible information using the minimum possible words. 
* Do not repeat content from other sections of documentation. Each section should serve a purpose and don’t let it overlap.
  * For example, don’t talk about all the possible parameters that a method can take, just point to the class reference.
* Avoid any form of marketing content.
* Do not explain code.
  * For example, here we are instantiating the chart using the overload that takes a string and a number, then we..
* Code samples should be accompanied by text that provides additional insights. 
  * For example, DateTime axis has been used here but the chart also has built-in support for handling several other data types (link to other sections of user guide or API reference)
* Write content from an user perspective and not from the developer or product perspective.
* Constantly check the flow of the document as you write it. Users shouldn’t feel lost.
* Write documentation keeping the target audience in mind. In our case, we need to fix a specific level of technical user. 
  * For example, we have to assume that the user would know how to create a project in Visual Studio and add reference to the required assemblies


### Referencing

* For API references (i.e. functions, operators, methods, settings) always reference only the **first occurrence** of the reference in a section. You should always reference objects, except in section headings.
* Structure references with the why first; the link second.

_For example, instead of this:_

refer the same steps mentioned here in the [manual method](/js/control-initialization#adding-syncfusion-widget-into-your-html-page) to add the Syncfusion datepicker widget into the HTML page.

_Type this:_
to add the Syncfusion datepicker widget into the HTML page, refer the same steps mentioned here in the [manual method](/js/control-initialization#adding-syncfusion-widget-into-your-html-page).


### Things to avoid
* Remove all out of date content
* Ensure that there are no missing steps in a tutorial. Also, ensure that all code in tutorials are working.
* Avoid having large amounts of text without accompanying code
* Incomplete API documentation makes the product look immature.
 
### General English guidelines
* Use the second person instead of first person
  * We will now see how to create a line chart - Incorrect
  * _You can create a line chart as shown below_ - Correct
* Do not use a period after every item in a list
* Write units in words
  * _50 megabytes_  - Correct
  * 50 MB - Incorrect
* Each paragraph should only talk about one topic. Each sentence should only talk about one idea.
* Each sentence should have less than 25 words. 
* Write in a neutral tone without marketing content
  * Essential chart has built in support for over 10 powerful technical indicators - Incorrect
  * Essential chart has built in support for over 10 technical indicators - Correct
* Constantly review the document that you are writing to see if any words can be removed without changing the information conveyed.
* You can use a colon after the words "following" or "follows." 
* Use American English and date formats.
  * Behavior vs Behaviour
* Prefer present tense to past tense
  * You will have to send the corrupted word document for troubleshooting. - Incorrect
  * Please send the corrupted word document for troubleshooting. - Correct
* Avoid using gender specific words like she, he, him or her.
* When you first use an acronym in a document, you should write out the full term and enclose the acronym in parentheses immediately after the term 
  * This guide shows you how to configure the chart control within your favorite Integrated Development Environment (IDE)
* Use oxford comma when referring to a list of three or more items
  * The data visualization suite consists of Chart, Gauge, and Map.
* Always refer to the control name with proper casing
  * SfDataGrid vs Datagrid or Data Grid etc.
* Always spell check using a tool like Microsoft Word.
 
### Structure of good documentation
* Getting started tutorials
* Write from a real world usage perspective
  * For example, customers would use DocIO for one of the following purposes
* Dynamically generate reports based on templates.
  * Load Template
  * Mail merge
  * Save as Doc or PDF
* Document structure manipulation
  * Load document
  * Find a specific table 
  * Read its contents
  * Replace with another table
  * Save changes
* Creating documents from code
  * Is there a reason why we need this in documentation since no end user would create the document from scratch instead of using a template since that option is a lot easier.
  * This can be documented as a side note under the "Dynamic document generation" section.
* Converting from one file format to another (DOC To PDF)
* Document best practices. For example, do we create an invoice from scratch or is it recommended to start from a template?
* Document the most common issues encountered.
* Link to demos where necessary.
* Let users edit sample code in playground.
* Possible workflow
  * Create document outline
  * Document first purely using bullet points
  * Form sentences using language guidelines.
 
 
### External references
* <http://www.bartleby.com/141/> 
* <https://wiki.ubuntu.com/DocumentationTeam/StyleGuide/SpellingPunctuationGrammar> 
* <http://wiki.openbravo.com/wiki/Documentation_Style_Guide#Use_US_English> 
* <http://docs.basho.com/riak/latest/community/style-guide/>