HELLO WORLD! 
"---"表示变动前的文件，"+++"表示变动后的文件。

第二部分，变动的位置用两个@作为起首和结束。

工作目录 vs 暂存区
$ git diff <filename>
意义：查看文件在工作目录与暂存区的差别。如果还没 add 进暂存区，则查看文件自身修改前后的差别。也可查看和另一分支的区别。
https://www.jianshu.com/p/80542dc3164e
暂存区 vs Git仓库
git diff --cached <filename>
意义：表示查看已经 add 进暂存区但是尚未 commit 的内容同最新一次 commit 时的内容的差异。 也可以指定仓库版本：

git commit --dry-run
git add -patch select hunks interactively 

git.exe daemon --verbose --export-all 创建一个 git 服务器

