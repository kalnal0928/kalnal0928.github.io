<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>테트리스 게임</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f0f0f0;
        }
        #gameBoard {
            border: 2px solid #333;
        }
    </style>
</head>
<body>
    <canvas id="gameBoard" width="240" height="400"></canvas>
    <script>
        const canvas = document.getElementById('gameBoard');
        const ctx = canvas.getContext('2d');
        const ROWS = 20;
        const COLS = 12;
        const BLOCK_SIZE = 20;
        let board = Array(ROWS).fill().map(() => Array(COLS).fill(0));
        let currentPiece;
        let score = 0;

        const SHAPES = [
            [[1, 1, 1, 1]],
            [[1, 1], [1, 1]],
            [[1, 1, 1], [0, 1, 0]],
            [[1, 1, 1], [1, 0, 0]],
            [[1, 1, 1], [0, 0, 1]],
            [[1, 1, 0], [0, 1, 1]],
            [[0, 1, 1], [1, 1, 0]]
        ];

        function createPiece() {
            const shape = SHAPES[Math.floor(Math.random() * SHAPES.length)];
            return {
                shape,
                x: Math.floor(COLS / 2) - Math.floor(shape[0].length / 2),
                y: 0
            };
        }

        function drawBoard() {
            ctx.fillStyle = '#fff';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            for (let y = 0; y < ROWS; y++) {
                for (let x = 0; x < COLS; x++) {
                    if (board[y][x]) {
                        ctx.fillStyle = '#000';
                        ctx.fillRect(x * BLOCK_SIZE, y * BLOCK_SIZE, BLOCK_SIZE - 1, BLOCK_SIZE - 1);
                    }
                }
            }
        }

        function drawPiece() {
            ctx.fillStyle = '#f00';
            currentPiece.shape.forEach((row, y) => {
                row.forEach((value, x) => {
                    if (value) {
                        ctx.fillRect((currentPiece.x + x) * BLOCK_SIZE, (currentPiece.y + y) * BLOCK_SIZE, BLOCK_SIZE - 1, BLOCK_SIZE - 1);
                    }
                });
            });
        }

        function collision() {
            return currentPiece.shape.some((row, y) => {
                return row.some((value, x) => {
                    if (value && (board[y + currentPiece.y] && board[y + currentPiece.y][x + currentPiece.x]) !== 0) {
                        return true;
                    }
                    return false;
                });
            });
        }

        function merge() {
            currentPiece.shape.forEach((row, y) => {
                row.forEach((value, x) => {
                    if (value) {
                        board[y + currentPiece.y][x + currentPiece.x] = value;
                    }
                });
            });
        }

        function rotate() {
            const rotated = currentPiece.shape[0].map((_, i) =>
                currentPiece.shape.map(row => row[i]).reverse()
            );
            const prevShape = currentPiece.shape;
            currentPiece.shape = rotated;
            if (collision()) {
                currentPiece.shape = prevShape;
            }
        }

        function clearLines() {
            let linesCleared = 0;
            for (let y = ROWS - 1; y >= 0; y--) {
                if (board[y].every(value => value !== 0)) {
                    board.splice(y, 1);
                    board.unshift(Array(COLS).fill(0));
                    linesCleared++;
                }
            }
            score += linesCleared * 100;
        }

        function gameLoop() {
            currentPiece.y++;
            if (collision()) {
                currentPiece.y--;
                merge();
                clearLines();
                currentPiece = createPiece();
                if (collision()) {
                    alert('Game Over! Score: ' + score);
                    board = Array(ROWS).fill().map(() => Array(COLS).fill(0));
                    score = 0;
                }
            }
            drawBoard();
            drawPiece();
            requestAnimationFrame(gameLoop);
        }

        document.addEventListener('keydown', event => {
            switch (event.keyCode) {
                case 37: // left
                    currentPiece.x--;
                    if (collision()) currentPiece.x++;
                    break;
                case 39: // right
                    currentPiece.x++;
                    if (collision()) currentPiece.x--;
                    break;
                case 40: // down
                    currentPiece.y++;
                    if (collision()) currentPiece.y--;
                    break;
                case 38: // up (rotate)
                    rotate();
                    break;
            }
        });

        currentPiece = createPiece();
        gameLoop();
    </script>
</body>
</html>
