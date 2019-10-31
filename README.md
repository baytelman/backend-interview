# Noken • Backend Interview • Letters game

_Version 1.0.1_

## This is a coding challenge for applicants interested in joining Noken as Backend Engineers.

We ask you to _read this file carefully_ **before** you begin writing a solution.

There is a Q&A and an example section at the end of the file, which may help you to complete this challenge faster.

If you decide to continue with this process, **write us back WHEN** you expect to submit your solution before you begin implementing it.
This is really important so we can better arrange to wait for you, specially if you want to take a little bit longer.

If you decide NOT to continue with this process, let us know! ... So we stop spamming you with reminders.

We sincerely thank you for your interest and your time.

Best,
The Noken team!

## Submit the minimum possible

- You should **not implement features not required explicitly**.
- Coding more than required will waste your time, and waste our time. Please, don't.

## Challenge: Create an API server/application

- Write a server application that offers at least 3 endpoints:
  - Define the game's known dictionary (see below).
  - Start a new game by providing a board.
  - Validate a play.
- You can use any boilerplate or start project. If you need help with this, let us know and we will share a quick-starter project promptly.
- Keep your code **separated from the boilerplate**, so it's easier to review your work.
- We prefer TypeScript or typed JavaScript, or GoLang.

### Rules of the game

- Each game has a board of 16 tiles (4x4):
  - Tiles have a single letter to each of them.
- Players for a game can make a play by selecting a series of tiles to form words.
- Plays are valid if the tiles satisfy all these conditions:
  - Consecutive tiles are neighbors (including diagonals).
  - Tiles can only be used once in each play, but they can be used again in future plays.
  - The formed word is at least 3 letters.
  - The formed word is present in the app's dictionary.

### API design

Design an API to play, including endpoints to allow:

- Defining the app's dictionary.
- Starting a new game with a specific board distribution.
- Validating a play on one of the games previously started.

### Implementing your code

- Your app should satify the rules of the game and follow your API design.
- Your API routes should be documented (including parameters), implicitly (in code) or explicitly. 
- You can use any type of persistence (app memory, in-memory database, database engine, etc).

### Testing

- Describe your testing strategy.
- Implement a **single** test as an example of your testing strategy.
  - You can submit more tests if it is required to demonstrate different aspects of your strategy.

## Stretch goals

These are **not required**, but would make your submission stand out. You can implement none, one or all of these. If you do, let us know your decision so we evaluate them.

- Allow specific players to make plays.
- It will track which words were already played by past plays, and won't allow the same player to submit the same word twice (even if it can be formed by sequences of different tiles).
- Implement a new route to output the score: Valid plays score 1, 2, 4, 8, etc points for words with 3, 4, 5, 6, etc letters.

#### Example

In the following example, the app is initialized with the dictionary defined in [this json dictionary file](files/dictionary.json).

Then, a game is initialized with the board in the [test json file 1](files/test-board-1.json). If we would get to visualize the board, it would look like this:

```
    A  B  C  D
    E  F  G  H
    I  J  K  L
    M  N  O  P
```

Then, a user submits the word "fab" formed by these tiles:

```
    A  B  C  D         [A] B  C  D         [A][B] C  D
    E [F] G  H          E [F] G  H          E [F] G  H
    I  J  K  L          I  J  K  L          I  J  K  L
    M  N  O  P          M  N  O  P          M  N  O  P
```

The server should accept the word. If you implement the score system (stretch goal), the score for this play is **1 point**.

---

## Submitting your work

Your deliverable should satisfy all these requirements:

- Describe what features you've implemented, included optional stretch goals.

- It should include _instructions on how to run_ (installing dependencies, starting it, etc) and it shouldn't have any obscure environment requirements.

- It should include _instructions on how to test_.

- Describe your endpoints, and how to use them.

- It should be submitted using one of the following alternatives:
  1. bitbucket.org or github.com repo (_Note: Do NOT clone our repo because other candidates can find it_).
  1. Upload a compressed file somewhere and send us the URL.
  1. Email us your code.
  - _Note: Do NOT include `node_modules` or any other files that will be auto-generated_.

---

## Frequently asked question

- Q: Can I use external libraries (npm)?
  - Of course you can!
  - However, if some functionality is very easy to implement, try to implement it yourself (i.e. Don't install a library to figure out if a number is odd/even).
  - Choosing *when* to use libraries and *what libraries* you imported will speak about your judgement.
- Q: This coding challenge is too long. Is it OK if I implement it partially?
  - Although we recognize this exercise may take some time, it does measure if you have the skills we need to work at Noken.
  - Submitting an incomplete solution is acceptable, especially if you explain the reasons.
  - However, a complete solution will increase the likelihood of being selected to continue our process, and it will save time during our in-person interview.

---

## Playing the Letters Game with our secondary file

The [secondary board file](files/test-board-2.json) describes the following board:

```
L I S T
O F A T
S T R S
O R A Y
```

When playing with the "neighbors rule", this board contains (at least) the following English words defined in [our (limited) dictionary file](files/dictionary.json).

- ARTS
- FAST
- FIST
- LIST
- RATS
- SOFT
- SORT
- START

The following words cannot be formed in this board (because the tiles are not neighbors):
- SOS (The letter S on the left can only be used ONCE)
- TOLL (There's only ONE L)
- TOTAL (No L is neighbor of an A)

This board (obviously) does NOT include the following words from our [dictionary file](files/dictionary.json) (because there's neither D, E or U present in the board):

- LOAD
- LURE
- RENT
- STREET

## Thanks for your time!

The Noken team!
