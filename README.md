<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Math Quiz Game</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            max-width: 800px;
            margin: auto;
            padding: 20px;
            background-color: #282c34;
            color: #abb2bf;
        }

        h1 {
            color: #61dafb;
        }

        h2 {
            color: #c678dd;
        }

        p {
            color: #abb2bf;
        }

        code {
            background-color: #3e4451;
            padding: 5px;
            border-radius: 4px;
            font-family: 'Courier New', monospace;
            color: #abb2bf;
        }

        pre {
            background-color: #2b2d3a;
            padding: 10px;
            border-radius: 6px;
            overflow: auto;
        }

        footer {
            margin-top: 20px;
            padding-top: 10px;
            border-top: 1px solid #444c56;
            text-align: center;
            color: #abb2bf;
        }
    </style>
</head>

<body>

    <h1>Math Quiz Game</h1>

    <h2>Description</h2>
    <p>This is a Python math quiz game that challenges the player with basic mathematical operations. The project consists of two main files:</p>

    <ul>
        <li><code>game.py</code>: Contains the main logic of the game, including the functions <code>main</code> and <code>play</code>.</li>
        <li><code>calculate.py</code>: Located in the models folder, it defines the <code>Calculate</code> class, responsible for generating random mathematical operations based on a chosen difficulty.</li>
    </ul>

    <h2>Calculate Class</h2>
    <p>The <code>Calculate</code> class has the following attributes:</p>

    <ul>
        <li><code>difficulty</code>: Difficulty level chosen by the player (1 to 4).</li>
        <li><code>value1</code> and <code>value2</code>: Numbers randomly generated for the operations.</li>
        <li><code>operation</code>: Integer representing the operation to be performed (1 = add, 2 = subtract, 3 = multiply).</li>
        <li><code>result</code>: Result of the generated operation.</li>
    </ul>

    <h2>Methods</h2>

    <pre>
        <code>show_operation():</code> Displays the generated operation.
        <code>check_result(response: int) -> bool:</code> Checks if the user's response is correct.
    </pre>

    <h2>game.py</h2>
    <p>The <code>game.py</code> file controls the execution of the game, interacting with the player and managing the accumulated points.</p>

    <h3>How to Run</h3>

    <pre>
        <code>python game.py</code>
    </pre>

    <h3>Features</h3>

    <pre>
        <code>main():</code> Main function that starts the game.
        <code>play(points: int) -> None:</code> Function that implements the game logic, allowing the player to perform mathematical operations.
    </pre>

    <h3>Example Usage</h3>

    <pre>
        <code>from models.calculate import Calculate</code>

        <code>def main() -> None:</code>
        <code>    points: int = 0</code>
        <code>    play(points)</code>

        <code>def play(points: int) -> None:</code>
        <code>    difficulty: int = int(input('Enter the desired difficulty level [1, 2, 3, or 4]: '))</code>

        <code>    calc: Calculate = Calculate(difficulty)</code>

        <code>    print('Enter the result for the following operation: ')</code>
        <code>    calc.show_operation()</code>

        <code>    result: int = int(input())</code>

        <code>    if calc.check_result(result):</code>
        <code>        points += 1</code>
        <code>        print(f'You have {points} point(s).')</code>

        <code>    continue_game: int = int(input('Do you want to continue playing? [1 - yes, 0 - no] '))</code>

        <code>    if continue_game:</code>
        <code>        play(points)</code>
        <code>    else:</code>
        <code>        print(f'You finished with {points} point(s).')</code>
        <code>        print('Until next time!')</code>

        <code>if __name__ == '__main__':</code>
        <code>    main()</code>
    </pre>

    <h2>calculate.py</h2>
    <p>The <code>calculate.py</code> file defines the <code>Calculate</code> class, which encapsulates the logic to generate and verify mathematical operations.</p>

    <h3>Usage</h3>

    <pre>
        <code>from models.calculate import Calculate</code>

        <code># Create an instance of the Calculate class with the desired difficulty</code>
        <code>calc = Calculate(difficulty=2)</code>

        <code># Display the generated operation</code>
        <code>calc.show_operation()</code>

        <code># Wait for the user's response</code>
        <code>response = int(input('Your response: '))</code>

        <code># Check if the response is correct</code>
        <code>if calc.check_result(response):</code>
        <code>    print('Correct answer!')</code>
        <code>else:</code>
        <code>    print('Wrong answer.')</code>
    </pre>

    <h3>Calculate Class</h3>
    <p>The <code>Calculate</code> class generates random mathematical operations based on a chosen difficulty.</p>

    <h4>Properties</h4>

    <ul>
        <li><code>difficulty:</code> Integer representing the difficulty level (1 to 4).</li>
        <li><code>value1</code> and <code>value2:</code> Randomly generated integers.</li>
        <li><code>operation:</code> Represents the operation to be performed (1 = add, 2 = subtract, 3 = multiply).</li>
        <li><code>result:</code> Result of the generated operation.</li>
    </ul>

    <h4>Methods</h4>

    <pre>
        <code>show_operation():</code> Displays the generated operation.
        <code>check_result(response: int) -> bool:</code> Verifies if the user's response is correct.
    </pre>

    <h2>Contribution</h2>
    <p>Contributions are welcome! Feel free to open issues or send pull requests.</p>

</body>

</html>