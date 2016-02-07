# Compilation guide

## Dependencies

CMake, SDL2

Linux: Make (for default CMake generator)

Windows: Visual Studio (tested on VS 2015)

## Linux compilation

1. `git clone https://github.com/jozef-mitro/project-walking-code.git`
2. `cd project-walking-code`
3. `mkdir build && cd build`
4. `cmake .. && make`
5. Binary will be located in `.../project-walking-code/bin/`

## Windows compilation (using Visual Studio)

1. `git clone https://github.com/jozef-mitro/project-walking-code.git` in Git Bash or use your favourite git client to clone
  the project.
2. Create Windows environment variable called SDL2 and set it to path to your SDL2 folder.
3. Run CMake GUI and set source code directory to directory where you cloned the project (NOT the src subdirectory inside it).
4. Set build directory to same path but add `/build` to the end.
5. Click `Configure` and then `Generate`. When asked choose your version of Visual Studio and whether you want to build 32bit
  or 64bit binaries.
6. There should be VS Solution file inside build directory now. Open it using Visual Studio and compile.
7. Binary will be located in `.../project-walking-code/bin/BUILD_PROFILE_NAME/` where BUILD_PROFILE_NAME is either
  `Debug` or `Release` depending on compilation.
8. In order to run the game you might need to copy appropriate (32bit or 64bit) SDL2 dll file to directory containing binary.

# Contribution guide

1. Fork the project.
2. `git clone LINK_TO_YOUR_FORK`
3. `git remote add upstream https://github.com/jozef-mitro/project-walking-code.git`
4. `git pull --rebase upstream master` to stay up to date with upstream changes (this might result in conflicts which you need
  to resolve manually).
5. When done, open pull request and wait for one of the collaborators to review your code.

# Collaboration guide

1. `git clone https://github.com/jozef-mitro/project-walking-code.git`
2. `git checkout -b feature/NAME_OF_YOUR_FEATURE` to create and checkout sepparate branch for your feature.
3. `git rebase master` to stay up to date with changes on master branch (this might result in conflicts which you need to
  resolve manually).
4. When done, open pull request and wait for one of the other collaborators to review your code.

# Style guide

1. Rule of the thumb, look a the existing code and follow that.
2. Use spaces instead of tabs (4 spaces per tab).
3. Curly brackets generally start at new line (for functions, ifs, fors, etc.)
4. `SHOUTING_SNAKE_CASE` for preprocessor macros (NOT for constants), `PascalCase` for class, structs and such, `camelCase` for
  class members, functions, local variables and such.
