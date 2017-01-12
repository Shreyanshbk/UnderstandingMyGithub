# 1. Basic Command Line
This tutorial contains unix-based system commands. A command line is a powerful text-based interface to your system that can allow you to run scripts, automate stuffs, handle difficult task, combine simple commands. 

## Understanding the Filesystem
The unix file system is arranged in a tree like fashion. The top most directory is the 'root directory', while the entire tree comprises of other files, folders and directories. This every directory has a parent directory except the root directory. And every directory have child directories except the leaf directories.

## ls
### ls
'$' is the shell prompt that accepts the commands. 'ls' lists all the child directory of the current directory.

### ls -a
This command displays files with a dot in the beginning (.music). This file are generally hidden and not seen with ls. '-a' is an option for ls and modifies the behaviour of ls. 

### ls -l 
lists directories in long format.
#### long format 
The long format lists files in 7 space separated fields.
1. Access rights : Permitted actions on the file.                                    
2. Number of hard links including ('..')- link to parent and link to self ('.'). 
3. File owner's name.                 
4. Groups name that owns the file.     
5. size of file.  
6. Date last modified.  
7. name of the file.

### ls -t
lists in order of time of last modification. 

### ls -alt
This is a combination of option 'a', 'l' and 't' with the ls command and produces the result of all the three.    


## pwd
'pwd' stands for print working directory. It prints the name of the current directory(working directory) you are in.

## cd <argument = path>
'cd' stands for change directory and helps you to switch between directories and gets you to a new working directory provided as the argument to the command. (ex: 'cd movies'). If the arguments are ' ..'. cd takes you one directory up (towards the root) i.e. to the parent of the directory. A complete path to the directory can be provided to cd as argument and cd will take you directly to the directory. 

## mkdir <dir_name>
'mkdir' stands for make directory (same as making a new folder). It makes a new directory as a child to the working directory with the given directory name. 

## touch <filename>
'touch' command is used to make a empty new file in the working directory with the filename and extension provided as argument.

## history
Displays the all the commands types in the session. 

# 2. Tweaking with Command Line

## cp <src/s> <dest>
copies file from the source path to the destination path. The path can just be the filename if copy is done in the working directory. There can be multiple sources used at the same time and cp will copy all to the destination folder.

### cp * <dest> 
copies all the files from the working directory to the destination diractory.

### cp a*.txt <dest>
copies all text files starting with 'a' in the working directory to the destination directory.

## mv <src/s> <dest> or renaming a file
moves files from source to destination. Like 'cp', 'mv' can also move multiple 'src' files to the destination specified by the last argument. if 'mv' is used with a new file name in the destination, it will rename the src file and save it. 

## rm <filename> or rm -r <dir_name>
rm is used to remove file or directory specified by the paths as arguments. For deleting a directory, use '-r' (recursive) option with 'rm'. 'rm' command deletes file permanently from the system. 

# 3. I/O Operations - Redirect

## echo <String>
Will print the string on the command line. This is done as the command will accept the string as standard input and received as standard output.

## Standard Streams
stdin - information inputted in command line. 
stdout - information returned from the process
stderr - error message

## cat <filename>
Displays the contents of the file on the terminal.

## '>'
This is used to redirect the standard output to a file name specified. (ex: echo "Focus is the key to success" > success.txt, cat <filename> > <filename> )

## '>>'
Takes the standard output and appends it to the destination file.

## '<'
Takes standard input from the file specified and the standard output is produced.

## pipe '|'
Pipe can thought like a '.' operator in function chaining. Pipe takes the standard output of a function on the left and passes it as standard input to the function on the right. ex: echo 'print it to file' | cat > xyz.txt   

# 4. Special Commands 
'wc' - command is used to give the lines, words and character count.

'sort' - command used to sort the contents of a file. 

'uniq' - command deletes adjacent occurence of duplicates. To remove all duplicates 'sort' can be piped with uniq. 
Use: uniq <optional_filename -- if there is no stdout> --> removes immediate next duplicates from file or stdout. 

'grep' - stands for global regular expression. Searches for the given pattern in the file.   
--- With an option '-i' grep can be used to make case insensitive search. 
--- With an option '-R'(recursive) grep can search all files in any directory and output the filename along with the pattern containing lines. 
--- With an option '-Rl' (l for files with matches) grep searches for the pattern and results all file names containing the pattern. 
Use : grep <option> Car Cars.txt --> outputs all lines with the pattern Car in it. 


'sed' - takes standard input from file and modifies it based on an expression. 
Use1: sed 's/helicopter/plane' airlines.txt --> replaces plane for helicopter for the first occurences of helicopter in each line. 
Use2: sed 's/helicopter/plane' airlines.txt --> replaces plane for helicopter for all the instances of helicopter in each line of file. 


# 5. Environment
Every new terminal is opened, creates a new session and sets up the environment. Its is possible to configure the environment to support your commands and programs, customize greetings, create variables, common aliases and sharing, etc.

## nano <filename>
nano is the GNU text editor. Its displays a screen to write a file. 'CTRL + O(output) and ENTER' is used to save the file. 'CTRL + X(exit) and clear' to get back to bash. 	CTRL - G opens help in nano. 

## ~/.bash_profile
Start of session loads content of this file. This file name is unique and used to store environment variables settings. '~' represents your home directory. '.' indicates a hidden file 
#### nano ~/.bash_profile --> opens up the file.
#### source ~/.bash_profile --> activates the changes in the file. 

## alias 
alias change="cd" (no spaces between word an =) --> gives new name cd-- must be written in bash_profile and then activate it. 

## Environment Variables
Environment variables are used accross commands and programs to hold information about the enviornment. 
export - helps to reflect this change in all the child process and to persists against programs. 
USER="Shreyanshbk" sets USER environment variable.
HOME is environment variable containing the home address. 
PATH variable stores all the path to directories (mainly /bin) containing script to be excuted by command line. It is possible to customize path variable when adding own scripts. 
'env' --> command lists all the environment variables. 

## PS1=">> "
Sets the command prompt to ">> " from the default "$"



# 6. For windows.
Cygwin is one of the very good command line that gives a Unix like environment to windows.

--- ref : Codecademy Command Line Tutorials.  
