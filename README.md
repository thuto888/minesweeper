# minesweeper
A bot which plays minesweeper  
Minesweeper.exe must be in the source folder  
Note: this was built for speed, not win rate

import random
from collections import defaultdict

class MinesweeperBot:
    def __init__(self, board):
        self.board = board  # 2D list, -1: mine, 0-n: revealed, None: unknown
        self.height = len(board)
        self.width = len(board[0])
        self.known_safe = set()
        self.known_mines = set()
        self.moves_made = set()

    def get_neighbors(self, x, y):
