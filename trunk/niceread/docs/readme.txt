Nice Reader
��Ŀ��ʼ��
Linux / Mac

    * ��װ virtaulenv: ��ʹ�� easy_install ���а�װ��
    * ������Ŀ������ virtualenv nicereader ��
    * �������⻷���� source nicereader/bin/active ��
    * ��ȡ��Ŀ���룺 ���� nicereader Ŀ¼��ִ�� git clone https://wwq0327@bitbucket.org/wwq0327/nicereader.git �����û��git�����Ȱ�װ��
    * ��װ��Ŀ����ģ�飺 ������ĿĿ¼ nicereader �� ִ�� pip install -r requirements/prj.txt ���ȴ�ģ�鰲װ��ɡ�

Windows

��δ���һ�����⻷�����ɲο����

http://www.cnblogs.com/harrychinese/archive/2012/01/09/2317385.html
����
����������

ʹ�õ������ļ��� settings_local.py .

./dev_manage.py runserver
����������

ʹ�õ������ļ��� settings.py

./manage.py runserver
������
����

��������Ա��ӵ������ߺ󣬿���ͨ����������ύ���룺

    * ��README����������һ�����⻷��
    * pull ���뵽����
    * ���Ӳ��ύ

git ��������

    * ��Զ�̷�����ͬ�������أ� git pull (����ÿ�ι���ǰ������һ��)
    * �����µ��޸ģ� git add .
    * �鿴���£� git status
    * �鿴���죺 git diff
    * �ύ���£� git commint -m '<�������޸�˵��>'
    * �ύ���µ�Զ�̷������� git push

git ��֧

    * �������л���֧�� git checkout -b iss53 (iss53Ϊ��֧��)
    * �л���֧�� git checkout master (masterΪ����֧)
    * ��֧�ϲ��� git merge iss53
    * ɾ����֧�� git branch -d iss53
    * �鿴��֧�� git branch
    * ���ͷ�֧��Զ�̷������� git push origin iss53
    * ɾ��Զ�̷�֧�� git push origin :iss53

��������뿴��� http://progit.org/book/zh/
Ŀ¼

�ṹ��

(nice)[wyatt@wyatt nice]$ tree -L 2 nicereader/
nicereader/
|-- apps
|   `-- __init__.py
|-- conf
|   |-- env
|   |-- git
|   `-- tools
|-- dev_manage.py
|-- __init__.py
|-- manage.py
|-- media
|   |-- css
|   |-- images
|   |-- js
|   `-- uploads
|-- README
|-- requirements
|   `-- prj.txt
|-- settings_local.py
|-- settings.py
|-- templates
|   `-- base.html
`-- urls.py

    * apps Ӧ�ö���������Ŀ¼�У�ÿ���һ���µ�Ŀ¼��Ӧ�ã�����Ҫ�� settings.py �����ͬ���Ƶ�Ӧ�á�
    * templates Ϊģ���Ŵ���Ŀ¼������ apps ��Ŀ¼��ʹ�õ�������ͬ��

South���ݿ�������

��Django�У��� models.py �е��ֶ����ݱ�������ݿ����ݲ��ᷢ���仯��ʹ�� south ������Model�еı仯�����ݿ�ͬ����

python manage.py schemamigration youappname --initial  # youappnameĿ¼���洴��һ��migrations����Ŀ¼��ע�⣡�������ж��app��ҲֻҪinitialһ���Ϳ��ԣ�

python manage.py syncdb                                #��ʼ�����ݱ��


#�Ժ�ÿ�ζ�models���ĺ󣬿�������������������ͬ�������ݿ�

python manage.py schemamigration youappname --auto     #����models�ĸ���

python manage.py migrate youappnam  #�����ķ�Ӧ�����ݿ⣨������ֱ��Ѵ��ڵĴ��󣬺���� --fake��


Django==1.3.1
Markdown==2.1.0
PIL==1.1.7
South==0.7.3
django-debug-toolbar==0.9.2
django-guardian==1.0.3
django-pagination==1.0.7
django-tagging==0.3.1
django-userena==1.0.2
douban-python==0.3.0
easy-thumbnails==1.0-alpha-21
gdata==2.0.16
ipython==0.12
simplejson==2.3.2
wsgiref==0.1.2



===================
pylogs, һ�����˵Ĳ���ϵͳ, 
http://code.google.com/p/pylogs/
http://pylogs.googlecode.com/svn/trunk/ 

tmitter, һ������twitter��pythonʵ��
http://code.google.com/p/tmitter/
http://tmitter.googlecode.com/svn/trunk/


��һ������ youflog
http://youflog.googlecode.com/svn/trunk/youflog/

django ϵ��
http://www.danfi.cn/tag/django

Djangoѧϰ�ʼ�
http://zhoubo.sinaapp.com/?p=575

д��һ��Django app �ʼ�(��װ����)
http://www.cnblogs.com/ubunoon/archive/2008/05/20/pythondjangoinstall.html

Python and django ϵ��
http://www.cnblogs.com/tenghoo/category/185556.html


django is pythonϵ��
http://xlp223.ycool.com 


The Django Book ���İ�
 http://djangobook.py3k.cn/2.0/chapter01/

The Django Book 2.0 ���İ� chm�汾
http://www.ppurl.com/2011/04/the-django-book-2-0-%e4%b8%ad%e6%96%87%e7%89%88.html
 
  
A Django setup using Nginx and Gunicorn
 http://senko.net/en/django-nginx-gunicorn/
 
Django (web framework) on wikipedia
http://en.wikipedia.org/wiki/Django_%28web_framework%29