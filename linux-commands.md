create three subheadings like basic commands, most commonly used commands and advanced commands with description of each command

# basic commands
1. ls # list the files and directories in the current directory
    ls sub-commands
    -a # list all files and directories including hidden files and directories
    -l # list files and directories in long format
    -h # list files and directories in human-readable format
    -t # sort files and directories by modification time
    -r # reverse the order of the sort
    -d # list directories only
    -
5. mkdir # create a new directory
    mkdir sub-commands
    -p # create parent directories as needed
    -v # print a message for each created directory

6. rm # remove a file or directory
    rm sub-commands
    -f # force the removal of a file or directory
    -i # prompt before every removal
    -r # remove directories and their contents recursively
    -v # explain what is being done
    --help # display help information
    --version # display version information

7. rmdir # remove a directory
8. cp # copy a file or directory
    cp sub-commands
    -a # archive files and directories
    -i # prompt before overwriting
    -r # copy directories and their contents recursively
    -v # explain what is being done
    --help # display help information
    --version # display version information

9. mv # move a file or directory
    mv sub-commands
    -i # prompt before overwriting
    -v # explain what is being done
    --help # display help information
    --version # display version information

10. touch # create a new file
    touch sub-commands
    -a # change the access time of a file
    -c # do not create a file if it does not exist
    -m # change the modification time of a file
    -r # use the access and modification times of another file
    -t # use a specific time instead of the current time
    --help # display help information
    --version # display version information

11. cat # concatenate and display the content of a file
12. more # display the content of a file page by page
13. less # display the content of a file page by page
13. head # display the first few lines of a file
14. tail # display the last few lines of a file
15. grep # search for a pattern in a file
16. find # find files and directories
17. wc # count the number of lines, words, and characters in a file
18. sort # sort the lines of a file
19. cut # cut the fields of a file
20. paste # merge the lines of files
21. tr # translate the characters of a file
22. sed # stream editor
23. awk # pattern scanning and processing language
24. diff # find the difference between two files
25. tar # archive files
26. gzip # compress files
27. gunzip # uncompress files
28. zip # compress files
29. unzip # uncompress files
30. ps # process status
31. top # display the top processes
32. kill # kill a process
33. killall # kill all processes
34. pkill # signal processes based on name and other attributes
35. pgrep # list processes based on name and other attributes
36. jobs # list the jobs running in the background
37. bg # resume a job in the background
38. fg # resume a job in the foreground
39. nohup # run a command immune to hangups
40. & # run a command in the background
41. ctrl+z # suspend a command
42. ctrl+c # terminate a command
43. ctrl+d # exit the shell
44. history # display the command history
45. clear # clear the screen
46. date # display the current date and time
47. cal # display the calendar
48. who # display the users who are currently logged in
49. whoami # display the current user
50. finger # display information about the users
51. w # display information about the users
52. uptime
53. uname
54.

s -lr --> reverse alphabetic order
ls -lt --> latest files are on the top
ls -ltr --> old files are on the top
ls -la --> list all files and folders including hidden


file create
------------
touch --> creates an empty file
mkdir --> make directory

update file with content
-----------------------
cat > <file-name> --> file will open
enter the content
enter and ctrl+d

> --> replaces the content
>> --> appends the content

reading file
-----------------------
cat file-name

remove file and folder
----------------------
rm <file-name> 
rmdir <folder-name> --> removes empty directory
rm -r devops --> recursive --> go inside every folder and delete everything


copy
----------------------
cp <source> <destination>
cp -r --> recursive

cut
----------------------
mv --> move
with in the same folder if you use mv command, it works as rename

mv sivakumar sivakumar-1 --> this will rename the file from sivakumar sivakumar-1


grep command
----------------
grep <word-to-find> <file-name>

Linux is by default case sensitive
Devops and DEVOPS are different

| --> piping one command output will become input to another command

wget vs curl
---------------
https://github.com/git-for-windows/git/releases/download/v2.43.0.windows.1/Git-2.43.0-64-bit.exe

wget --> download files
curl --> downloads the text content directly on to terminal

cut and awk
--------------
https://github.com/daws-76s/notes/blob/master/session-01.txt

delimiter --> we get fragments
:
/
---
https:

github.com
daws-76s

cut -d / -f 1

awk
------
awk -F / '{print $1F}'
awk -F / '{print $NF}' --> last fragment

awk command is used to divide the data based on columns

uname
ls
cat
cp
mv
grep
cut
awk
head and tail

head <file-name> --> first 10lines
tail <file-name< --> last 10 lines

Editors
-------------
vim --> visually improved

vim <file-name>

colon/command mode
------------------
:/<word-to-search> --> search from top
:?<word-to-search> --> search from bottom

sudo cp /etc/ssh/sshd_config sshd_config
sudo chown ec2-user:ec2-user sshd_config

replace the content/word
-----------------------
:s/<word-to-find>/<word-to-replace> --> replace the word where your cursor is, this will replace only first occurence in that line

:2s/<word-to-find>/<word-to-replace>
:%s/<word-to-find>/<word-to-replace>/g --> all occurences

SDLC
------
Requirements
Design
Develop
Test
Deploy
Maintain

4-7

head 7 | tail 3

:wq!

dd

// Navigation commands
cd [directory]       // Change directory
ls                   // List files and directories
pwd                  // Print current working directory

// File and directory manipulation
mkdir [directory]    // Create a new directory
touch [file]         // Create a new file
cp [source] [target] // Copy a file or directory
mv [source] [target] // Move or rename a file or directory
rm [file]            // Remove a file
rmdir [directory]    // Remove an empty directory

// File content manipulation
cat [file]           // Display file content
head [file]          // Display the first few lines of a file
tail [file]          // Display the last few lines of a file
grep [pattern] [file]// Search for a pattern in a file
sed [pattern] [file] // Stream editor for text transformation

// Process management
ps                   // List running processes
kill [PID]           // Terminate a process
top                  // Display system processes in real-time

// File permissions
chmod [permissions] [file] // Change file permissions
chown [user] [file]        // Change file ownership

// Network commands
ping [host]          // Send ICMP echo requests to a host
curl [URL]           // Transfer data from or to a server
ssh [user@host]      // Connect to a remote server using SSH

// Package management
apt-get [package]    // Install or manage packages (Debian-based systems)
yum [package]        // Install or manage packages (Red Hat-based systems)
brew [package]       // Install or manage packages (macOS)

// Version control
git [command]        // Version control system commands

// Text manipulation
awk [pattern] [file] // Text processing and pattern matching
cut [options] [file] // Extract sections from lines of files
sort [file]          // Sort lines of text files
