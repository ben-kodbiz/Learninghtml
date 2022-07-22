# Lesson 2

Lesson two introduces a few more HTML tags and what is known as *inline styling*.

### Instructions
1. Open Notepad
2. Save the file as about.html
3. Make sure this file is in the same folder as your index.html file.
4. Using the example below, reproduce the webpage with your own content

**Need an idea?  Pick from these prompts:**
* You are marketing a new product. Tell the world about the product.
* You've started your own business.  What is it?  Give us some backstory on you, the founder and CEO.
* There is something important happening in the community that needs more awareness.  What is it?

**Criteria for the Lesson 2 webpage:**
* Must include a title
* Must include at least one hx (h1-h6) tag with at least one attribute (such as color or font)
* Must contain at least two images with at least two attributes each (such as width, height, alternative text, etc)
* One image must be contained within a FIGURE tag and have a caption
* Must contain at least one paragraph with a MARK tag within it
* At least one paragraph should be contained within a div
* The div must have an id and a class name
* Must include at least one link to index.html
* Must include at least one character entity
* Must include at least one video OR audio file

```HTML
<!doctype html>
<head>
	<title>My First Company Website</title>
</head>

<body>

<video
width="400" height="300"
poster=""
autoplay="autoplay"
controls="controls"
loop="loop">
<source src="assets/video.mp4" type="video/mp4">
<source src="assets/video.ogv" type='video/ogg; codecs="theora, vorbis"'>
Sorry, Your browser does not support HTML5 videos.
</video>

<h1 class="mainHeading" style="color: green; font-family: Cooper Black">Company Name</h1>

<figure>
<img src="assets/company.jpg" alt="logo" style="height:200px; width:auto" />
<img src="assets/shoe.jpg" alt="Nike Shoe" style="height:200px; width:auto"  />
<img src="assets/xbox.jpg" alt="xbox controller" style="height:200px; width:auto" />
<figcaption>Product Images</figcaption>
</figure>

<div id="welcomeMessage" class="welcome">
	<p>Welcome to <mark>the Chocolate Factory</mark>!  My name is <mark>Willy Wonka</mark>.</p>
</div>

<p><a href="index.html">For more information click here!</a></p>

<p> &phone; <b>Call us at 813-888-1234.</p>

</body>
</html>
```

## Details

* `<video></video>`
    * `<source src="..." type="...">`
        * This tag defines what the video file is/where it is stored.  You should include two source tags,
        placed between the video tags. One source should point to an .ogv file, and the other an .mp4 
        **When the browser loads a video, it plays the first compatible video file (.ogv or mp4).**
        Additionally, you should include a line under both source tags in case neither file loads:
        "Sorry, your browser does not support HTML5 Video." for example.
        * `<video> <source src="assets/newWave.mp4" type="video/mp4"> <source src="assets/newWave.ogv" type="video/ogg"></video>`
    * `width=""` and `height=""`
        * Specify a width and height for the video.  Place WITHIN the video tag.
        * `<video width="400" height="300">`
    * `autoplay="autoplay"`
        * Autoplay lets the video start on its own, as soon as the page loads.  Place WITHIN the video tag.
        * `<video autoplay="autoplay">`
    * `loop="loop"`
        * Loop continously plays the video over and over again, infinitely.  Place WITHIN the video tag.
        * `<video loop="loop">`
    * `controls="controls"`
        * Display controls for the viewer to stop/play the video.  Place WITHIN the video tag.
        * `<video controls="controls">`
    * `poster="..."`
        * Define an image to represent the video before it is played.  Place WITHIN the video tag.
        * `<video poster="hannah.jpg">`
    * `preload="none"`
        * PRELOAD is optional.  The default value is AUTO, which means the video loads when the entire page loads.
        * NONE means the video does not load when the page loads.
        * If the video autoplays when the page is loaded, then PRELOAD is not needed.
        * `<video preload="none">`
* `<h1 class="mainHeading"></h1>`
    * CLASSES may be assigned to any HTML tag.  Classes give elements a name, which makes it easy to style the document. The above header tag has been named 'mainHeading.'
* `<style ="color: green;">`
    * **Inline Styling** is not recommended, but occasionally used, and is great for learning the beginnings
    of **CSS (Cascading Style Sheets)**.  Pay close attention to the syntax.
    * **Property:** *attribute;*
    * Properties are defined keywords - you will learn many different ones!  Attributes are your "choice", or how you define the property.
    * `<p style="color: red;">` This text is red. `</p>` Anything outside the paragraph is normally formatted.
* `<style ="font-family: Arial;">`
* `<figure></figure>`
    * FIGURE is a way of grouping images together.  Multiple images between the figure tag are placed side-by-side.
* `<figcaption></figcaption>`
    * Set a caption under the grouping of images, such as "Product Images"
* `<mark></mark>`
    * Highlights any text contained within its tags. Can be nested within other paragraph and header tags.
* `<div></div>`
    * DIV is a way to divide up your content and page so it can be styled separately.  Think of DIV as a room in a 
    house - it's still part of the house, but might have a different "theme" or appearance.  
* `<div id="...">`
    * DIVs should be named, just like within a house we have names for rooms such as the kitchen or bedroom.
    Sometimes you willl need to **nest** your DIVs to give them extra styling power.  We will go into this more later, 
    but as an example, a kitchen might contain the dining room all in one. IDs are usually used with JavaScript to 
    make your web pages dynamic and interactive. DIVs may also be given both an ID and a CLASS name.

# Challenge 2

Check the Lesson 2 Challenge on Repl.it: https://repl.it/classroom/invite/CJuYkDU
