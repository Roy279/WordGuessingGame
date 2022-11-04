# WordScrambleGame
  
## A simple word guessing game where the user has to guess the word by the given hint in the game.

In this Git Repository you will find 4 files.

1. index.html:
  -This file includes the html code for the game. and it links to "style.css", "script.js" & "words.js"
2. style.css:
  -Includes the formating for the game.
3. words.js:
  -Includes the words that will be in our game
4. script.js:
  -Includes the functionality of the game.
  
Further Comments are put inside the code to explain what each part does.

```html
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Guess a Word Game JavaScript</title>
    <link rel="stylesheet" href="style.css">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
  </head>
  <body>
    <div class="wrapper">
      <h1>Guess the Word</h1>
      <div class="content">
        <input type="text" class="typing-input" maxlength="1">
        <div class="inputs"></div>
        <div class="details">
          <p class="hint">Hint: <span></span></p>
          <p class="guess-left">Remaining guesses: <span></span></p>
          <p class="wrong-letter">Wrong letters: <span></span></p>
        </div>
        <button class="reset-btn">Reset Game</button>
      </div>
    </div>

    <script src="js/words.js"></script>
    <script src="js/script.js"></script>

  </body>
</html>
```
This is what is in the index.html file.This mainly builds up the basis & components of our game.We have the title of the Game in an h1.Then a div with the class content is made to house our content for the game. In content we have:

-A Div tag with class "inputs".This will show the text of our guessing to find the answer with the given hint.
-A Div tag with class "details". This will house the hint,guess left and wrong letters for the user to see.  
  -The div tag has 3 p tags,one with the class "hint",second,with class "time" and third,with the class "wrong-letter".All of them will display the hint,guess left and wrong letters for the user respectively.   
	-Input tag for the input field for the users answer  
	-Another div tag with a button tag with class "reset-btn", will reset the current question to another for the user has to guess.  
