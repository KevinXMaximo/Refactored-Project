What were the objectives of the project?
The objectives were to identify potential opportunities for refactoring and applying design patterns for the following project:
https://github.com/russs123/brawler_tut
 
What and how did you do, and why?
Fixing nested if statements:
Nested if statements muddy up code and make it a lot harder to read, so changing all of them to a single if statement (and using python’s syntax to bring the code closer to natural language) makes it a lot easier to understand that this if statement is only meant to run if the round is not over and player_1 is not alive. 
 
 
Readability: 
Moving variable declarations closer to where they are used and typing them in lower case in order to fit with the rest of the code’s standard can help readability.



Redundant Code:

This section of code is completely redundant, testing for the same thing twice with two if statements when only one should be necessary.







Python specific features:

Python allows for f-strings which are ideal for concatenation as they read better and are less error prone.



Simplify if statement:

Use ranges to fix long if statement.



Unnecessary Cast:














Large Function:

The function Move is 73 lines long and does many things, such as grabbing keypresses, checking both players controls, applying gravity ensuring the players are facing each other and updating their positions. This makes the function hard to read and overly complicated, something which can easily be fixed by applying these functionalities to other functions which get called inside Move( )

Before: 



After:



Cohesion and Coupling

The changes made have greatly increased the program’s cohesion, and slightly increased it’s coupling. But, the small coupling increasing is a negligible price to pay when compared to how readable and efficient the code now is.

Main Challenges

The main challenges involved making changes without affecting what the code actually does. Sometimes a change would allow the game to still run, but things like the win counter or character attacks would not be working correctly, and that required me to go back and analyze the changes made in order to certify that I was making the code more efficient without breaking irs functions.

The main trick was to implement changes in small intervals, testing every time to make sure everything worked correctly. If I made too many changes it would be hard to pinpoint which one was the change that broke everything.

Also, getting acquainted enough with the code and its functions in order to be able to make changes in the first place was a challenge, as I was not familiar with the pycharm library and had to learn that too before understanding the code. 

Resources 

A good resource for identifying refactoring techniques is the following: 

https://refactoring.guru/refactoring/techniques

Also, the code was made for a youtube video and it is good to check it in order to understand the original rationale of the writer and to see if the game is running properly:

https://www.youtube.com/watch?v=s5bd9KMSSW4
