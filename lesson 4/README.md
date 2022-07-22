# Lesson 4

In Lesson 4 you will learn how to create and modify tables and lists.

### Instructions
1. Open Notepad, or your favorite text editor.
2. Save the file as stats.html
3. Using the example below, reproduce the webpage with your own content

**Need an idea?  Pick from these prompts:**
* Pick a social issue or cause that you care about and replace the sample statistics with some of your own.
    * Animal Adoptions
    * Abuse
    * Bullying
    * Hunger
    * Homelessness
    * Cancer
    * Violence

**Criteria for the Lesson 4 webpage:**
* Must choose a topic different from the example or have completely different information
* Create a table to represent data
* Make a list of ways people can get involved
* Create a Contact form (https://formspree.io/)
* Change colors and fonts to make the page appealing

```HTML5
<!doctype html>
<html>
<head><title>Pollution Awareness</title></head>
<body>

<h1>Did you know?</h1>
<p>Pollution accounts for.... </p>

<table>
  <tr>
    <th>Effects of Pollution on the Environment</th>
  </tr>
  <tr>
    <th>Types of Pollution</th>
    <th>Effects</th>
  </tr>
  <tr>
    <td>Land</td>
    <td>4.3lbs of waste per person goes to the landfill each day</td>
  </tr>
  <tr>
    <td>Water</td>
  </tr>
  <tr>
    <td>Air</td>
  </tr>  
  <tr>
    <td>Noise</td>
  </tr>  
  <tr>
    <td>Light</td>
  </tr>
</table>
 
 <h2>Things You Can Do</h2> 
  <ul>
    <li> Recyle</li>
    <li> Avoid buing cars with high O2 emission</li>
    <li> Carpool when possible</li>
    <li> Dispose of trash in proper public recepticle</li>
    <li> Turn off lights not in use</li>
  </ul>
  
  <h2>Where Does Your Garbage Go?</h2>
    <ol>
    <li> Your trash can gets full</li>
    <li> You take it to the curb</li>
    <li> Garbage man comes around and takes it </li>
    <li> He takes it to a transfer station before it goes to either:</li>
      		<ul>
            	<li>A landfill</li>
                <li>An incinerator</li>
                <li>Or a recyling center</li>
            </ul>
      
  </ol>
  
  <h3> Sign Up for Our Newsletter</h3>
  <h4>For bi-weekly updates on environmental news</h4>

  <form method="POST" action="http://formspree.io/YOUREMAILHERE">
  <input type="email" name="email" placeholder="Your email"> 
    <br />
     <br />
  <textarea name="message" placeholder="Tell Us How Awesome We Are"></textarea>
  <button type="submit">Send</button>
</form>
  

</body>
</html>
```

## Details
Details about what the code above goes here

* `<table> </table>`
    * Tables are used for organizing data and providing a layout for emails
    * Tables are **not** to be used to styling websites other than to represent data
    * **Really important stuff should be bold like this**
    * Keywords should be *italicized*
    
* `<th> </th>`
   * Nested within the table row elements or table element, use the `<th> </th>` tags to define cells which contain table headers.
   * The table heading spans across all columns.
   * **TH** stands for TABLE HEADER

* `<tr> </tr>`
   * Nested within the table element, use the `<tr> </tr>` tags to define a row.
   * Rows are horizontal.
   * **TR** stands for TABLE ROW

* `<td> </td>`
   * Nested within the table row elements, use the `<td> </td>` tags to define cells which contain table data.
   * Cells are boxes, like in excel, that hold information.
   * **TD** stands for TABLE DATA
   
   Example:
   `<table>
   <th>This is my table heading!</th>
   <tr><td>Row 1, Column 1</td> <td>Row 1, Column 2</td></tr>
   <tr><td>Row 2, Column 1</td> <td>Row 2, Column 2</td></tr>
   </table>`
   
**Table Row must be nested (contained) within the table.  Table Data is also nested, within the Table Row.**
   
* `<ul> </ul>`
   * List items nested within UL tags uses bullets, or graphics to represent each list item.
   * UL stands for UNORDERED LIST

* `<ol> </ol>`
   * List items nested within OL tags are represented using numbers.
   * OL stands for ORDERED LIST (Number order!)

* `<li> </li>`
   * Once you've established whether you want to make a bulleted list or numbered list, each item must be wrapped within LI tags.
   * LI stands for List Item.

### Form Elements ###
* `<form method="" action=""> </form>`

* `<input type="" name="" placeholder=""> </input>`

* `<textarea name=""></textarea>`

* `<button type=""></button>`

For more information:
* Input Types - https://www.w3schools.com/html/html_form_input_types.asp
* Form Methods - https://www.w3schools.com/tags/att_form_method.asp
* Form Actions - https://www.w3schools.com/tags/att_form_action.asp
   * For an email form, we'll set the method to `POST` and the action to `http://formspree.io/YOUREMAILHERE`
# Challenge 4

Check out this lesson's challenge on Repl.it:
https://repl.it/classroom/invite/CJuYkDU
