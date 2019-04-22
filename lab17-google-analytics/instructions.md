# Lab 17: Google Analytics
*Due: Thursday, April 25, 2019*

NOTE: there are a lot of unknown steps in this lab assignment because you're using online, off-the-shelf products that may change their steps and procedures whenever they want.  Just keep in mind, that the goal of this lab assignment is to (#1) practice installing Google Analytics, and (#2) practice creating an XML Sitemap and installing it.  

## Step 1: Login to Google Analytics

- Go to **www.google.com/analytics**
- Create a Google Analytics account using your UR email address
  - If you're already using Google Analytics, skip to Step 3
  - If you created an UR alias, don't use that.  Use the actual UR address
  - Alternatively, you can use another Google-registered email address

## Step 2: Sign up

- Assuming you've never used Google Analytics before, you'll see the **Sign up** button. Click it.
- In Google Analytics, setup your account and enter an **Account Name**.  Use: *your name* (which of course, should be your name)

## Step 3: Setting up a New Property

Next you will create a "property" (which is what Google calls a website) that points to your CSC 170 **Project 2 webpage** that you've installed on the webserver. To prepare for this step, in another browser window, open your Project 2 webpage and copy the Project 2 URL to your clipboard to ensure you get it exactly right.

- In the "Setting up your property" section, enter a **Website Name**. Use:  **Your Project 2 topic**  ...where *your project 2 topic* is whatever your project 2 is about.
- Enter (paste) into the **Website URL** field, the full web address of your Project 2 Change the **Reporting Time Zone** to **(GMT-05:00) Eastern Time**
- Leave all other settings as-is, scroll down and click the **Get Tracking ID** button.
- Accept the Terms and Conditions

## Step 3: Get and Insert the Tracking Code your Project 2

Here you will copy the tracking code from Google Analytics and paste it into the HTML code of your Project 2. Be prepared to edit your Project 2 index.html file.

- Copy the **Tracking Code** to your computer's clipboard.<br>*The "tracking code" is that entire JavaScript snippet, including the opening and closing `<script>` tags – not just the UA number.*

- Open your Project 2 index.html file in a text editor.

- [ ] Paste the tracking code into the bottom of your HTML, just *above* the closing `</body>` tag.

  - Note: Google says to put the tracking code in the HEAD of your code.  That's okay ...just not the Professor's preference for reasons explained in a previous lecture.

- [ ] Save the HTML file and re-upload it to the web server.

## Step 4: Browse your Account

- In Google Analytics, navigate to your new account/view to see the dashboard ("Home")

Data will start coming-in to your account immediately or soon. (Visit your own Project 2 from time to time over the next day to make sure there's some data for Google to record.)

# Part II: Google Webmaster Tools

## Step 1: Login to Google Webmaster tools

- Go to **www.google.com/webmaster/tools**

Using the same credentials of your Google-registered email address (from Part I), login to Google Webmaster tools.

## Step 2: Get the URL of your Project 2

You must make sure you get the right URL, so follow these steps...

- Open another browser window or tab, and go to your Project 2 on the web server
- When you see your Project 2, copy the web address to your computer's clipboard.

## Step 3: Add Project 2 to Google Webmaster Tools

- Toggle back to Google Webmaster Tools and click the **ADD A PROPERTY** button. Paste the URL from your Project 2 into the text field and then click **Add**
- Assuming you've successfully added a tracking code to your Project 2 **index.html** file, when you get to the Verify page, simply click the **VERIFY** button, then click **Continue** on the confirmation page.

## Step 4: Create a Sitemap

- Leaving the web page pointed to Google Webmaster Tools open, start another browser window or tab, and go to: **www.xml-sitemaps.com**
- Paste the web address of your Project 2 in the **Your Website URL** box.
- Scroll down to the **Start** button and click it
- Click the **VIEW SITEMAP DETAILS** button and then the **DOWNLOAD YOUR XML SITEMAP FILE** button
- Depending on the web browser you're using, the file (your sitemap) will download to your computer. (Take note of where it's downloading – you'll need to retrieve it.)

## Step 5: Upload your Sitemap

- Open an FTP tool and login to your account on the web server
- Navigate to your Project 2 files
- Upload the **sitemap.xml** file you created in Step 4 to the "webroot" (the folder named **project2**) on the web server

## Step 6: Register your Sitemap

- Go back to the Site Dashboard in Google Webmaster Tools
- Click the **Sitemaps** bar (the third column)
- On the Sitemaps page, click the button: **ADD/TEST SITEMAP**
- In the pop-up, type-in **sitemap.xml**
- Click the **Submit Sitemap** button
- Refresh the webpage you're looking at

If you received no error messages, you're done. Google will do the rest.

## Step 7: Report your work

To receive credit for this lab:

- In our Blackboard section, in the Lab 17 assignment, (re)post a link to your **Project 2** webpage.