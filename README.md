Download Link: https://assignmentchef.com/product/solved-coen171-homework-2-object-oriented-programming
<br>
In this assignment, you will use C++ and Smalltalk, two object-oriented languages discussed in class. Use the Linux machines in the Engineering Computing Center for this assignment. The Smalltalk interpreter is gst (you will need to execute “setup smalltalk” first) and the C++ compiler is g++.

<h1>1        BinarySearchTrees</h1>

Under/scratch/coen171/homework2,youwillfindanimplementationinSmalltalkofabinarysearchtree. Translate this program to C++ using templates, keeping the same class and operation names. A small test program is also provided, which will become the function main in C++.

<strong>Goal:               </strong>To learn about classes as a mechanism for information hiding.

<h1>2        The8-QueensProblem</h1>

In chess, a queen can move any number of squares horizontally, vertically, or diagonally. The <strong><em>8-queens problem </em></strong>is the problem of trying to place eight queens on an empty chessboard in such a way that no queen can attack any other queen. This problem is intriguing because there is no efficient algorithm known for solving the general problem. Rather, the straightforward algorithm of trying all possible placements is most often used in practice, with the only optimization being that each queen must be placed in a separate row and column:

<ol>

 <li>Starting with the first row, try to place a queen in the current column.</li>

 <li>If you can safely place a queen in that column, move on to the next column.</li>

 <li>If you are unable to safely place a queen in that column, go back to the previous column, and move thatqueen down to the next row where it can safely be placed. Move on to the next column.</li>

</ol>

In the course folder, you will find my solution to the 8-Queens Problem in the file Queens.cpp. My solution provides the following generalizations:

<ol>

 <li>Solves the <em>n</em>-Queens Problem rather than the 8-Queens Problem. The chessboard is of size <em>n×n </em>rather than of size 8<em>×</em>8, and <em>n </em>queens are to be placed on the board.</li>

 <li>Computes and displays the <strong><em>total </em></strong>number of solutions possible. Rather than finding one solution and exiting, my program will find all possible solutions and write the total number of possible solutions to standard output.</li>

 <li>Solves the <em>n</em>–<strong><em>Pieces </em></strong>Problem rather than the <em>n</em>-Queens Problem. Given any kind of chess piece, not just a queen, my program displays the total number of solutions possible for placing <em>n </em>of those pieces on the board such that no piece can attack any other piece.</li>

</ol>

You will need to write a file called Queens.h that contains the class and function definitions for each chess piece. Write a base chess piece class with which my algorithm works. The base class should provide at least the following methods:

1

<ul>

 <li>int row(): returns the row number of this piece</li>

 <li>int column(): returns the column number of this piece</li>

 <li>void place(int row, int col): placesthispieceontheboardgivenarownumberandacolumnnumber</li>

 <li>bool menaces(const Piece *p): given another piece, returns true if this piece can attack the given piece, and false otherwise</li>

</ul>

Now write classes for each of the following chess pieces:

<ul>

 <li>rooks: A rook can move any number of squares horizontally or vertically, but cannot move diagonally.</li>

 <li>bishop: A bishop can move any number of squares diagonally, but cannot move horizontally or vertically.</li>

 <li>knight: A knight can move two spaces in either a horizontal or vertical direction and an additional space inthe other direction.</li>

 <li>queens: A queen can move any number of squares horizontally, vertically, or diagonally. Thus, it can moveas either a rook or a bishop.</li>

 <li>amazon: An amazon can move either as a queen or as a knight.</li>

</ul>

Use virtual multiple inheritance in your solution. Prove that your solution is correct my filling in the missing values in the table at the top of Queens.cpp.

<strong>Goal:              </strong>To generalize a problem using object-oriented techniques.

<strong>Hints:            </strong>Write and test each piece in the order listed.