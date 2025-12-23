# Entry 2
##### 12/15/2025

### Context
<p> We have spent the past couple of weeks learning and exploring our tool. As of right now, I learned how to use loops and Arrays in less;css. To learn this, I used the offical; webiste of <a href ="https://lesscss.org/#"> less.js </a>. to continue to look through all the properties of less. I found how to call a function in less;css, variable, Mixkins. loops However, I did not see on the website how to use Arrays while coding less;css. So, to learn about it, I used google to get my information. In particular, I searched, ¨How could I use Arrays while coding less;css¨ and found a snippet of code of how I could involve Arrays in my less code.

<p>The code I found</p>

```css
@colors: blue, gray, green, red;

.item-1 {
  color: extract(@colors, 1); // access the first item: blue
}

.item-2 {
  color: extract(@colors, 2); // access the second item: gray
}
```

<p> From this little snippet of code that was given by google, I learned that I could use Arrays in less by first giving the array of colors a variable. However setting a variable in less needs to have a @ in front of it. After seeting the variable, I could put the colors I want in the array. Later into the code, I noticed that accessing the colors in an Array is very similar to the same way I would need to access it while coding regular javascript. To do that, I would need to use the function extraxt which basically access the items by their index but unlike regualr javascript, in less, the index starts at one. So, while in javascript the index of the array would have been 3, in this case it is 4. After calling the fucntion, I would put () and within them I would first call the variable of the Array I created, then I would put the index of the color I want to access. So, this code taught me how I could create an Array in less and how I would need to access them. </p>



<p>Through the <a href ="https://lesscss.org/#"> less.js </a>.website, I learned how to use loops while coding less;css. Specficically I used <a href = ¨https://lesscss.org/functions/#logical-functions"> this section (logical functions) </a> to learn how to involve and what I could use loops for in less. I also used google since I found it very helpful with providng me more information about loops and how I could use it in less. </p>

<p> After asking google the same thing with Arrays instead this time replacing it with loops, I saw this code snippet</p>


```js
const colors = ['red', 'green', 'blue'];
for (const color of colors) {
  console.log(color);
}
```

<p>and</p>

```js
const numbers = [1, 2, 3];
numbers.forEach(function(number) {
  console.log(number);
});
```

<p> For the first code snippet, I learned how to loop through an array using less. This part > for (const color of colors) is where the loops happens. It loops through every color in the array. Which then the cosnole will print out each color the loop lands on as it loops. </p>


<p>The second code snippet shows the same thing but with numbers</p>



### Engineering Design Process

<p>After learning about how to use Loops and Arrays in less;css I used the information and examples I saw on google and information I picked up from the less wesbite to try and code something myself implying everything I learned. </p>


```css

@colors: red, green, blue, yellow, pink, notacolor, purple;



.box-loop(@i) when (@i <= length(@colors)) {

  @current-color: extract(@colors, @i); // get color from array

  .box-@{i} {
    width: 100px;
    height: 100px;
    display: inline-block;
    margin: 5px;
    background-color: if(iscolor(@current-color), @current-color, gray);
    text-align: center;
    line-height: 100px;
    color: white;
    font-weight: bold;
  }

  .box-loop(@i + 1); // recursive loop
}

.box-loop(1);
```

<p>This code is using conditionals, arrays, and loops to have a different and according color of box made everytime the array is looped through. First, I created an Array of colors that I wanted the boxes to be. Then I created a loop function > .box-loop(@i) when (@i <= length(@colors)) that will only loop and run as long as @i is less then or equal to the length of teh Array in which in this case 7. Then I created a variable that will store the color that is being looped through currently and use that colorto create the next box > @current-color: extract(@colors, @i);. the @i allows each coolor that is in the Array to be used. At, the end of the code, calling the function, in between the () there is 1. That basically says to loop through the first color of the array and create the box using that color. In this case it is red.</p>


### Skills
<p> The Skills that I gained through the process was how to implement loops and Arrays in my less;css code. Up until now, I perfectly knew how I could get the containers and carousels to align directly in the center. I knew how to code the smooth drop down from the navbar and create the darkened color when the navbar is hovered on. Along the way, I also learned how I could involve conditional statments as well. Those are the skills I learned. </p>


### Summary

<p> In summary, After learning how to use Arrays and Loops in less;css, it continues to give more ideas of how I could use them in my freedom project for this year. Additionally, It also taught more about the flexability of less;css usage. </p>



