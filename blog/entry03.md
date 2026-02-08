# Entry 3
##### 2/2/2026

### Progress:
<p>While learning about my tool, I learned and dove deep into how I could use Logic statements and artimetic and color functions in css. I was able to learn about this through google and <a href ="https://lesscss.org/#"> the offical website: less;css </a>. Specfically, I learned that I could use logic statements to apply certain styles on certain events like buttons. With functions, I learned how I could use math operataions to get certain events like buttons, boxes to be fixed to a certain size. I also learned about color functions which maniplualte a solid color such as blue to either lighten or darken depdedning on the situation.  </p>


### FUNCTIONS

<p> COLOR FUNCTIONS: </p>

<p>In color functions there are many ways you could manipulate a color. The ways I learned where lighten and darken, and fadeIn and fadeOut functions. Each of these for functions chnage a color in multiple ways depending on how you apply it in the code</p>

<p>Lighten and Darken:</p>

```css
@base-color: blue;
@base-color: pink;
.color {
  color: lighten(blue, 20%);
}


.color {
  color: darken(pink, 10%);
}
```

<p> In these codes, the fucntions lighten and darken are being used to change the base color which is blue to either become lighter or become darker. In between the () you see values such as 20% and 10%. These values represented what each of the function will lighten or darken by. In the first code, the fucntion is making the color blue lighter by 20%. In the second code, the fucntion is making the color pink darker by 10%. These properties could be used for any colors that are being used in the code so that the colors are able to change accordingly.</p>

<p> FADEIN AND FADEOUT: </p>

```css
@base-color: pink;
@base-color: blue;

@fadein-color: fadein(@base-color, 30%);


@fadeout-color: fadeout(@base-color, 20%);
```

<p>fadein and fadeout work to manipluate a oolor based on its transparency. Specifically, fadein makes a color less transparent while fadeout makes a color more trasnparent. In the first code, the color pink is being manipulated to being less transparent and the second one is being manipluated to becoming more transparent. Each line of code also have a number value which indicates how transparent they are becoming. Pink is lessening in transparency by 30% and Blue is darkening in transparency by 20%. </p>


<p> MATH FUNCTIONS: </p>

<p> In math fucntions, you could use math operations such as multiplying/dividing/subtracting/adding to manipluate the size of boxes, buttons, carousels, etc. on the less;css website, it introudced me to some propterties of math functions and how they are usually coded. But, i wanted to see them used in actual css code put together because that is what helps me best understand how each code/property work. So, to understand more, I used google. Spefically, I was curious on learning how I could use things such as sqrt, ciel, and floor, and as multiplying/dividing/subtracting/adding in my css code. So, I searched each one indivually to not only learn more but to get an actual visual of how each property is supposed to work. I focused on how I could use these math functions on things such as boxes and buttons.</p>

<p>SQRT AND OPERATIONS: </p>

<p> sqrt stand for squre root </p>

<p> This is a code snippet given by google. Specfically, I asked how would I could a button using sqrt and math operations. Google gave me the snippet below in which I used it to learn what each property is doing. </p>

```css

@base-size: 16px;
@scale-factor: 1.25;
@gutter: 10px;
@button-multiplier: 1.5;


.button {
  width: @base-size * @button-multiplier * 4;
  height: @base-size * @button-multiplier * 2;
  padding: percentage(0.1);
  border-radius: unit(sqrt(@base-size), px);
  font-size: @base-size * 1.1;
  background: #e74c3c;
  color: white;
  border: none;
  cursor: pointer;
```

<p> First, google Sets the base unit for sizing elements such as the base size. scale factor, gutter, and button multiplier. Thier values are the values being used to multiply. Multiplying and square rooting the values of the buttons is fixing it to be exactly perfect. </p>

<p>what the code is doing...</p>

```css
width: @base-size * @button-multiplier * 4;
```

<p> The base size is being multiplied by the button multiplier and 4. So, the numbers/equatation is (16)(1.5)(4) which is 96. What this is doing is its calculating the width of the button</p>

```css
height: @base-size * @button-multiplier * 2;
```

<p>The base size is being multiplied by the button multipler and 2. So, the number/equtation is (16)(1.5)(2) which is 48. This is calculating the height of the button.</p>

```css
border-radius: unit(sqrt(@base-size), px);
  font-size: @base-size * 1.1;
  ```

<p>The border radius is being square rooted using the value of the base size which the result would be 4. But, to ensure that the prgram understands the units of the value so that it could work accordingly, we have to code in units and at the end add px so that the program understands that the code for button has to follow 4px. The code is also fixing the content that goes on the button which would be the text. So, it fixes the font size by multiplying the base size by 1.1 which would be (16)(1.1) = 17.6. </p>

<p> So, in conclusion sqrt and math operations in Less let you calculate and scale CSS values automatically instead of hard-coding numbers, so sizes, spacing, and shapes stay consistent and keep up when one base value changes. </p>


<p>CEIL AND FLOOR</p>

<p>Another math function I learned was ceil and floor. Though I learned how to use ciel and floor in javascript, when I saw it was used in css as well I wanted to learn more about how I could use them in my code. So, it was a nother thing I asked google about after seeing it on the less;css website.</p>


```css

@base-size: 16px;
@scale-factor: 1.25;
@gutter: 10px;
@button-multiplier: 1.5;

.box {
  width: @base-size * 10;
  height: @base-size * 5;
  padding: ceil(@gutter / 2);
  margin: floor(@gutter / 1.5);
  border-radius: round(@base-size / 4);
  background: #3498db;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: @base-size;
}
```

<p> This is the full code of the box being made, given by google </p>

```css
padding: ceil(@gutter / 2);
margin: floor(@gutter / 1.5);
  ```

<p> In this code, ciel is dividing the gutter by 2 and then rounding that number up. So it would be, 10/2 = 5 = 5. It's job in that spefcic code is to make sure that the padding of the box isnt too small and always at perfect size. It also works to perfecting the padding to always be at perfect whole number for if the number ever changes so that the padding never sizes down. So, if later the padding size would change into 9px/2 = 4.5 it would round up and have padding stay at the size of 5. Floor does the same thing but instead of rounding up, it rounds down. In this code, it is ensuring that the space between elements is not to big. So, it would be 10/1.5 = 6.66 = 6. Each element would get 6px of space. </p>

<p>In conclusion, ciel and floor help maintain the sizng of elements by sizing them out all proportionally. You could choose whther you want those elemment always sized bigger or smaller by using either ciel or floor</p>


### LOGIC/CONDITIONALS:

<p> Before winter and during winter break, I was learning on how i could apply arrays and loops into css. While doing that, I got a litte knowledge on how conditionals could be used in css as well since I had to use it to try out the loops and arryas I was working with.

```css
if(iscolor(@current-color), @current-color, gray);
```

<p> The code looked like this from my last blog. What this code is saying/doing is that if the current color is being checked off and is true then use that current color and if not then fall back and use the color grey. It is basically checking to see if the staement is true or not. So, after finishing blog 2, I wanted to learn more about how I could involve conditionals/logic statements coding css. Instead of using google to give me code snippets to teach me about the conditiona I searched up "using conditionals in less;css" and found a website called <a href ="https://stackoverflow.com/questions/40722626/conditional-when-in-less-file"> stackoverflow </a>. This website, taught me the difference of using if and when in conditionals used in css and showed me actual snippets of code that use the conditionals.</p>

<p> In css for conditionals, if is only used one property at a time which is why it isn't used as much in css since css works with many variables, properties, and elements at the same time. This is why in css, when() is used isnteaf of if().When() is used with mixins (reausbale code blocks).</p>

<p>To evulate conditionals in css to get a better understanding, I chose a code from the  <a href ="https://stackoverflow.com/questions/40722626/conditional-when-in-less-file"> stackoverflow </a> website and read the notes/information about that code to learn how when() is used. </p>

```css
/*
Source - https://stackoverflow.com/a/40722788
Posted by Harry
Retrieved 2026-02-08, License - CC BY-SA 3.0
*/

@banner-separation-style: 'thick_border';
.border-styles() when (@banner-separation-style = 'thick_border') {
    header { border: 2px solid red; }
    nav { border: 2px solid green; }
}
.border-styles;
```

<p> From reading about this snippet of code, I learned what the code is doing/saying and learned how I could use when() when I use conditionals to build something.</p>

<p> Tne first line of code, is a variable that stores the string 'thick_border'. This varaible is used to decide what kind of borders to put on the elements. The first part of the second line of code is a mixin, which would be the reuasable block of css and what we will call at the end after the conditioal is checked. The mixin was picked by the person who created the code. The second part of the second line of code is the condtional itself. This conditional is saying that when banner-seperation-style = 'thick_border' then apply all its css to the border style. In this case, for when that conditional is checked, the header's border is going to be 2px soild red and the nav's border will be 2px solid green. </p>

<p>Conditionals are known to have else statments as well for when the first if statement or in this case when() is not true. However, the website did not mention anything about that. So, I tried it myself. However, I did not know what to use for a false when() statement in css. So, I searched up "when using conditioanls in css, what is the oppostite of when() when the first when() is false?". I learned I would have to use when not(). After learning this, I applied when not() to the code I got from the website above and just added to it.</p>

```css

@banner-separation-style: 'thick_border';
.border-styles() when (@banner-separation-style = 'thick_border') {
    header { border: 2px solid red; }
    nav { border: 2px solid green; }
}

.border-styles() when not (@banner-separation-style = 'thick_border') {
  header {border: 1px solid grey; }
  nav {border: 1px solid purple; }
}

.border-styles;

```

<p> The when not() is doing exactly what else if or else would in javascript, it activates the second else if the first one is false. In this case, the code is saying that when banner-separation-style does not equal 'thick_border' then the header's border will be 1px and grey instead of 2px and red and the nav's border will be 1px and purple instead of 2px and green.</p>

<p>The main difference between the conditionals from my last blog to this one was that during my last blog I knew very little about hot I could use conditionals in css fully. This blog, I learned that I could treat a css logic the same way as a java logic except I have to use when()/when not() instead of if/else if/else. </p>


### Engineering Design Process:

<p> Learning about math fucntions, color fucntions, and logic conditionals in css helped me code something of my own. I used all of the properties and rules I learned to create a css code that is converted into lss since that is the whole point of less;css - making css shorter and more readable. To decide how I was going to use everything I learned in the code was going to create, I had to decide what I wanted to make using these properties. I know I needed and wanted to use a logic statement, so, I came up with the idea of a dark theme and light theme and decided that I was going to manipulate margins, padding, font, and width and have them do different things based on the theme. I also decided to code in paragraphs and headings. </p>

```css
@base-font: 16px;
@base-padding: 10px;
@base-margin: 12px;
@base-width: 200px;



.theme() when (@theme = dark) {

  body {
    background-color: #1a1a1a;
    color: #f5f5f5;
    font-size: floor(@base-font * 1.2);      // slightly bigger font
    padding: ceil(@base-padding * 1.5);     // 10 * 1.5 = 15px, rounded up
    margin: floor(@base-margin / 2);        // 12 / 2 = 6px, rounded down
    width: @base-width * 1.1;               // slightly wider layout
  }

  h1 {
    font-size: sqrt(@base-font) * 5;       // sqrt(16) = 4 * 5 = 20px
    margin-bottom: ceil(@base-margin / 1.5);
  }

  p {
    font-size: @base-font;
    padding: floor(@base-padding / 1.5);
  }
}

.theme() when not (@theme = dark) {

  body {
    background-color: white;
    color: dark grey;
    font-size: floor(@base-font * 1);        // 16px
    padding: ceil(@base-padding * 1);        // 10px
    margin: floor(@base-margin / 1);         // 12px
    width: @base-width * 1;                  // 200px
  }

  h1 {
    font-size: sqrt(@base-font) * 4;        // 4 * 4 = 16px
    margin-bottom: ceil(@base-margin / 2);
  }

  p {
    font-size: floor(@base-font * 0.9);     // 16 * 0.9 = 14.4px -> 14px
    padding: ceil(@base-padding / 2);       // 5px
  }
}


.theme();
```

<p> DARK THEME CODE:</p>

```css

.theme() when (@theme = dark) {

  body {
    background-color:dark grey;
    color: light grey;
    font-size: floor(@base-font * 1.2);
    padding: ceil(@base-padding * 1.5);
    margin: floor(@base-margin / 2);
    width: @base-width * 1.1;
  }

  h1 {
    font-size: sqrt(@base-font) * 5;
    margin-bottom: ceil(@base-margin / 1.5);

  p {
    font-size: @base-font;
    padding: floor(@base-padding / 1.5);
  }
}
```

<p> For this logic statement that is dark theme, I coded it for when the theme is indeed dark then the background color is black. For the font size, I used floor so that when base font is multiplied by 1.2 it rounds that number down and makes it a whole number. Here the font, is increaed a bit from 16px to 19px. For the padding, I used ciel to increase the padding size in the body. I multiplied the base padding by 1.5 increasing it from the orginal size of 10px too 15px. For the margin, I divided base margin by 2 then floored it so that it would make the margin size 6px. I increased the width of the body by 1.1 so that there would be a wider layout. For the h1 (heading), I manipulated the font by having it square rooted then multipled by 5 which in the end would give me 20. This would make the font of the heading 20px. For the margin bottom which would be the size below an element, I divided its base by 1.5 then cieled it to round up. The result would be 8px meaning that the space between below each element is 8px. Then for the paragrapgh part, I kept the font size the same base font size which is 16px. For the padding of the paragraph, I divided its base by 1.5 then floored it which became 6px. The size of the padding of the paragrapgh is 6px. </p>


<p> For when the them is NOT dark, I coded everything the same, only changing around the numbers and colors making the background white and the text grey. So that both themes have way different styles </p>


### SKILLS:

<p> After learning all of this, the skills I gained, was now accuartley involving math functions and logic statemenst into my css code. At first, I did not know that i could use math functions to manipulate and fix boxes, buttons, etc. After reaseraching and using less;css websites I was able to gain those skills. So now, I could easily be able to build a css code that uses all of these math fucntions and logic statements. To be more specific in terms of the skills gained from learning math fucntions, at first I would have manipulated boxes and buttons and other things only using solid numbers for each one. After learning the power of the operataions and ciel and floor, I gained the skill of being knowledgable of diving and multiplying and rounding up and down for each element so not I could code faster and easier. </p>


### SUMMARY:

<p> In summary, for this blog, I was able to pick where I left off on conditionals from my last blog and was able to learn a new property of css and applying to my own creation of code. I not only learned how to code it, I learned what each property meant and did and how it was used. </p>






[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
