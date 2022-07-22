# Lesson 1

In Lesson one you will learn basic HTML5 tags to create a structure and content for your webpage. 

### Instructions
1. Open Notepad, or your favorite text editor.
2. Save the file as index.html
3. Using the example below, reproduce the webpage with your own content

**Need an idea?  Pick from these prompts:**
* Make the page about something you care about:
    * Types of Music
    * Favorite Sport
    * Shoes
    * Social Issues
* Make a biography about yourself, your pet, or role model.


**Criteria for the Lesson 1 webpage:**
* Must include a title
* Must use at least two hx (h1-h6) tags
* Must contain at least one image
* Must contain at least one paragraph
* Must include at least one link
* Must include at least two character entities


```html
<!doctype html>
<html>
    <head>
        <title>78704 Pet Care</title>
    </head>
    <body>
        <h1>Pet Care</h1>
        <img src="assets/dog.jpg" />
        <p>Your dog is a friend for life. Why not provide the best care possible?</p>     
        <p>Make sure your pet has plenty of <i><b>fresh water</b></i> during hot weather.</p>
        <p><a href="http://www.google.com">Click here for more information</a></p>
        <br/>
  &copy; Student Name 2017
    </body>
</html>
```
## Details
The code above produces a simple webpage about Pet Care.  The page includes an image, heading tags, paragraphs, and a character entity symbol.  For information about these tags, see the list below.

* `<!doctype html>`
    * DOCTYPE declares the document type so the browser can determine what language the document is using.  In this case, we are using HTML, or **HyperText Markup Language**  
* `<head><head>`
    * Head tags go at the top of the HTML document.  The head is used for defining the document style and linking to scripts.  Usually the stuff you type in here won't be seen on the page.  Think of it as "behind the scenes".
* `<title></title>`
    * Title tags are the text that shows at the top of your **browser window**, not within the document.  This is also "behind the scenes" and is **nested** within the head tags.  Nested simply means placing a tag within another.
* `<meta charset="">`
    * Meta tags, short for metadata, define some preliminary characteristics of your webpage. The above example allows you to select the type of character encoding that your webpage will employ. Similar to title tags, this tag is located between the head tags. For additional uses of the meta tag, please navigate to https://www.w3schools.com/tags/tag_meta.asp. 
* `<body></body>`
    * Anything you put between the body tags is your actual content, which displays on the webpage document. 
* `<h1></h1>` through `<h6></h6>`
    * Tags h1-h6 provide a variety of header sizes.  h1 is the largest and h6 is the smallest.
* `<b></b>` and `<strong></strong>`
    * Text placed between either sets of these tags is **bolded**  
* `<i></i>` and `<em></em>`
    * Text placed between either sets of these tags is *italicized*
* `<img src="" />`
    * Between the quotes, place the address to an image!  You can do a google search for an image you like, click on it, then copy/paste the web address.  Make sure the web address you're pasting ends with .jpg .jpeg or .png.  This tag is **self-closing** and doesn't have a pair to close it.  Instead, finish the tag simply with a `/>`.
* `<img ... alt="" />`
    * The alt attribute, which stands for alternative text, allows you to add a description to your image. This description pops up when a user hovers over the image. Whenever including an `<img>` tag, make sure to include an alt attribute and a description between the quotes.
* `<a href="" />` Your clickable text `</a>`
    * Link to other pages or websites using the ANCHOR <a> tag.  HREF stands for
Hypertext REFerence, which is the techy way of saying "Point to this website".  Put
the website address between quotes, and the text you'd like to display (the "Click Me" text) between the <a> tags.
* `<br/>`
    * Another self-closing tag, this is a **line break**.  If you did not need a new paragraph, but simply wanted to insert a new line, use this command.
* `<p></p>`
    * Paragraph tags wrap around blocks of text.  Each paragraph will have a space between the next paragraph.
* `&copy;` and other character entities
    * **Character Entities** are a cool way to use icons on your site.  They begin with the & symbol and end with the ; symbol.  Check out all the different character entities and their code here -https://dev.w3.org/html5/html-author/charref


# Challenge 1

Check the Lesson 1 Challenge on Repl.it: https://repl.it/classroom/invite/CJuYkDU
