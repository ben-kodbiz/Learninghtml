# Lesson 6

In Lesson six you will learn Advanced CSS topics, especially as they relate to transforming and drawing objects on the screen.

### Instructions
1. Open Notepad, or your favorite text editor.
2. Save the file as greetings.html
3. Open a second Notepad window, or your favorite text editor.
4. Save the second window as style.css
5. Using the example below, reproduce the web page with your own content to create a greeting card for any occasion of your choice.

**Need an idea?  Pick from these greetings:**
* Birthday Card
* Thinking of You
* Christmas Card
* Be My Valentine
* Thank You
* Or think of this as a start screen to a video game you're making.

**Criteria for the Lesson 6 webpage:**
* Create a greeting that uses any transform effect.
* Create a message that uses keyframe animations.
* Include one additional element you've learned previously (such as video, images, audio, lists, tables, buttons, links, etc)
* Have two separate files, one for HTML and another for CSS

Use the following code for greeting.html file:
```HTML5
<!DOCTYPE html>
<html>

<head>
   <title>Merry Christmas Greeting Card</title>
   <link href="https://fonts.googleapis.com/css?family=Great+Vibes" rel="stylesheet">
   <link rel="stylesheet" type="text/css" href="style.css">
</head>

<body>
   <div class="container">
	   <div class="greeting">Merry Christmas</div>
	   <div class="message">With Love, <br/> My Name</div>

	
      <audio autoplay controls id="winterSong"> 
         <source src="http://mfrisco.github.io/winter16/assets/we-wish-you-a-merry-christmas.mp3">
         <source src="http://mfrisco.github.io/winter16/assets/we-wish-you-a-merry-christmas.ogg">
	      Your browser does not support audio for this webpage!
		</audio>
   </div>
</body>
</html>
```

Save the following code for the style.css file:
```HTML5
body {
	background: #eeeeee;
	background: linear-gradient(to bottom, rgba(255, 255, 255, .4), rgba(0, 100, 200, .5)) no-repeat;
	height: 250px;
	}

.container {
	text-align:center;
	}

.greeting {
	margin: 0 auto;
	padding: 20px;
	background: tomato;
	width: 400px;
	height: 220px;
	font-family: 'Great Vibes', cursive;
	font-size: 72pt;
	text-align: center;
	color: #ffffff;
	animation: spin 8s ease 1;
	-o-animation: spin 8s ease 1;
	-webkit-animation: spin 8s ease 1;
	-moz-animation: spin 8s ease 1;
	border-radius: 5px;
	border: 10px double white;
	opacity: 1;
}


.message {
	margin: 1em 0 0 0;
	padding: 0 0 1em 0;
	font-family: Century Gothic;
	font-size: 40pt;
	animation: colors 4s infinite alternate;
}


/* Spinning Flipcard Keyframes */

@keyframes spin {
	from {
		transform: rotate3d(0, 1, 1, 90deg) scale(.5, .5) rotate(360deg);
		opacity: .2;
	}
	to {
		transform: rotate3d(0, 1, 1, 360deg) scale(1, 1);
		opacity: 1;
	}
}


@-o-keyframes spin {
	from {
		transform: rotate3d(0, 1, 1, 90deg) scale(.5, .5) rotate(360deg);
		opacity: .2;
	}
	to {
		transform: rotate3d(0, 1, 1, 360deg) scale(1, 1);
		opacity: 1;
	}
}

@-moz-keyframes spin {
	from {
		transform: rotate3d(0, 1, 1, 90deg) scale(.5, .5) rotate(360deg);
		opacity: .2;
	}
	to {
		transform: rotate3d(0, 1, 1, 360deg) scale(1, 1);
		opacity: 1;
	}
}

@-webkit-keyframes spin {
	from {
		transform: rotate3d(0, 1, 1, 90deg) scale(.5, .5) rotate(360deg);
		opacity: .2;
	}
	to {
		transform: rotate3d(0, 1, 1, 360deg) scale(1, 1);
		opacity: 1;
	}
}


/* Color Changing Message */

@keyframes colors {
	0% {
		opacity: .5;
		color: blue;
	}
	
	50%  {
		color: green;
		opacity: .5;
	}
	100% {
		opacity: .5;
		color: red;
	}
}

@-webkit-keyframes colors {
	0% {
		opacity: .5;
		color: blue;
	}
	
	50%  {
		color: green;
		opacity: .5;
	}
	100% {
		opacity: .5;
		color: red;
	}
}

@-moz-keyframes colors {
	0% {
		opacity: .5;
		color: blue;
	}
	
	50%  {
		color: green;
		opacity: .5;
	}
	100% {
		opacity: .5;
		color: red;
	}
}

@-o-keyframes colors {
	0% {
		opacity: .5;
		color: blue;
	}
	
	50%  {
		color: green;
		opacity: .5;
	}
	100% {
		opacity: .5;
		color: red;
	}
}


```

## About the Code

### KeyFrames
* `@keyframes` 
	* This is used in the CSS File to create the animation
	* Specify the name of the animation you'd like to create, such as: `@keyframes spin { }`
	* Within the brackets, define your animation:
	`@keyframes a1 { from {background: limegreen;}  to {background: dodgerblue;} }`
	*In the example above, the a1 animation changes the background from limegreen to dodgerblue for whichever element is ends up being assigned to.*
	
	* To improve compatibility across all browsers, the same code is written multiple times using VENDOR PREFIXES such as:
	* Opera: `@-o-keyframes`
	* Firefox: `@-moz-keyframes`
	* Chrome/Safari: `@-webkit-keyframes`
	* Microsoft: `@-ms-keyframes`
	
* `animation` 
	* Use this in CSS properties list for the element you'd like to animate.
	* This is a shorthand property used to specify all the animation properties at once.
	* Example:
` div {width: 200px; height: 200px; background: limegreen; animation: a1 3s;}`
*All divs will be 200x200px in dimension and will change according to how @keyframe a1 is defined.*
	* Animation properties are specified in the following order:
`animation: name duration timing-function delay iteration-count direction fill-mode play-state;`

* `animation-name` 
	* Name the animation anything you want when defining the @keyframes
	* Call the animation using its name in the properties for the element you want to animate
	
* `animation-duration` 
	* How long will the animation run?
	* Defined in seconds (s) or milliseconds (ms).
	* Example:
`div {animation: spin 3s;}`

* `animation-timing-function` 
	* Specifies the animation progression.
	* Linear goes straight through one cycle
	* Ease is a linear path, but it starts slow.  Ease-in and Ease-out are available as well.
	
* `animation-delay` 
	* How long should it take for the animation to begin?
	* Defined in seconds (s) or milliseconds (ms)
	
* `animation-iteration-count` 
	* How many times should the animation run?
	* Use a number or `infinite`
	
* `animation-fill-mode` 
	* Does the animation maintain it's state at the end? (forwards)
	* Or should the animation go back to its start? (backwards)
	* None: Does not apply any styles after execution
	
* `animation-direction`
	* Reverse:  The animation plays in reverse
	* Alternate: The animation plays normal, then runs backwards through the progression.  Runs normal every odd pass, reverse every even pass.
	* Altenate-Reverse: The animation runs as normal every even pass, then reverse every odd pass
	* Normal: play as normal
	
* `animation-play-state` 
	* Paused
	* Running - Default Value
	* JAVASCRIPT can be used to toggle an animation playstate.


### Transforms

* `transform: translate(100px, 50px);`
    * This moves an element to the x and y coordinates specified.

* `transform: rotate(125);`
    * Rotates an element in 2D to 125 degrees (or any specified).  
    
* `transform: rotate3d(x,y,z,angle);`
    * Rotates an element as if it is in a 3D space
    * Elements will appear skewed or distorted as they mimick a 3D appearance
        
* `transform: scale(x,y);`
    * Resizes an image or element (width, height)
        
* `transform: scale3d(x,y,z);`
    * Resizes an image using width, height, and Z - which gives the appearance of moving in 3D space
    
 * `transform: skew(x-angle, y-angle);`
    * Skews an element in 2D along the x-axis and y-axis  

* `transform: translate3d(x,y,z);`
    * Moves an element in 3D space
   
* `transform: translateX(x);`
    * Move an element along the x axis

* `transform: translateY(y);`
    * Move an element along the y axis
    
* `transform: translateZ(z);`
    * Move an element along the z axis
  
    

# Challenge 6

 What would you change in the CSS file to animate the red box to move up? 

```HTML5
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width">
<title>repl.it</title>
<style>
   #boxStyle {
   -ms-animation-name: moveUp;
   -ms-animation-duration: 5s;
   -webkit-animation-name: moveUp;
   -webkit-animation-duration: 5s;
   animation-name: moveUp;
   animation-duration: 5s;
   width: 200px;
   height: 20px;
   position: relative;
   left: 0px;
   top: 0px;
   background-color: red;
   text-align: center;
   color: white;
   font-family: arial;
   padding: 1em;
   }

   @-moz-keyframes moveUp {
   0% { }
   100% { top: 0px; }
   }
   
   @-o-keyframes moveUp {
   0% { }
   100% { top: 0px; }
   }
   
   @-webkit-keyframes moveUp {
   0% { }
   100% { top: 0px; }
   }
   
  @-keyframes moveUp {
   0% { }
   100% { top: 0px; }
   }
</style>
</head>

<body>
<div id="boxStyle">Hello!</div>
</body>
</html>
```

Complete Challenge 6 on Repl.it: https://repl.it/classroom/invite/CJuYkDU
