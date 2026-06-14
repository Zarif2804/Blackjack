## 1. How to Compile and Run

### Compilation
The project uses a `Makefile`. To build both the server and client executables, run:

1. make
This will generate two executables: `server` and `client`.

To clean up build files:
2. make clean

### Running the Game

1. Start the Server:
Open a terminal and run:
./server

2. Start Clients (Players):
Open new terminals (one for each player) and run:
./client
*   You will be prompted to enter the **Server IP**. If running locally, enter: `127.0.0.1`
*   Enter your **Name** when prompted.
*   Wait for the "Welcome" message.

3. Start the Game:
Once at least 2 players have connected, the **Server Admin** (in the server terminal) must type:
y to begin the game session.

In-Game Actions (Client):
When it is your turn, you will see `>>> YOUR TURN <<<` and a menu.
Type the command exactly as shown:

*   `CHECK`       : Pass action to next player (if bet matches).
*   `CALL`        : Match the current highest bet.
*   `FOLD`        : Give up hand.
*   `BET:100`     : Bet 100 chips.
*   `RAISE:200`   : Raise the bet to 200 chips.

## 2. Game Rules Summary
*   Objective: Win chips by Best Hand or Bluf.
*   Session: A session consists of **5 Hands**.
*   Winner: Determining solely by **Chip Count** at the end of hand 5.
*   Bankruptcy: If you reach 0 chips, you are out of the hand but can spectate. Chips reset to 1000 after 5 hands.

Hand Phases
1.  Pre-Flop: 2 Hole Cards dealt. Betting.
2.  Flop: 3 Community Cards dealt. Betting.
3.  Turn: 4th Community Card. Betting.
4.  River: 5th Community Card. Betting.
5.  Showdown: Best 5-card hand wins.

## 3. Mode Supported
*   Support Mode: TCP/IP (Process-Based Hybrid Server)