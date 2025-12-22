# Tool Learning Log

## Tool: ** Less: Css **

## Project: ** Outfit planner **

<p> For today I decided to code and create a weekly planner to get familiar of how my project may look. Since it is only the begining I used the offical Less:css website (https://lesscss.org/) and google to get a little more information .


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Weekly Planner</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="planner">
        <h1>Weekly Planner</h1>
        <div class="week">
            <div class="day" id="monday">
                <h2>Monday</h2>
                <ul class="tasks">
                    <li class="task">Task 1</li>
                    <li class="task">Task 2</li>
                    <li class="task">Task 3</li>
                </ul>
            </div>
            <div class="day" id="tuesday">
                <h2>Tuesday</h2>
                <ul class="tasks">
                    <li class="task">Task 1</li>
                    <li class="task">Task 2</li>
                    <li class="task">Task 3</li>
                </ul>
            </div>
            <div class="day" id="wednesday">
                <h2>Wednesday</h2>
                <ul class="tasks">
                    <li class="task">Task 1</li>
                    <li class="task">Task 2</li>
                    <li class="task">Task 3</li>
                </ul>
            </div>
            <div class="day" id="thursday">
                <h2>Thursday</h2>
                <ul class="tasks">
                    <li class="task">Task 1</li>
                    <li class="task">Task 2</li>
                    <li class="task">Task 3</li>
                </ul>
            </div>
            <div class="day" id="friday">
                <h2>Friday</h2>
                <ul class="tasks">
                    <li class="task">Task 1</li>
                    <li class="task">Task 2</li>
                    <li class="task">Task 3</li>
                </ul>
            </div>
            <div class="day" id="saturday">
                <h2>Saturday</h2>
                <ul class="tasks">
                    <li class="task">Task 1</li>
                    <li class="task">Task 2</li>
                    <li class="task">Task 3</li>
                </ul>
            </div>
            <div class="day" id="sunday">
                <h2>Sunday</h2>
                <ul class="tasks">
                    <li class="task">Task 1</li>
                    <li class="task">Task 2</li>
                    <li class="task">Task 3</li>
                </ul>
            </div>
        </div>
    </div>
</body>
</html>

```css
@primary-color: #3498db;
@secondary-color: #2ecc71;
@task-bg-color: #ecf0f1;
@border-color: #ddd;
@hover-color: lighten(@primary-color, 10%);


.planner {
    font-family: 'Arial', sans-serif;
    background-color: #f5f5f5;
    width: 80%;
    margin: 0 auto;
    padding: 20px;
    border-radius: 15px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);

    h1 {
        text-align: center;
        color: @primary-color;
        font-size: 2.5em;
    }
}

.week {
    display: grid;
    grid-template-columns: repeat(7, 1fr);
    grid-gap: 20px;
    margin-top: 20px;
}

.day {
    background-color: white;
    border-radius: 10px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    padding: 15px;
    text-align: center;

    h2 {
        color: @primary-color;
        font-size: 1.5em;
        margin-bottom: 15px;
    }

    .tasks {
        list-style-type: none;
        padding: 0;

        .task {
            background-color: @task-bg-color;
            margin: 10px 0;
            padding: 10px;
            border-radius: 5px;
            font-size: 1.2em;
            transition: background-color 0.3s ease;

            &:hover {
                background-color: @hover-color;
            }
        }
    }

    // Responsive Design: If the screen is small (like a mobile device), make the grid stack
    @media (max-width: 768px) {
        .week {
            grid-template-columns: 1fr;
        }
    }
}

```




### 11/2/2025
I wanted to learn how I could use my code and what I could make out if it. So I went on the less;css website to look at how the codes were used. For Example, I learned that if I was to use a certain color like blue and want to reuse it but want it darker, I do not have to rewrite the code for a darker blue but instead increase its complexion by whatever percentage I want. @link-color:        #428bca; // sea blue
@link-color-hover:  darken(@link-color, 10%);     the "darken" and the "10%" keeps the blue but just makes it a darker version. I could also lighten it by 10 or 20 percent if I swap out the darken to lighten.  I also learned about the usage of primary and secondary colors where you could use these codes to get the colors of your design to look good against each other.

``` css
 @primary:  green;
@secondary: blue;
.section {
  @color: primary;

  .element {
    color: @@color;
  }
}
```

So, after going over some of the commonly used codes in less;css I tinkered with it by picking out potential headings and background colors for the project I am trying to create.

``` css
  // Base colors
@primary-color: #ff6f61;    // coral, for main buttons/links
@secondary-color: #b19cd9;  // light purple, for secondary elements
@bg-color: #ffc0cb;          // light pink
@text-color: #ffffff;        // white

// Body styling
body {
  background-color: @bg-color;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  font-family: Arial, sans-serif;
  margin: 0;
}

// Main message
.main-message {
  color: @text-color;
  font-weight: bold;
  font-size: 2rem;
  text-align: center;
  margin-bottom: 20px;
}

// Example buttons using primary/secondary
.button {
  padding: 12px 24px;
  border: none;
  border-radius: 5px;
  font-weight: bold;
  cursor: pointer;
  text-transform: uppercase;
  color: @text-color;
  transition: all 0.3s ease;
}

.button-primary {
  background-color: @primary-color;
  &:hover { background-color: lighten(@primary-color, 10%); }
}

.button-secondary {
  background-color: @secondary-color;
  &:hover { background-color: lighten(@secondary-color, 10%); }
}
```
This shows the potential starting for my project. I wanted the background to be pink and for the primary and secondary colors to lighly blend with the pink so I chose to make the primary colors a coral and the secondary color purple. Then I chose to make the text colors white. I made the font a bold Arial so that the heading would be written like that. This code just shows the beginning of the designs and illustrations.
Class comments



### 11/9/2025:
* I watched youtube videos that explain less;css better. For example in this youtube video it explains how to first set up less;css while you are coding it. <a href = "https://www.youtube.com/watch?v=YD91G8DdUsw"> youtube viedeo </a>

* This youtube video taught me how I could use functions in less <a href = "https://www.youtube.com/watch?v=U9mJmy0YhmQ> youtube
* Text


### 11/16/2025
* To tinker with my tool, I decided to use my old sep10 freedome project code to add the less;css code to. To help me out I used google, and the offical website of less;css
* Using less;css on my old code porject made the code be more readable and easier to understand.
* what I changed and what I did was; create a variable for each of things I used. I made blue the primaery color since that was the most noticable on my project for the links. I have grey the secondary color since it was noticable but less than blue for the borders. I also leanred that while coding (!important) could be used when there is certain things that needs to be used smoothly. Some fo the biggest changes I made was that beofre my navbar did not change colors when it was hovered on since i did not code it that way when i first started making myy project but now with the new chnages using less the navbar changes color when it is hovered 0n. less did not only make this more creative but it also ensured that the chnages are strict and stay the same no matter what.

``` css
// Step 1: Global Variables
@primary-color: #0d6efd;       // Primary color (Blue) for accents like links and buttons
@secondary-color: #6c757d;     // Secondary color (Gray) for borders, etc.
@bg-dark: #2c2c2c;             // Dark background color for the body and navbar
@bg-light: #ffffff;            // Light background color for content boxes
@text-color: #ffffff;          // Default text color (white for readability on dark background)
@text-link-color: #0d6efd;     // Link color (matching primary color)
@border-color: #6c757d;        // Border color (grayish) for containers
@padding: 15px;                // Standard padding to maintain consistent spacing
@font-family: 'Arial', sans-serif;  // Set the font for the page

// Step 2: Mixins for Reusable Styles
// Mixin to apply border-radius to any element
.border-radius(@radius: 5px) {
  border-radius: @radius;
}

// Mixin to center content using Flexbox
.flex-center {
  display: flex;
  justify-content: center;
  align-items: center;
}

// Mixin for smooth transitions (e.g., for background-color changes on hover)
.smooth-transition(@property: background-color, @duration: 0.3s) {
  transition: @property @duration ease;
}

// Step 3: Global Styles
// Body styles including background and text color
body {
  background-color: @bg-dark;
  color: @text-color;
  font-family: @font-family;
  scroll-behavior: smooth;
}

// Navbar customization with link hover effects
.navbar {
  background-color: @bg-dark;  // Set background color of navbar
  .navbar-nav {
    margin-left: auto;         // Align navbar items to the right
  }
}

.navbar a {
  color: @text-color !important;  // Ensure navbar links are white
  margin-right: 20px;
  .smooth-transition(background-color);  // Smooth transition for background color
  &:hover {
    background-color: darken(@primary-color, 10%);  // Darken the background when hovering over links
  }
}

// Hero Section with background image and centered text
.hero-section {
  background: url('https://img.freepik.com/free-photo/gradient-navy-blue-digital-grid-wallpaper_53876-104785.jpg?semt=ais_hybrid&w=740') no-repeat center center/cover;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  h1 {
    color: white;
    font-size: 5rem;
    font-weight: bold;
    text-shadow: 2px 2px 8px black;  // Add a shadow effect to make the text pop
  }
}

// Main content section style
.main-content {
  background-color: @bg-dark;
  padding-top: 60px;  // Add padding to top for spacing
}

// Heading styles
h2 {
  color: @primary-color;  // Set heading color to blue
  text-align: center;
  margin-top: 60px;  // Margin for spacing
}

// Container Border Style (used in intro, hardware, and software sections)
.container-bordered {
  border: 2px solid @border-color;  // Use gray border color
  padding: @padding;  // Apply standard padding
  margin: 10px;
  background-color: @bg-light;  // Light background for content
  color: black;
  .border-radius(5px);  // Apply border radius (rounded corners)
}

// Hardware & Software Section - Flexbox to wrap items responsively
.hardware-section, .software-section {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;  // Center items within the flex container
}

// Carousel adjustments to ensure consistent sizing
.carousel {
  margin: 40px auto;
  max-width: 800px;
}

.carousel-item img {
  max-height: 400px;  // Ensure images don't get too large everytime the website is visted
  object-fit: contain;  // Mkes sure there is a good fitting ratio of whatevrr contenet is inside the conatainer.
}

// Link hover effects and color transitions
.container-link a {
  font-weight: bold;
  text-decoration: none;
  color: @text-link-color;  // Use primary color for links
  .smooth-transition(color);  // Smooth transition for color changes
  &:hover {
    color: darken(@text-link-color, 15%);  // Darken the link color on hover
  }
}

.link-title {
  margin-bottom: 10px;
  font-size: 1.2rem;  // Slightly larger font for better readability
}

// Responsive Styling (for smaller screens)
@media (max-width: 768px) {
  .hero-section h1 {
    font-size: 3rem;  // makes the font on smaller screens automically smaller
  }
  .container-bordered {
    max-width: 90%;  // Adjust width of content containers on mobile
  }
  .carousel-item img {
    max-height: 300px;  // sctricly makes sure that the size of the coursel will automatically switch to its needed size without issues
  }
}
```

### 11/23/2025

* Today i learned the donts while using less;css. I used google and youtube videos to learn about this.

<a href = "https://www.youtube.com/watch?v=RctP49SwyT0&t=483s" >

* Don't over nest
* Don't forget variable usage since they are constants in less;css
* Don't link files inncorrectly
* Don't use @import without a plan
* Don't neglect fendemntals of css



* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->



### 12/7/2025

```css
/* Variables for color */
@primary-color: #4CAF50; /* Green */
@secondary-color: #333;   /* Dark gray */
@light-gray: #f4f4f4;     /* Light gray */
@white: #fff;             /* White */

/* General Page Styles */
body {
    font-family: Arial, sans-serif;
    background-color: @light-gray;
    margin: 0;
    padding: 0;
}

/* Header Styles */
header {
    background-color: @primary-color;
    color: @white;
    padding: 20px;
    text-align: center;

    h1 {
        margin: 0;
        font-size: 36px;
    }
}

/* Navigation Bar */
nav {
    background-color: @secondary-color;
    overflow: hidden;

    a {
        float: left;
        display: block;
        color: @white;
        text-align: center;
        padding: 14px 20px;
        text-decoration: none;

        &:hover {
            background-color: lighten(@secondary-color, 10%);
            color: black;
        }
    }
}

/* Main Content Area */
main {
    padding: 20px;
    background-color: @white;
    max-width: 1100px;
    margin: 20px auto;
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);

    h2 {
        color: @secondary-color;
        font-size: 28px;
    }

    p {
        font-size: 18px;
        line-height: 1.6;
        color: darken(@secondary-color, 20%);
    }
}

/* Section Styles */
section {
    margin-bottom: 30px;
}

/* Footer Styles */
footer {
    background-color: @secondary-color;
    color: @white;
    text-align: center;
    padding: 10px;
    position: fixed;
    width: 100%;
    bottom: 0;

    p {
        margin: 0;
        font-size: 16px;
    }
}

/* Forms */
form {
    background-color: lighten(@light-gray, 10%);
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.1);

    input[type="text"],
    input[type="email"],
    textarea {
        width: 100%;
        padding: 10px;
        margin: 10px 0;
        border: 1px solid #ccc;
        border-radius: 4px;
        font-size: 16px;
    }

    button {
        background-color: @primary-color;
        color: @white;
        border: none;
        padding: 15px 20px;
        font-size: 18px;
        cursor: pointer;
        border-radius: 4px;

        &:hover {
            background-color: darken(@primary-color, 10%);
        }
    }
}
```
### 12/8/2025
I learned to use Arrays and loops ia a less;css code

```css
@colors: #3498db, #e74c3c, #2ecc71, #f39c12; // these are all the colors put in an array because they are all the ones that are going to be looped through and used

// instead of writing out each of the color and its code, you could code a loop that involves all the colors that are going to be used.
// .each is a loop that is used to pass through each of the colors in an array so that the program uses them accordingly
// @value helps the code apply the styles without repitiion of code
// code will go through every color and change the background when the next color is up
.each(@colors, {
  .color-@{value} {
    background-color: @value;
    color: white;
    padding: 10px;
    margin: 10px;
    text-align: center;
    border-radius: 5px;
  }
});
```

### 12/21/25

```css
const less = require('less');
const fs = require('fs');

fs.readFile('styles.less', 'utf8', (err, lessCode) => {
    if (err) throw err;

    less.render(lessCode)
        .then(output => {
            console.log(output.css);  // Compiled CSS
        })
        .catch(err => {
            console.error(err);
        });
});
```

```css
// Define an array of colors
@colors: #ff5733, #33ff57, #3357ff, #f5a623;

// Loop through the array to create styles for each color
.generate-buttons(@colors) {
  .each(@index) when (@index <= length(@colors)) {
    @color: extract(@colors, @index); // Get the color from the array

    // Create a class for each button color
    .button-@{index} {
      background-color: @color;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
      cursor: pointer;

      &:hover {
        opacity: 0.8;
      }
    }

    // Recursive call to process the next item in the array
    .each(@index + 1);
  }
}

// Call the mixin to generate button styles
.generate-buttons(@colors);
```


