# SpirosKaridis.github.io

Exercise 2 methodology:

bandit0: A simple modification of the ssh command using the -p parameter.

bandit1: Connect to bandit1, there is a single dashed file. Access the contents using cat < -.

bandit2: -//-, to view the contents of a file with spaces in it's name use cat followed by the file name contained in " ".

bandit3: -//-, cd in the inhere directory, using ls -a -l I get the list of all hidden files, cat the .hidden file to get code.

bandit4: -//-, once in the inhere directory and using the ls command we find multiple -fileXX files. All are dashed file names so we use once again the cat < -fileXX to find the one with the code inside

bandit5: -//-, we don't proceed into the inhere directory in order to use the find command. We use the parameters given by the instructions (find ~/inhere -size 1033c -type f) and then once in the correct directory ls -a to reveal the hidden file.

bandit6: -//-, this one is a bit trickier as need to search the whole server. For that we use find / -type f -user bandit7 -group bandit6 -size 33c with a bit of added code such as 2>/dev/null to not be given the error messages of "Permission denied".

bandit7: -//-, the file data.txt is filled with many randome words and codes. Using grep -rw 'data.txt' -e 'millionth' we search from the source "data.txt" the pattern "millionth" and we get the corresponding line which includes the code.

bandit8: -//-, same as before we have a plethora of codes and we look for the one that is unique. instinctively we use the uniq command with the -u parameter. but that return many wrong results so first we sort the list and we end up using sort data.txt | uniq -u.

bandit9: -//-, to find the single readable string we use strings data.txt | grep =. By using strings we only keep the human readable parts of the file and with grep we keep the lines which contain the symbol '=' and we get the code

bandit10: -//-, this one is fairly simple. Base64 is an encoding method of randomizing characters. Luckily by typing base64 --decode we get the decoded version.
