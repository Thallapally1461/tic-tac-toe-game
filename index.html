<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tic Tac Toe</title>
  <style>
    /* General reset and font settings */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Arial', sans-serif;
      background-color: #f4f4f9;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .game-container {
      text-align: center;
      background: #fff;
      border-radius: 12px;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
      padding: 20px;
      width: 400px;
    }

    h1 {
      font-size: 36px;
      margin-bottom: 20px;
      color: #333;
    }

    .game-board {
      display: grid;
      grid-template-columns: repeat(3, 100px);
      grid-template-rows: repeat(3, 100px);
      gap: 15px;
      justify-content: center;
      margin-bottom: 20px;
    }

    .game-board div {
      width: 100px;
      height: 100px;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 36px;
      background-color: #fff;
      border: 2px solid #ccc;
      cursor: pointer;
      border-radius: 8px;
      transition: background-color 0.2s;
    }

    .game-board div:hover {
      background-color: #f0f0f0;
    }

    .game-board div.X {
      color: #2c3e50;
    }

    .game-board div.O {
      color: #e74c3c;
    }

    #reset-button {
      margin-top: 20px;
      padding: 10px 20px;
      background-color: #3498db;
      color: white;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      font-size: 16px;
    }

    #reset-button:hover {
      background-color: #2980b9;
    }

    .winning-cell {
      background-color: #2ecc71;
      color: white;
      font-weight: bold;
    }

  </style>
</head>
<body>
  <div class="game-container">
    <h1>Tic Tac Toe</h1>
    <div id="game-board" class="game-board">
     
    </div>
    <button id="reset-button">Restart Game</button>
  </div>
d
  <script>
    const PLAYER_X = 'X';
    const PLAYER_O = 'O';

    let currentPlayer = PLAYER_X;
    let board = ['', '', '', '', '', '', '', '', ''];
    let gameActive = true;

    const gameBoard = document.getElementById('game-board');
    const resetButton = document.getElementById('reset-button');

   
    function initGameBoard() {
      gameBoard.innerHTML = '';
      for (let i = 0; i < 9; i++) {
        const cell = document.createElement('div');
        cell.setAttribute('data-index', i);
        cell.addEventListener('click', handleCellClick);
        gameBoard.appendChild(cell);
      }
    }

  
    function handleCellClick(event) {
      const index = event.target.getAttribute('data-index');
      if (board[index] !== '' || !gameActive) return;

     
      board[index] = currentPlayer;
      event.target.textContent = currentPlayer;
      event.target.classList.add(currentPlayer);

     
      if (checkWinner(currentPlayer)) {
        gameActive = false;
        highlightWinningCells(currentPlayer);
        alert(`${currentPlayer} wins!`);
        return;
      }

      
      if (!board.includes('')) {
        gameActive = false;
        alert("It's a draw!");
        return;
      }

 
      if (currentPlayer === PLAYER_X) {
        currentPlayer = PLAYER_O;
        setTimeout(systemMove, 500); 
      } else {
        currentPlayer = PLAYER_X;
      }
    }

 
    function systemMove() {
      let bestMove = minimax(board, PLAYER_O);
      const cell = gameBoard.children[bestMove.index];
      board[bestMove.index] = PLAYER_O;
      cell.textContent = PLAYER_O;
      cell.classList.add('O');

      
      if (checkWinner(PLAYER_O)) {
        gameActive = false;
        highlightWinningCells(PLAYER_O);
        alert(`${PLAYER_O} wins!`);
        return;
      }

      
      currentPlayer = PLAYER_X;
    }

    function minimax(board, player) {
      const availableCells = board.map((value, index) => value === '' ? index : -1).filter(index => index !== -1);

      if (checkWinner(PLAYER_X)) return { score: -10 };
      if (checkWinner(PLAYER_O)) return { score: 10 };
      if (availableCells.length === 0) return { score: 0 };

      const moves = [];

      availableCells.forEach(index => {
        const move = { index: index };
        board[index] = player;

        if (player === PLAYER_O) {
          const result = minimax(board, PLAYER_X);
          move.score = result.score;
        } else {
          const result = minimax(board, PLAYER_O);
          move.score = result.score;
        }

        board[index] = '';  
        moves.push(move);
      });

      
      if (player === PLAYER_O) {
        return moves.reduce((bestMove, move) => move.score > bestMove.score ? move : bestMove);
      } else {
        return moves.reduce((bestMove, move) => move.score < bestMove.score ? move : bestMove);
      }
    }

    function checkWinner(player) {
      const winningCombinations = [
        [0, 1, 2], 
        [3, 4, 5], 
        [6, 7, 8], 
        [0, 3, 6], 
        [1, 4, 7], 
        [2, 5, 8], 
        [0, 4, 8], 
        [2, 4, 6]  
      ];

      return winningCombinations.some(combination => {
        return combination.every(index => board[index] === player);
      });
    }

    function highlightWinningCells(player) {
      const winningCombinations = [
        [0, 1, 2],
        [3, 4, 5],
        [6, 7, 8],
        [0, 3, 6],
        [1, 4, 7],
        [2, 5, 8],
        [0, 4, 8],
        [2, 4, 6]
      ];

      for (let combination of winningCombinations) {
        if (combination.every(index => board[index] === player)) {
          combination.forEach(index => {
            gameBoard.children[index].classList.add('winning-cell');
          });
        }
      }
    }

    function resetGame() {
      board = ['', '', '', '', '', '', '', '', ''];
      currentPlayer = PLAYER_X;
      gameActive = true;
      initGameBoard();
    }

    resetButton.addEventListener('click', resetGame);
    initGameBoard();
  </script>
</body>
</html>
