# useful_linux_cmds
Some useful Linux shell commands

#Convert DOS newlines (CR/LF) to Unix format using sed command

If you are using BASH shell type the following command (press Ctrl-V then Ctrl-M to get pattern or special symbol)

`sed 's/^M$//' input.txt > output.txt`

