# When You Run a Program

Suppose you execute `python app.py`:

31. Who receives this command?

The command is entered into a shell (such as PowerShell, Command Prompt, or Bash). The shell looks up `python`, starts that executable, and passes `app.py` as an argument; a terminal displays the interaction but usually does not interpret the command itself.

32. How does the operating system know where Python is?

The shell searches locations configured in its command lookup rules, commonly directories listed in `PATH`, then asks the OS to start the executable. If no matching executable is found, the command fails; virtual environments can change which Python is found first.
