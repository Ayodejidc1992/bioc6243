Commands
○ $ whoami
○ $ pwd
○ $ hostname
○ $ ls
○ $ ls -l
○ $ ls -a
○ $ cd
○ $ cd .. 
○ $ cd ~

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

The funtions of all the commands are listed bellow;
$ whoami displays my logged-in username and confirms which account I'm operating under
$ pwd stands for print working directory. It displays the absolute path of my current location in the file system(e.g. project-rnaseq).
$ hostname displays the name of the computer/server you are logged into (login01)
$ ls Lists files and directories in the current directory it shows names only (no details)
$ ls -l	Lists files and directories in long format. Shows:	permissions,	owner, group, file size, last modified date/time, filename
$ ls -a Lists all files, including hidden files. Hidden files begin with a dot (.), e.g. .bashrc
$ cd Stands for change directory, With no argument, moves to the home directory
$ cd .. Moves one directory up (to the parent directory)
$ cd ~ Changes directory to the home directory(~). ~ is a shortcut for /home/username
$ mkdir ~/mybioc6243 creates a new directory named mybioc6243 inside my home directory
$ mkdir ~/mybioc6243/project-linux creates a subdirectory called project-linux inside mybioc6243
$ cd ~/mybioc6243/project-linux changes my current directory to project-linux
$ pwd confirms that I'm now inside: ~/mybioc6243/project-linux
$ touch file.txt creates an empty text file named file.txt
•	If the file already existed, it would update its timestamp
$ ls -ltr Lists files: in long format (-l), sorted by time (-t), in reverse order (oldest first, -r)
$ cp file.txt file_copy.txt creates a copy of file.txt. New file is named file_copy.txt, Original file remains unchanged
$ ls -ltr Lists files again, Shows: file.txt (older), file_copy.txt (newer)
$ mv file_copy.txt /tmp/ Moves file_copy.txt from the current directory to /tmp. The file is no longer in the project directory, /tmp is a temporary system directory
$ rm /tmp/file_copy.txt Permanently deletes file_copy.txt. The file is gone forever.	There is no undo option
$ rm -r ~/mybioc6243 -r means recursive. Deletes:	the directory mybioc6243, all subdirectories,	all files inside

