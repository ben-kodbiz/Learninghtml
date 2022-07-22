# Lesson 5

So for lesson 5, you will be learning about <strong>flexboxes.</strong>
<strong>Flexbox </strong> refers to a layout that can be applied to a container in html, like divs, that changes the way we organzie things in them; more specifically it allows containers to spread out/distribute/align space among the items it contains. To accomplish this, the container (in accordance to how you direct it as you will learn here) alters its items' width, height and order.

Now flexboxes can get pretty confusing when its just you reading text so to help teach you how to direct flexboxes we will call upon the help of some frogs. 

Open the link below in another tab to begin. You will complete all 24 levels but we will provide some tips here under <strong>Details</strong> for you to come back to if it seems too confusing
<h2> http://flexboxfroggy.com/ </h2>

We will also cover more CSS techniques and Media Queries. 

### Instructions
1. Complete all 24 levels at http://flexboxfroggy.com/

## Details
Tips and help for Flexboxfroggy

* `Levels 1-4`
    * Notice **justify-content** handles the horizontal componant of how and where the space is arranged
    
* `Levels 5-7`
    * **align-content** on the other hand handles the vertical componant.
    * Combining these first 2 properties should be intuative.
  
* `Levels 8-13`
    * **flex-direction** alters the order of the items in the flexbox
    * Notice that reversing the order mirrors the items, such that **flex-end** now pushes the items to the far left not right anymore.
    
* `Levels 14-17`
    * Here you learn how to manipulate a specific item(s) 
    * Remember that **order** assums the initial position of every item to be zero, thus moving the items is like moving them along a number line.
 
* `Level 24`
    * If you're having difficulty with the last level, try to begin by arranging the items in the right orientation first (vertically).
  
  


# Challenge 5

1. In your favorite text editor create a div with the class name "myFlexbox".  
2. Nested within the new div you created, make a list.  The list should be an ORDERED or UNORDERED list - does not matter which one! 
3. Apply the CSS styling below:

```HTML5
body {
    background-color: #def;
}

.myFlexbox ul { 
    display: flex;      
    flex-direction: column;
    width: 200px;
  }   
  
  li {
      background-color: #0f9;
      margin: 10px;
      padding: 10px;
      border: 0px solid #000;
      font-family: 'Caveat Brush', cursive;
      font-size: 30pt;
      list-style: square;
  }
 
 li:hover {
     background-color: #0ff;
 } 
```

* CRITERIA
    * You need to use a flexbox so that new content you add to the container displays at the top of the list.  Do not assign an order.
    * Fix the CSS Flex Direction to properly flip your list.
    * Find this assignment at Challenge 5: https://repl.it/classroom/invite/CJuYkDU



See also: http://cssgridgarden.com/
