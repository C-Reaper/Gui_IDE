## Overview
The project is a GUI application written in C using the Alx library. It allows users to save their data on a PC and provides options for backing up data via USB, Mi Cloud, or ADB.

## Features
- Backup data to PC directly through USB
- Backup data via Mi Cloud
- Backup data using ADB (Android Debug Bridge)
- Option to increase/decrease font size of the text editor
- Option to scroll through the text editor

## Project Structure
```
Gui_IDE/
├── build/              # .exe files produced by Main.c
├── src/                # src code
│   ├── Main.c          # Entry point
│   └── *.h             # stand alone Header-based C-files, without *.c files that implement it
├── Makefile.linux      # Linux Build configuration
├── Makefile.windows    # Windows Build configuration
├── Makefile.wine       # Wine Build configuration
└── README.md           # This file
```

### Prerequisites
- GCC or Clang C/C++ Compiler and Debugger
- Make utility
- Standard development tools

## Build & Run
To build the project for Linux:
```bash
cd Gui_IDE
make -f Makefile.linux all
```
To run the application:
```bash
make -f Makefile.linux exe
```

To clean and rebuild:
```bash
make -f Makefile.linux clean
make -f Makefile.linux all
```

For Windows cross compilation:
```bash
make -f Makefile.windows all
```
And to run the application on Windows, you will need to copy the produced `.exe` file to a Windows machine and run it.

To build for WebAssembly using Emscripten:
```bash
make -f Makefile.web all
```

Note: This README provides information based on the provided project structure and files.