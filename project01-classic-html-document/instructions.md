# Project 1: Classic HTML Document

*Due: Thursday, February 28, 2019*

<hr>

Remembering that the original use of the web was to post academic research papers online, we will start a series of projects by replicating the type of documents that were created at that time.  In later projects: we will format our own document with CSS, and after that, we will stitch together multiple documents into multipage websites, complete with their own architecture, look & feel,and navigation.

This first step, Project 1, you will use NO formatting – you will do nothing to your HTML document to try and make it look nice.  The goal is to simply gather content, and mark it up semantically correct using HTML5 tags, and let the formatting be done automatically by the browser’s built-in styles.  

## Requirements

In this assignment, you will create an HTML document (a single page website) and FTP it to your account on the class web server.  

- The report can simply be a compilation of important facts and background information about the topic. You can lift complete sections of content from other sources if you properly cite its origins. 
- The report must be about an important **person** who has made or is making important contributions to the Internet, Web, the field of computer science, or society in general.
- Hint: you can go back to Wikipedia and get more content so long as you do *not* reuse the content you used for the lab assignments. 

**Step 1 (recommended):** create your report in any word processing format (e.g. MS Word).  (Note: you will *not* need to turn-in this part.)  Your document must contain a minimum of the following:

- At least 1400 **words** (Note: Nobody is going to count your words.  Just make you have a lot of content.  Your Project 2 will depend on it.)
- A proper **document outline** that contains lots of paragraphs
- At least two **images or diagrams** (more is better)
- A **data table** with at least three columns and five rows
- A **list of things**
- **Citations**, at least two, which you will turn into hypertext (so make sure you're including citations that refer to documents on the Web)

**Step 2:** replicate your report in HTML.  Your HTML document must contain a minimum of the following types of elements:

- **A proper HTML template** using the HTML5 specification.  (HEAD tags, BODY tags, et cetera)

- A **title** in the TITLE tag (in the HEAD) that says, "Project 1 - " ...followed by your topic, for example: `<title>Project1 - Marc Andreessen</title>`

- **A proper document structure** - you must use the appropriate HTML structural tags to create the document "scaffolding" in which all the content will go.  Be sure to use each structural tag in the way they were intended to be used. i.e. semantically correct.  

  - Typical structural HTML elements include:

    ```html
    <header></header>
    <main></main>
    <section></section>
    <article></article>
    <aside></aside>
    <footer></footer>
    ...and more 
    ```

    Look here for the full list and info on each tag: https://www.w3schools.com/html/html5_semantic_elements.asp

  - Do NOT use the same four structural elements in the same way we used them in the lab assignments!  (I.e. HEADER, ARTICLE, ASIDE, FOOTER ...you *must* do something different!) Remember: the *content* determines what tags you should use, not the other way around.

  - Note: you can use each structural HTML tag multiple times in any HTML document and nest them inside each other as appropriate for your content.  (Except the `main` tag - it has special rules; see here: https://www.w3schools.com/tags/tag_main.asp)

- You must use a **Level 1 Heading** that states the name of your topic, for example: `<h1>Marc Andreessen</h1>` <br>(Note: this will be the only Level 1 Heading you will use in this document.)

- **Multiple sections with their own titles** (i.e. a proper document outline) – you will format the section titles as Level 2 Headings; if there are more sub-sections, you can use Level3, Level 4, et cetera

- Lots of **paragraphs** of text.

- **Semantic markup** – any combination of inline elements like: strong, emphasis or any other valid HTML tag used properly wherever it makes semantic sense.  

- **A table**, in which you present “tabular data” only.

  - Required: in the opening table tag, use the attribute `border` to turn on borders to make it easier to see the table in your plain HTML document.
    - You'll remove that when we get to Project 2 and use CSS instead. But in the meantime, the validator might mark the "border" attribute with a warning or error, but in this case it's okay.  

- **Images** which should be appropriately sized for the document 

- **A list of things**, either unordered, ordered, or definition

  - You *can* use a list for your citations at the end of the document, but that does *not* count toward the requirement of "a list of things."  You need to have another list somewhere in the main content area of your document.

- **Citations (references)** to other online documents – you will use anchor tags to link directly to your references
  - You can use inline citations and/or citations at the end of the document.  (A combination of both would be nice.)
  - Note: you can also have old fashioned citations in MLA or ALA format in your document too; but there has to be at least two hyperlinks using anchor tags

NOTE: in your HTML document you can have lots of examples of each of the elements listed above, but the minimum is at least one of each.

### Location

- Your one-page web site must be mounted on the class web server, within your account where you’ll create a new folder that must be exactly this: **project1** …all lower case, spelled exactly like that.
- The name of the HTML document must be exactly this: **index.html** (*not* **start**.html this time) …all lower case, spelled exactly like that. 
- The image you use must be in a subdirectory of the **project1** folder, and it must be named **images** 
- Validate the HTML file (**http://validator.w3.org/**)

## Report your work

To receive credit for this lab: in our CSC 170 Blackboard section, in the the "Projects" area, in the **Project 1** assignment, post a link to your webpage.