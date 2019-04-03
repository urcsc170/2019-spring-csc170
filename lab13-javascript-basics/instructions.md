# Lab 13: JavaScript Basics
*Due: Monday, April 8, 2018*

For this lab, you will re-incorporate your **start.php** file (and rename it "index") to have it work like a normal index (home) page for your website.  On you index page you will incorporate two JavaScript behaviors (which will be very basic, but we'll spice them up in a later lab).

## Step 0 (prep): Get Two New Identically-sized Images

Find and prepare two new images

- [ ] The two new images must be related to your website’s topic
- [ ] The two new images must have identical height and width
- [ ] The two new images must have a width dimension of no less than 200px and no more than say about 300px

Preparing identically-sized images might take some extra work using software on your PC or Mac.

- On a PC, the application “Paint” comes with Windows and will work well enough
- On a Mac, the application “Preview” has “tools” that will work well enough
- The two new images must have filenames that comport to the rules for naming web files (all lower case, no spaces)

## Step 1: Copy Lab 12

- [ ] Make a copy of your Lab 12 - put it in a folder named **lab13**
- [ ] Add the two images you created in the previous step into the **lab13/images** folder

## Step 2: Create a Home Page

- [ ] Rename your **start.php** file to **index.php**
- [ ] Edit your **inc/nav.inc** file:
  - Add a menu item that links to the new **index.php** file
  - Have the text for the link say something like "Home" ...or something like that
  - Save and close the **inc/nav.inc** file
- [ ] Edit your **index.php** file:
  - Directly under the *nav.inc* remove the contents of the SECTION element with the  `class="lead"` (leave the SECTION tags there - just delete everything inside it)
- [ ] Add an H2 in the SECTION element - some kind of welcome message, something like this:<br> `<h2>Welcome to The World of William Shakespeare</h2>` <br>_(It doesn’t have to say, “Welcome to….”  You can be creative here)_
- [ ] Within the SECTION element, add a FIGURE element and a DIV like this:

```html
<section class="lead">
    
  <h2>Welcome to The World of William Shakespeare</h2>
  <figure>

  </figure>

  <div>

  </div>
    
</section><!--.lead-->
```



## Step 3: Add a Swappable Image

Continuing in the **index.php** file...

- [ ] Within the new FIGURE element, add a FIGCAPTION and an IMG tag to embed one of the new images from Step 0; something like this:

```html
<figure>
  <img src="images/______.jpg" alt="_________">
  <figcaption>Some words  - you write here</figcaption>
</figure>
```

…In the blanks (above) use whatever you named one of your new images in the SRC and write its description in the ALT

- [ ] Add a JavaScript **onmouseover** event to the image element to change the source (the “src”) to the other new image when a mouse hovers over that element
  - Remember to be careful with quotes inside the quotes!

- [ ] Add another JavaScript **onmouseout** event to the *same image element* to change the source (the “src”) to back to the original image when the mouse moves *out* from hovering over that element

Test the JavaScript events in a web browser.  When you load the index file into your web browser, you should see an image.  When you hover your mouse over it, it should change.  When you move your mouse away, it should change back to the original image.

## Step 4: Add Some Hidden Content

Still editing the **index.php** file...

- [ ] Insert two DIV elements within the DIV after the FIGURE element like this:

```html
<div>
    <div>
       
    </div>
    <div>
        
    </div>
</div>
```

- Add a button element that says “More…” between the two DIVs like this:

```html
<div>
    <div>
       
    </div>
    
    <button>More...</button>
    
    <div>
        
    </div>
</div>
```

- “Steal” some content from your ARTICLE and/or ASIDE (in the same file, below)
  - A good candidate is some “Introduction” content if you have one
  - You need at least two paragraphs with headings; insert the two paragraphs (and their headers preferably) into the two DIVs (respectively); something like this (using your content, not Shakespeare)

```html
<div>
	<div>
		<h3>About Shakespeare</h3>
		<p>William Shakespeare was an English poet...p>
	</div>
	<button>More...</button>
	<div>
		<h3>More About Shakespeare</h3>
		<p>His extant works, including...</p>
	</div>
</div>
```

- Delete the rest of the content on the page: the ARTICLE, ASIDE, and FOOTER 
  - Delete not only the contents of those elements, but the elements themselves too.

From an appearance standpoint, you should have something that looks like this:

![screen capture](media\figure1.png)

...when you hover your mouse of the image, it should change.  When you move your mouse away, it should change back.

The More... button doesn't do anything until we give it some power via JavaScript...

### Power the 'More...' Button

Continuing to edit the **index.php** file

- Add an ID to the BUTTON element
- Add an ID to the second DIV element (directly below the BUTTON element)

In the file system, in your **lab13** folder...

- Add a new folder named: **js**

- Create a file in the **js** folder named **scripts.js**

- Near the bottom of the Index page, just above the closing BODY tag, add an embedded JavaScript block using the `<script>` tag to connect the external JavaScript file named: **js/scripts.js**

  

Edit the **scripts.js** file.  Add this starter code (you can copy and paste this into your editor):

```js
//	*******************************************************
//	Toggle element to hide/show
//	*******************************************************
// Step 1: Get a handle on the clickable element and create a variable to hold it
var __________ = document.getElementById("__________");

// Step 2: Get a handle on the element to be toggled and create a variable to hold it
var __________ = document.getElementById("__________");

// Step 3: Set the default state of the element to be toggled; either "block" (showing) or "none" (hidden)
__________.style.display = 'none';

// Step 4: write the function to do the toggling (won't execute 'til called) - have it take-in an 'element' to toggle (note: there's nothing in this step to edit)
function toggleElement(e) { 

	// Step 4a: IF display:block, it must be showing, so hide it
	if (e.style.display == 'block') {
		e.style.display = 'none'
	} 		
	// Step 4b: ELSE it must be hidden, so show it
	else {
		e.style.display = 'block'
	}
}; 

// Step 5: Apply a "click listener" to the clickable element, and when the element is clicked, run the function on the element to be toggled
__________.addEventListener("click", function(){
	toggleElement(__________)
});
```

- [ ] In Step 1 and Step 2: replace the blanks with the IDs that you used in the HTML (on the BUTTON and the DIV) and create appropriately named variables
- [ ] Use the correct variables in the correct places in Step 3 and Step 5

Save and close all your files.

## Step 6: Upload, Test and Report your Work

If your home page works correctly:

- When you first load the webpage the second paragraph is NOT showing
- When you hover your mouse over the image, it changes
- When you move your mouse away from the image, it changes back
- When you click the “More…” button, the hidden paragraph appears
- When you click the “More…”button again, the paragraph disappears again

When you are done with your webpage, close everything and FTP your files to your account on the class web server:

In a web browser (any), go to this address to check your handiwork: 

**www.csc170.org/accountname/lab13/index.php**<br>(where “*accountname*” is your account name)

- Make sure the HTML and CSS pass their respective validators.
- In our CSC 170 Blackboard section in the Lab 13 assignment, post a link to your webpage to receive credit for this Lab.

