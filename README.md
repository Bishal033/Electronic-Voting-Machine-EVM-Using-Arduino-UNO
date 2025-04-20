Electronic Voting Machine (EVM) Using Arduino UNO
This project simulates a basic electronic voting machine using an Arduino UNO board, push buttons, and a 16x2 LCD display. It allows voting for four political parties and displays the winning party or announces a tie/no result based on the votes cast.

📌 Project Overview
The Electronic Voting Machine (EVM) is a simplified prototype that accepts votes via buttons and displays the live count and final result on an LCD screen. It can be used as a foundational project to understand how voting machines work using microcontrollers like Arduino.

🛠️ Features
Four political parties: BJP, INC, AAP, and OTH

Displays real-time vote count on a 16x2 LCD

Button-press based voting

Result button to display the winner or tie

LED indicators for vote confirmation and result announcement

Automatically resets vote count after result declaration

Components Used:

Arduino UNO	1	Main microcontroller board
LCD Display (16x2)	1	To display votes and result
Breadboard	1	For component connection
Push Buttons	4 for voting (one per party), 1 for result
LEDs	2	Green for vote confirmation, Red for result
Resistors	5	For button pull-up or LED control (if needed)
Jumper Wires	As needed	For connections
Power Source	1	USB or external 5V power supply.

Circuit Diagram
The circuit is designed using Tinkercad. Here's how the buttons are mapped:

A0 – BJP

A1 – INC

A2 – AAP

A3 – OTH

A4 – Result

Pin 12 – Green LED (Vote Confirmation)

Pin 13 – Red LED (Result Display)

Pins 6 to 11 – LCD control and data pins

🧾 How It Works
On boot, the LCD displays a welcome message and lists the party abbreviations.

Voters press one of the four buttons to vote. A green LED flashes to confirm the vote.

Pressing the Result Button (A4):

Activates the red LED

Displays which party has the highest votes

Shows “Tie Up or No Result” if no clear winner

Resets vote counters for the next round

💡 Logic for Result Calculation
If one party has more votes than all others, it is declared the winner.

If no party has a clear majority, the system displays a "Tie Up or No Result" message.

No voting = "No Voting" message.

🧠 Code Explanation
LiquidCrystal lcd(11,10,9,8,7,6); – Initializes LCD with pin mappings

Button presses increment respective vote counters

LEDs are used for visual confirmation

Voting logic is handled using simple if-else conditions

Vote count and winner are shown on the LCD

Votes are reset after each result check

📷 Demo (Optional)
![Circuit Diagram](![Stunning Kasi-Juttuli (1)](https://github.com/user-attachments/assets/910de023-abed-4f97-a61a-8973d4f5c48e)
)


🧪 Future Improvements
Add EEPROM memory to store vote data after reset

Add more parties or user interface with a keypad

Use RFID for voter authentication

Secure vote storage and encryption
