# Boilerplate for OpenGL with GLEW and GLFW on Windows

This project provides a simple setup for using OpenGL with GLEW and GLFW on Windows. Follow the steps below to get started.

## Prerequisites
- Install [GLEW 2.1.0](http://glew.sourceforge.net/) in `C:/`
- Install [GLFW 3.3.8](https://www.glfw.org/download.html) in `C:/`
  - If you are using a newer version, rename the folder to `glfw-3.3.8.bin.WIN64` for compatibility with the commands.
- Add env variable path `C:\glfw-3.3.8.bin.WIN64\lib-mingw-w64` and `C:\glew-2.1.0\lib\Release\x64 ` in both system variable and user variable (just in case).
## Setup

1. **Code Runner Configuration**
   Add the following entry in the `settings.json` of your Code Runner extension for C++:
   ```json
   "cpp": "cd $dir && g++ $fileName -o $fileNameWithoutExt -I C:\\glfw-3.3.8.bin.WIN64\\include -I C:\\glew-2.1.0\\include -L C:\\glfw-3.3.8.bin.WIN64\\lib-mingw-w64 -L C:\\glew-2.1.0\\lib\\Release\\x64 -lglfw3dll -lglew32 -lopengl32 && ./$fileNameWithoutExt"

### run the code using `Ctrl + Alt + N` and stop the code runner using `Ctrl + Alt + M`
