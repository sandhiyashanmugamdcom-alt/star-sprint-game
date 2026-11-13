# Star Sprint — Game Design Document

## 1. Game overview
**Title:** Star Sprint  
**Genre:** Short arcade / reaction game  
**Core mechanic:** Click appearing stars before they disappear.  
**Platform:** Desktop and mobile browser  
**Audience:** Beginners and casual players  
**Session length:** About 30 seconds

## 2. Goal
Collect at least 15 stars in 30 seconds. Each star gives one point.

## 3. Rules
1. Press **Start game** to begin a 30-second round.
2. Stars appear at random positions in the play area.
3. Click or tap a star to earn 1 point.
4. Each star disappears after about 1.5 seconds.
5. Reaching 15 points wins immediately.
6. If the timer reaches zero before 15 points, the player loses.
7. Press **Reset** to return to the initial state.

## 4. Controls
- Mouse click or touchscreen tap: collect a star.
- Start game: begin/restart a round.
- Reset: clear the score and timer.

## 5. Feedback states
- **Ready:** instructions are shown before the game starts.
- **Playing:** score and timer update; a short message confirms collected stars.
- **Win:** a success message and final score appear at 15 points.
- **Time up:** a retry message and final score appear when time runs out.
- **Reset:** score returns to 0 and time returns to 30 seconds.

## 6. Main screen sketch
```text
+--------------------------------------------------+
| Star Sprint                                      |
| Click stars before time runs out                 |
| Score: 0       Time: 30       Target: 15 points  |
|                                                  |
|       [★]              [★]                       |
|                    [★]                           |
|  [★]                         [★]                 |
|                                                  |
| Ready / score feedback                           |
| [Start game] [Reset]                             |
+--------------------------------------------------+
```

## 7. Core gameplay loop
Start round → show stars → player clicks stars → increase score → update feedback → check win condition → continue until 15 points or timer ends → show result → restart.

## 8. Success criteria / test plan
- Start begins at score 0 and time 30.
- Clicking a star increases the score by exactly 1.
- A star disappears after being clicked.
- Stars disappear automatically after a short time.
- Score 15 triggers the win message.
- Timer reaching 0 ends the round if the target was not reached.
- Reset clears stars and restores the initial screen.
- The layout works with a mouse and a touchscreen.

## 9. Placeholder art and sound
The prototype uses a simple star symbol and clean coloured play area as placeholder art. No external assets or audio are required.

## 10. Future improvements
Add sound effects, difficulty levels, a high-score table, keyboard accessibility, and a pause button after the core prototype passes testing.

## 11. Repository
Keep `index.html` and this `README.md` in the same public GitHub repository. Publish `index.html` with GitHub Pages and submit the repository or live game URL as the single proof link.
