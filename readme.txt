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
