# MOBILE-TECHNOLOGY-BASED-BULLETIN-BOARD

**Block Diagram**
Mobile Phone
      │
      │ SMS
      ▼
+--------------+
|   GSM Module |
+--------------+
        │ UART
        ▼
+--------------------+
| LPC2148 Controller |
+--------------------+
        │
        │
        ▼
+--------------------+
| Shift Registers    |
| 74HC164 / 74HC573  |
+--------------------+
        │
        ▼
+--------------------+
| Dot Matrix Display |
+--------------------+

**** Project Folder Structure****

 Mobile-Bulletin-Board
│
├── README.md
├── LICENSE
│
├── Code
│   ├── main.c
│   ├── gsm.c
│   ├── gsm.h
│   ├── dotmatrix.c
│   ├── dotmatrix.h
│   ├── uart.c
│   └── uart.h
│
├── Proteus_Simulation
│   └── bulletin_board.pdsprj
│
├── Circuit_Diagram
│   └── circuit.png
│
├── Images
│   ├── project_setup.jpg
│   ├── dot_matrix_display.jpg
│   └── output_display.jpg
│
└── Documentation
    └── Project_Report.pdf
    
    **Short Project Description**
    
    Developed a GSM-based wireless bulletin board using LPC2148 microcontroller and Dot Matrix Display.
    The system receives SMS messages through a GSM module and displays them as scrolling text on LED display. Implemented        UART communication, EEPROM storage, and shift register interfacing for efficient message processing and display control.
    Technologies: Embedded C, ARM7 (LPC2148), GSM Communication, UART, Dot Matrix Display.

**PROJECT WORKING FLOW**

This project implements a GSM-based wireless bulletin board that displays scrolling messages on a Dot Matrix LED display using a microcontroller. The message is stored in EEPROM and continuously displayed until a new SMS is received.

When a new message arrives, the system verifies the sender’s mobile number and security key. If authorized, the new message replaces the old one in EEPROM and starts scrolling on the display. Unauthorized access triggers an alert SMS to the owner, ensuring secure and reliable message updates.
