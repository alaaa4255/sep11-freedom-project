# Entry 4
##### 05/15/2026

### Progress
<p>Since starting my freedom project, not just planning, but also coding it, I have been getting myself to practice coding certain css that I plan to use in my project as I build it. I use all of the rules and properties that I have learned up until now. </p>

<p> I am creating a event planning ¨App¨ and I have planned to use lots of conatiners, colors, dropdwon menus, and other things that will work according to what the user is planning. Since my tool is less;css, I have been using less;css to see how I could code things such as bubble letters to give my code a more creatice/colorfull/fun look</p>

### Bubble Letters (Less;css)

```css
html, body {
  height: 100%;
  margin: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: Arial, sans-serif;
  background-color: #f0f0f0;
}

.bubble-text {
  font-size: 80px;
  font-weight: bold;
  color: white;
  text-transform: uppercase;
  background-color: #ff6f61;
  padding: 20px 40px;
  border-radius: 20px;
  box-shadow: 6px 6px 15px rgba(0, 0, 0, 0.1);
  display: inline-block;
  text-align: center;
  letter-spacing: 5px;
}
```

<p>To practice making the bubble letters I used google and  <a href ="https://lesscss.org/#"> the offical website: less;css </a> and  <a href ="https://www.geeksforgeeks.org/css/css-preprocessor-less/"> geeksforgeeks (less;css) to guide me through the proccess. In the css code above, font-size: 80px;Sets the font size to 80px, making the text large enough for a noticeable bubble effect. I used font-weight: bold; to Make the text bold, so it appears thick and like a bubble, color: white; to Set the text color to white, which contrasts with the bubble's background color, text-transform: uppercase;to Make all the text uppercase ( "bubble letters" becomes "BUBBLE LETTERS¨), background-color: @bg-color;: to Use the @bg-color variable to set the background color of the text to a pinkish red (#ff6f61), padding: 20px 40px; to Add padding inside the text, giving it space around the letters to create a rounder, fuller look, like inflating the text, border-radius: 20px; to Round the corners of the background, making the edges of the text more bubble-like and smooth, box-shadow: 6px 6px 15px @shadow-color; to Add a shadow to the text to create depth. The values (6px 6px 15px) control the shadow’s position and blur, while the @shadow-color variable defines its color (a soft black), display: inline-block; to make the div behave like an inline element (it flows with other elements) but also behaves like a block element (so we can control its size and margins), text-align: center; to Ensure that any text inside the div is centered within the bubble. letter-spacing: 5px;: Increases the space between each letter, giving the bubble letters more room and enhancing the bubbly look. </p>

<p> Learning how to make bubble letters using less;css helped me visualize how I want my projects bubble letters look like/be. Now that I learned how to make the bubble letters, I planned that for my project, I will code out the word event planning as bubble letters. </p>


<p> The next thing I practiced making using my tool for my project was containers. I planned to use many containers in my project so practcing how I could perfect their positioning so that they do not move everytime I refresh the page was important (a problem I ran into with my sep10 project ). Using the webiste, I used the informataion on there to build a container</p> 

### Container (less;css)

```css
@bg-color: #ff6f61; 
@text-color: white;  

html, body {
  height: 100%;        
  margin: 0;           
  padding: 0;          
  display: flex;        
  justify-content: center; 
  align-items: center;     
  font-family: Arial, sans-serif; 
  background-color: #f0f0f0; 
}

.centered-container {
  width: 300px;         
  height: 200px;       
  background-color: @bg-color; 
  display: flex;        
  justify-content: center;  
  align-items: center;    
  border-radius: 10px;      
  box-shadow: 0px 4px 10px 
  color: @text-color;  
  text-align: center;  
}

p {
  margin: 0;           
  font-size: 18px;     
}
```

<p> On the webiste, It showed me mini codes in which connects to the building of the oontainer. For example, it taught me that using  display: flex; allows you to easily center items both horizontally and vertically, and control their spacing and alignment. What I did in the code above to perfect a containers positioning use display: flex; on the .centered-container allows us to center the content inside the container as well, while justify-content: center; and align-items: center; ensure horizontal and vertical centering. The container itself is given specific dimensions (300px by 200px) and has additional styling, such as rounded corners (border-radius: 10px) and a subtle shadow (box-shadow), to make it visually appealing. Removing other margin and padding ensures there’s no unwanted spacing around the edges. Using variables like @bg-color and @text-color for styling allows easy creations of the container’s background and text color. This combination of styles guarantees that the content is smoothly and consistently centered and visually balanced on any screen size. </p>


<p> ANOTHER thing I made it a plan to practice was having my projectś color scheme change when the user decides on what color they want their event to be. For example, if the user wanted their event color scheme to be purple and my app color scheme was currenlty blue then whenever the user puts in purple my app will instenially turn purple instead of staying blue. </p>

<p>However, since the less;css website could only help me to an extent I used google to help guide me through how that will look like so that when I code it into my project, I know how that whole proccess should look like. </p>


### COLOR CHANGE


```css
@primary-color: #3498db;  
@secondary-color: #2ecc71; 
@background-color: #f0f0f0; 
@text-color: #333; 


:root {
  --primary-color: @primary-color;
  --secondary-color: @secondary-color;
  --background-color: @background-color;
  --text-color: @text-color;
}


body {
  background-color: var(--background-color);
  color: var(--text-color);
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

// Container styling
.container {
  width: 80%;
  margin: 50px auto;
  padding: 20px;
  background-color: var(--primary-color);
  color: var(--secondary-color);
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

button {
  background-color: var(--primary-color);
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  margin-top: 20px;
}

button:hover {
  background-color: var(--secondary-color);
}
```

<p>This is the css part of the code, in which we start by setting up all of the colors so that we could use their variables in the js code to offcially code the color changing part. First, we define default colors using variables like @primary-color, @secondary-color, @background-color, and @text-color. These variables allow us to easily change the colors throughout the page by only modifying the value of the variable. For example, @primary-color is used for the container’s background color and the button's color, while @secondary-color is used for the text and button hover effect. We then apply these variables using the :root selector, which makes them accessible throughout the entire page. The body and .container styles use the var(--primary-color) and var(--secondary-color) to apply the color scheme to the page. By using Flexbox, the container and content are centered both horizontally and vertically on the page, ensuring that the layout is clean and responsive. The button also changes its background color when hovered over (button:hover), making the design interactive. This setup ensures that the page looks good and is easy to modify. </p>

<p> The webiste and google said that whatever was done in the css part of the code has to connect to the js part</p>

```js
document.getElementById('applyColor').addEventListener('click', function() {
  // Get the color picked by the user
  const pickedColor = document.getElementById('colorPicker').value;

  
  document.documentElement.style.setProperty('--primary-color', pickedColor);

  // Generate a secondary color based on the primary color (slightly lighter or darker)
  const secondaryColor = shadeColor(pickedColor, -20); // Darken by 20%
  document.documentElement.style.setProperty('--secondary-color', secondaryColor);
});

// Function to darken/lighten a color
function shadeColor(color, percent) {
  let R = parseInt(color.substring(1, 3), 16);
  let G = parseInt(color.substring(3, 5), 16);
  let B = parseInt(color.substring(5, 7), 16);

  // Apply the shading
  R = parseInt(R * (100 + percent) / 100);
  G = parseInt(G * (100 + percent) / 100);
  B = parseInt(B * (100 + percent) / 100);

  // Make sure the values don't go below 0 or above 255
  R = (R < 255) ? R : 255;
  G = (G < 255) ? G : 255;
  B = (B < 255) ? B : 255;

  // Return the new color in hex format
  return `#${(0x1000000 + (R << 16) + (G << 8) + B).toString(16).slice(1)}`;
}
```

<p> With the help of google, I was able to learn how I would need to use the js part of the css to get the code to actually work. And although this isnt the actual code to my freedom project, this was a parctice one that I learned so taht I could apply the way it needs to be coded to/for my actual project so that the color would be able to change easily. </p>

<p> In the JavaScript part of the code, we use event listeners and DOM to make the page work. When the user picks a color from the color picker and clicks the "Apply Color" button, an event listener is triggered. This listener gets the value of the selected color (#colorPicker.value). The selected color is then used to update the --primary-color CSS variable by using document.documentElement.style.setProperty('--primary-color', pickedColor). This directly changes the primary color of the page without reloading it. Additionally, to create a secondary color that looks good with the primary color, we use the shadeColor() function. This function takes the picked color and slightly darkens it by 20%, creating a contrasting secondary color for text and hover effects. The shadeColor function works by converting the color from hexadecimal to RGB, adjusting the brightness, and then converting it back to hexadecimal. This ensures that the design remains smooth and coherent, with dynamic color changes based on the user’s input. I even used the less;css function of darkening and lightening the shades of a color in js which, (100 + percent) / 100 either increases or decreases the color intensity, depending on whether the percent is positive (lighten) or negative (darken). This allows us to create a new color that is either lighter or darker than the original, depending on the user’s color choice.  </p>

<p> By using less;css in the js code, this is how I would be able to code thsi part of my project which its color scheme will orginally be pink and grey and will change depening on the users choice in color of the event thet are trying to plan</p>


### Summary

<p> In summary, I have been tinkering with my freedom project tool by using it to practice ways I want to use it in my actual project. Although, I did not code my exact code using the less;css, I coded examles of HOW i would want to use them in the app that I am coding/making. </p>
