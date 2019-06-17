# Memory Game Project

## Table of Contents

- [Introduction](#Introduction)
- [Scratch Project's Link](#Scratch-Projects-Link)
- [Folders and files used in this project](#Folders-and-files-used-in-this-project)
- [Game Criteria](#Game-Criteria)
- [How to play?](#How-to-play)
- [Steps followed in building this project](#Steps-that-I-have-followed-in-building-this-project)
- [Contributing](#Contributing)

## Introduction

This project is of creating a **Memory Game** which can be a **Matching game**. Matching game is a game that require players to match similar elements-It's a memory testing game. As the name implies, participants need to find a match for a word, picture, or a card. In this created game, players are made to match the cards.

_Benefits of Memory Game:_

```
  * Improves concentration.
  * Increases short term memory.
  * Increases attention to detail.
  * Improves the ability to find similarities and differences in objects.
  * Helps to classify objects that are grouped by similar traits.
```

--------------------------------------------------------------------------------

## Scratch Project's Link

This project's scratch which is a static version of memory game (zip folder) can be downloaded from the following links:
    * <https://github.com/udacity/fend-project-memory-game>

    * <https://github.com/udacity/fend-project-memory-game/archive/master.zip>

--------------------------------------------------------------------------------

## Folders and files used in this project

The folders used in this project are **css, js, img, sounds**. The files that are used in this project are **index.html,app.js,app.css**.

==>css: This folder consist "app.css" file which consist of styles to be applied for HTML components.

==>js: This folder consists of "app.js" file which consist of logic required for game in "java script".

==>img: This folder consists of all the images required in building the game.

==>sounds: This folder consists of all the sounds, that is with ".mp3" extension, which are required in building the game.

==>index.html: This file consists of HTML code which plays main role in getting the view of game window.


--------------------------------------------------------------------------------

## Game Criteria

The criteria that is followed in building this game is:

- A deck of 16 cards with 8 different symbols(2 cards each) play vital role in this game. Initially, they are shuffled.
- `Player` is supposed to click on the cards.
- When a card is clicked, it is made to flip.
- When the `Player` clicked on the first card, the timer starts.
- A comparison of two cards by the `Player` is considered to be made a single move, so the count of moves will be incremented by 1(each time the player make a comparison).
- When the `Player` make comparison, if the two cards match, then they are made to be not get flipped again and the count of matches is incremented by 1.If they do not match, they are flipped again.
- A star rating is given to the player's performance based on the number of moves he/she made to win the game.
- A score panel is displayed above the deck of cards which provide the current status of star rating, time and number of moves along with pause and restart buttons of game.
- When the `Player` match all the cards, that is, the count of matches is equal to 8(as there are 16 cards),then the `Player` is considered to be won the game. Then, a window is displayed in which star rating, time taken, count of moves along with a close button, a play again button are provided.

--------------------------------------------------------------------------------

## How to play?

- This game do not have any rules to play.
- The `Player` has to click on a card and then one more card to make a comparison, this should be done until all the cards are matched.
- The `Player` has to try to complete the game with in as few as possible moves, so that he/she can get good star rating for his/her performance.
- The `Player` can pause the game by clicking on "pause" button.
- The `Player` can resume the game by clicking on "resume" button.
- The `Player` can restart the game by clicking on "restart" button.
- The `Player` can play again once he/she won the game by clicking on "Play again" button.

--------------------------------------------------------------------------------

## Steps that I have followed in building this project

1.First,I have downloaded the scratch project, then unzipped the files and opened index.html file in chrome browser to take a look at the static view of the game.  

2.Initially, two cards are made matched and a card opened. So, I have removed the required classes of those cards in index.html in order to make them close, that is, to their initial view.

3.Then, I have written the required code for getting the game window view in "index.html" and added styles to them in "app.css" file.

4.Next, I have written the logic required for the game in "app.js" file.

5.In app.js file, first I have declared the variables required and used "DOM selectors" to get HTML elements by their class names.

6.Then,I have added an event listener to those elements if required.

7.By using a "for loop", I have added event listeners to all the 16 cards in order to make them flip, when clicked.

8.I have added sounds to the game in order to make it effective, so, created objects to "Audio" class.

9.I have written a condition, that is, if the count of clicked cards is 2, then I have to invoke the `compare()` function.

10.In `compare()` function, I have used "if else". If the two cards matched, then added the classes "match, animated, wobble" and removed the classes "open, show" for the card's class list and incremented `match_cnt` by 1.

11.If the two clicked cards do not match, then I have removed the classes "open, show, disabled" from the class list.

12.Then,I have emptied the `clickedcards` array.

13.I have used one more "if condition", that is, when `match_cnt` is 8, then I have made the timer to be stopped using "clearInterval" and the final star rating is stored in a variable. And a pop-up window is made to be displayed which contain time taken, final star rating, number of moves along with a close button and play again button.

14.Finally,I have written code to shuffle the cards in `shuffle()` function.

_The functions that I have defined in the app.js file are:_

- displayCard():This function is invoked when a card is clicked. The card is made to be flipped, when clicked, in this function.
- compare():This function is invoked when the length of `clickedcards` is 2.This performs the comparison of two clicked cards.
- time():This function is invoked when the first card is clicked and when resume button is clicked. This holds the values of `min` and `sec`.
- mcount():This function is invoked in `compare()` function. This holds the count of moves.
- restart_Game():This function is invoked when restart button is clicked.
- pause_Game():This function is invoked when clicked on pause button.
- resume_Game():This function is invoked when clicked on resume button.
- shuffle(array):This function is invoked once the window is loaded or reloaded. This function performs the shuffling of cards.

--------------------------------------------------------------------------------

## Contributing

This zip folder consists of folders and files that consists of all the code and components that are required for building a memory game. This zip folder is for the one, who want to take a look at and know how to build a memory game using **basic java script**
