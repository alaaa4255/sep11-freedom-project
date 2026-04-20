# Entry 5
##### 04/13/2026

### Progress
<p>After learning our tool for some while, we started and finished coding our freedom project mvp. In my freedom project mvp, the most less css skill/code I involved in my project was the perfect and solid positioning of all of the content I had added onto to the page. I chose to use that for the mvp since I will expand onto my project less css for beyond the mvp. Other than using the specfic coding elements of less css for absoulote positioning, I also used less css to achieve the bubble lettes effect across my whole project. Furthermore, in terms of what I created for my freedom project; I wanted to create a event planing page. For my mvp, I created a checklist to which the user can create a checklist planning an event - they could delete off of it - and coded a shopping section to where the user could choose the shopping section, choose what type of event they are planning, and then be provided with online websites that sell the materials for that specfic event. To guide me through coding less css throughout my project I used <a href ="https://lesscss.org/#"> the offical website: less;css </a>.  </p>


## Engineering Designing Proccess

<p> THE CODING PART:

<p> After adding a pink background to the page, I started to add the content to slowly build how I wanted my project to look like and behave. The first thing I started with was a container in which is where I decided to add my intro summary. </p>

<p>HTML PART OF THE CONTAINER: <p>

```html
<div class="my-container1"> 
            EVENT PLANNING SOCIETY provides with the ability to not only make a checklist that you could use to track what you need to do and get done in which you could add and delete off the checklist but it also provides you with the ability to be provided with online shopping centers that fits within the event you are planning.

        </div>
    ```


<p> LESS CSS PART OF THE CONTAINER: </p>

```css
.my-container1 {
                    width: 800px;
                    padding: 30px;
                    background: #939393;
                    border-radius: 20px;
                    font-size: 18px;
                    font-weight: 900;
                    font-family: "Arial Rounded MT Bold", Arial, sans-serif;
                    color: #ffffff;

                    text-shadow:
                        2px 2px 0 darken(@color, 25%),
                        5px 5px 0 rgba(0, 0, 0, 0.2),
                        8px 8px 15px rgba(0, 0, 0, 0.2);

                    line-height: 2.5;
                    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);

                    position: absolute;  
                    top: 50%;            
                    left: 50%;           
                    transform: translate(-50%, -50%);  

                    display: flex;
                    flex-direction: column;
                    align-items: center;
                    justify-content: flex-start;
            }
```

<p> I wanted the container to be positioned perfectly in the middle of the page. Most importantly, I wanted it to be completly solid and not shift at some point. So, I used absoulote positiing to try and establish that. The part that shows top 50% and left 50% and transform: translate(-50%, -50%) forced the container to be positioned perfectly in the middle of the page without moving. To be more specfic, top 50% placed it at the middle of the top of the page and left 50% placed it directly in the middle of the page overall .</p>

<p>Using, less;css, I turned the writing content that went inside the container to have a bubble letter effect. in order to acheive that I had to use the property of text shadow so that the letters would have the effect of pooping out the page. To that I added the font of the content which is Arial. Using these two properties, helped illustrate the font into a more simpler organized way. </p>

<p>THIS IS THE WHOLE JS CODE </p>


```js
document.addEventListener('DOMContentLoaded', function() {
                    //select all the elements for the checklist section content
                var checklistBtn = document.querySelector(".checklist-btn");  
                var checklist = document.getElementById('checklist');  
                var checklistInput = document.getElementById('checklistInput');   
                var addItemBtn = document.getElementById('addItemBtn');  
                var checklistPlan = document.getElementById('checklistPlan');  

                // Select all of the elements for the shop ssection content 
                var shopBtn = document.getElementById("shopPlanBtn");
                var shopSection = document.getElementById("shopSection");
                var eventSelect = document.getElementById("events");
                var decorLinks = document.getElementById("decorLinks");
                var decorList = document.getElementById("decorList");

                // Hide both checklist and shop sections at first
                checklist.style.display = 'none'; // no checklist showing
                shopSection.style.display = 'none';  // no shop content showing
                decorLinks.style.display = 'none'; // no decor links showing

                // Show checklist input when "Checklist" button is clicked
                checklistBtn.addEventListener('click', function() {
                    checklist.style.display = 'block';  // Show checklist
                    shopSection.style.display = 'none'; // Hide shop
                    decorLinks.style.display = 'none'; // Hide decor links
                });

                // Show shop section when "Shop" button is clicked
                shopBtn.addEventListener('click', function() {
                    shopSection.style.display = 'block';  // Show shop section
                    checklist.style.display = 'none';    // Hide checklist
                    decorLinks.style.display = 'none'; // Hide decor links 
                });

                // Function to add a checklist item
                var addChecklistItem = (itemText) => {
                    if (!itemText.trim()) return;  // Don't allow users to add empty items


                    // Create the list 
                    var listItem = document.createElement('li'); 
                    listItem.classList.add('checklist-item'); // adding a class

                    // Create the label for the checklist text
                    var label = document.createElement('span');
                    label.textContent = itemText; // setting the text of the label

                    // Create the delete button
                    var deleteBtn = document.createElement('button');
                    deleteBtn.textContent = 'Delete'; // the text on the button
                    deleteBtn.classList.add('delete-btn'); // adding a class

                    // Append the label and delete button to the list 
                    listItem.appendChild(label);
                    listItem.appendChild(deleteBtn);

                    // Append the list item to the checklist plan (UL)
                    checklistPlan.appendChild(listItem);

                    // Clear the input area after an ¨item¨ list was added
                    checklistInput.value = '';

                    // Add event listener to the delete button
                    deleteBtn.addEventListener('click', function() {
                        checklistPlan.removeChild(listItem);  // Remove the item from the list when delete button is clicked
                    });
                };

                // Add item when the "Add" button is clicked
                addItemBtn.addEventListener('click', function() {
                    var itemText = checklistInput.value;
                    addChecklistItem(itemText);  
                });

                // Handle the event type selection
                eventSelect.addEventListener('change', function() {
                    var selectedEvent = eventSelect.value; // get the value being chosen

                    // Clear existing links
                    decorList.innerHTML = '';

                    // Show the decor links depending on the event selected
                    if (selectedEvent === 'event3') {  // Halloween Party
                        decorLinks.style.display = 'block';
                        decorList.innerHTML = `
                            <li><a href="https://www.halloween-decor.com" target="_blank">Halloween Decorations</a></li>
                            <li><a href="https://www.partycity.com/halloween-decorations" target="_blank">Party City Halloween Decorations</a></li>
                        `;
                    } else if (selectedEvent === 'event1') {  // Birthday
                        decorLinks.style.display = 'block';
                        decorList.innerHTML = `
                            <li><a href="https://www.birthdayexpress.com" target="_blank">Birthday Decorations</a></li>
                            <li><a href="https://www.partycity.com/birthday-decorations" target="_blank">Party City Birthday Decorations</a></li>
                        `;
                    } else if (selectedEvent === 'event2') {  // Wedding
                        decorLinks.style.display = 'block';
                        decorList.innerHTML = `
                            <li><a href="https://www.weddingstar.com" target="_blank">Wedding Decorations</a></li>
                            <li><a href="https://www.theknot.com/wedding-decor" target="_blank">The Knot Wedding Decorations</a></li>
                        `;
                    } else if (selectedEvent === 'event4') {  // Christmas Party
                        decorLinks.style.display = 'block';
                        decorList.innerHTML = `
                            <li><a href="https://www.christmascentral.com" target="_blank">Christmas Decorations</a></li>
                            <li><a href="https://www.holidaywarehouse.com" target="_blank">Holiday Warehouse Christmas Decorations</a></li>
                        `;
                    } else if (selectedEvent === 'event5') {  // Cultural Party
                        decorLinks.style.display = 'block';
                        decorList.innerHTML = `
                            <li><a href="https://www.southasianpartyshop.com" target="_blank">Cultural Party Decorations</a></li>
                            <li><a href="https://www.partycity.com/cultural-decorations" target="_blank">Party City Cultural Decorations</a></li>
                        `;
                    } else {
                        decorLinks.style.display = 'none';  // Hide the decor links if no event selected
                    }
                });
            });
```

<p>Now, to the more active part of my code, when coding the checklist part, I used the same less css coding to have the text boc be placed directly in the middle. Then I used the same coding to have the list items be added right underneath the text box yet this time I had to take something else out to make the proccess smooth. </p>

<p>When creating the checklist, one of the biggest challenges that came when using my tool was messing up and getting confused on why the item lists keep on overlapping instead of not moving under the pervious item list when something new was added. The main issue had something to do with what I added into the positiong of the checklist item part </p> 

```css
#checklistPlan {
                    position: absolute;
                    top: 130%;  
                    left: 50%;
                    transform: translateX(-50%); 
                    padding: 0;
                    margin-top: 5px; 
                }



                #checklistPlan li {
                        padding: 20px;
                        border-bottom: 1px solid #ccc;
                    
                    font-size: 40px;
                    font-weight: 900;
                    font-family: "Arial Rounded MT Bold", Arial, sans-serif;
                    color: #000000;

                    text-shadow:
                        2px 2px 0 darken(@color, 25%),
                        5px 5px 0 rgba(0, 0, 0, 0.2),
                        8px 8px 15px rgba(0, 0, 0, 0.2);


                }
```

<p> This is the css part of the checklist code. The line of code that kept on messing me up was the border bottom . At first I thought I would have to put something like transform: translateX(-50%, -50%); since I wanted my list items to be positioned where the cheklist was positioned which is in the middle. However, after looking at the less;css website, it showed me border bottom which leaves space in betwwen content so that it is not that close to each other, on top of each other or even far from each other. So, I added the border-bottom line of code on top of the psoitioning and saw that now whenever one of my checklist items are added to the list, they do not overlap on another positions and instead just follow one another to the bottom of the pervious one. </p>

<p> Additionally, while coding the checklist and shopping list, my orginal goal was to have the shop button at the end of the checklist conent so that when the shop button is pressed the shop conent would roll out to further into the bottom of the page. But since it was a challenge to code that when I attempted, I made the checklist and shop conent hidden from display until one of the buttons is clicked. If the checklist button is clicked than the checklist conent would appear and if the shop button was clicked than the checklist conent would disapear and so on. </p>

```js

// Show checklist input when "Checklist" button is clicked
                checklistBtn.addEventListener('click', function() {
                    checklist.style.display = 'block';  // Show checklist
                    shopSection.style.display = 'none'; // Hide shop
                    decorLinks.style.display = 'none'; // Hide decor links
                });

                // Show shop section when "Shop" button is clicked
                shopBtn.addEventListener('click', function() {
                    shopSection.style.display = 'block';  // Show shop section
                    checklist.style.display = 'none';    // Hide checklist
                    decorLinks.style.display = 'none'; // Hide decor links 
                });
```

<p> This is the coded hiiden checklist and shopping content </p>


<p> These were some/most of the ways I involved less;css in my mvp freedom project. Since I wanted to keep the page simple at first, I continued the pattern with using ... </p>

```css
position: absolute;
                    top: 130%;  
                    left: 50%;
                    transform: translateX(-50%); 
                    
```

<p> And </p>


```css
 font-size: 40px;
                    font-weight: 900;
                    font-family: "Arial Rounded MT Bold", Arial, sans-serif;
                    color: #000000;

                    text-shadow:
                        2px 2px 0 darken(@color, 25%),
                        5px 5px 0 rgba(0, 0, 0, 0.2),
                        8px 8px 15px rgba(0, 0, 0, 0.2);
```

### SUMMARY
<p> In summary, for my mvp freedom project I created a event planning checklist and shopping effect. To expand on to that beyond my mvp, I want to create more options on to the page such as a budgeting section and more. I also want to use more concepts and elemenst of my tool instead of just absouloute positioning and buuble letters. </p>
