**Registry Editor:** A hierarchical database that stores low-level settings for the Microsoft Windows operating system and for applications that opt to use the registry.

## Add programs to Run Command

In the path "Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\App Paths"

* Create a Key called "your_program.exe"
* Change the default string value to be the absolute file name of the shortcut/executable you want to add.
* Add a "string value" with the name "PATH" and value of the absolute path to the exe/lnk (not including file name itself)
* Verify it works by attempting to run it using the RUN Command (Windows+R)

## Add shortcuts to Run Command
*  Place the shortcut in the "C:\Windows" directory.
   *  Note - Does not work for "Internet Shortcuts"

## Add programs to be recognized by command line

* In "environmental variables", add to PATH the absolute path of the directory that contains the EXE/LNK you want to be able to execute.
  * Update PATHEXT variable to include "LNK" if you want to use shortcuts, or other file extensions for respective extension. [StackOverflow Link](https://superuser.com/questions/1026918/how-can-i-execute-a-shortcut-in-my-path)
  * Verify using command line that you can execute the exe/lnk by the name of the file.

## Symlink

```bash 
# Create a file symlink with no flag
mklink Awesome_story.txt "C:\Windows\Users\Lee\Desktop\Awesome_story.txt"

# Create a directory symlink with \D
mklink /D Hearthstone "D:\Battlenet\Hearthstone"
```
* [Complete Guide to Symbolic Links Symlinks on Windows or Linux](https://www.howtogeek.com/howto/16226/complete-guide-to-symbolic-links-symlinks-on-windows-or-linux/)