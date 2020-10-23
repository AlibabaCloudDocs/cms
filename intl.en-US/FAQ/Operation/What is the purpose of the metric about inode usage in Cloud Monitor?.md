# What is the purpose of the metric about inode usage in Cloud Monitor?

This topic describes the purpose of the metric about inode usage in Cloud Monitor.

The file system in Linux or UNIX uses inode numbers rather than file names to identify files. File names are aliases of inode numbers. File names are provided only for you to recognize files with ease.

When you open a file based on its file name, the operating system performs the following steps:

1.  Obtains the inode number of the file based on the file name.
2.  Finds the inode based the inode number and retrieves the information that is stored in the inode.
3.  Finds the block where the file resides based on the retrieved information and read the file from the block.

Each file uses an inode. When the inodes of a disk are used up, you cannot create more files on the disk even when the disk still has free space. Therefore, you need to monitor inode usage.

To view the total number of inodes and the number of used inodes for each disk partition, run the `df -i` command.

To view the size of each inode, run the `sudo dumpe2fs -h /dev/hda | grep "Inode size"` command.

