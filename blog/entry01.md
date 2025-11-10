# Entry 1
##### 11/3/2025

### Context:
<p>For this years freedom project, instead of building a website we are building mini games among other things. I chose to create a event planner. Specfically, the event planner is supposed to help users to be able to plan out an event for the special and specfic occasian they are hosting. The planner will help them in things such as color schemes, decor, etc. Like last yeat, we are supposed to use a tool while buildinng our projects. I chose <a href ="https://lesscss.org/#"> less;css </a>. Less;css is a backwards-compatible language extension for CSS as the website states. I plan to use this tool by perfecting the creative side of my project using this type of css. Other than using the offical website of less;css I also used <a href = "https://www.geeksforgeeks.org/css/css-preprocessor-less" > css preprocessor </a> to learn about my tool. On both websites I learned how I could maniplate colors togther. </p>

### Enigneering design process:
<p> As of right now, I am in the process of learning about my tool. After exploring both websites specfically  <a href ="https://lesscss.org/#"> less;css </a> I was able to learn a couple of things. One of the things I learned was that I could darken a specific color I used to either a lighter shade or a darker one </p>

``` css
@link-color:        #428bca; // sea blue
@link-color-hover:  darken(@link-color, 10%);
```
</p> This is showing how the sea blue color is being darkened from it's orginal shade to a darker one by 10%. So, instead of rewriting a whole new code for a different shade of a color I could use the variable it was given and just lighten and darken whenever. Another thing I learned was that I coud code colors to blend in together to create a whole new shade. Though with this, operations are required so that program understands what to blend together.


``` css
@red: 255;
@green: 100;
@blue: 50;

@mix-color: rgb(@red - 50, @green + 20, @blue + 30);  // rgb(205, 120, 80)
```
<p> This is showing red, green, and blue mixing together to make a new color. However, the numbers play an importamt role in this. The 255 in the @red is to show the dominance and intensity the shade of the color (255 is the highest shade a color could be). The 100 for the @green is the same thing as the red except it has less of a dominent shade compared to the red . The 50 for the @blue means the exact same thing leaving it to be the lighest dominent shade of the rest. The code inside the variable @mix-color is adding and subtracting to the colors off an obvious new shade. For example, @red is being subtracted by 50 which really means that 50 is being subtracted from 255 since red was orginally 255. This means that the darkness of the red is being reduced to a lighter red. The green is being added by 20 (100 + 20) giving it a darker shade than before and the blue is being added by 30 (50 + 30) also giving it a darker shade. All in all, when the new changes to each indivual color is added it would mean that the new color made would mostly of the red shade since 255 - 50 = 205 making it still the darkest shade of he other color. Then new color would have a darker green then blue but a ligher green then red since 100 + 20 = 120. Finally, the shade would have a darker blue than before but still lighter than the more intense shades it is being mixed with.<p>

<p> This basically taught me that If I can't find an exact shade I need or want, I can pick a couple of shades and mix them together to a get a potential suitable shade of color for what I am making </p>


### Skills
<p> Since I am only currently still learning about my tool, the skills other than the codes listed above that I gained was actually learning how to look in depth on a webiste to learn new things.  For example, after learning about being able to darken and lighten indivual colors, I wondered what else I could do with colors. So, while being on the less;css website I learned how I could use operations to get a carousel to be a certain way or how I could subtract the thickness of a border. So, I went to the search bar styped in color operations in which I learned how I could mix colors together to create a new one. </p>


### Summary
<p> In summary, although I am only in the begining of learning about my tool, I started brainstorming how I could use these codes in my projects and what colors I may want to use and create.

