## File System Basics

# touch

'''bash
touch
'''

This creates a new empty file. & Overwrites timestamp of prexisting file only.

# mkdir

'''bash
mkdir greendir
'''

this command makes directories.

# rm

'''bash
rm -i newtext.file
'''

This command removes files; flag/option [ -i ] prompts your for confirmation before command is executed.

# rmdir

'''bash
rmdir 



# mv

'''bash
mv dir1 dir2 dir3 /path/to/destination/
'''
You can use [mv] to move multiple directories at once.

syntax mv [source_directory] [destination_directory].

# Useful flags with [ mv ]

-i: Prompt before overwriting an existing file or directory. 
-n: Do not overwrite an existing file. 
-f: Force overwrite without prompting. 
-v: Verbose mode, showing each file as it is moved.


# remember
- If destination directory does not exist, mv will rename the source directory to the destination name.

- Becareful with flags.

- [mv] renaming or relocating the folder without creating duplicates.

