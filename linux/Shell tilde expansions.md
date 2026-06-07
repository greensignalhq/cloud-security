## Shell tilde expansions

I thought that [~] was a flag but it is not. Even in the way that it effects the behavior of a command line.

# ~

'''bash
cd ~/greenray
'''

This tilde modifes the file path before the command is executed. In this case the command [cd] changes shell working directory, while the tilde [~] expands to the user's home directory.


# Note

- unlike flags, which are command-line parameters (options) that modify command behavior, the tilde [~] is expanded by the shell into a [file path] before the command is executed. 

- It is not passed to the program as an argument or option.
