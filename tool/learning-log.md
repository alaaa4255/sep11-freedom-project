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






### X/X/XX:
* Text

### X/X/XX:
* Text


<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
