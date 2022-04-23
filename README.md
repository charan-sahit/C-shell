Aim:
Implement a shell that supports a semi-colon separated list of commands. Uses 'strtok' to tokenize the command. Also, supports '&' operator which lets a program run in the background after printing the process id of the newly created process

Builtin Commands:
cd
ls
echo
pwd
pinfo

Files used:
main.c:
main function that executes prompt and runs the while loop

display.c:
shows the display prompt with username and other stuff

read_command.c:
Reads the entire command and returns it in the form a string

interpret_command.c:
interprets the command and checks which function should be executed

exit_children.c:
checks if any child is terminated and prints it

ls_command.c:
executes the ls command with all the flags

repeat.c:
executes the repeat command

fgbgprocess.c:
runs the background process and foreground processes which arent built in commands

built_in_command.c:
runs the builtin commands

redirection.c
handles input and output redirection also handles multiples redirections

pipe.c:
handles piping and multiple pipes as well

jobs.c:
displays the job number, status of the process, and its pid

sig.c:
the sig command does its job according to the given signal number on the given job number

fg.c and bg.c:
fg Brings the running or stopped background job corresponding to ​job number​ to the foreground, and changes its state to ​running .​The shell should throw an error if no job with the given job number exists. bg Changes the state of a stopped background job to running (in the background). The shell should throw an error if no background job corresponding to the given job number exists, and do nothing if the job is already running in the background.

signal_handling.c
contains code for ctrl C, ctrl Z and ctrl D
1. CTRL-Z It should push any currently running foreground job into the background, and change its state from running to stopped. This should have no effect on the
shell if there is no foreground process running.
2. CTRL-C It should interrupt any currently running foreground job, by sending it the ​SIGINT​ signal. This should have no effect on the shell if there is no foreground
process running.
3. CTRL-D It should log you out of your shell, without having any effect on the actual terminal.

Execution:
make
./shell