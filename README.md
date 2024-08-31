# Rock-Paper-Scissors-Game
This project is a simple Rock, Paper, Scissors game built using HTML, CSS, and JavaScript. It serves as a review of fundamental web development concepts, including conditionals, functions, DOM manipulation, and event handling. By building this game, you'll strengthen your understanding of these basics while having some fun.

## Overview
This project is a simple Rock, Paper, Scissors game built using HTML, CSS, and JavaScript. It serves as a review of fundamental web development concepts, including conditionals, functions, DOM manipulation, and event handling. By building this game, you'll strengthen your understanding of these basics while having some fun.

## Features
- Interactive Gameplay:
- Users can choose between Rock, Paper, or Scissors to play against the computer.
- Score Tracking: The game keeps track of the player's and computer's scores.
- Dynamic Results Display: The results of each round are displayed, and the game announces the winner once a score of 3 is reached.
- Reset Functionality: Players can reset the game to play again.

## How to Play
1. Choose an Option: Click on one of the buttons labeled "Rock," "Paper," or "Scissors."

2. View Results: The game will compare your choice against the computer's randomly selected option and display the result.

3. Win the Game: The first to reach 3 points wins. The game will announce the winner and provide an option to reset and play again.





## JavaScript Code

**Random Computer Choice:**

The computer's choice is randomly generated using the getRandomComputerResult() function:

```javascript
function getRandomComputerResult() {
  const options = ["Rock", "Paper", "Scissors"];
  const randomIndex = Math.floor(Math.random() * options.length);
  return options[randomIndex];
}

```

**Determining the Winner:**

The game logic to determine if the player has won the round is encapsulated in the hasPlayerWonTheRound() function:

```javascript
function hasPlayerWonTheRound(player, computer) {
  return (
    (player === "Rock" && computer === "Scissors") ||
    (player === "Scissors" && computer === "Paper") ||
    (player === "Paper" && computer === "Rock")
  );
}

```

**Resetting the Game:**

To allow players to start over, the resetGame() function resets scores and the UI:

```javascript
function resetGame() {
  playerScore = 0;
  computerScore = 0;
  playerScoreSpanElement.innerText = "0";
  computerScoreSpanElement.innerText = "0";
  resetGameBtn.style.display = "none";
  optionsContainer.style.display = "block";
  roundResultsMsg.innerText = "";
  winnerMsgElement.innerText = "";
};

resetGameBtn.addEventListener("click", resetGame);

```

**Event Listeners:**

Buttons for Rock, Paper, and Scissors are linked to the showResults() function using event listeners:

```javascript
const rockBtn = document.getElementById("rock-btn");
const paperBtn = document.getElementById("paper-btn");
const scissorsBtn = document.getElementById("scissors-btn");

rockBtn.addEventListener("click", function () {
  showResults("Rock");
});

paperBtn.addEventListener("click", function () {
  showResults("Paper");
});

scissorsBtn.addEventListener("click", function () {
  showResults("Scissors");
});

```


## Future Improvements

 - Add a scoreboard that persists across multiple sessions.
 - Implement additional game modes (e.g., "Best of 5").
 - Enhance the UI with animations and sound effects.


## How to Run the Project


- Clone the repository.

- Open index.html in your browser.

- Start playing!

    
