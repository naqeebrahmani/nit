# **nit**
nit is an easy to use command line version controller made using C++ and the zlib library.

## Features
- Can be used easily in the command prompt
- Features an "exclude.nit" file, in which you can type the names of the files/directories that you want to be excluded (1 name per file). This works only if you type the name and not the path.
- Has a log file that saves the date, as well as the save description for each save.

## Commands
- **nit init**
     - Initializes a repository by creating a .nit directory
       
- **nit save**
     - Saves a compressed copy of your directory. It also includes all child directories and requires you to type a save description.
       
- **nit replace x (x = save number)**
     - Replaces the current directory with a specified save.
     - When replacing with a save that contains a file or directory that is currently excluded, the program will ask whether you want to replace that file or directory.
       
- **nit preview x (x = save number)**
     - Creates a preview directory inside the .nit directory where the specified save will be uncompressed and made available for preview.
     - Usually recommended before replacing.

- **nit log**
     - Displays the contents of the log file in the command prompt.
     - Shows each save's date, time and save description.

- **nit help**
     - Displays all available commands in the command prompt.

## Installation guide
So far, the application is Windows only, mostly because it is my main operating system and because i barely have any experience with other operating systems i.e. Linux.
### Installation and set up
1. Clone the repository or download the zip file
2. Navigate to the directory with the nit executable - "nit.exe"
3. Add the directory as a path to your system's environment variables
   - Now, you should be able to use nit in any directory. You can type "nit help" in your command prompt to test.

## Building the project
To be able to compile the source code you would need to have the compiled Zlib library with the corresponding headers on your device. You would also need to have a C++ compiler, as well as CMake and a build system if you're planning on using CMake.
<br>
Once you have these dependencies, you should be able to just change the Zlib and include directories path in the CMakeLists.txt and be able to build, given that you're using CMake, otherwise you would need to configure the project yourself.
