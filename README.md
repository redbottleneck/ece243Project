📈 Stock Market Visualization Dashboard (RISC-V Platform)
A real-time interactive stock dashboard built for embedded systems using the RISC-V architecture. This project integrates graphical display, PS/2 mouse and keyboard input, and audio playback to offer a fully immersive financial data visualization experience.

🔧 Overview
This system renders historical stock market data on a VGA display, enabling users to navigate through company stock trends using either a PS/2 mouse or keyboard. Developed for a DE1-SoC-style FPGA running a RISC-V core, it highlights a blend of low-level hardware interfacing with high-level data processing.

🚀 Features
Pre-loaded Stock Visualization:

Display historical data for Apple, Amazon, Google, Meta, and Netflix.

Navigate stock price trends over customizable time windows (years, months, weeks, days).

User Interaction:

PS/2 Mouse: Select stocks, inspect data points, and trigger audio playback.

PS/2 Keyboard:

Arrow keys: change sampling mode, scroll through data, adjust year range.

Direct keys: switch between stocks.

Hotkeys for showing help/instructions.

Audio Integration:

Playback encoded audio clips per stock to enhance interactivity.

Graphical Rendering:

Custom VGA driver logic to render graphs, mouse cursor, date/price tooltips.

Interactive overlays that update based on user input.

Optimized Data Handling:

Efficient sampling (daily, weekly, monthly) using pre-parsed timestamps.

Dynamic normalization and graph scaling for different datasets.

🧠 Skills & Technologies Used
Skill Area	        Implementation Details
Embedded C    	    Core application logic in low-level C tailored to hardware memory-mapped I/O
VGA Graphics	      Custom line drawing, pixel plotting, and frame buffer manipulation
PS/2 Protocols	    Raw byte decoding and state management for mouse and keyboard input
Audio Driver	      Real-time mono audio streaming via memory-mapped audio controller
Time Handling  	    Parsing and manipulation of timestamps using time.h for interval-based filtering
Data Sampling	      Filtering, normalization, and dynamic range scaling of financial time-series data
System Programming	Direct register access (volatile pointers), low-level event polling, and buffer management
Team Collaboration	Modular code structure, consistent documentation, and multi-developer integration


💡 Usage
Connect a VGA monitor, PS/2 keyboard, and mouse to the FPGA board.

Flash the RISC-V binary containing this project.

Interact with the interface:

Use keys 1-5 to switch stocks.

Use arrow keys and +/- to change the year range and sampling mode.

Hover with mouse to view price and date tooltips.

Click stock list to play audio summary.


🛠 Future Improvements
Dynamic loading of stock data (SD card / serial input).

Real-time stock price updates via Ethernet or UART.

Enhanced GUI design with additional metrics (volume, high/low).

Improved pointer rendering and input smoothing.

👥 Authors
Andre Brian Danny
Rehan Bhatti

📩 Contact
Feel free to connect via [Andre Brian Danny](https://www.linkedin.com/in/andre-brian-danny)
or reach out via email at andrebdanny@gmail.com if you’re interested in discussing this project or similar system-level embedded applications.






