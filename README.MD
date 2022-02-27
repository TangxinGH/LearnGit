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

git reset file 对应 用来撤销最后一次git add : 第一次add ,第二次add： git reset 使用staged 区会恢复到第一次add状态?目前看到的是暂存区被清空了。从history 到stage的 对应commit
git checkout file 对应 git add files 
-p
Revision Graph 刷新不起作用https://gitlab.com/tortoisegit/tortoisegit/-/issues/1663
git commit --amend 将父亲节点一起提交

有人在main分支上新提交了。
detached HEAD

git reset  什么选项都不跟：指向提交。如果--hard  reset HEAD, index and working tree 。 如 git reset HEAD-3回到三个cOmmit之前 --hard 工作目录会更新
  --hard                reset HEAD, index and working tree 这里的index指的是暂存区

解决冲突后 git add .\README.MD 到stage 叹号就不见了
commit;

所以什么情况下会发生冲突

https://developpaper.com/principle-of-git-merge-recursive-three-way-merge-algorithm/#:~:text=If%20the%20relative%20base%20of,base%20as%20the%20final%20result.&text=The%20above%20is%20the%20basic,%E2%80%9Cthree%2Dway%20merge%E2%80%9D.

http://marklodato.github.io/visual-git-guide/index-zh-cn.html

kiss 原则： 编码之前解决问题；问题拆分足够小。尽量简单

这里插入一行
三路合并s
同一文件修改在下面插入一行
git merge --abort 终止合并

add new line

三路合并只要有两路相同就可以合并：基于块
如果Git在寻找共同祖先时，在参与合并的两个分支上找到了不只一个满足条件的共同祖先，它会先对共同祖先进行合并，建立临时快照。然后，把临时产生的“虚拟祖先”作为合并依据，再对分支进行合并。
https://morningspace.github.io/tech/git-merge-stories-2/