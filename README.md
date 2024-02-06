# Math Quiz Game

## Description

This is a Python math quiz game that challenges the player with basic mathematical operations. The project consists of two main files:

- **game.py**: Contains the main logic of the game, including the functions main and play.
- **calculate.py**: Located in the models folder, it defines the Calculate class, responsible for generating random mathematical operations based on a chosen difficulty.

## Calculate Class

The Calculate class has the following attributes:

- **difficulty**: Difficulty level chosen by the player (1 to 4).
- **value1** and **value2**: Numbers randomly generated for the operations.
- **operation**: Integer representing the operation to be performed (1 = add, 2 = subtract, 3 = multiply).
- **result**: Result of the generated operation.

### Methods

- `show_operation()`: Displays the generated operation.
- `check_result(response: int) -> bool`: Checks if the user's response is correct.

# game.py

The `game.py` file controls the execution of the game, interacting with the player and managing the accumulated points.

### How to Run

```bash
python game.py
```
## Features

- 'main()': Main function that starts the game.
- 'play(points: int) -> None': Function that implements the game logic, allowing the player to perform mathematical operations.


# Example Usage
```bash

from models.calculate import Calculate
        
        def main() -> None:
            points: int = 0
            play(points)

        def play(points: int) -> None:
            difficulty: int = int(input('Enter the desired difficulty level [1, 2, 3, or 4]: '))

            calc: Calculate = Calculate(difficulty)

            print('Enter the result for the following operation: ')
            calc.show_operation()

            result: int = int(input())

            if calc.check_result(result):
                points += 1
                print(f'You have {points} point(s).')

            continue_game: int = int(input('Do you want to continue playing? [1 - yes, 0 - no] '))

            if continue_game:
                play(points)
            else:
                print(f'You finished with {points} point(s).')
                print('Until next time!')

        if __name__ == '__main__':
            main()
```
# calculate.py
The  'calculate.py' file defines the Calculate class, which encapsulates the logic to generate and verify mathematical operations.

## Usage
```bash
        from models.calculate import Calculate

        # Create an instance of the Calculate class with the desired difficulty
        calc = Calculate(difficulty=2)

        # Display the generated operation
        calc.show_operation()

        # Wait for the user's response
        response = int(input('Your response: '))

        # Check if the response is correct
        if calc.check_result(response):
            print('Correct answer!')
        else:
            print('Wrong answer.')
```   
# Calculate Class
The 'Calculate' class generates random mathematical operations based on a chosen difficulty.

## Properties

- difficulty: Integer representing the difficulty level (1 to 4).
- value1 and value2: Randomly generated integers.
- operation: Represents the operation to be performed (1 = add, 2 = subtract, 3 = multiply).
- result: Result of the generated operation.

## Methods
```bash  
        show_operation(): Displays the generated operation.
        check_result(response: int) -> bool: Verifies if the user's response is correct.
```   
# Contribution
Contributions are welcome! Feel free to open issues or send pull requests.
