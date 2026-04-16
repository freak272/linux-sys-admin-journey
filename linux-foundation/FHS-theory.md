Linux filesystem hierarchy standard (FHS) - theory
-----------------------------------------------------
in linux everyuthing is a file, it is a designed principle in linux where 
devices, processes and resources are represented as files. FHS defines how those 
files are organized in the filesystem.

-----------------------------------------------------

what is FHS ?
FHS (filesystem hierarchy standard) is a reference that defines the structure 
and layout of directories in linux and unix-like operating systems.
FHS functions :
1. FHS defines where system files go.
2. where user files go
3. where programs store data, configurations, logs etc are stored.

this ensures that :
* different distros behave consistently
* system admins can navigate any system confidently
* software knows where to read/write data.

-----------------------------------------------------
important directories in the filesystem :
   * /  root directory - it is the entry point for file access.
                       - the kernel uses it as the base of the filesystem tree.
                       - all paths begin from it /
     funtion : acts as the top level directory that connects all files and directories into a single
     unified structure.
     roles it plays :
                     * anchor for the filesystem.
                     * mount point foundation
                     * reference point for all paths : there are always two types of paths - absolute path starts from /
                                                       and relative path starts from the current working dirctory
/ is the logical root of the entire operating system : even if the are multiple disks they are always mounted into /.

---------------------------------------------------













