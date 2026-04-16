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
   * / -- root directory 
