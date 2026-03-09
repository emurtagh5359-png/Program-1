# Developer Log (DEVLOG.md)
## Monopoly Board Simulator (Spring 2026)

---
## Allowed Entry Types
Each entry may be one of the following:
1) **Bug Fix Entry**
- The issue encountered.
- Error messages or symptoms.
- Attempts made.
- Final resolution.
2) **Edge Case / Testing Entry**
- A failure discovered through testing.
- The specific input/state that caused it.
- The change you made to handle it correctly.
3) **Engineering Decision Entry (up to 2 allowed)**
- A design decision you made.
- An alternative approach you considered.
- Why you chose one approach over another (tradeoffs).
---
### Entry 1
**Date:** 2026-03-04
**Entry Type:** Bug Fix 
**Task worked on:** Defining overloaded constructor
**Issue or decision:** tried assigning variables to the parameters, but the parameters were greyed out when setting equal to each other
**Error message / symptom (if applicable):** greyed out parameters.
**What I tried:** Looked up why this might be happening, found out when dealing with naming parameters the same name as variables you should put "this->" infront of it.
**Fix / resolution (or final decision):** Added a "this ->" in fornt like "this->propertyName = propertyName;"
**Commit(s):** Commit #3 
---
### Entry 2
**Date:** 2026-03-06
**Entry Type:** Engineering Decision
**Task worked on:** Core C
**Issue or decision:** Made sure that if the steps inputted are 0 or less than zero movePlayer will return since the player can not move in that situation. 
**Error message / symptom (if applicable):** None
**What I tried:** added "steps <= 0"
**Fix / resolution (or final decision):** This makes it so the steps inputted can not be 0 or less than 0 which would normally cause an error.
**Commit(s):** Commit #6
---
### Entry 3
**Date:** 2026-03-05
**Entry Type:** Engineering Decision
**Task worked on:** Core A
**Issue or decision:** Couldn't figure out if the insertion code should be in an else statement after using return in the block above it.
**Error message / symptom (if applicable):** CLion greyed out the else statement I had put.
**What I tried:** I just compared the two different options with and without an else statement.
**Fix / resolution (or final decision):** Since the case above returns instantly the else statement is not needed and makes the code more cluttered, so I removed it.
**Commit(s):** Commit #4
---
### Entry 4
**Date:** 2026-03-07
**Entry Type:** Edge Case
**Task worked on:** Core D optional helper
**Issue or decision:** Stopping an infinite loop from happening or the code not running at all.
**Error message / symptom (if applicable):** Using "while(currentNode != headNode)" would do nothing since the condition would fail right away because it starts at headNode.
**What I tried:** I tried using a while loop and then a do-while loop
**Fix / resolution (or final decision):** I used a do-while loop because that automatically runs once no matter what cause the function to traverse the list one time fully and print the board once.
**Commit(s):** commit #7
---
### Entry 5
**Date:** 2026-03-06
**Entry Type:** Bug Fix 
**Task worked on:** Core C, passing go with movePlayer()
**Issue or decision:** Figuring out when to increment the pass go count
**Error message / symptom (if applicable):** Passing go was not being counted right.
**What I tried:**  At first I was checking if the player landed on GO after moving. But this wouldn't return the correct number.
**Fix / resolution (or final decision):** I changed the code to increment the count when the player node is on the tailNode about to advance. This fixed the problem.
**Commit(s):** Commit #6
---
### Entry 6
**Date:** 2026-03-08
**Entry Type:** Bug Fix
**Task worked on:** addMany at the end of the program.
**Issue or decision:** addMany() was not doing anything when I called it originally.
**Error message / symptom (if applicable):** Originally when adding the spaces I had accidentally used board.addSpace for all 40 spaces. This meant addMany() could not add any more spaces.
**What I tried:** I put all 40 spaces under board.addSpace leaving no room for addMany(). 
**Fix / resolution (or final decision):** I split the work up in half, 20 of the spaces were added using board.addSpace, and the other 20 were added using addMany(). This allowed me to use both ways of adding spaces to the board.
**Commit(s):** Commit #11
