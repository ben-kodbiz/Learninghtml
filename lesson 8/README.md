# Lesson 8.1

**What is JavaScript?  JavaScript adds interactivity to your website!**
In Lesson 8.1 we cover a brief introduction to JavaScript and important concepts.

### Instructions
1. Open Notepad, or your favorite text editor.
2. Save the file as calculator.html
3. Using the example below, reproduce the webpage with your own content

**Criteria for the Lesson NUMBER webpage:**
* Create a form named "Calculator"
* Add all the common calculator buttons to your calculator
* Style the calculator using an external stylesheet named style.css
* Use onClick to trigger JavaScript reactions for the form

```HTML5
<html>
<head>
<title>HTML Calculator</title>
<link rel = "stylesheet" type = "text/css" href = "style.css" />
</head>
<form name="calculator" >
<input type="button" value="1" onClick="document.calculator.ans.value+='1'">
<input type="button" value="2" onClick="document.calculator.ans.value+='2'">
<input type="button" value="3" onClick="document.calculator.ans.value+='3'">
<input type="button" value="+" onClick="document.calculator.ans.value+='+'">
 
<input type="button" value="4" onClick="document.calculator.ans.value+='4'">
<input type="button" value="5" onClick="document.calculator.ans.value+='5'">
<input type="button" value="6" onClick="document.calculator.ans.value+='6'">
<input type="button" value="-" onClick="document.calculator.ans.value+='-'">
 
<input type="button" value="7" onClick="document.calculator.ans.value+='7'">
<input type="button" value="8" onClick="document.calculator.ans.value+='8'">
<input type="button" value="9" onClick="document.calculator.ans.value+='9'">
<input type="button" value="*" onClick="document.calculator.ans.value+='*'">
<input type="button" value="/" onClick="document.calculator.ans.value+='/'">
 
<input type="button" value="0" onClick="document.calculator.ans.value+='0'">
<input type="reset" value="Reset">
<input type="button" value="=" onClick="document.calculator.ans.value=eval(document.calculator.ans.value)">
<br>Solution is <input type="textfield" name="ans" value="">
</form>
</body>
</html>
```

## Details
Details about what the code above goes here

* `<form name="calculator">`
    * Name the form so it can be targeted by JavaScript
* `<input type="button">`
    * This defines the type of input that is displayed.  Other options include "text", "textarea", "password".
* `<input type="button" value="0">`
    * Value is what is contained in the input field or button.  For example, this button will say "0" on it.
* `<input type="button" value="5" onClick="document.calculator.ans.value+='5'">`
    * onClick describes a JavaScript event.  When the button is "clicked" JavaScript looks in the **Document** for **calculator** (defined by *`<form name="calculator">`*) and locates the **ans** field (*`<input type="textfield" name="ans" value="">`*).  The value of the **ans** field by default is "", but the **+=** places the number **5** into the field.  *+=* appends values.
* `<br/>`
    * Stands for linebreak.  Will start a new line wherever it is placed.

Need a refresher on styles? http://www.dummies.com/web-design-development/html5-and-css3/how-to-use-an-external-style-sheet-for-html5-and-css3-programming/


# Lesson 8.2: "Vote for Pedro!"

### Instructions
1. Open your web browser and visit Codepen.io
2. Create a New Pen (You do not have to register, unless you'd like to save your project.)
3. Using the example below, reproduce the web page, but with your own twist!

**Criteria for the Lesson 8.2 webpage:**
* Style the button colors using hexidecimal (#000000) or rgba(255,255,255,1) values.
* Change the text inside the button
* Change fonts (google.com/fonts)
* Style the "Clicks" counter


**In the HTML section type the following:**
```HTML
<button onclick="clickMe()">Vote for Pedro</button>
<p>Clicks: <a id="clicks">0</div></p>
```

**In the CSS section, type and customize the following:**
```HTML5
button {
  height: 300px;
  width: 300px;
  border-radius: 200px;
  background: green;
  color: white;
  font-family: Impact;
  font-size: 40pt;
  text-transform: uppercase;
  }

button:hover {
  background: red;
  transition: 2s;
}
```

**In the JavaScript (JS) section, type the following:**
```Javascript
  var clicks=0;
  function clickMe(){
    clicks += 1;
    document.getElementById("clicks").innerHTML = clicks;
  }
```

## Details

* `var clicks = 0;`
* Establishes a variable named "clicks" with the value of 0.

* `function clickMe(){`
* Establishes the name of a new function (or feature!).  In this case, the function is named clickMe. 

* `clicks += 1;`
* Increments the value of the variable "clicks" by 1.  The number could be changed to anything you want.  If you'd like the number to go up by even numbers you could change it to "2", or even 1000!

* `document.getElementById("clicks").innerHTML = clicks;`
* This is where a lot of the magic happens.  This piece of code searches the web page document for anything with an ID="clicks". (document.getElementById).  This piece of code is **case sensitive** meaning uppercase/lowercase matters!
* the .innerHTML piece changes the content of the element assigned to the id="clicks".  In this case, it is changing the content to match our "clicks" variable value.
* If the value of our "clicks" variable is 100, then .innerHTML will update to read "100".

* `}`
* Always make sure to close your JavaScript functions with a curly brace.

#### Do you want to save your CodePen Button Project?  Click EXPORT - EXPORT .ZIP at the bottom right corner.####

# Lesson 8.3: File API

In Lesson 8.3 we cover the JavaScript File API

### Instructions
1. Open Notepad, or your favorite text editor.  Codepen.io may also be used.
2. Save the file as fileAPI.html
3. Using the example below, reproduce the webpage with your own style


**Criteria for the Lesson 8.3 webpage:**
* Style the form generated by the code below:
* Must style #page-wrapper
* Must style h1
* Optional: Apply a background color to the #fileDisplayArea


```HTML5
<div id="page-wrapper">

		<h1>Text File Reader</h1>
		<div>
			Select a text file: 
			<input type="file" id="fileInput">
		</div>
		<pre id="fileDisplayArea"><pre>

	</div>
	 <script src="text.js"></script> <!-- ERASE THIS LINE IF YOU'RE USING CODEPEN -->
```

### File API JavaScript
1. Create a new file called fileAPI.js
2. Type the JavaScript text as seen below:

```JavaScript
window.onload = function() {
		var fileInput = document.getElementById('fileInput');
		var fileDisplayArea = document.getElementById('fileDisplayArea');

		fileInput.addEventListener('change', function(e) {
			var file = fileInput.files[0];
			var textType = /text.*/;

			if (file.type.match(textType)) {
				var reader = new FileReader();

				reader.onload = function(e) {
					fileDisplayArea.innerText = reader.result;
				}

				reader.readAsText(file);	
			} else {
				fileDisplayArea.innerText = "File not supported!"
			}
		});
}

```
## Details
Details about what the code above goes here

* `window.onload = function() {}`
    * Anything within the {} is executed after the web page is completely loaded.

* `var fileInput = document.getElementById('fileInput');`
    * Set a variable called fileInput that is linked to the input with id="fileInput"
    
 * `var fileDisplayArea = document.getElementById('fileDisplayArea');`
    * Set a variable called fileDisplayArea that is linked to the id="fileDisplayArea"
        
  * `fileInput.addEventListener('change', function(e) {}`
    * An EventListener is added to the fileInput variable
    * Whenever the user selects a file the function is executed
    
  * `var file = fileInput.files[0];`
    * This variable, named file, looks at the fileInput files property and fetches the first file
    
  * `var textType = /text.*/;`
    * Checks to see if the submitted file is a text file (*.txt)  
    
  * `if (file.type.match(textType)) {}`
    * If the submitted file is a TEXT file, code within the {} brackets is executed.
    
  * `var reader = new FileReader();`
  	* The FileReader interface provides a number of methods that can be used to read either File or Blob objects. These methods are all asynchronous which means that your program will not stall whilst a file is being read. This is particularly useful when dealing with large files.

  * `reader.onload = function(e) { fileDisplayArea.innerText = reader.result; }`
    * When the reader is completed (or the text file is completely added to the File Reader Instance), the RESULT is the text within the file - This text will update the "innerText" of the id="fileDisplayArea".
    
* `reader.readAsText(file);`
    * The readAsText() method can be used to read text files. This method has two parameters. The first parameter is for the File or Blob object that is to be read. The second parameter is used to specify the encoding of the file. This second parameter is optional. If you don’t specify an encoding UTF-8 is assumed by default.
    * As this is an asynchronous method we need to setup an event listener for when the file has finished loading. When the onload event is called we can examine the result property of our FileReader instance to get the file’s contents. You will need to use this same approach for all of the read methods provided by FileReader.
    
* `else {fileDisplayArea.innerText = "File not supported!"}`
    * If the submitted file is not a text file, display "File Not Supported!"
   
 
 ### Some more...
 
 * readAsDataURL()
 	* The readAsDataURL() method takes in a File or Blob and produces a data URL. This is basically a base64 encoded string of the file data. You can use this data URL for things like setting the src property for an image. We will look at how to do this later in the images demo.
```JavaScript
var reader = new FileReader();

reader.onload = function(e) {
  var dataURL = reader.result;
}

reader.readAsDataURL(file);
```

 * readAsBinaryString()
 	* The readAsBinaryString() method can be used to read any type of file. The method returns the raw binary data from the file. If you use readAsBinaryString() along with the XMLHttpRequest.sendAsBinary() method you can upload any file to a server using JavaScript.
```JavaScript
var reader = new FileReader();

reader.onload = function(e) {
  var rawData = reader.result;
}

reader.readAsBinaryString(file);
```

 * readAsArrayBuffer()
 	* The readAsArrayBuffer() method will read a Blob or File object and produce an ArrayBuffer. An ArrayBuffer is a fixed-length binary data buffer. They can come in handy when manipulating files (like converting a JPEG image to PNG).
```JavaScript
var reader = new FileReader();

reader.onload = function(e) {
  var arrayBuffer = reader.result;
}

reader.readAsArrayBuffer(file);
```

 * abort()
    	* The abort() method will stop a read operation. This can come in handy when reading large files.
```JavaScript
reader.abort();
```


# Lesson 8.4: Web Workers
Web workers are JavaScripts that run independent of other scripts (i.e. the script runs in the background). Often times, these scripts are used to connect to multiple webpages and fetch real-time data. However, a web worker can complete a simple background task like counting numbers as well.

In order to employ a web worker, you need to create a worker thread as follows:
`var worker = new Worker(‘worker.js’);`

As far as sample code goes, the below can be typed up in webworker.html

```
<!doctype html>
<html lang="en">
<head>
<script>
var worker = new Worker('doWork.js');
// Send a message to start the worker and pass a variable to it
var info = 'Web Workers';
worker.postMessage(info);
// Receive a message from the worker
worker.onmessage = function (event) {
 // Do something
 alert(event.data);
};
</script>
<title>Web Workers Example</title>
</head>
<body>
</body>
</html>
```

And the below can be saved as doWork.js
```
onmessage = function(event) { 
var info = event.data; 
var result = 'Hello ' + info + ' everywhere'; 
postMessage(result); 
};
```

# Mad Libs Lesson and Additional Animation Demos
To access this lesson, you will need to navigate to the following link and create an account. Follow the slides at the top of the page for lesson material and instructions.
https://dash.generalassemb.ly/projects/mad-libs-1

#### Moving Paragraph Animation
Copy the code below into paragraph.html
```
<!doctype html>
<html>
<head>
<title>Animate with JavaScript</title>
<script type = "text/javascript">
 // Create a "ticker-tape" effect by sliding
 // the paragraph of text one pixel to the
 // right, over and over, until the right-hand
 // limit of 300 pixels is reached. At that
 // point, restart the animation all the way
 // to the left.
function move_paragraph() {
 next = current + "px";
 current += 1;
 if (current > 300) {
 current = 0;
 }
 paragraph.style.left = next;
 // Pause for 18 milliseconds before
 // the next move.
 var rate = 18;
 setTimeout(move_paragraph, rate);
}
function init() {
 paragraph = document.getElementById("original");
 paragraph.style.position = "absolute";
 current = 0;
 move_paragraph();
}
</script>
</head>
<body onload = "init();">
<h1>Animate with JavaScript</h1>
<p id = "original">Do you see me scrolling across the
 screen?</p>
</body>
</html>
```

# Lesson 8.5: Cookies
Cookies are essentially the bits of information that a webpage stores on a user's computer. This can include browsing preferences, configurations, and usage, all of which can support a site's functionality. Quite often, a website may inform its user about cookie usage to uphold a privacy policy. Regardless, the key point of cookies is to retain a user's information from visit to visit.

To demonstrate JavaScript's ability to remember such information, code the following. Cookies can only be enabled through webpages accessed on a network, and not locally, so you may need to contact your instructor.
```
<!doctype html>
<html>
<head>
<title>Use of cookies</title>
<script type = "text/javascript">
function getCookie(c_name) {
 var i,x,y,ARRcookies=document.cookie.split(";");
 for (i=0;i<ARRcookies.length;i++)
 {
 x=ARRcookies[i].substr(0,ARRcookies[i].indexOf("="));
 y=ARRcookies[i].substr(ARRcookies[i].indexOf("=")+1);
 x=x.replace(/^\s+|\s+$/g,"");
 if (x==c_name)
 {
 return unescape(y);
 }
 }
}
function init() {
 var message;
 level_object = document.getElementById("level");
 var welcome = document.getElementById("welcome");
 var level = getCookie("level");
 if (level == null || level == '') {
 message = "It appears this is your first time
 to play. You will start at level 1.";
 level = 1;
 } else {
 message = "When you last played, you reached
 level " + level +". You will start there now.";
 }
 welcome.innerHTML = message;
 level_object.value = level;
}
function save_level() {
 setCookie("level", level_object.value, 10);
}
function setCookie(c_name,value,exdays) {
 var exdate=new Date();
 exdate.setDate(exdate.getDate() + exdays);
 var c_value=escape(value) + ((exdays==null) ? ""
 : "; expires="+exdate.toUTC
String());
 document.cookie=c_name + "=" + c_value;
}
c09CreatingAnimationsWorkingwithGraphicsandAccessingData.indd Page 236 10/18/12 10:49 AM F-400
Creating Animations, Working with Graphics, and Accessing Data | 237
</script>
</head>
<body onload = "init();">
<h1>Use of cookies</h1>
<p id = "welcome">Welcome.</p>
<form>
You can update your level at any time. It is
 currently set at
<input id = "level" type = "number" min = "1" max =
 "100"
 oninput = "save_level();" />.
</form>
</body>
</html>
```

Through the use of cookies, the webpage should be able to remember whatever level you input. Remember, cookies are not a perfect solution, and can be pretty limited in what they do. Privacy concerns regarding cookies are not uncommon. To be precise, it is important to be aware of the limitations and advantages that cookies can provide.



For more JavaScript practice, check this site out:
https://www.teaching-materials.org/javascript/
