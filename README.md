exttools
========

Some tools for reading ext2/ext3/ext4 filesystem images.

I use these mostly to extract files from android system images.

EXAMPLE
=======

This will export the entire filesystem to 'savedir'

    ext2rd  system.img  ./:savedir

BUILD
=====

As a prerequisite, install `autoreconf` and `libboost-all-dev`.

sudo apt-get install autoconf

sudo apt-get install libboost-all-dev


Then run the following commands:

```
./autogen.sh
./configure
cd itslibs/src; g++ -v -c -I .. -std=c++11 stringutils.cpp; cd ../..
#add "-std=c++11" to Makefile/CXXFLAGS
make
```

ext2rd
======


    Usage: ext2rd [-l] [-v] <fsname> [exports...]
         -l       lists all files
         -B       open as block device
         -d       verbosely lists all inodes
         -o OFS1/OFS2  specify offset to efs/sparse image
         -b from[-until]   hexdump blocks
       #123       hexdump inode 123
       #123:path  save inode 123 to path
       ext2path   hexdump ext2fs path
       ext2path:path   save ext2fs path to path
       ext2path/:path  recursively save ext2fs dir to path
    note: ext2path must not start with a slash
    note2: /dev/rdiskNN is much faster than /dev/diskNN

ext2dump
========

    Usage: ext2dump [-l] [-d] <fsname> [exports...]
         -l       lists all files
         -d       verbosely lists all inodes
         -o OFS1/OFS2  specify offset to efs/sparse image
         -b from[-until]   hexdump blocks
       #123       hexdump inode 123
       #123:path  save inode 123 to path
       ext2path   hexdump ext2fs path
       ext2path:path   save ext2fs path to path
       ext2path/:path  recursively save ext2fs dir to path


AUTHOR
======

Willem Hengeveld <itsme@xs4all.nl>

