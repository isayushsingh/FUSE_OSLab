# FUSE_OSLab
Built a new user-level file system to understand how file systems work in Linux.

Steps

    Install fuse
    Modify the strings in fuse1.c
    Compile using gcc fuse1.c -o fuse1 -g 'pkg-config fuse --cflags --libs'
    Create mount dir using mkdir <name>
    Run fuse using ./fuse1 -f <name>
    Change dir cd <name>
    Do your things

