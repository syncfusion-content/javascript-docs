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

## General
* Do not bold the words unnecessarily.
* Use [inline code style](http://kramdown.gettalong.org/quickref.html#inline-code) wherever it is possible to highlight the keywords, variables or one line code snippets which comes within the paragraph.

## Hyperlinks
* Todo -> How to link the content within the page?
* Todo -> How to link to the other page in the documentation?

## Table
* Todo -> How to create a table and whatelse need to be instructed the content contributor
* Todo -> can we give code snippet within the table? if possible, how?
* Do not provide table captions.
* Provide TH tag for table headers.

## Image
* Make sure image is not resized or blurred.
* Todo -> how to include the image?
* Caption is not necessary to provide for all images except for the case where we will have displayed more than one image.
* Todo -> If we need to include the caption, how?
* Todo -> What is the minimum & maximum size?
* If you are including the image to show an output of a code block, make sure the exact output can see the user also when he executes the same code snippet.

## Code Blocks
* Align the code snippets using following free formatters:
	[JS](http://jsbeautifier.org/) ,
	[HTML](http://www.freeformatter.com/html-formatter.html)
* Remove extra lines added within the code block.
* Todo -> How to include the code block and what needs to be followed?
* Todo -> How to use JSRender template syntax in the code block?
* Make sure the given code block runs without any issues.

## Bullet style
* Todo -> How to provide numbering bullet style?
* Do not provide a line gap between the bullet points.

## Notes style
* Todo -> How to provide Important style
* Todo -> How to provide warning style
* Todo -> How to provide other topics which we would like to highlight. For ex, Notes or Tips.

## API Reference 

### Version information
* Todo -> how to specify when the property is added.
* Todo -> how to specify when the property is depricated.
* Todo -> how to specify when the property is changed.

### Naming Standards
* Use the JS API naming standards mentioned in the following page - [API Naming Standards](https://syncfusion.atlassian.net/wiki/display/JS/API+Naming+Standards)

## See also
* Todo -> How to add see also section? What is the syntax?

## JS Playground integration
* Todo -> How to link the JS Playground link on top of the each code blocks?

## Style Guide

This includes the local typesetting, English, grammatical, conventions and preferences that all documents in the manual should use. The goal here is to choose good standards, that are clear, and have a stylistic minimalism that does not interfere with or distract from the content. A uniform style will improve user experience and minimize the effect of a multi-authored document.

### Punctuation
* Use the Oxford comma. Oxford commas are the commas in a list of things (e.g. “something, something else, and another thing”) before the conjunction (e.g. “and” or “or.”).
* Do not add two spaces after terminal punctuation, such as periods.
* Place commas and periods inside quotation marks.

### Headings
* Use title case for headings and document titles. Title case capitalizes the first letter of the first, last, and all significant words.

### Verbs
Verb tense and mood preferences, with examples:

* **Avoid the first person.** For example do not say, “We will begin the backup process by locking the database,” or “I begin the backup process by locking my database instance.”
* **Use the second person.** “If you need to back up your database, start by locking the database first.” In practice, however, it’s more concise to **imply second person using the imperative**, as in “Before initiating a backup, lock the database.”
* When indicated, use the imperative mood. For example: “Backup your databases often” and “To prevent data loss, back up your databases.”
* The future perfect is also useful in some cases. For example, “Creating disk snapshots without locking the database will lead to an invalid state.”
* Avoid helper verbs, as possible, to increase clarity and concision. For example, attempt to avoid “this does foo” and “this will do foo” when possible. Use “does foo” over “will do foo” in situations where “this foos” is unacceptable.

### Referencing

* For API references (i.e. functions, operators, methods, settings) always reference only the **first occurrence** of the reference in a section. You should always reference objects, except in section headings.
* Structure references with the why first; the link second.

_For example, instead of this:_

refer the same steps mentioned here in the [manual method](/js/control-initialization#adding-syncfusion-widget-into-your-html-page) to add the Syncfusion datepicker widget into the HTML page.

_Type this:_
to add the Syncfusion datepicker widget into the HTML page, refer the same steps mentioned here in the [manual method](/js/control-initialization#adding-syncfusion-widget-into-your-html-page).

### General Formulations
* Contractions are acceptable insofar as they are necessary to increase readability and flow. Avoid otherwise.
* Make lists grammatically correct.
* Do not use a period after every item unless the list item completes the unfinished sentence before the list.
* Use appropriate commas and conjunctions in the list items.
* Typically begin a bulleted list with an introductory sentence or clause, with a colon or comma.
* Always write out units (e.g. “megabytes”) rather than using abbreviations (e.g. “MB”.)

### Structural Formulations
* Section headers are in title case (capitalize first, last, and all important words) and should effectively describe the contents of the section. In a single document you should strive to have section titles that are not redundant and grammatically consistent with each other.
* Use paragraphs and paragraph breaks to increase clarity and flow. Avoid burying critical information in the middle of long paragraphs. Err on the side of shorter paragraphs.
* Prefer shorter sentences to longer sentences. Use complex formations only as a last resort, if at all (e.g. compound complex structures that require semi-colons).
* Avoid paragraphs that consist of single sentences as they often represent a sentence that has unintentionally become too complex or incomplete. However, sometimes such paragraphs are useful for emphasis, summary, or introductions.
* As a corollary, most sections should have multiple paragraphs.
* For longer lists and more complex lists, use bulleted items rather than integrating them inline into a sentence.
* Do not expect that the content of any example (inline or blocked) will be self explanatory. Even when it feels redundant, make sure that the function and use of every example is clearly described.