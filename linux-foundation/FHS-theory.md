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
 1.  * /  root directory - it is the entry point for file access.
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

2, /etc - is the central place for configurations.
        function : stores configuration files that define how the system and services operate.
                  -this are usually : * text files
                                      * are read at startup or when a service starts/runs
                  -example : Network settings, user info, service configs (like SSH, cron etc)
        role :
              * control center of the system -programs dont hardcode behavior they read from etc meaning
              /etc tells programs and the system how to behave.
              * system wide configurations - affect all users. eg /etc/ssh/ssh_config - affects all SSH connections.
              * boot configs - the system reads critical files from /etc when starting.
    /etc simplifies how a user can modify behaviour of the system by grouping allconfigurations in one place making it simple
    for users to navigate when they need to modify the system.
  
---------------------------------------------------
3. /bin - contains essential user commands required for the system to function and operate.
          contains essential user command binaries required for basic system operation, especially during boot and recovery
     function : stores fundamental executable programs (binaries) that are required or needed by all users.
               this are actual commands that are executed by user inside the shell.
   example : ls, cd, mv, etc
   role : * they provide core command line functionality that helps users to navigate they system.

----------------------------------------------------
4. /sbin - contains essential system administration binaries used managing, reparing and controlling the system,
           typically by the root user.
        function : contains critical executables used for system administration and low-level operations.
                  they interact directly with the system state.
   role : * system control layer.
          * administrative use.
          * they are required during boot and recovery ( maintance of the system ).
   /bin - general commands.
   /sbin - administrative commands.

----------------------------------------------------
5.









