Git is a distributed version control system.
Git is free software. distributed under the GPL.
git log命令显示从最近到最远的提交日志，
我们可以看到3次提交，
最近的一次是append GPL，
上一次是update readme file
最早的一次是write a readme file
如果嫌输出信息太多，看得眼花缭乱的，可以试试加上--pretty=oneline参数

$ git log --pretty=oneline
3aa913b04c3cc221a77555ec049a20223da4c52f (HEAD -> master) append GPL
71c9c4a17b818dcc606a15717143a17b26fcc714 update readme file
d3187c743cdb80f1786112e48c07052f10733bdb write a readme file


======================================================================
查看文件内容：cat readme.txt
添加文件：git add readme.txt
提交文件到版本库：git commit -m "append GPL"
后悔时使用：git reflog 
按版本号回退：git reset --hard 3628164
回退到上一个版本：git reset --hard HEAD^
显示提交记录：git log --pretty=oneline
查看工作区和版本库里面最新版本的区别：git diff HEAD -- readme.txt

撤销命令（让这个文件回到最近一次git commit或git add时的状态）：git checkout -- readme.txt

场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。

场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD file，就回到了场景1，第二步按场景1操作。

场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。
