### Navigating the File System
```
$ whoami
$ pwd
$ hostname
$ ls
$ ls -l
$ ls -a
$ cd
$ cd .. 
$ cd ~
```
whoami displays my logged-in username and confirms which account I'm operating under
pwd stands for print working directory. It displays the absolute path of my current location in the file system(e.g. project-rnaseq).
hostname displays the name of the computer/server you are logged into (login01)
ls Lists files and directories in the current directory it shows names only (no details)
ls -l	Lists files and directories in long format. Shows:	permissions,	owner, group, file size, last modified date/time, filename
ls -a Lists all files, including hidden files. Hidden files begin with a dot (.), e.g. .bashrc
cd Stands for change directory, With no argument, moves to the home directory
cd .. Moves one directory up (to the parent directory)
cd ~ Changes directory to the home directory(~). ~ is a shortcut for /home/username

### Working with files and directories
```
$ pwd
$ mkdir ~/mybioc6243
$ mkdir ~/mybioc6243/project-linux
$ cd ~/mybioc6243/project-linux
$ touch file.txt
$ ls -ltr
$ cp file.txt file_copy.txt
$ ls -ltr
$ mv file_copy.txt /tmp/
$ rm /tmp/file_copy.txt
$ rm -r ~/mybioc6243
```
The first command (pwd) gives the current location, fdfasfafa
pwd stands for print working directory.
mkdir ~/mybioc6243 creates a new directory named mybioc6243 inside my home directory
mkdir ~/mybioc6243/project-linux creates a subdirectory called project-linux inside mybioc6243
cd ~/mybioc6243/project-linux changes my current directory to project-linux
pwd confirms that I'm now inside: ~/mybioc6243/project-linux
touch file.txt creates an empty text file named file.txt
If the file already existed, it would update its timestamp
ls -ltr Lists files: in long format (-l), sorted by time (-t), in reverse order (oldest first, -r)
cp file.txt file_copy.txt creates a copy of file.txt. New file is named file_copy.txt, Original file remains unchanged
ls -ltr Lists files again, Shows: file.txt (older), file_copy.txt (newer)
mv file_copy.txt /tmp/ Moves file_copy.txt from the current directory to /tmp. The file is no longer in the project directory, /tmp is a temporary system directory
rm /tmp/file_copy.txt Permanently deletes file_copy.txt. The file is gone forever.	There is no undo option
rm -r ~/mybioc6243 -r means recursive. Deletes:	the directory mybioc6243, all subdirectories,	all files inside

### Viewing and editing text files`
```
$ cd ~/mybioc6243/project-linux
$ cp /groups/bioc6243_0/data/fastq/toy.fastq .
$ ls -ltr
$ cat toy.fastq
$ less toy.fastq
$ head -20 toy.fastq
$ tail -20 toy.fastq
$ ls -ltr
$ nano file.txt
```
The first code (cd ~/mybioc6243/project-linux) Moves into the project directory where files will be stored and inspected.
cp /groups/bioc6243_0/data/fastq/toy.fastq. copies the FASTQ file toy.fastq into the current directory(~/mybioc6243/project-linux)	.means current directory and keeps a local copy for inspection
cat toy.fastq Prints the entire contents of the FASTQ file to the terminal. Only suitable for very small files. Not recommended for large FASTQ files
less toy.fastq opens the file in an interactive viewer. Scroll up/down
head -20 toy.fastq displays the first 20 lines of the file.
tail -20 toy.fastq displays the last 20 lines of the file.
Why this matters confirms the file ends properly and is not truncated.
ls -ltr Lists files again to verify file timestamps and contents.
nano file.txt opens the nano text editor to create or edit file.txt. Ctrl + O → save, Press Enter to confirm
```
### Searching Pipes & Redirection
```
$ cd ~/mybioc6243/project-linux
$ grep "mistake" file.txt
$ grep -i "gene" file.txt
$ echo "hello" > file.txt
$ echo "world" >> file.txt
$ cat file.txt | grep "hello"
$ ls | grep ".txt"
```
The first command (cd ~/mybioc6243/project-linux) Moves into the directory project-linux. All subsequent commands act on files in this directory.
grep "mistake" file.txt: Searches for the exact word mistake in file.txt. Prints any line that contains mistake. 
grep -i "gene" file.txt: Searches for the word gene, ignoring case. Matches: gene, Gene, GENE Prints all matching lines
echo "hello" > file.txt: Writes the text hello into file.txt. > overwrites the file Any previous content in file.txt is erased
echo "world" >> file.txt Appends the text world to the end of file.txt. >> means append. Does not erase existing content after these two commands, file.txt contains: hello world
cat file.txt | grep "hello": cat file.txt prints the contents of the file. | (pipe) sends output to the next command. grep "hello" filters and prints only lines containing hello Output: hello
ls | grep ".txt": ls lists all files in the directory. grep ".txt" filters the list to show only files ending with .txt

### Permissions & Processes
```
$ cd ~/mybioc6243/project-linux
$ ls -l
$ chmod 755 file.txt
$ ps
$ top
$ htop
Ctrl + C
```
The funtions of all the commands are listed bellow;
cd ~/mybioc6243/project-linux: Moves into the project directory.
ls -l: Lists files in long format, showing permissions, owner, size, and modification time.
chmod 755 file.txt: Changes the permissions of file.txt.
755 means:
7 = rwx (read, write, execute) for the owner
5 = r-x (read, execute) for the group
5 = r-x (read, execute) for others
Ps: Displays currently running processes in the current terminal session.
top: Shows real-time system activity including CPU and memory usage.
htop: An enhanced and more user-friendly version of top (may not be installed on all systems).
Ctrl + C: Stops a running process or exits commands like top or htop.
