# C-RealTime-Digital-Clock

A high-fidelity console application that emulates a 12-hour digital clock. This project demonstrates the core principles of iterative logic, temporal synchronization using system delays, and dynamic terminal UI updates in the C programming language.

## 🛠️ Technical Overview
The application functions as a continuous state machine where time increments are managed through a controlled infinite loop. It showcases how software can interface with operating system-specific libraries to manage execution flow.

### Key Engineering Concepts:
- **Temporal Synchronization:** Utilizes the `Sleep()` function from the `windows.h` library to synchronize the software loop with the real-world 1000ms interval.
- **Buffer Management:** Implements `system("cls")` calls to clear the standard output buffer, creating a seamless "refresh" effect in the terminal.
- **Overflow Logic:** Features a nested conditional structure to handle time rollovers (seconds to minutes, minutes to hours, and 12-hour cycle resets).
- **Data Validation:** Includes pre-execution guard clauses to ensure user input adheres to standard time formats ($H \le 12, M \le 59, S \le 59$).

## ✨ Features
- **Manual Time Configuration:** Allows users to set a custom starting point for the clock.
- **Real-Time Simulation:** Accurate 1-second increments maintained via system-level thread pausing.
- **Formatted Visualization:** Uses `%02d` format specifiers to maintain a consistent 00:00:00 aesthetic, ensuring a professional digital display.
- **Automated Rollover:** Intelligent logic that resets hours to 1 after reaching 12, simulating a standard analog-to-digital cycle.

## 🛠️ Tech Stack
- **Language:** C (Standard C11)
- **Library:** `windows.h` (for `Sleep` and `system` calls)
- **Operating System:** Optimized for Windows environments.

## 📂 Installation & Execution
### Prerequisites
- A C compiler (GCC/MinGW recommended) on a Windows environment.

### Compilation
Build the application using the following command:
```bash
gcc -o digital_clock main.c
