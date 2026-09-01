# ColorSwitch Game (Java Swing)

## Overview

This Java program is an interactive color-matching game built using Java Swing. Players must quickly identify the correct color of a displayed word and select the corresponding button. The game includes both timed and relaxed modes, along with sound effects for feedback.

---

## How It Works

1. Displays instructions and prompts the user to choose a game mode:

   * Timed mode (10 seconds)
   * Relaxed mode (no time limit)

2. Shows a word and a color:

   * The word may not match its displayed color

3. Player selects the correct color using buttons

4. The game:

   * Increases score for correct answers
   * Tracks missed attempts
   * Plays sound effects for feedback

5. Buttons shuffle positions after each selection

6. In timed mode:

   * Game ends after 10 seconds
   * Displays final score and replay option

---

## Key Components

### GUI (Java Swing)

* Uses `JFrame`, `JPanel`, `JButton`, and `JLabel`
* Grid layout for button arrangement
* Dynamic updates using `revalidate()` and `repaint()`

### Game Logic

* Randomly selects:

  * A color word
  * A display color
* Player must match the **display color**, not the word

### Timer System

* Uses `javax.swing.Timer` for timed mode
* Ends game and shows results after time expires

### Sound Effects

* Plays audio clips for:

  * Correct answers
  * Incorrect answers
  * Game over
* Uses `AudioInputStream` and `Clip`

### Button Shuffling

* Randomizes button positions after each action
* Increases difficulty and reaction time

---

## Program Flow

Show instructions → Select mode
→ Display word/color → User selects button
→ Update score → Shuffle buttons → Repeat
→ End game (timed mode)

---

## Inputs

* User button clicks
* Game mode selection

---

## Outputs

* Score and missed count
* Visual feedback (word + color)
* Audio feedback (correct/incorrect/game over)
* Game over dialog (timed mode)

---

## Related File

* Main game file: mian.java

---

## Limitations

* Requires audio files to be in the same directory
* No persistent high score tracking
* Limited to four colors
* UI layout is fixed (not responsive)

---

## How to Run

1. Compile the program:

   ```bash
   javac ColorSwitch.java
   ```

2. Ensure the following files are in the same directory:

   * `mixkit-correct-answer-notification-947.wav`
   * `mixkit-tech-break-fail-2947.wav`
   * `mixkit-arcade-game-complete-or-approved-mission-205.wav`

3. Run the program:

   ```bash
   java ColorSwitch
   ```

4. Follow the on-screen instructions

