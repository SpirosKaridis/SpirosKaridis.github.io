# SpirosKaridis.github.io

Exercise 2 methodology:

bandit0: A simple modification of the ssh command using the -p parameter.

bandit1: Connect to bandit1, there is a single dashed file. Access the contents using cat < -.

bandit2: -//-, to view the contents of a file with spaces in it's name use cat followed by the file name contained in " ".

bandit3: -//-, cd in the inhere directory, using ls -a -l I get the list of all hidden files, cat the .hidden file to get code.

bandit4: -//-, once in the inhere directory and using the ls command we find multiple -fileXX files. All are dashed file names so we use once again the cat < -fileXX to find the one with the code inside

bandit5: -//-, we don't proceed into the inhere directory in order to use the find command. We use the parameters given by the instructions (find ~/inhere -size 1033c -type f) and then once in the correct directory ls -a to reveal the hidden file.

bandit6: -//-, this one is a bit trickier as need to search the whole server. For that we use find / -type f -user bandit7 -group bandit6 -size 33c with a bit of added code such as 2>/dev/null to not be given the error messages of "Permission denied".

bandit7: -//-, the file data.txt is filled with many randome words and codes. Using grep -rw 'data.txt' -e 'millionth' we search from the source "data.txt" the pattern "millionth" and we get the corresponding line which includes the code
