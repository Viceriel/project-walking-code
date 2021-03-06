# Compilation guide

## Dependencies

Build: CMake, SDL2, Make (on Linux), Visual Studio (on Windows)

Runtime: SDL2

For windows users this might require manually copying the appropriate (32bit or 64bit) SDL2 dll
file to the directory containing the binary file.

## Linux compilation

1. `git clone https://github.com/jozef-mitro/project-walking-code.git`
2. `cd project-walking-code`
3. `mkdir build && cd build`
4. `cmake .. && make`
5. The binary file will be located in `.../project-walking-code/bin/`

## Windows compilation (using Visual Studio)

1. `git clone https://github.com/jozef-mitro/project-walking-code.git` in Git Bash or use your
favourite git client to clone the project.
2. Create Windows environment variable called SDL2 and set it to path to your SDL2 folder.
3. Run CMake GUI and set the source code directory to the directory where you cloned the project
(NOT the src subdirectory inside it).
4. Set the build directory to the same path but add `/build` to the end.
5. Click `Configure` and then `Generate`. When asked, choose your version of Visual Studio and
whether you want to build 32bit or 64bit binaries.
6. There should be a VS Solution file inside the build directory now. Open it using Visual Studio
and compile.
7. Binary will be located in `.../project-walking-code/bin/BUILD_PROFILE_NAME/`, where
BUILD_PROFILE_NAME is either `Debug` or `Release` depending on compilation.
8. In order to run the game, you might need to manually copy appropriate (32bit or 64bit) SDL2 dll
file to the directory containing the binary file.

# Contribution guide

1. Fork the project.
2. `git clone LINK_TO_YOUR_FORK`
3. `git remote add upstream https://github.com/jozef-mitro/project-walking-code.git`
4. `git pull --rebase upstream master` to stay up to date with upstream changes (this might result
in conflicts, which you need to resolve manually).
5. When done, open pull a request and wait for one of the collaborators to review your code.

Or equivalent in your git gui client of choice.

# Style guide

1. Rule of the thumb, look at the existing code and follow that.
2. Use spaces instead of tabs (4 spaces per tab).
3. Curly brackets generally start at new line (for functions, ifs, fors, etc.).
4. `SHOUTING_SNAKE_CASE` for preprocessor macros (NOT for constants), `PascalCase` for types,
`camelCase` for pretty much everything else (local variables, class members, functions, etc.).
5. Lines should be less than 100 characters long.

# Some "useful" links

- [Video tutorial for generating Visual Studio Solution using CMake](https://www.youtube.com/watch?v=gYmgbqGfv-8)
- [How to fork a github repository](https://help.github.com/articles/fork-a-repo/)
- [How to keep your fork updated](http://stackoverflow.com/questions/7244321/how-to-update-a-github-forked-repository)
- [How to resolve merge conflicts](https://help.github.com/articles/resolving-a-merge-conflict-from-the-command-line/)
- [Somewhat more thorough description of sample git workflow](https://musescore.org/en/developers-handbook/git-workflow)
