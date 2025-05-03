# 📈 Stock Market Visualization Dashboard (RISC-V Platform)

A real-time interactive stock dashboard built for embedded systems using the RISC-V architecture. This project integrates graphical display, PS/2 mouse and keyboard input, and audio playback to offer a fully immersive financial data visualization experience.

---

## 🔧 Overview

Designed for an FPGA development board (e.g., DE1-SoC) running a RISC-V core, this system renders historical stock market data on a VGA monitor. Users can explore data interactively through both keyboard and mouse input. The project blends **low-level hardware control** with **efficient financial data processing** for a complete embedded visualization solution.

---

## 🚀 Features

### 📊 Pre-loaded Stock Visualization
- Display historical stock price data for:
  - **Apple**
  - **Amazon**
  - **Google**
  - **Meta**
  - **Netflix**
- Toggle between **daily**, **weekly**, and **monthly** sampling.
- Adjustable time windows (from 1 to 10 years).

### 🖱 User Interaction
- **PS/2 Mouse Support**:
  - Hover to inspect prices and dates.
  - Click to select stocks and trigger audio playback.
- **PS/2 Keyboard Support**:
  - Arrow keys to scroll and zoom data.
  - Number keys (1–5) to switch stocks.
  - `+ / -` to modify year range.
  - Space/H for instructions screen.

### 🔊 Audio Integration
- Each stock is associated with an **audio clip** summarizing key data.
- Audio playback via memory-mapped audio controller (mono output).

### 🎨 Graphical Rendering
- Custom **VGA driver logic** for:
  - Drawing axis lines, stock graphs, tooltips, and overlays.
  - Smooth line-drawing with Bresenham’s algorithm.
- Real-time updates during interaction.

### 📁 Optimized Data Handling
- Fast filtering of stock values based on parsed UNIX timestamps.
- Normalization and scaling of y-axis for accurate plotting.
- Minimal memory footprint with dynamic array reuse.

---

## 🧠 Skills & Technologies Used

| Skill Area          | Description                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| **Embedded C**      | System logic using memory-mapped I/O, registers, and hardware interfacing   |
| **VGA Graphics**    | Custom pixel rendering, line drawing, and buffer control                    |
| **PS/2 Protocols**  | Byte decoding and mouse/keyboard state machines                             |
| **Audio Driver**    | Mono playback with FIFO buffering and I²S interfacing                       |
| **Time Handling**   | `time.h` for date parsing, interval computation, and formatting             |
| **Data Sampling**   | Daily/weekly/monthly aggregations for windowed visualization                |
| **System Programming** | Event polling, register access, and real-time rendering                 |
| **Team Collaboration** | Clean modular architecture with consistent documentation and naming     |

---

## 💡 Usage

1. Connect a **VGA monitor**, **PS/2 mouse**, and **PS/2 keyboard** to the FPGA board.
2. Flash the board with the compiled **RISC-V binary**.
3. Interact with the dashboard:
   - Press `1–5` to switch between different stock datasets.
   - Use arrow keys and `+/-` to adjust sampling rate and time range.
   - Hover with the mouse to view dynamic date and price tooltips.
   - Click stock labels to **trigger audio playback**.

to try the project online go to [cpulator](https://cpulator.01xz.net/?sys=rv32-de1soc) which emulates the project,

1. near the compile and load button change language to C
2. copy/paste the project.c code, or copy the raw file and place it into the editor
3. click compile and load
4. once its compiled press continue or F3
5. in the devices tab set irq 22 to a keyboard and irq 23 to a mouse
6. press H using the keyboard and follow the help page on from the project to use the dashboard

Note: the mouse moves in the opposite direction in the y axis as the true implementation of the vga graphics has the coordinate axes flipped,all else is the same
---

## 🛠 Future Improvements

- 📥 **Dynamic stock loading** (via SD card or serial port)
- 🌐 **Real-time stock updates** through Ethernet or UART
- 📊 Additional metrics (high/low, volume, trends)
- 🖼 Enhanced UI design with smoothed mouse cursor rendering

---

## 👥 Authors

- **Andre Brian Danny**
- **Rehan Bhatti**

---

## 📩 Contact

Feel free to connect via [LinkedIn](https://linkedin.com/in/andrebdanny) or reach out via email at **andrebdanny@gmail.com** if you're interested in discussing this project or other embedded systems applications.

---
