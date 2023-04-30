Download Link: https://assignmentchef.com/product/solved-cs2400-homework-5-card-game
<br>
<strong>Objectives: </strong>

Use arrays, random number generators, command line arguments.

This card game requires a certain number of cards, n, where n is a triangular number. A triangular number is a number that represent the sum of a sequence: 1, 2, 3, 4, etc. For example, 21 = 1 + 2 + 3 + 4 + 5 + 6.  The first few triangular numbers are 1, 3,

6, 15, 21, 28, 36, 45, etc.




<strong>The Game: </strong>

You will start the game with an n value (default 45) for the number of cards.  Divide the cards into a random number of piles.




<strong>Playing the game (Assuming n = 45): </strong>

<strong> </strong>

Each round, take one card from each pile and create a new pile. Repeat the process until you have 9 piles of sizes 1, 2, 3, 4, 5, 6, 7, 8, and 9.

For example, if you start with 4 piles of 20, 15, 6, and 4, they would be transformed into

19, 14, 5, 3, and 4, etc.

<strong>Simulator: </strong>

Write a C++ program that simulates the game. Your program must obtain the number of cards (n) from the command line (see below). Assume the number of cards will never exceed 500. If the number is not provided, then use 45 as the default value of n.  If the user, enters more than one value, print an error message and quit the program (return 0).

Start by producing a random number of piles. Make sure the total is n.  Apply the steps outlined above repeatedly until the final configuration is reached. At each step, print the number of cards in each of the piles. The final configuration is reached when the number of cards in the piles are in sequence: 1, 2, 3, 4, 5, 6, 7, etc. Display the number of steps it took to reach the final configuration.<strong>           </strong>

<strong>Hints: </strong>

<ul>

 <li>Store the number of cards in each pile into an array of integers.</li>

 <li>Write a function (isTriangular) that returns true if a number n is a triangular number, false</li>

 <li>To generate a random number use the function rand()in &lt;cstdlib&gt; o First seed the random number generator with the current time. Do this only once in the program (beginning of main)</li>

 <li>srand(time(NULL));</li>

</ul>

o To generate a random integer between 0 and 2147483647

<ul>

 <li>randomInteger = rand();</li>

 <li>Write a function to print all the elements of the array</li>

 <li>Write a function that checks if the game is done by confirming the last sequence. You may want to sort the values to make it easier to check.</li>

 <li>To convert a string to an integer, use atoi() function. For example,</li>

</ul>

number = atoi(st);




<strong>Parsing command line arguments </strong>

<strong> </strong>

In C++ you can input data (strings) into your program on the command line (command line arguments).  You can capture these data by adding two parameters to your main program as follows:

int main (int argc, char *argv[])

argc:  (argument count) number of arguments on the line, including the name of the program

argv:  (argument vector) list of c-style strings that represent all the arguments including the name of the program (two dimensional array of characters).




For example, executing the command:

./a.out 45

Assigns:

argc = 2

argv[0] will be “./a.out” argv[1] will be “45” <strong>Sample output (n = 45): </strong>

./a.out 5

Error: the number 5 is not a triangular number

<strong> </strong>

./a.out  5   7

Error: too many parameters.

<strong> </strong>

./a.out 10 number of cards: 10 8       2

7       2       1

6       3       1

5       3       2

4       3       2       1

Number of rounds: 5

<strong> </strong>

./a.out

34      7       3       1

33      6       4       2

32      5       4       3       1

31      5       4       3       2

…

…

11      8       7       6       5       4       3       1

10      8       7       6       5       4       3       2

9       8       7       6       5       4       3       2       1

—————————————————————-

Number of rounds: 28