# Entry 2
##### 12/15/2025

### Context
<p> We continued to explore, learn, and practice our tool. To do this, I decided to switch up the css part of my freedom project for sep10.  </p>


### Enigneering designing proccess
<p> To tinker with my tool, I decided to use my old sep10 freedom project code to add the less;css code to. To help me out I used google, and the offical website of less;css Using less;css on my old code porject made the code be more readable and easier to understand. what I changed and what I did was; create a variable for each of things I used. I made blue the primaery color since that was the most noticable on my project for the links. I have grey the secondary color since it was noticable but less than blue for the borders. I also leanred that while coding (!important) could be used when there is certain things that needs to be used smoothly. Some fo the biggest changes I made was that beofre my navbar did not change colors when it was hovered on since i did not code it that way when i first started making myy project but now with the new chnages using less the navbar changes color when it is hovered 0n. less did not only make this more creative but it also ensured that the chnages are strict and stay the same no matter what.



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
  border-radius: @radius;  // Apply border-radius to make corners rounded. Default value is 5px
}

// Mixin to center content using Flexbox
.flex-center {
  display: flex;  // Make the container a Flexbox container
  justify-content: center;  // Center content horizontally
  align-items: center;  // Center content vertically
}

// Mixin for smooth transitions (e.g., for background-color changes on hover)
.smooth-transition(@property: background-color, @duration: 0.3s) {
  transition: @property @duration ease;  // Add smooth transition for changes to a specified property (default is background-color)
}

// Step 3: Global Styles
// Body styles including background and text color
body {
  background-color: @bg-dark;  // Set the background color of the body to dark
  color: @text-color;  // Set the text color to white for readability
  font-family: @font-family;  // Use the 'Arial' font family (or sans-serif as a fallback)
  scroll-behavior: smooth;  // Smooth scrolling behavior when navigating the page
}

// Navbar customization with link hover effects
.navbar {
  background-color: @bg-dark;  // Set the navbar background color to dark

  .navbar-nav {
    margin-left: auto;  // This pushes the navbar items to the right side of the navbar (if using Flexbox)
  }
}

// Styling navbar links
.navbar a {
  color: @text-color !important;  // Set the color of navbar links to white (text color)
  margin-right: 20px;  // Add some space between each navbar link
  .smooth-transition(background-color);  // Add a smooth transition effect for background-color on hover

  &:hover {  // When hovering over a navbar link
    background-color: darken(@primary-color, 10%);  // Darken the primary color by 10% for a hover effect
  }
}

// Hero Section with background image and centered text
.hero-section {
  background: url('https://img.freepik.com/free-photo/gradient-navy-blue-digital-grid-wallpaper_53876-104785.jpg?semt=ais_hybrid&w=740') no-repeat center center/cover;
  // Set a background image, and make sure it covers the entire hero section (no-repeat ensures it doesn't repeat)
  height: 100vh;  // Set the height of the hero section to take up the full screen height
  display: flex;  // Make the hero section a Flexbox container
  align-items: center;  // Vertically align items in the center
  justify-content: center;  // Horizontally align items in the center

  h1 {
    color: white;  // Set the heading text color to white
    font-size: 5rem;  // Set the font size of the heading to 5rem (large)
    font-weight: bold;  // Make the heading text bold
    text-shadow: 2px 2px 8px black;  // Add a shadow effect to the text to make it stand out from the background
  }
}

// Main content section style
.main-content {
  background-color: @bg-dark;  // Set the background color of the main content section to dark
  padding-top: 60px;  // Add 60px of padding to the top of the section (for spacing)
}

// Heading styles
h2 {
  color: @primary-color;  // Set the color of all <h2> headings to the primary blue color
  text-align: center;  // Center the heading text
  margin-top: 60px;  // Add 60px of margin to the top for spacing
}

// Container Border Style (used in intro, hardware, and software sections)
.container-bordered {
  border: 2px solid @border-color;  // Apply a 2px border with the gray border color
  padding: @padding;  // Apply standard padding to the inside of the container
  margin: 10px;  // Add a 10px margin around the container
  background-color: @bg-light;  // Set the container's background color to light
  color: black;  // Set the text color to black
  .border-radius(5px);  // Apply 5px rounded corners to the container
}

// Hardware & Software Section - Flexbox to wrap items responsively
.hardware-section, .software-section {
  display: flex;  // Set the sections as Flexbox containers
  flex-wrap: wrap;  // Allow items to wrap into new lines if there is not enough space
  justify-content: center;  // Center the items horizontally within the container
}

// Carousel adjustments to ensure consistent sizing
.carousel {
  margin: 40px auto;  // Add 40px of space above and below the carousel and center it horizontally
  max-width: 800px;  // Set the maximum width of the carousel to 800px
}

.carousel-item img {
  max-height: 400px;  // Set a maximum height for the images inside the carousel
  object-fit: contain;  // Make sure the images fit well without stretching, keeping their aspect ratio
}

// Link hover effects and color transitions
.container-link a {
  font-weight: bold;  // Make links bold
  text-decoration: none;  // Remove underline from links
  color: @text-link-color;  // Set the link color to the primary blue color
  .smooth-transition(color);  // Add a smooth transition effect for color changes when hovering over links

  &:hover {  // When hovering over a link
    color: darken(@text-link-color, 15%);  // Darken the link color by 15% for a hover effect
  }
}

.link-title {
  margin-bottom: 10px;  // Add 10px of margin below the link title
  font-size: 1.2rem;  // Set the font size of the link title to 1.2rem (slightly larger than normal text)
}

// Responsive Styling (for smaller screens)
@media (max-width: 768px) {  // Apply these styles when the screen width is 768px or smaller (for mobile devices)
  .hero-section h1 {
    font-size: 3rem;  // Make the hero section heading smaller on smaller screens
  }
  .container-bordered {
    max-width: 90%;  // Allow content containers to take up 90% of the screen width on mobile
  }
  .carousel-item img {
    max-height: 300px;  // Reduce the height of the images in the carousel on mobile screens
  }
}
```

<p>If I had used this during the my sep10 freedom project things like my navbar woukd darken when it would get hovered on, the drop down process would not lag and would transistion smoothly,  my carosuel and containers would be permentaly postioned perfectly, etc.</p>


### Skills
<p>I learned how to organize my code better and use the right sizes of text depending on the sizes of the container for more of a visual appeal.  </p>


### SUMMARY:

<p> In summary, To test out how my old freedom project code would have been or looked like I used less;css to practice. 
