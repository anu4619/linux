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
- `clear` : clears the terminal ofc. or use `ctrl + l`
### Working with Files
- `cat filename` : Displays content of file.
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
- `cp fileA fileB` : Copies the content of fileA and makes another file fileB and paste the content there.
### Working with Directories
- `mkdir dirname` : make directory.
- `rmdir` or `rm -rf dirname`: remove directory.
- `cd dirname/dirname...` : change directory, jumping to new directory(s).
- `cd ../..` : change directory, removing previous directory(s).
- `cp filename /destination/path` : copy and paste files from one folder to another.
  * `../folder` referes to a folder in previous folder.
  * `.` refers to the current folder.
- 
### Additional commands

- `scp /local/file/path user@<ip-config>:/destination/path` : Secure Copy Protocol (SCP) used for file transfer between a local and remote server, or between two remote servers, using ssh.



