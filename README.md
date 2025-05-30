# Linux Commands
### Basic Commands
- `pwd` : Present Work Directory.
- `whoami` : Shows current logged-in user.
- `date` : Shows current date and details. e.g.: `Tuesday 27 May 2025 02:39:09 AM IST`
  * `date +%D` shows only date `05/27/25`
  * `date +%H:+%M` shows hours and minutes and so on...
- `ls` : lists files in the current directory.
   * use `-lt` to get list of files with details,
   * `-ltr` to get reverse order of latest modified files,
   * use `-lh` to et file size in human readable form.
   * `-R` will list file in sub-directories as well.
   * `-a` will show hidden files as well.
   * `-al` will show details as well like permissions, owner etc.
- `clear` : clears the terminal ofc. or use `ctrl + l`
### Working with Files
- `cat filename` : Displays content of file.
  * `cat > filename` created the file.
  * `cat filename1 filename2 > filename3` joins two files and copies its output in a new file. 
- `less filename` : Used to search certain content in a file. Opens a new editor, just type `/search-key` to search anything from top to bottom.
    * Type `n` for next occurrence of the search-key.
    * Type `ctrl + g` to get to the bottom of the file.
    * Type `p` to get to the first line.
    * To search from bottom to top use `?search-key` to search.
    * Enter `q` to quit.
- `more filename` : to view the content of a file page by page. Prints in the content of the file in the terminal itself. No new editor is opened. If we press `↓` notice how contents change page by page.
- `touch filename` : to create a file.
- `rm filename` : Removes/Deletes a file.
- `vi filename` : Used to create as well as edit a file
  * Enter `i` to insert something.
  * Enter `Esc` to Escape.
  * Enter `shift + :` to save file.
  * After `:` enter `wq` to save and exit.
- `nano filename` : Esay alternative to vi command.
- `cp fileA fileB` : Copies the content of fileA and makes another file fileB, and paste the content there.
### Working with Directories
- `mkdir dirname` : make directory.
- `rmdir` or `rm -rf dirname`: remove directory.
  * `rm -r` removes a directory and all its files.
- `cd dirname/dirname...` : change directory, jumping to new directory(s).
  * `cd ../..` : change directory, removing previous directory(s).
  * `cd` to goto root directory
  * `cd-` to go to the previous directory. 
- `cp filename /destination/path` : copy and paste files from one folder to another.
  * `../folder` refers to a folder in previous folder.
  * `.` refers to the current folder.
- `mv filename /destination/dir` : Cut-paste a file from the current dir to the destination.
- `mv fileA fileB` : Renames fileA to fileB.
### Head and Tail Commands
- `head -lines filename` : if lines=5, it will output top 5 lines.
- `tail -lines filename` : Displays bottom 5 lines.
### Sort Commands
- `sort filename` : sorts the content of the file.
- `sort -r filename` : sorts in reverse fashion.
- `sort filename | uniq` : gives unique entries, removing duplicates.
- `split -l 3 filename` : splits the content of the file into 3-3 lines files.
### Grep(Global Regular Expression Print), Egrep Commands
- `grep word filename` or `grep "word" filename` : searched the occurrences of word and prints it on terminal. More visibility thn less command.
- `grep -i word filename` : -i removes case sensitivity.
  * `-v` : print every line except the word.
  * `-c` : if you want count of the occurences.
  * `-w` or `-iw` : to match the exact match. normal grep will give same output for "word" and :wor", -w doesnot.
  * `-n` : gives line no. of the word.
- `grep -i word file1 file2 ...` : search accross multiples files and tells in which files.
  * `-h` : to supress the file names of multiple files.
  * `-e word1 -e word2` or `egrep word1|word2....`: search for multiple words.
  * `-l` : to find only file name where word is located.
  * `grep -f keyword.txt filename1 filename2 ....` or `grep -f keyword.txt * `: to get the keyword/pattern from a afile and match with another file.
- `grep ^100 filename` : give every line starting with 100.
- `grep er$ ` : endes with er.
- `grep -R word dirA` : searches in all files in dirA.
- `-q` : quick search does not return anything.
- `ls grep -i abc` : returns all files starting with abc.
- `ps -ef | grep ngnix` : searches ngnix in processess.
- `pgrep ngnix` : returns the process ID.
- `fgrep hello.world filename` : considers . as a normal ecpression not as a regular exp.
- `zgrep word file.zip` : search in zip file.
- `pdfgrep word file.pdf` : search in pdf file.
### Additional commands

- `scp /local/file/path user@<ip-config>:/destination/path` : Secure Copy Protocol (SCP) used for file transfer between a local and remote server, or between two remote servers, using ssh.



