# FUSE_OSLab
Built a new user-level file system to understand how file systems work in Linux.

# Steps

   1. Install fuse
   2. Modify the strings in fuse1.c
   3. Compile using gcc fuse1.c -o fuse1 -g 'pkg-config fuse --cflags --libs'
   4. Create mount dir using mkdir <name>
   5. Run fuse using ./fuse1 -f <name>
   6. Change dir cd <name>
   7. Do your things

# FUSE API callbacks Implemented
   1. getattr
   2. open
   3. read
   4. readdir
   
# getattr
   1. if the value of path equals to root /, we declare it as a directory and return.
   2. if the value of path equals to filepath /file, we declare it as a file and explicit its size and then return.
   3. Otherwise nothing exists at the given path, and we return -ENOENT.
