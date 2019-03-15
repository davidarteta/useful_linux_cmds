# useful_linux_cmds
Some useful Linux shell commands

## Convert DOS newlines (CR/LF) to Unix format using sed command

- If you are using BASH shell type the following command (press Ctrl-V then Ctrl-M to get pattern or special symbol)

`sed 's/^M$//' filein > fileout`

- Using a perl one liner

`perl -pi -e 's/\r\n/\n/g' filein > fileout`

## Searching for some IDs in a larger file with several column fields (database.txt)
Prepare an IDs.txt file with one column of IDs and then do:

`while read line; do grep "\<$line\>"  database.txt >> fileout ; done < IDs.txt`

## Finding files in directories
Find all files ending with pdf  in a directory and subdirectories and copy them elsewhere

`find . -name '*.pdf' -print0 | xargs -0 cp -t myPDFs/`

## Find text in a file and send the line, one line before and two lines after the matching line

`grep -A 2 -B 1 "^TTTTC" filein >> fileout`

## Replace all the spaces in a given file by an underscore in-place

`sed -i 's/\ /_/g' filein`
