# Battleship Game
In this project, we have designed a BattleShip game using OOPs concepts. We used Ruby as the language of choice.

## Requirements
1. You need to run this game in an OSX or Linux machine
2. This needs [Ruby to be installed](https://www.ruby-lang.org/en/documentation/installation/).

## Directory Structure
We have two main directories in this project.

1. bin
2. lib

### 1. bin

bin contains all the executable command line tools. To run any command first, install [Ruby](https://www.ruby-lang.org/en/documentation/installation/). Then you can run the commands under the bin directory or you can execute the command by giving the absolute/relative path to the executable

Following is the command available for now

* `battleship`

#### Usage of the commands

* `battleship` - This command runs the program and launches the shell. To exit the prompt use the `exit` command

### 2. lib
`lib` contains all the classes used to implement the `battleship` program. These classes are implemented using Ruby language.


#Functionalities of `battleship` program
Execute the `battleship` to start the interactive shell.

## Register User

Use the command `add_player`.  
It takes one argument as described below

* name of the player - It's a mandatory argument. Pass a unique name

### Example
```
$add_player souman
```

## Start a Game

Use the command `start_game`  
It takes two arguments in order as described below

* Player1 Name - It's a mandatory argument. The name should  be unique and should not contain space
* Player2 Name - It's a mandatory argument. The name should  be unique and should not contain space

### Example
```
$start_game souman mandal
```

## Fire in opponents board

Use the command `fire`  
It takes one argument in order as described below

* coordinate - It's a mandatory argument, should be the coordinate where the current player wants to hit. This is case sensitive, so `C5` is valid but `c5` is not.

### Example
```
$fire C5
```

## Status of your board

Use the command `my_board_status`. It takes no arguments and prints the details of the current player's board.

### Example output


|    	| A  	| B 	| C 	| D 	| E  	| F 	| G 	| H 	| I 	| J 	|
|----	|----	|---	|---	|---	|----	|---	|---	|---	|---	|---	|
| 1  	| -  	| - 	| - 	| - 	| -  	| - 	| - 	| - 	| - 	| - 	|
| 2  	| *  	| * 	| - 	| - 	| *B 	| B 	| B 	| B 	| - 	|   	|
| 3  	| *S 	| - 	| - 	| - 	| -  	| - 	| * 	| - 	| - 	| - 	|
| 4  	| *S 	| - 	| - 	| * 	| -  	| - 	| - 	| - 	| - 	| - 	|
| 5  	| S  	| - 	| * 	| - 	| C  	| C 	| C 	| C 	| C 	| - 	|
| 6  	| -  	| - 	| - 	| - 	| -  	| C 	| - 	| D 	| - 	| - 	|
| 7  	| -  	| - 	| * 	| - 	| -  	| C 	| - 	| D 	| - 	| - 	|
| 8  	| -  	| - 	| - 	| - 	| -  	| C 	| - 	| - 	| - 	| - 	|
| 9  	| -  	| - 	| - 	| - 	| -  	| - 	| - 	| - 	| - 	| - 	|
| 10 	| -  	| - 	| - 	| - 	| -  	| - 	| - 	| - 	| - 	| - 	|

`*` denotes a hit

## Status of opponent's board

Use the command `other_player_board_status`. It takes no arguments and prints the details of the other player's board.

### Example output

|    	| A 	| B 	| C 	| D 	| E 	| F 	| G 	| H 	| I 	| J 	|
|----	|---	|---	|---	|---	|---	|---	|---	|---	|---	|---	|
| 1  	| - 	| - 	| - 	| - 	| - 	| - 	| - 	| - 	| - 	| - 	|
| 2  	| * 	| * 	| - 	| - 	| H 	| - 	| - 	| - 	| - 	| - 	|
| 3  	| H 	| - 	| - 	| - 	| - 	| - 	| - 	| * 	| - 	| - 	|
| 4  	| H 	| - 	| - 	| - 	| - 	| - 	| - 	| - 	| - 	| - 	|
| 5  	| - 	| - 	| * 	| - 	| - 	| - 	| - 	| - 	| - 	| - 	|
| 6  	| - 	| - 	| - 	| - 	| - 	| - 	| - 	| - 	| - 	| - 	|
| 7  	| - 	| - 	| * 	| - 	| - 	| - 	| - 	| - 	| - 	| - 	|
| 8  	| - 	| - 	| - 	| - 	| - 	| - 	| - 	| - 	| - 	| - 	|
| 9  	| - 	| - 	| - 	| - 	| - 	| - 	| - 	| - 	| - 	| - 	|
| 10 	| - 	| - 	| - 	| - 	| - 	| - 	| - 	| - 	| - 	| - 	|

`*` denotes a hit where there are no ships

`H` denotes a hit where there is a ship 

## Additional Methods

* `help` prints the available commands


# Assumptions
* A player can not play with himself/herself
* Boards has total 10*10 coordinates. x_coordinates are denoted by [A,B,C...J], y_coordinates are denoted by [1,2,3...10]
* Player names have to be unique
* Both players use the same console to provide input
* Ships cannot overlap with each other in the same coordinates
* Player cannot hit the same coordinate multiple times


# Future roadmap
* Units and functional tests for the code
* Allow users to join the game from different consoles
* Track the history of how the game has progressed (store each shot with a time stamp) and generate insights(like avg number of shots to close a game)
* Building a GUI.
* Option to increase/decrease the board size
* Option to have different number of ships
* Improve time complexity to draw the board randomly
* Keep track of games participated/won/lost by a player
