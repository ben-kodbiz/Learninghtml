# Lesson 7

In Lesson 7, we explore the differences between drawing with Canvas and SVG web technologies. In order to do so, we will utilize some JavaScript. In the next lesson, you will acquire a more rounded foundation of JavaScript.

### Instructions
1. Visit www.codepen.io
2. Click Create - New Pen
3. Please note, this will be a temporary design unless you choose to make an account on Codepen.io
4. Using the information provided, try to draw a picture using SVG and Canvas - this could be your logo!


**Criteria for the Lesson 7 web page:**
* Must use SVG (Scalable Vector Graphics)
* Must use Canvas
* Implement a design into your own website 





# Canvas

## Drawing a Red Square in Canvas

In the HTML side of your codepen, put:
```HTML5
<canvas id="myCanvas" width="800" height="800"></canvas>
```

In the JavaScript side of your codepen, put:
```Javascript
var canvas = document.getElementById('myCanvas');
var context = canvas.getContext('2d');
context.fillStyle = '#c00';
context.fillRect(10, 10, 100, 100);
```

## Drawing a Circle in Canvas
In the JavaScript side of your codepen, put:
```JavaScript
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.beginPath();
ctx.arc(95,50,40,0,2*Math.PI);
ctx.stroke();
```

## Drawing Text in Canvas
In the JavaScript side of your codepen, put:
```JavaScript
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.font = "30px Arial";
ctx.fillText("Hello World",10,50);
```


## Using Gradients in Canvas
In the JavaScript side of your codepen, put:
```JavaScript
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");

// Create gradient
var grd = ctx.createLinearGradient(0,0,200,0);
grd.addColorStop(0,"red");
grd.addColorStop(1,"white");

// Fill with gradient
ctx.fillStyle = grd;
ctx.fillRect(10,10,150,80);
```

For the full Canvas Reference, visit: https://www.w3schools.com/graphics/canvas_reference.asp


# SVG (Scalable Vector Graphics)

## Drawing a Red Square in SVG

In the HTML side only, put:
```HTML5
<svg xmlns="http://www.w3.org/2000/svg" viewbox="0 0 600 600">
  <desc>Red rectangle shape</desc>
  <rect x="10" y="10" width="100" height="100" fill="#c00"  />  
</svg>
```


## Drawing a Yellow Circle with a Green Border in SVG
In the HTML side only, put:
```HTML5
<svg width="100" height="100">
  <circle cx="50" cy="50" r="40" stroke="green" stroke-width="4" fill="yellow" />
</svg>
```

## A Sample SVG Logo with a Fiery Gradient
In the HTML side only, put:
```HTML5
<svg height="130" width="500">
  <defs>
    <linearGradient id="grad1" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" style="stop-color:rgb(255,255,0);stop-opacity:1" />
      <stop offset="100%" style="stop-color:rgb(255,0,0);stop-opacity:1" />
    </linearGradient>
  </defs>
  <ellipse cx="100" cy="70" rx="85" ry="55" fill="url(#grad1)" />
  <text fill="#ffffff" font-size="45" font-family="Verdana" x="50" y="86">SVG</text>
  Sorry, your browser does not support inline SVG.
</svg>
```

### Description
* The cx attribute defines the x coordinate of the center of the ellipse
* The cy attribute defines the y coordinate of the center of the ellipse
* The rx attribute defines the horizontal radius
* The ry attribute defines the vertical radius
* The id attribute of the `<linearGradient>` tag defines a unique name for the gradient
* The x1, x2, y1,y2 attributes of the `<linearGradient>` tag define the start and end position of the gradient
* The color range for a gradient can be composed of two or more colors. Each color is specified with a `<stop>` tag. The offset attribute is used to define where the gradient color begin and end
* The fill attribute links the ellipse element to the gradient
* The `<text>` element is used to add text


For the full SVG Reference, visit: https://www.w3schools.com/graphics/svg_reference.asp



## What's the difference between SVG and Canvas?

* SVG is great for two dimensional graphics.
* SVG uses XML to create vector based 2D graphics - meaning the images are scalable without deteriorating the quality (resolution independent)
* SVG is not suited for gaming.
* You may use programs like Inkscape.com or Adobe Photoshop to generate SVG code for your images
* SVG may be used with JavaScript event handlers.
* SVG graphics use **retained mode** which means you give the object some properties and the browser stores the process to create the image in its memory.
* Canvas uses **immediate mode** which means you, as a developer, need to work out the commands to draw each object to show exactly what you want.  It uses a "Fire and Forget" model, meaning it runs the commands once to display the image and is not aware of the object afterwards.
* Canvas is drawn pixel by pixel.  If the position of an image changes the entire canvas must be changed (see previous bullet).
* Canvas is great for creating 3D graphics
* Canvas is NOT great for high quality resizing of graphics (scalability)
* Canvas requires JavaScript
* Canvas does not render text well
* You can save the resulting image as a PNG or JPG
* Great for graphic intensive games



# Challenge 7 Part 1

```HTML5
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width">
<title>repl.it</title>
</head>
<body>
<svg height="130" width="500">
  <defs>
    <linearGradient id="grad1" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" style="stop-color:rgb(50,150,255);stop-opacity:1" />
      <stop offset="100%" style="stop-color:rgb(0,0,255);stop-opacity:1" />
    </linearGradient>
  </defs>
  <ellipse cx="100" cy="70" rx="85" ry="55" fill="url(#grad1)" style="stroke: #333; stroke-width: 10;" />
  <text fill="#ffffff" font-size="45" font-family="Verdana" x="50" y="86">SVG</text>
  Sorry, your browser does not support inline SVG.
</svg>
</body>
</html>
```

* CRITERIA
1. The ellipse has fallen off the canvas!  Change the x coordinate to 100.
2. Add a third gradient color stop to the ellipse (any color)
3. Change the text (anything)
4. Resize the Ellipse so your text fits in it
5. Move the Ellipse x and y coordinates if needed.
6. Move the text x and y coordinates if needed.
7. Change the outline color or thickness (or both!)
    
Complete Challenge 7 on Repl.it: https://repl.it/classroom/invite/CJuYkDU


# Challenge 7 Part 2

```HTML5
<!DOCTYPE html>
<html>
<head>
    <title>Triangle Canvas Example</title>

	<style>
		body {
			text-align: center;
		}		
		canvas {
			border: 5px solid black;
		}
	</style>
</head>
<body>

<canvas id="myCanvas" width="309" height="110"></canvas>

    <script>
		
	var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");


// gradient
var grd = ctx.createLinearGradient(0,0,200,0);
grd.addColorStop(0,"coral");
grd.addColorStop(0.5,"tomato");
grd.addColorStop(1,"gold");
ctx.fillStyle = grd;
ctx.fillRect(2,2,300,100);


ctx.beginPath();
ctx.arc (155,50,60,0,2*Math.PI);
ctx.stroke();


ctx.font = "30px Times New Roman";
ctx.fillStyle = "white";
ctx.fillText("Hakuna Matata",30,80);



/*var canvas = document.getElementById('myCanvas');
var context = canvas.getContext('2d');
context.fillStyle = '#c00';
context.fillRect(2, 2, 100, 100);
*/ 
    </script>
 
</body>
</html>
```

* CRITERIA
1. The Gradient currently has three colors, one of those colors is "Tomato". Remove it to only have two colors.
2. The Canvas itself should not have a visible border surrounding it.
3. The Circle should have a radius of 45, not 60. (hint: Circles are made using arcs)
4. The text should have the Font Family "Broadway".
5. The text should also have a hexadecimal color of ef2545. (remember, hex colors require a # sign before the hex code) 

Complete Challenge 7 on Repl.it: https://repl.it/classroom/invite/CJuYkDU
