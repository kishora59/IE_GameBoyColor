# A GameBoyColor Emulator
This is a GameBoyColor emulator written in my favorite language `C`. I use [SDL2](https://github.com/libsdl-org/SDL)+[Dear ImGui](https://github.com/ocornut/imgui) for
sounds, graphics and input. So it can run on any platform that supports SDL2. And the GUI part is totally separated from the core emulator, so you can easily
replace it with your own GUI. Check the `gui/gui.h`.

<div style="text-align: center;">
  <img src="https://github.com/user-attachments/assets/b1b2ed18-1986-4619-83d4-64be2433993b" alt="screenshot" width="500"/>
</div>


# Build
## Windows
You need MSYS2 to build as I used some POSIX functions.
1. Install [MSYS2](https://www.msys2.org/)
2. Clone the project
```bash
git clone https://github.com/Kaushik2201/KameBoyColor.git
cd Colored_Game_Boy_Emulator
git submodule update --init
```
3. Open `MSYS2 shell` and install the necessary packages
4. Go to the root directory ```cd ..```
5. Then open the Emulator folder in MSYS2 by using ```cd "[Path of your folder]"```
```bash
pacman -S mingw-w64-x86_64-cmake mingw-w64-x86_64-toolchain mingw-w64-x86_64-SDL2
```
6. Set the `MSYS2_PATH` in `CMakeLists.txt` to your MSYS2 installation path
```cmake
set(MSYS2_PATH "C:\\MyPrograms\\msys2")
```
7. Build the project (`This step is supposed to be done in MSYS2 shell. DO NOT USE Git Bash shell!!`)
```bash
cmake -G Ninja
```
8. Go to the ```build``` directory
9. Type ```ninja```
10. Finally execute ```./kgbc```

# Controls
Its in the `gui/main_sdl2.cpp` file. You can change it to whatever you like.

| Keyboard | Gameboy |
|-----|--------|
| A   | A      |
| B   | B      |
| Enter | Start |
| S   | Select |
| ↑   | Up     |
| ↓   | Down   |
| ←   | Left   |
| →   | Right  |

