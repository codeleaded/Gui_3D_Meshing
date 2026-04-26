# Project README

## Overview
This project is a 3D meshing application written in C. The application uses advanced graphics libraries and algorithms to render 3D meshes on various platforms, including Linux, Windows, WebAssembly (using Emscripten), and Wine.

## Features
- Real-time rendering of 3D meshes.
- Support for importing and exporting various mesh formats.
- Cross-platform compatibility: runs on Linux, Windows, WebAssembly, and Wine.
- Debugging capabilities using GCC and GDB.

## Project Structure

### Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools
- Libraries needed for specific platforms:
  - Linux: X11, PNG, JPEG
  - Windows: WINAPI
  - WebAssembly: Emscripten
  - Wine: MinGW-w64

## Build & Run
### Building on Linux
To build and run the project on a Linux system:

```bash
cd /path/to/Gui_3D_Meshing
make -f Makefile.linux all
```

To clean the build artifacts and rebuild:

```bash
make -f Makefile.linux clean
make -f Makefile.linux all
```

### Building on Windows
To build and run the project on a Windows system:

```cmd
cd /path/to/Gui_3D_Meshing
make -f Makefile.windows all
```

To clean the build artifacts and rebuild:

```cmd
make -f Makefile.windows clean
make -f Makefile.windows all
```

### Building for WebAssembly
To build and run the project for web using Emscripten:

```bash
cd /path/to/Gui_3D_Meshing
emmake make -f Makefile.web all
```

To run the WebAssembly application locally:

```bash
emrun --no_browser --port 8080 ./build/index.html
```

### Building for Wine
To build and run the project on a Linux system using Wine:

```bash
cd /path/to/Gui_3D_Meshing
make -f Makefile.wine all
```

To clean the build artifacts and rebuild:

```bash
make -f Makefile.wine clean
make -f Makefile.wine all
```

### Build Options
- `all`: Build the output executable.
- `do`: Build the project and execute the output.
- `clean`: Remove all build artifacts.
- `exe`: Execute the built application.