# Electronic Voting Machine using AT89C51

## Overview
Brief description of what the project does.

## Features
- Voter ID authentication
- Duplicate vote prevention
- Two-candidate voting
- Admin mode for result display

## Hardware Used
- AT89C51
- ULN2003
- 5V Stepper Motor
- 4×4 Keypad
- LEDs
- Push Buttons
- Crystal Oscillator

## Software Used
- Keil μVision
- 8051 Assembly Language

## Working
1. On power-up, the AT89C51 initializes the ports, clears all vote counters, and resets the voter status memory.

2. The voter enters a 6-character Voter ID using the 4×4 keypad.

3. The entered ID is compared with the stored voter database. If the ID is invalid or has already been used, the Red LED blinks and the system returns to the ID entry stage.

4. If the ID is valid and has not voted before, the Green LED turns ON, indicating that the voter is authorized to vote.

5. The voter casts a vote by pressing one of the two push buttons corresponding to Candidate A or Candidate B. The selected candidate's vote count is incremented, the voter is marked as having voted, and the Green LED turns OFF.

6. The system returns to the main loop and waits for the next voter.

7. When the predefined Administrator ID is entered, the system enters result mode. The stepper motor rotates according to the recorded vote count to indicate the election result.
