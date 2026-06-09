# Entry 6
##### 05/28/2026

### CONTEXT:
<p> After finishing the mvp and beyond mvp of my product, the next step was to create slides to present them to the class. The slides that were required to be presented had to consist of the product/project itself, the code that led to the establishment of your project, the tool that helped add on to your creation, and the takeaways you colected througout the proccess of coding such as challenges, etc. After presenting to the claas, the next step was to prep for the presentations at the expo. The biggest difference between the two presentations was the amount of time we had to present and what we were presenting. When it came to the in class presentation we had about ten minutes to present all we wanted to tell our classmates about our project and proccess. However, what was valued the most during the in class presentation was the proccess of the project. This would mean the codes that were coded and used, how we got from point A to point B, and how we continsouly added to our creations. Overall, the way we built our project and the visual of the jounrey was more of a importance for class presenatations. On the other hand, expo presentations valued the project/prodect more given we only had about a minute and thirty seconds to present. So, there was more showing off the project descriptively then briefly talking about what codes you used to get you your project. </p>


### CONTENT 

<p> or this year, I really liked the idea of making a type of checklist. I started to think about what type of checklist I wanted to make exactly. I then decided that I wanted to build a event planner and implement the checklist somewhere in my project. After thinking and seeing what I know I would be able to make, I decided that for my MVP I will make an event planner that has a checklist area for when users checklist a event they are planning and a shop section for users to be able to shop/purchase the materials for the event depending on what they are planning. For my tool, I decided that I wanted to use something that would lighten the tough proccess of coding. So, I chose less css js. Less css js is a javascript tool that provides coders with shortcuts and less dense easy to read css code. In fact the only difference the tool has from regular css is the amount of code that would be written. Adding to the checklist and the shopping section, beyond my MVP I decided to add a budgeting section, where a user could enter the most amount of money they would like to spend and then add a price to everything they are putting in the chechlist. Then the money being tracked will increase if the user deletes a chechlist item or decrease if the user adds something. Another thing I did for my project for beyond my mvp is making my product responsive which is something we learned how to do sophmore year </p>


### Engineering Design Process: 

<h3> IN CLASS PRESENTATION </h3> 

<p> My proccess after I had offically finished coding my freedom project was to set up the slides I wanted to present. I knew I had to present how my project looks like, its functions, how I made it, its purposes, and what I colleceted and learned while making it. </p>

<p> I first started by collecting screenshots of all of the codes I wanted to explain such as the javascript logic and the tool I used. When I had decided on what codes I was going to present, I chose a hook (¨Did you know that there are rarely any sources that provide you with not only the ability to plan for an event by also budget and shop for it ? ... here is what I made.¨). Then I decided that since the link to my project did not load yet, I will screen record myself using my product and narrate it to the class. After that I started to add everything into the slides and prepare a script of what I wanted to exactly say. </p>

<h2>FOR EXAMPLE...</h2>

<p> For this code I said... </p>

```js
    document.addEventListener('DOMContentLoaded', function() {
                    //select all the elements for the checklist section content
                var checklistBtn = document.querySelector(".checklist-btn");  
                var checklist = document.getElementById('checklist');  
                var checklistInput = document.getElementById('checklistInput');   
                var addItemBtn = document.getElementById('addItemBtn');  
                var checklistPlan = document.getElementById('checklistPlan');  

                // Select all of the elements for the shop section content 
                var shopBtn = document.getElementById("shopPlanBtn");
                var shopSection = document.getElementById("shopSection");
                var eventSelect = document.getElementById("events");
                var decorLinks = document.getElementById("decorLinks");
                var decorList = document.getElementById("decorList");
```

<p> that I called all of my existing html for the cheklist and shop section first in my javascript. I showed this part of my code so that I could show my classmates that I started by coding the the checklist and shop section first. I did this because, these two sectiosn are what made up the purpose of my project since that is where the budgeting and shopping links were. </p>


<p> For this code I said...</p>

```js
// Function to add a checklist item
                var addChecklistItem = (itemText, itemCost) => {
                    if (!itemText.trim()) return;  // Don't allow users to add empty items
                    itemCost = parseFloat(itemCost) || 0;

                    // Update remaining budget
                    remainingBudget -= itemCost;
                    if (remainingBudget < 0) remainingBudget = 0;

                    budgetDisplay.textContent = `Remaining Budget: $${remainingBudget.toFixed(2)}`;

                    // Add event listener to the delete button
                    deleteBtn.addEventListener('click', function() {
                        checklistPlan.removeChild(listItem);  // Remove the item from the list when delete button is clicked
                        remainingBudget += itemCost; // Add back the deleted item's cost
                        budgetDisplay.textContent = `Remaining Budget: $${remainingBudget.toFixed(2)}`;
                    });
                };
```

<p> that since I wanted to add the feature to where the user could increase and decrease their budget depening on what they do, I showed my classmates how I used DOM to implment that. I explained that when the user adds something to the list after they specfied what that certain thing cost then the budget input will be subtracted by the current item cost in which will update the budget right away shwoung the user how much that money is left. Then, I explained that the second code with += means that if the user decides to delete something off the list then the current budget number and the cost of whatever that certain list item was would be added back into the budgeting updating the user with it current new cost. I explained that this is only possible when the program ¨hears¨ the button being clicked which is where the event listener takes place. I decided to share this part with the class because it shows the proccess behind the budgeting and checklist section and shows how they both connect to one another </p>


<p> For this code I said ... </p>

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

<p> that I did not want the content of my project show up as soon the page loads. I wanted each section to only pop up when the button for that specfic section is clicked/pressed on. So, I explained that in order for me to do that I had to use the DOM concept of display to where if the checklist section is killed on then the shop section is hidden and the opposite if the shop section is clicked/pressed on. I presented this to my classmates because I thought that the layout I decided to do for my project is important because it shows the attemped mimication of an ¨app¨ in which it seperates certain content by itself as well. </p>


<p> For this code I said ... </p>

```js
@primary-color: #9b4f80;
                        @accent-color: #ff4fd8;
                        @gray-bg: #939393;
                        @white: #ffffff;
                        @black: #000000;


                     @main-font: "Arial Rounded MT Bold", Arial, sans-serif;

                    @main-shadow:
                        2px 2px 0 darken(@accent-color, 25%),
                        5px 5px 0 rgba(0, 0, 0, 0.2),
                        8px 8px 15px rgba(0, 0, 0, 0.2);

                    @soft-shadow:
                        5px 5px 0 rgba(0, 0, 0, 0.2),
                        8px 8px 15px rgba(0, 0, 0, 0.2);
                             
                        .text-style(@size, @color: @white) {
                            font-size: @size;
                            font-weight: 900;
                            font-family: @main-font;
                            color: @color;
                        }
```

<p> that less css js was my tool. I told my classmates that less css js is exactly was css is just givem more shortcuts and less dense hard to read code. I explained that the code above shows the way I used my tool to make the cosmetic part of it easier to deal with. I explained to them what the code was showing in which it shows multiple nfucntions being nested. I presented that the @ before the codes shows that it is a function. More specfically a resuable fucntion. So, all I would need to do is nest the other codes in and just reuse the fucntion each time instead of rewriting. I explained to them that this is different then regualr css since without less css js the code would need to be written each time. Then I explained how that is what I did for the rest of my css code. I kept on reusing the function for my colors and bubble letter effect which made the css codes shorter and easier. </p>


<p>For this code I said ... </p>

```js
                  @media (max-width: 768px) {
                        .checklist-btn {
                            width: 40%;
                            left: 25%;
                        }
```

<p> that using media queries is how I got over my challenge which would be making my project responsive. I explained that I was challenged with making it responsive because I was using absolute positiing which would make the content at a perment position and not make it adapt to different screen sizes. So, I prestented and explained to my classmates that media queries are used to make certain content adpat depening on the page of the screen. So, I removed absoulute positiong from content such as buttons and anything else that had something positioned next to something else. Then I replaced the code with media queries that positioned certian content to load correctly if viewed from a phone or ipad, etc. Media queries helped fix my checklist and shop section from overlapping and spaced them out from one another. Additonally, media queries were most helpful because they were apart of the less css concepts. Media queries were most helpful because they were a less css concept that were able to use in nesting. This helped me use a shortcut in using then same media queries when nesting instead of having to rewrite the whole thing each time. After implementing the code on certain content that needed to be aligned I refreshed the page and saw the each content was aligned perfectly. To show them the full proccess I provided them with visuals from before my content was resposive to after it was. </p>

<p> OVERALL this was my designing proccess in terms of slides and in class presentations </p>

<h1>EXPO:</h1>

<p> As mentioned before, the presentation during the expo was completely different than the presentation for the class. So, I had to decide how I was going to present my project to the judges. <p>

<p> I did not show any code to the judges regarding my project. I started off by showing them a  [HSTAT](https://www.hstat.org/) [narrataion video](https://docs.google.com/videos/d/12sNPImPY6DWB65zRK6RTMdfdgP_yCe2SbRGV4ds0JKE/edit?scene=id.p#scene=id.p) in which I explain to them that I made an event planner. ¨My event planner has two sections in which the user is able to use. It has a checklist section in which once it is clicked a budgeting section and a checklist appears. As you could see the user input the budget they want to track and spend from. After that the user could start adding things to the checklist while inputing how much that certain thing cost. Then when the user presses add, the budget is deccreased helping the user track how much money they have left to spend. But if the user decides to delete something from the list than however much that thing did cost is added back to the budget. Now, when the user goes to the shop section, they are provided with a dropdwon menu of every event there is to plan. So for when the user clicks on a event such as birthday then links to a online shopping website is provided where the user could shop for those materials. Building my project consisted lots of DOM codes from javascript such as event listeners in which the program listen to before taking action. For my tool this year, I used less css js which helped me code the css part of my project more easier and smoother. It helped me solve responsiveness challenge by using media queries in which I learned from the [official less css js website](https://lesscss.org/).¨

<p> That is what I ended up saying to the judges </p>


### SKILLS:

<p> Throughout the duration of the project, I developed many skills. One of the skills I developed was learning how to use less css js and dom. Since I spent all of the project only using these I was able to understand them fully and adapt them as a skill. Now, since I know how to use less css js as a coding tool, I plan not to use regular css again and use the shortcuts I learned. In terms if dom, I throughly learned how to use its concepts to maniuplate the way my project functions. Which is another skill I plan to use on future projects. I also learned the skill of browsing. I devloped the abilty to browse through the websites of my tool and google in order to guide me to my final result. This skill helped teh proccess of looking for help easier. </p>


### Takeaways: 
<ol>
                <Li> ALWAYS use sources to help you solve your issues. My challenges would not have been easy to handle if it wasnt for the webiste of my tool.</Li>
                <Li>PLAN throughly before starting the project. It helps you start your project comfortably and more organized.</Li>
                <Li>LEARN your tool before using it. Learning my tool before starting the project helped me understand and get an idea how I would need to be using it in my project.</Li>
          </ol>


### SUMMARY:
<p> The purpose of my project was to provide users with a source in which they can checklist a plan while being able to budget and shop for it </p>


[Previous](entry05.md) 
[Home](../README.md)