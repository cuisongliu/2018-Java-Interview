## 硬链接与软链接的区别
每个文件都是创建了一个指针指向inode（代表物理硬盘的一个区块），可以通过`ls -i`查看。  
硬链接是创建另一个文件，也通过创建指针指向inode。当你删除一个文件/硬链接时，它会删除一个到底层inode的指针。当inode的所有指针都被删除时，才会真正删除文件。  
软连接是另外一种类型的文件，保存的是它指向文件的全路径，访问时会替换成绝对路径

## 查看某个进程中的线程
`ps -T -p <pid>`

## 查看某个文件夹中每个文件夹的大小
`du --max-depth=1 -h`