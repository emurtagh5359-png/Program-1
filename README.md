# CS 210 Programing Assignment
## Monopoly Board Simulator (Spring 2026)

### Overview
This Project creates a board for Monopoly using a circular linked list.
The project also allows for a player to taverse around the board while tracking how many times the player passes go.The program will also show the board view from the player up to n spaces.

### Build and Run Instructions

In CLion, to build the program you just have to click the hammer icon at the top of the page. Then to run the program click the green play button to the right of the hammer icon.

Using the terminal in CLion to build you type "g++ -std=c++17 main.cpp -o monopoly" and then "./monopoly" to run the program 

### Description of Data Structures Used
The primary data structure used in this program is a circular singly linked list. The Monopoly board is represented as a chain of nodes where each node contains the information for a single Monopoly space. Each node stores a MonopolySpace object and pointer to the next node in the list. The list is circular because the tailNode is always pointing back to the headNode. This makes it so the player can traverse the board multiple times and pass "GO" which is the head node. There is also a playerNode pointer that is the players current position. The player moves by advancing the pointer node by node.

### List of Functions
#### MonopolySpace
This initializes an empty Monopoly space
#### MonopolySpace(string propertyName, string propertyColor, int value, int rent)
This is an overloaded version that initializes the space with a name, color, value, and rent
#### bool isEqual(MonopolySpace other)
This makes sure two spaces aren't the same
#### void print()
This prints the details of a Monopoly space
#### CircularLinkedList()
This initializes an empty circular linked list
#### bool addSpace(T value)
This adds a new node to the initialized list and makes sure it doesn't go over 40.
#### int AddMany(vector<T> values)
This allows for adding multiple spaces at once in order by repeating "addSpace. " This also stops once the size reaches 40.
#### void movePlayer(int steps)
This moves the pointer for the player forward node by node. 
#### getPassGoCount()
This returns the number of times the player pointer passed go
#### void printFromPlayer(int count)
This prints a certain number of board spaces in front of the player node.
#### void printBoardOnce()
This goes through the list once, printing all board spaces in the list.
#### void mirrorBoard()
This reverses the direction of the list and keeps the player on the same space they're on.
#### int countSpaces()
This traverses the list once and returns the total number of spaces in the list.
#### void clear()
This deletes all the nodes in the list and resets it to an empty list.
#### int rollDice2to12()
This "rolls" two dice and adds the numbers up to see how many spaces the player will move.

### Traversal and Movement Logic
As mentioned above, the Monopoly board is stored as a circular singly linked list. This means that the traversal of the player will go around the board, passing the head node (GO) as many times as needed. The players position is found using a pointer (playerNode). The player starts at the head node at the beginning of the program. When the player moves, playerNode gets advanced to the next node. Once it reached the last space, the next node it will go to is the head node. The program tracks how many times GO is passed by checking when the player moves from the tail node to the head node during traversal.
# THE MAX NUMBER OF SPACES THE BOARD CAN HAVE IS 40