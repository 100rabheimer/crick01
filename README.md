<!DOCTYPE html>
<html>
<head>
  <title>Cricket Game</title>
  <style>
    body {
      text-align: center;
      font-family: Arial, sans-serif;
    }

    button {
      padding: 10px 20px;
      margin: 10px;
      font-size: 16px;
    }
  </style>
</head>
<body>

<h1>Bat Ball Stump Game</h1>

<button onclick="playGame('Bat')">Bat</button>
<button onclick="playGame('Ball')">Ball</button>
<button onclick="playGame('Stump')">Stump</button>

<script>
  function playGame(userChoice) {
    const randomNumber = Math.random() * 3;
    let computerChoice;

    if (randomNumber <= 1) {
      computerChoice = 'Bat';
    } else if (randomNumber <= 2) {
      computerChoice = 'Ball';
    } else {
      computerChoice = 'Stump';
    }

    let resultMsg;

    if (userChoice === 'Bat') {
      if (computerChoice === 'Ball') {
        resultMsg = 'User won.';
      } else if (computerChoice === 'Bat') {
        resultMsg = 'It is a tie.';
      } else {
        resultMsg = 'Computer has won.';
      }
    } else if (userChoice === 'Ball') {
      if (computerChoice === 'Ball') {
        resultMsg = 'It is a tie.';
      } else if (computerChoice === 'Bat') {
        resultMsg = 'Computer has won.';
      } else {
        resultMsg = 'User won.';
      }
    } else if (userChoice === 'Stump') {
      if (computerChoice === 'Ball') {
        resultMsg = 'Computer has won.';
      } else if (computerChoice === 'Bat') {
        resultMsg = 'User won.';
      } else {
        resultMsg = 'It is a tie.';
      }
    }

    alert(`You chose ${userChoice}. Computer chose ${computerChoice}. ${resultMsg}`);
  }
</script>

</body>
</html>
