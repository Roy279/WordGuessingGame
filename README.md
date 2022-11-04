# WordGuessingGame
  
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
```
-A Div tag with class "inputs".This will show the text of our guessing to find the answer with the given hint.
-A Div tag with class "details". This will house the hint,guess left and wrong letters for the user to see.  
-The div tag has 3 p tags,one with the class "hint",second,with class "time" and third,with the class "wrong-letter".All of them will display the hint,guess left and wrong letters for the user respectively.   
-Input tag for the input field for the users answer  
-Another div tag with a button tag with class "reset-btn", will reset the current question to another for the user has to guess.  
```
There are 3 things linked inside the html file. we have:
```
1. A link for the CSS File style.css  
2. A script link for words.js file  
3. A script link for the script.js file   
```
## We will start with style.css:

The CSS File contains basically all the code we need to format how the game will look.Each element we gave it certain properties to make it the way it looks.

## words.js file:
```js 
let wordList = [
    {
        word: "python",
        hint: "programming language"
    },
    {
        word: "guitar",
        hint: "a musical instrument"
    },
    {
        word: "aim",
        hint: "a purpose or intention"
    },
    {
        word: "venus",
        hint: "planet of our solar system"
    },
    {
        word: "gold",
        hint: "a yellow precious metal"
    },
    {
        word: "ebay",
        hint: "online shopping site"
    },
    {
        word: "golang",
        hint: "programming language"
    },
    {
        word: "coding",
        hint: "related to programming"
    },
    {
        word: "matrix",
        hint: "science fiction movie"
    },
    {
        word: "bugs",
        hint: "related to programming"
    },
    {
        word: "avatar",
        hint: "epic science fiction film"
    },
    {
        word: "gif",
        hint: "a file format for image"
    },
    {
        word: "mental",
        hint: "related to the mind"
    },
    {
        word: "map",
        hint: "diagram represent of an area"
    },
    {
        word: "island",
        hint: "land surrounded by water"
    },
    {
        word: "hockey",
        hint: "a famous outdoor game"
    },
    {
        word: "chess",
        hint: "related to a indoor game"
    },
    {
        word: "viber",
        hint: "a social media app"
    },
    {
        word: "github",
        hint: "code hosting platform"
    },
    {
        word: "png",
        hint: "a image file format"
    },
    {
        word: "silver",
        hint: "precious greyish-white metal"
    },
    {
        word: "mobile",
        hint: "an electronic device"
    },
    {
        word: "gpu",
        hint: "computer component"
    },
    {
        word: "java",
        hint: "programming language"
    },
    {
        word: "google",
        hint: "famous search engine"
    },
    {
        word: "venice",
        hint: "famous city of waters"
    },
    {
        word: "excel",
        hint: "microsoft product for windows"
    },
    {
        word: "mysql",
        hint: "a relational database system"
    },
    {
        word: "nepal",
        hint: "developing country name"
    },
    {
        word: "flute",
        hint: "a musical instrument"
    },
    {
        word: "crypto",
        hint: "related to cryptocurrency"
    },
    {
        word: "tesla",
        hint: "unit of magnetic flux density"
    },
    {
        word: "mars",
        hint: "planet of our solar system"
    },
    {
        word: "proxy",
        hint: "related to server application"
    },
    {
        word: "email",
        hint: "related to exchanging message"
    },
    {
        word: "html",
        hint: "markup language for the web"
    },
    {
        word: "air",
        hint: "related to a gas"
    },
    {
        word: "idea",
        hint: "a thought or suggestion"
    },
    {
        word: "server",
        hint: "related to computer or system"
    },
    {
        word: "svg",
        hint: "a vector image format"
    },
    {
        word: "jpeg",
        hint: "a image file format"
    },
    {
        word: "search",
        hint: "act to find something"
    },
    {
        word: "key",
        hint: "small piece of metal"
    },
    {
        word: "egypt",
        hint: "a country name"
    },
    {
        word: "joker",
        hint: "psychological thriller film"
    },
    {
        word: "dubai",
        hint: "developed country name"
    },
    {
        word: "photo",
        hint: "representation of person or scene"
    },
    {
        word: "nile",
        hint: "largest river in the world"
    },
    {
        word: "rain",
        hint: "related to a water"
    },
]
```
This code basiaclly is the list of words & their hints.The said words are the words the user will try & guess.  

## Script.js file:

This file contains all the functionality of the game and it is very important.

in the file:
We have to declare the constant variables we need to make the game run.

```js
const inputs = document.querySelector(".inputs"),
hintTag = document.querySelector(".hint span"),
guessLeft = document.querySelector(".guess-left span"),
wrongLetter = document.querySelector(".wrong-letter span"),
resetBtn = document.querySelector(".reset-btn"),
typingInput = document.querySelector(".typing-input");

```
after declaring the previous variables that are constant we declare ones that arent

```js
let word, maxGuesses, incorrectLetters = [], correctLetters = [];
```
## The first function
## randomWord:
randomWord function written like this:
```js
function randomWord() {
    let ranItem = wordList[Math.floor(Math.random() * wordList.length)];
    word = ranItem.word;
    maxGuesses = word.length >= 5 ? 8 : 6;
    correctLetters = []; incorrectLetters = [];
    hintTag.innerText = ranItem.hint;
    guessLeft.innerText = maxGuesses;
    wrongLetter.innerText = incorrectLetters;

    let html = "";
    for (let i = 0; i < word.length; i++) {
        html += `<input type="text" disabled>`;
        inputs.innerHTML = html;
    }
}
```
-In the code above, ranItem is there to choose a random word inside the word.js for the user to answer. 
-maxGuesses is there to limit the max guessing availability to the user to answer the given word.
-hintTag.innertext is for show the hint text from the variable of ranItem.hint.
-guessLeft.innertext is for show the available guessing limit.
-wrongLetter.innertext is for show the wrong letters that have been guess by the user.
