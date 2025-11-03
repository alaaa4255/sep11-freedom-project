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
### X/X/XX:
* Text


<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
