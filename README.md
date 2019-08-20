# Word Game
As a part of the hiring assessment, you'll implement a word game. This game is a lot like Scrabble or Words With Friends, if you've played those. Letters are dealt to players, who then construct one or more words out of their letters. Each **valid** word receives a score, based on the length of the word and the letters in that word.

The rules of the game are as follows:

**Dealing**
- A player is dealt a hand of *n* letters chosen at random (assume *n = 7* for now).
- The player arranges the hand into as many words as they want out of the letters, using each letter at most once.
- Some letters may remain unused (these won't be scored).

**Scoring**
- The score for the hand is the sum of the scores for each valid word formed.
- The score for a word is the sum of the points for letters in the word, multiplied by the length of the word, plus 50 points if all *n* letters are used on the first word created. We have provided a text file *words.txt* which lists all valid words.
- Letters are scored as in Scrabble: A is worth 1, B is worth 3, C is worth 3, D is worth 2, E is worth 1, and so on. We have provided a JSON file *letter-values.json* which maps each lowercase letter to its Scrabble letter value.
- For example, "queen" would be worth 70 points ((10 + 1 + 1 + 1 + 1) for the five letters, then multiply by the number of letters to get (10 + 1 + 1 + 1 + 1) x 5 = 70). Be sure to check that the hand actually has 1 "q", 1 "u", 2 "e", and 1 "n" before scoring the word!
- As another example, if *n = 7* and you make the word "waybill" on the first try, it would be worth 155 points (the base score for "waybill" is (4 + 1 + 4 + 3 + 1 + 1 + 1) * 7 = 105, plus an additional 50 point bonus for using all *n* letters).

## User Stories
The user stories are categorized into 3 different groups: Must Have, Should Have, and Could Have:

Must Have: Missing such requirements will result in a non-viable solution and, as a result, failing the assessment.

Should Have: Missing such requirements can be painful, but the solution is still viable. While it does not necessarily lead to failing the assessment, it is still devastating.

Could Have: Such requirements are desirable but less important. This is a show-off zone where you can impress us.

Nevertheless, the order of the user stories in each group does not reflect the degree of importance.

**Must Have**
- As a player, I need to be able to know the hand when a new game starts.
- As a player, I need to be able to end the game.
- As a player, I need to be able to know the total number of points I have earned when the game ends.

**Should Have**
- As a player, I need to be able to see my hand throughout the game.
- As a player, I need to be able to see how many points I earn when I submit a word.
- As a player, I need to be able to see how many points I have earned throughout the game.
- As a player, I need to be able to replay a game with the same initial hand as a new game if I desire.
- As a player, I need to be informed when I run out of letters in my hand.
- As a player, at the end of a game, I need to be able to know what the optimal outcome of the game* is.

*: The optimal outcome of a game is a way to arrange and play the letters in a hand which results in the highest possible points of the game in total. For example, given a new game with an initial hand of "a r e t i i n", a player plays "tin" and "air" sequentially, earning 18 points in total at the end, but the optimal solution is playing "inertia", which the player could instead earn 99 points in total, and there is no other ways to get higher points in total.

**Could Have**
- As a player, I would like to be able to see my history of all played games.
- As a system administrator, I would like to be able to modify the value of each letter before a new game starts.
- As a system administrator, I would like to be able to modify the list of valid words.
- As a system administrator, I would like to be able to see a history of all played games.
- As a system administrator, I would like to be able to see a particular player's history of all played games.
- As a system administrator, I would like the players to have an enjoyable experience when interacting with the system.

## Engineering Requirements
While it might be slightly advantageous if your solution involves technologies/frameworks/programming languages in our tech stack,you are allowed to use any technology/framework/programming language you prefer or are most familiar with. Regardless of which you eventually use, we expect the code to be in high quality.
