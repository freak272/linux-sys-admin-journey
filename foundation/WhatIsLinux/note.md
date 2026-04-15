The true structure of linux

what is linux?
linux is a combination of GNU tools that allow the user to interact with the system and the LINUX kernel which is the
core that manages the hardware and system resources.
kernel's responsibilities.
1. CPU management
   -deciding which process runs
   -sheduling tasks
2. Memory management
   -allocating RAM/memory space to processes
   -isolating processes from each other
3. Device management
   -disks management
   -keyboard managemnt
   -network management
4. Process management
   -creating processes
   -terminating processes
   -tracking processes
the kernel is the only one that communicates with hardware.
what is a linux os ?
kernel and GNU tools make up a linux os.
example of GNU tools :
1. core utilities :ls, cp, rm. cat, mkdir, etc
2. the shell, example - Bourne again shell (BASH)
3. Development tools: example - GCC (GNU compiler collection)
4. text editors : example - Emacs and nano
what is a linux distribution ?
it is a collection of the linux kernel, GNU tools, libraries and additional software packaged together to form
a usable operating system.
how they connect or work together :
  user & appications
  (firefox, VS code)
    ↓(system call)
   shell (bash)
   (interprets commands)
     ↓(sys call)
   kernel
   (cpu scheduler, process management,
   device management and disk management ) 
      ↓(hardware interfaces)
   hardware
   (CPU, RAM, Disk, Network, etc )
   
programs do not communicate directly with the hardware they must go through the kernel
What would happen if the was no kernel ?
1. programs would hog the CPU.
2. programs would write into memory space being used by other programs.
3. the would be no multitasking
4. no security boundries
5. no device coordination
