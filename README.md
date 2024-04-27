![image](https://github.com/maplesoup1/chess-game/assets/91361133/3c959cc2-06c5-4b89-b5e9-2b98d3163b64)# chess-game
The project is mainly divided into four parts to implement. The first part is the model package, the second part is the App class, the third part is the Consts class, and the last part is testing. The functionality of each part of the project is different.

The Consts class contains all constants that may be used during the project process. In this way, we can easily maintain the constants in the program. If a constant needs to be modified, it can be directly modified in the Consts class for easy program maintenance.

The Model package contains game models, such as abstracting the chessboard into the ChessBoard class and the chess pieces into the Chess class. This makes it more convenient for us to write game logic because the data structure and specific algorithms are separate. Due to the varying range of positions that different chess pieces can move during program execution, we cannot use just one function to determine the range of positions that the current chess piece can move. Therefore, I have written a function getAccessiblePositions, which returns the range of all positions that the current chess piece can reach based on its type and the current chess board situation, In this way, we can achieve subsequent chess and AI functions.

In the App class, we have written logic for reading configuration and for player interaction. In addition, we have directly embedded the AI part into the App class, making it easy to call. However, improvements can also be made here by categorizing the game logic and interface, which can reduce the coupling of the program. Finally, we also implemented user interaction logic in the app, allowing users to play chess by clicking on the interface. For the implementation of AI, we used some rules in the document to implement them, which are:

Rule 1: If possible, attack the opponent's king.

Rule 2: If possible, attack the square adjacent to the opponent's king, if it has not yet been attacked.

Rule 3: Determine all blocks that can be attacked and choose the one with the highest value.

Rule 4: If everything else fails, choose to move randomly.

Through these simple rules, we have implemented an AI with basic functionality.

In the testing section, as the game's UI cannot be tested, we added the isTest field to Consts, so that when we conduct testing, we can disable UI painting because if this is not the case, errors will be reported during the testing process. Next, we tested different parts of the game and basically achieved satisfactory results.

I think there are many areas for improvement in this project, such as further increasing the rules of AI to achieve stronger AI, and the difficulty of the game can also be adjusted according to the changes in AI rules. In addition, the UI and logic of the program can also be separated, which will be more conducive to subsequent maintenance.
