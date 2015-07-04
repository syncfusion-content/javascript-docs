# Documentation Guidelines

This section contains guidelines on naming files, sections, documents and other document elements.

> **NOTE**: Some of the items are marked as TODO which will be documented later.

## File naming Convention:
* All files should have `.md` extension.
* Separate words in file names should be hyphenated
* File names of the documents should have one or two-word names that describe the material covered in the document. 
* The full title of the document should be in the file name. 
* Phrase title and description in a way that users can determine what questions the text will answer, and material that will be addressed, without reading the content. This eases the time spent looking for answers, and improvises search/scanning, and possibly **SEO**.
* Provide titles and headers in the form of “Using foo” over “How to Foo.”

> For example, at the top section of each MD file,

> **Title :** Getting started with Chart widget for Syncfusion Essential JS 

> **Description :** File should describe or help the user how to create a chart, add series, enable tooltip and other functionalities.


## Markdown Syntax Guideline
* Follow the syntax mentioned in this [link](http://kramdown.gettalong.org/syntax.html) for most of the elements. There are some elements which need special styling or additional settings to do. Those have been described in the below topics.

## General
* Do not bold the words unnecessarily.
* Use [inline code style](http://kramdown.gettalong.org/quickref.html#inline-code) wherever it is possible to highlight the keywords, variables or one line code examples that come within the paragraph.

### Cross-reference
* Link within the page (if you have a title with space, use hyphen (-))

>	**Syntax**: \[Link name](#title-name)

>	**Example**: \[How to best read this user guide] (#how-to-best-read-this-user-guide)

* Link to the other page within the same platform documentation (using relative path). Tooltip text is optional.

> **Syntax**: \[Link name](relative path "Tooltip text")

> **Example**: \[Barcode](/js/Barcode/Getting-Started "Barcode Getting Started")

### Table
* Use the [kramdown syntax](http://kramdown.gettalong.org/syntax.html#tables) for creating the tables.
* **Advanced tables**: If you want to create an advanced tables with row span or column span or with code snippets, you can go with the standard html table syntax as described below.

> 1. start with `<table>` tag. Tag should be left indented and should have empty space in left side. 

> 2. Provide `TH` tag for table headers.

> 3. Code snippet can include within `<td> [code snippet] </td>`. Follow the same pattern like code snippet. 

* Do not provide table captions.
* You should use the below markdown syntax if you want to use markdown syntax within the html tags.

> \{{'<MarkdownSyntax>' | markdownify }}

> **Example**:

> \{{'\[syncfusion](http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js)'| markdownify }}



### Image

* Make sure image is not resized or blurred. 
* Caption is not necessary to provide for all images except for the case where we will have displayed more than one image.

* Adding Image : General markdown [syntax](http://kramdown.gettalong.org/syntax.html#images) will work.

> **Syntax**: \!\[Alt text](imagepath)

> **Example**: \!\[Alt text](/path/to/img.jpg)

* Adding image with caption:

> **Syntax**: \{% include image.html url="image path" caption="caption text"%}

> **Example**: \{% include image.html url="/js/DatePicker/Appearance-and-Styling_images/Appearance-and-Styling_img2.png" caption="caption text"%}

* Maximum width of the image should be 750 PX
* Maximum height of the image should be 550 PX
* Image format should be either .jpeg or .png format 
* Size of the image should not exceed  20 to 40 KB  
* If you are including the image to show an output of a code block, make sure the exact output can see the user also when he executes the same code snippet.

### Code Blocks
* Refer [this page](http://haisum.github.io/2014/11/07/jekyll-pygments-supported-highlighters/) for Code block syntax and supported languages.
* Align the code snippets using following free formatters:
	[JS](http://jsbeautifier.org/) ,
	[HTML](http://www.freeformatter.com/html-formatter.html)
* Remove extra lines added within the code block.
* Make sure the given code block runs without any issues.
* JSRender template syntax can be rendered by the following syntax :

> \{{"{{"}} code block here {{}}}}


### Bullet style
* Refer the syntax provided in the [Kramdown site](http://kramdown.gettalong.org/syntax.html#lists).
* Do not provide a line gap between the bullet points.

### Notes style
* Todo -> How to provide Important style
* Todo -> How to provide warning style
* Todo -> How to provide other topics which we would like to highlight. For ex, Notes or Tips.

### See also
* Todo -> How to add see also section? What is the syntax?

### JS Playground integration
* Todo -> How to link the JS Playground link on top of the each code blocks?

### Keyboard shortcuts
* Enclose the each keys with `<kbd>` tag to display the keys with different styling. For ex, <kbd>Ctrl</kbd>+<kbd>A</kbd> .
## API Reference Guideline

### Product Release Version variable 
* To add the version number in the documentation, use the below variables that replace the corresponding release version number while publishing. So that, always your content will contains the latest release version number. 

| Variable Name     	           | Output         | Description            					                             |  
| ---------------------------------|:--------------:|:----------------------------------------------------------------------:|  
| {{ site.releaseversion }}        | 13.2.0.29      |Syncfusion Essential Studio version                                     |  
| {{ site.20esreleaseversion }}    | 13.1200.0.29   |Syncfusion Essential Studio assemblies version for .NET Framework 2.0   |  
| {{ site.35esreleaseversion }}    | 13.1350.0.29   |Syncfusion Essential Studio assemblies version for .NET Framework 3.5   |  
| {{ site.40esreleaseversion }}    | 13.1400.0.29   |Syncfusion Essential Studio assemblies version for .NET Framework 4.0   |  
| {{ site.45esreleaseversion }}    | 13.1450.0.29   |Syncfusion Essential Studio assemblies version for .NET Framework 4.5   |  
| {{ site.451esreleaseversion }}   | 13.1451.0.29   |Syncfusion Essential Studio assemblies version for .NET Framework 4.5.1 |  
| {{ site.mvc3releaseversion }}    | 13.1300.0.29   |Syncfusion Essential Studio assemblies based on MVC Version 3.0         |  
| {{ site.mvc4releaseversion }}    | 13.1400.0.29   |Syncfusion Essential Studio assemblies based on MVC Version 4.0         |  
| {{ site.mvc5releaseversion }}    | 13.1500.0.29   |Syncfusion Essential Studio assemblies based on MVC Version 5.0         |  


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
    * _Essential chart has built in support for over 10 technical indicators_ - Correct
* Constantly review the document that you are writing to see if any words can be removed without changing the information conveyed.
* You can use a colon after the words "following" or "follows." 
* Use [American English](https://syncfusion.atlassian.net/wiki/display/SYNC/American+and+British+English+spelling+differences) and date formats.
    * Behavior vs Behaviour
* Prefer **present tense** always except in some special criteria to use other tenses.
    * You will have to send the corrupted word document for troubleshooting. - Incorrect
    * _Please send the corrupted word document for troubleshooting._ - Correct
* Avoid using gender specific words like she, he, him or her.
* When you first use an acronym in a document, you should write out the full term and enclose the acronym in parentheses immediately after the term 
    * This guide shows you how to configure the chart control within your favorite Integrated Development Environment (IDE)
* Use oxford comma when referring to a list of three or more items
    * The data visualization suite consists of Chart, Gauge, and Map.
* Always refer to the control name with proper casing
    * SfDataGrid vs Datagrid or Data Grid etc.
* Make sure you do not confuse with these [tricky words](https://syncfusion.atlassian.net/wiki/display/SYNC/Similar+sounding+words+-+Homophones).
* Always spell check using a tool like Microsoft Word.
 
### Structure of good documentation
* Getting started tutorials
* Write from a real world usage perspective
    * For example, customers would use DocIO for one of the following purposes
* Dynamically generate reports based on templates.
    1. Load Template
    2. Mail merge
    3. Save as Doc or PDF
* Document structure manipulation
    1. Load document
    2. Find a specific table 
    3. Read its contents
    4. Replace with another table
    5. Save changes
* Creating documents from code
    * Is there a reason why we need this in documentation since no end user would create the document from scratch instead of using a template since that option is a lot easier.
    * This can be documented as a side note under the "Dynamic document generation" section.
* Converting from one file format to another (DOC To PDF)
* Document best practices. For example, do we create an invoice from scratch or is it recommended to start from a template?
* Document the most common issues encountered.
* Link to demos where necessary.
* Let users edit sample code in playground.
* Possible workflow
    1. Create document outline
    2. Document first purely using bullet points
    3. Form sentences using language guidelines.
 
 
### External references
* <http://www.bartleby.com/141/> 
* <https://wiki.ubuntu.com/DocumentationTeam/StyleGuide/SpellingPunctuationGrammar> 
* <http://wiki.openbravo.com/wiki/Documentation_Style_Guide#Use_US_English> 
* <http://docs.basho.com/riak/latest/community/style-guide/>