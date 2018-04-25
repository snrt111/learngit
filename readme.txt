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
