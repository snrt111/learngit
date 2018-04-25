Git is a distributed version control system.
Git is free software. distributed under the GPL.
git log������ʾ���������Զ���ύ��־��
���ǿ��Կ���3���ύ��
�����һ����append GPL��
��һ����update readme file
�����һ����write a readme file
����������Ϣ̫�࣬�����ۻ����ҵģ��������Լ���--pretty=oneline����

$ git log --pretty=oneline
3aa913b04c3cc221a77555ec049a20223da4c52f (HEAD -> master) append GPL
71c9c4a17b818dcc606a15717143a17b26fcc714 update readme file
d3187c743cdb80f1786112e48c07052f10733bdb write a readme file


======================================================================
�鿴�ļ����ݣ�cat readme.txt
����ļ���git add readme.txt
�ύ�ļ����汾�⣺git commit -m "append GPL"
���ʱʹ�ã�git reflog 
���汾�Ż��ˣ�git reset --hard 3628164
���˵���һ���汾��git reset --hard HEAD^
��ʾ�ύ��¼��git log --pretty=oneline
�鿴�������Ͱ汾���������°汾������git diff HEAD -- readme.txt

�������������ļ��ص����һ��git commit��git addʱ��״̬����git checkout -- readme.txt

����1����������˹�����ĳ���ļ������ݣ���ֱ�Ӷ������������޸�ʱ��������git checkout -- file��

����2�����㲻�������˹�����ĳ���ļ������ݣ�����ӵ����ݴ���ʱ���붪���޸ģ�����������һ��������git reset HEAD file���ͻص��˳���1���ڶ���������1������

����3���Ѿ��ύ�˲����ʵ��޸ĵ��汾��ʱ����Ҫ���������ύ���ο��汾����һ�ڣ�����ǰ����û�����͵�Զ�̿⡣


Creating a new branch is quick.

������ϲ���֧
�Ķ�: 999244
�ڰ汾��������Ѿ�֪����ÿ���ύ��Git�������Ǵ���һ��ʱ���ߣ�����ʱ���߾���һ����֧����ֹ��Ŀǰ��ֻ��һ��ʱ���ߣ���Git������֧������֧����master��֧��HEAD�ϸ���˵����ָ���ύ������ָ��master��master����ָ���ύ�ģ����ԣ�HEADָ��ľ��ǵ�ǰ��֧��

һ��ʼ��ʱ��master��֧��һ���ߣ�Git��masterָ�����µ��ύ������HEADָ��master������ȷ����ǰ��֧���Լ���ǰ��֧���ύ�㣺

git-br-initial

ÿ���ύ��master��֧������ǰ�ƶ�һ���������������㲻���ύ��master��֧����ҲԽ��Խ����

 �����Ǵ����µķ�֧������devʱ��Git�½���һ��ָ���dev��ָ��master��ͬ���ύ���ٰ�HEADָ��dev���ͱ�ʾ��ǰ��֧��dev�ϣ�

git-br-create

�㿴��Git����һ����֧�ܿ죬��Ϊ��������һ��devָ�룬�ĸ�HEAD��ָ�򣬹��������ļ���û���κα仯��

�����������ڿ�ʼ���Թ��������޸ĺ��ύ�������dev��֧�ˣ��������ύһ�κ�devָ����ǰ�ƶ�һ������masterָ�벻�䣺

git-br-dev-fd

����������dev�ϵĹ�������ˣ��Ϳ��԰�dev�ϲ���master�ϡ�Git��ô�ϲ��أ���򵥵ķ���������ֱ�Ӱ�masterָ��dev�ĵ�ǰ�ύ��������˺ϲ���

git-br-ff-merge

����Git�ϲ���֧Ҳ�ܿ죡�͸ĸ�ָ�룬����������Ҳ���䣡

�ϲ����֧����������ɾ��dev��֧��ɾ��dev��֧���ǰ�devָ���ɾ����ɾ�������Ǿ�ʣ����һ��master��֧��

git-br-rm

����̫�����ˣ��㿴�ó�����Щ�ύ��ͨ����֧��ɵ���

 ���濪ʼʵս��

���ȣ����Ǵ���dev��֧��Ȼ���л���dev��֧��

$ git checkout -b dev
Switched to a new branch 'dev'
git checkout�������-b������ʾ�������л����൱�������������

$ git branch dev
$ git checkout dev
Switched to branch 'dev'
Ȼ����git branch����鿴��ǰ��֧��

$ git branch
* dev
  master
git branch������г����з�֧����ǰ��֧ǰ����һ��*�š�

Ȼ�����ǾͿ�����dev��֧�������ύ�������readme.txt�����޸ģ�����һ�У�

Creating a new branch is quick.
Ȼ���ύ��

$ git add readme.txt 
$ git commit -m "branch test"
[dev fec145a] branch test
 1 file changed, 1 insertion(+)
���ڣ�dev��֧�Ĺ�����ɣ����ǾͿ����л���master��֧��

$ git checkout master
Switched to branch 'master'
�л���master��֧���ٲ鿴һ��readme.txt�ļ����ղ���ӵ����ݲ����ˣ���Ϊ�Ǹ��ύ����dev��֧�ϣ���master��֧�˿̵��ύ�㲢û�б䣺

git-br-on-master

���ڣ����ǰ�dev��֧�Ĺ����ɹ��ϲ���master��֧�ϣ�

$ git merge dev
Updating d17efd8..fec145a
Fast-forward
 readme.txt |    1 +
 1 file changed, 1 insertion(+)
git merge�������ںϲ�ָ����֧����ǰ��֧���ϲ����ٲ鿴readme.txt�����ݣ��Ϳ��Կ�������dev��֧�������ύ����ȫһ���ġ�

ע�⵽�����Fast-forward��Ϣ��Git�������ǣ���κϲ��ǡ����ģʽ����Ҳ����ֱ�Ӱ�masterָ��dev�ĵ�ǰ�ύ�����Ժϲ��ٶȷǳ��졣

��Ȼ��Ҳ����ÿ�κϲ�����Fast-forward�����Ǻ���ὲ������ʽ�ĺϲ���

�ϲ���ɺ󣬾Ϳ��Է��ĵ�ɾ��dev��֧�ˣ�

$ git branch -d dev
Deleted branch dev (was fec145a).
ɾ���󣬲鿴branch����ֻʣ��master��֧�ˣ�

$ git branch
* master
��Ϊ�������ϲ���ɾ����֧�ǳ��죬����Git������ʹ�÷�֧���ĳ�����񣬺ϲ�����ɾ����֧�����ֱ����master��֧�Ϲ���Ч����һ���ģ������̸���ȫ��

С��
Git��������ʹ�÷�֧��

�鿴��֧��git branch

������֧��git branch <name>

�л���֧��git checkout <name>

����+�л���֧��git checkout -b <name>

�ϲ�ĳ��֧����ǰ��֧��git merge <name>

ɾ����֧��git branch -d <name>


����������֮��ʮ֮�˾ţ��ϲ���֧����Ҳ����һ����˳�ġ�

׼���µ�feature1��֧���������ǵ��·�֧������

$ git checkout -b feature1
Switched to a new branch 'feature1'
�޸�readme.txt���һ�У���Ϊ��

Creating a new branch is quick AND simple.
��feature1��֧���ύ��

$ git add readme.txt 
$ git commit -m "AND simple"
[feature1 75a857c] AND simple
 1 file changed, 1 insertion(+), 1 deletion(-)
�л���master��֧��

$ git checkout master
Switched to branch 'master'
Your branch is ahead of 'origin/master' by 1 commit.
Git�����Զ���ʾ���ǵ�ǰmaster��֧��Զ�̵�master��֧Ҫ��ǰ1���ύ��

��master��֧�ϰ�readme.txt�ļ������һ�и�Ϊ��

Creating a new branch is quick & simple.
�ύ��

$ git add readme.txt 
$ git commit -m "& simple"
[master 400b400] & simple
 1 file changed, 1 insertion(+), 1 deletion(-)
���ڣ�master��֧��feature1��֧���Զ��ֱ����µ��ύ�������������

git-br-feature1

��������£�Git�޷�ִ�С����ٺϲ�����ֻ����ͼ�Ѹ��Ե��޸ĺϲ������������ֺϲ��Ϳ��ܻ��г�ͻ���������Կ���

$ git merge feature1
Auto-merging readme.txt
CONFLICT (content): Merge conflict in readme.txt
Automatic merge failed; fix conflicts and then commit the result.
��Ȼ��ͻ�ˣ�Git�������ǣ�readme.txt�ļ����ڳ�ͻ�������ֶ������ͻ�����ύ��git statusҲ���Ը������ǳ�ͻ���ļ���

$ git status
# On branch master
# Your branch is ahead of 'origin/master' by 2 commits.
#
# Unmerged paths:
#   (use "git add/rm <file>..." as appropriate to mark resolution)
#
#       both modified:      readme.txt
#
no changes added to commit (use "git add" and/or "git commit -a")
���ǿ���ֱ�Ӳ鿴readme.txt�����ݣ�

Git is a distributed version control system.
Git is free software distributed under the GPL.
Git has a mutable index called stage.
Git tracks changes of files.
<<<<<<< HEAD
Creating a new branch is quick & simple.
=======
Creating a new branch is quick AND simple.
>>>>>>> feature1
Git��<<<<<<<��=======��>>>>>>>��ǳ���ͬ��֧�����ݣ������޸����º󱣴棺

Creating a new branch is quick and simple.
���ύ��

$ git add readme.txt 
$ git commit -m "conflict fixed"
[master 59bc1cb] conflict fixed
���ڣ�master��֧��feature1��֧�������ͼ��ʾ��

git-br-conflict-merged

�ô�������git logҲ���Կ�����֧�ĺϲ������

$ git log --graph --pretty=oneline --abbrev-commit
*   59bc1cb conflict fixed
|\
| * 75a857c AND simple
* | 400b400 & simple
|/
* fec145a branch test
...
���ɾ��feature1��֧��

$ git branch -d feature1
Deleted branch feature1 (was 75a857c).
������ɡ�

С��
��Git�޷��Զ��ϲ���֧ʱ���ͱ������Ƚ����ͻ�������ͻ�����ύ���ϲ���ɡ�

��git log --graph������Կ�����֧�ϲ�ͼ��

