# Filesystems

## Filesystem Structure

The base of the filesystem in Unix-based operating systems (like Linux and Mac OS, which we will focus on in this class) is indicated with a single forward slash (`/`) and is known as the filesystem's root. The location of all files and folders can be written with a __path (i.e., address) that starts at the root__. Folders are hierarchical, so paths to highly nested folders will need to include all parent folders.
  
![ExampleMacFilesystem](https://github.com/IntroPhylogenomics/ComputingFundamentals/blob/master/exampleFilesystem.png)
  
For instance, in the example above, the location of the `Users` folder can be written as `/Users/`, the location of the home directory for `UserName` can be be written as `/Users/UserName/`, and the location of their desktop folder can be written as `/Users/UserName/Desktop/`.
  
## Absolute v Relative Paths
  
While the addresses for all files and folders can be written with paths that start at the root, it's sometimes cumbersome to do so. For instance, if you want to reference the parent folder of the folder you're in, it would be easier to provide the address that way (i.e., the parent of the folder I'm in), rather than write out the full path from the root. Paths that provide locations this way are known as __relative paths__. These are in contrast to __absolute paths__ that always start at the root, `/`. Relative paths simply indicate where to look based on where you are. For instance, if your working directory is already `/Users/UserName/`, then you can reference the user's desktop folder by just writing `Desktop`. There are special symbols used to indicate the folder you're in (i.e., the current working directory) - `.` - and the parent folder of the current working directory - `..`. Another commonly used special symbol is `~`, which indicates the home directory of the user.


> __Practice Exercise__
>
> If your current working directory is `/Users/UserName/`, write the absolute paths for the 
> directories referenced by the following relative paths.
>
> `Desktop`=> pathway would be /User/username/desktop
>>> this is an absolute pathway since it does not begin with '/' 

> `../Guest/` = '..' = parent folder of the directory currently working in so the absolute pathway would be /User/Guest
>>> this is a relative pathway since it starts with '/'

> `~/Library/`= '~' is a trick the '~' has a '/' built in so this is an absolute pathway. The pathway would just be /Library/
>
> `../../` = we are already in /user/username so going back to the parent directory 2x would just put us at the root filesystem??
  
## Hidden Files and Folders

In Unix-based filesystems, you can keep some files and folders from showing up by default if you add a period, `.`, to the beginning of their names. These files are hidden. One common use for hidden files is to specify configuration settings for a program or system. These hidden files are usually stored in a user's home directory (e.g., `/Users/UserName/`). They can be revealed by listing a directory's contents using the `-a` flag - `ls -a`.

#
Class Notes/Commands

'ls a' - shows entire directory contents 

'cat' - opens txt file but cannot edit
> so in order to open the content of the files you first do 'ls -a" find the file you want on the catalog and then type 'cat [INSERT FILE NAME]' and then you can open the file damn thats crazy...

Theres also permissions codes that have a series of 10 numbers which are a series of dashes and letters

These permissions can look like a range of different codes but they all have the '-' and the three letters'd''r''x''w' in common

> 'd' usually indicates that it is a directory
> '-' indicates that it is a file within the directory
>'r' who has permission to read the file
>'x' who has permission to execute the file
>'w' who can edit the file 
