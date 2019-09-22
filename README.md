# -2-version-Rock-Paper-Scissors
Full version  Rock Paper Scissors.js
const getUserChoice = userInput => {
userInput = userInput.toLowerCase();
if (userInput === 'rock' || userInput === 'paper' || userInput === 'scissors' || userInput === 'secret') {
  return userInput;
} else {
  console.log('Error!');
}
};
//console.log(getUserChoice('scissors'));

// for computer choice
function getComputerChoice() {
 randomNumber =  Math.floor(Math.random() * 3);
  switch (randomNumber) {
    case 0:
      return 'rock';
    case 1: 
      return 'paper';
    case 2:
      return 'scissors';
       }
         }
//console.log(getComputerChoice());

//for determine a winner - user/computer

function determineWinner(userChoice, computerChoice)  {
  if (userChoice === 'secret') {
  return 'You are Superwinner!';
  }
   else if (userChoice === computerChoice) {
  return 'The game was a tie!';
  }
 else if (userChoice === 'rock') {
  	if (computerChoice === 'paper') {
    return 'The computer won!';
  } else {
    return 'You won!';
  }
}
  else if (userChoice === 'paper') {
  	if (computerChoice === 'scissors') {
    return 'The computer won!';
  } else {
    return 'You won!';
  }
}
  else if (userChoice === 'scissors') {
  if (computerChoice === 'rock') {
    return 'The computer won!';
  } else {
    return 'You won!';
  }
}
};
//console.log(determineWinner('paper', 'scissors')); 
//console.log(determineWinner('paper', 'paper'));
//console.log(determineWinner('paper', 'rock')); 
//console.log(determineWinner('secret', 'scissors')); 
//console.log(determineWinner('secret', 'paper'));
//console.log(determineWinner('secret', 'rock')); 
//console.log(determineWinner('rock', 'rock')); 

//game result
const playGame = () => {
  const userChoice = getUserChoice();
  const computerChoice = getComputerChoice();
  console.log('You threw: ' + userChoice);
  console.log('The computer threw:' + computerChoice);
  console.log(determineWinner(userChoice, computerChoice));
};
playGame();
