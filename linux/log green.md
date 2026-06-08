## green log

Welcome to my green log. This is where I share my experience, beyond the shell & random things relative to linux.

# 1
I was trying to screenshot my shellwork coming from using a windows os. Obviously not the same os keyboard shortcut. Learning by doing, & reapplying what I knew to what I need to do now. settings-keyboard-keyboard shortcut, rerouted Fkey 1,2,3 keys to screenshot. Problem solved.

- [gnome-screenshot] in modern Ubuntu versions (22.04 and later), the standalone gnome-screenshot application was removed and replaced by a built-in GNOME Shell extension. 

Storage: Images are saved to ~/Pictures/Screenshots/ by default.

# 2

With each .md, and or notes screenshot my shell to show work. SEEing and DOing is doing & seeing. Helps me grasp and implement concepts.

text editors are lightweight and swift. help keep the modification speed, thought process speed balanced.

destination is important even with explaining how something works. There is always a destination.

spellcheck can cripple workforce

eversince I switched from windows to ubuntu, I am learning alot more.

# 3

Directories are just doors; it is what my purpose is with the access that gives commands context.

Ubuntu won't let me move a screenshot from ~ to a desktop folder

- Explanation

The issue likely stems from GNOME Shell’s hardcoded screenshot behavior in recent Ubuntu versions (20.04+), where the default screenshot tool ignores gsettings configurations and forces saves to the $HOME/Pictures directory.  Because the file is created by the system daemon, you may encounter permission issues or the file may not appear immediately in the source folder if the save path is misconfigured

In modern Ubuntu (22.04 and later), the system uses a specific sub-directory logic that ignores the general Pictures setting for screenshots. 

- Working Work Around

1. Remove the default subfolder

'''bash
rm -rf ~/Pictures/Screenshots
'''

2. Create a symbolic link named Screenshots that points directly to the Pictures folder

'''bash
ln -s ~/Pictures ~/Pictures/Screenshots
'''
- Result : When the system tries to save to [ ~/Pictures/Screenshots ] , it will actually drop file to [ Desktop ]. 

In modern Ubuntu (22.04 and later), the system uses a specific sub-directory logic that ignores the general Pictures setting for screenshots. 

at this point I am now trying to move a .png file using [ mv ] to a git folder on my desktop monitored by [GITKRAKEN]. Due

'''bash
sudo apt-get update
'''

'''bash
sudo apt-get install git-lfs
'''

'''bash
git lfs intall
'''

'''bash
chmod +w ~/Pictures/Screenshots/fix.png
'''

'''bash
mv ~/Pictures/Screenshots/fix.png ~/Desktop/cloud-security/linux
'''

# Simple Breakdown

1. The Hidden Rule: The repo’s .gitattributes file told Git: "Treat PNGs as special binary files. If they aren't explicitly 'locked' by a user, make them Read-Only to prevent accidents."

2. The Problem: Without git-lfs installed, your terminal didn't know how to handle this rule. GitKraken likely flagged the file as "in use" or "protected," and the OS enforced the Read-Only status, blocking the mv command.

3. The Fix: Installing git-lfs and running git lfs install taught your system how to read those rules. It likely automatically corrected the file permissions (making it writable) or allowed GitKraken to properly release its lock, enabling the move.

In short: The .txt file had standard permissions, but the .png was waiting for the LFS tool to unlock it.


ngl this was difficult for me it took me a few hours to wrap my head around the issue because it was layered. Not only did i have to move the screenshot save to the desktop (while tricking it) but chmod file permissions for moving .png files through git folders. with some research and trial/error I got it done. check ubuntuscreenshotsavelocationfix.png & gitkrakenpnglockfix.png for the shellshot.

shellshot - a screenshot of shellcode.

# 4

Using brace expansion for the first time to move multiple pngs
mv -v -- *.png /path/to/new/folder/

while pasting some oldcode into shell, while pressing up and down arrows (after pressing the right arrow to solidify paste, but before using left arrow to push cursor back to where I want to change file name) it switched between an array of old lines I just typed into the command line how?

Spaces between commands matter! I was getting ssh configured, and the space between the url and command made output display usage instead of execution.
