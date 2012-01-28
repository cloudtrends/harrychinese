Nice Reader
项目初始化
Linux / Mac

    * 安装 virtaulenv: 可使用 easy_install 进行安装。
    * 生成项目环境： virtualenv nicereader 。
    * 启动虚拟环境： source nicereader/bin/active 。
    * 获取项目代码： 进入 nicereader 目录，执行 git clone https://wwq0327@bitbucket.org/wwq0327/nicereader.git ，如果没有git，请先安装。
    * 安装项目所需模块： 进行项目目录 nicereader ， 执行 pip install -r requirements/prj.txt ，等待模块安装完成。

Windows

如何创建一个虚拟环境，可参考这里：

http://www.cnblogs.com/harrychinese/archive/2012/01/09/2317385.html
启动
开发服务器

使用的配置文件是 settings_local.py .

./dev_manage.py runserver
生产服务器

使用的配置文件是 settings.py

./manage.py runserver
服务器
合作

当被管理员添加到合作者后，可以通过下面操作提交代码：

    * 按README所述，创建一个虚拟环境
    * pull 代码到本地
    * 连接并提交

git 基本操作

    * 将远程服务变更同步到本地： git pull (建议每次工作前都操作一次)
    * 跟踪新的修改： git add .
    * 查看更新： git status
    * 查看差异： git diff
    * 提交更新： git commint -m '<这里是修改说明>'
    * 提交更新到远程服务器： git push

git 分支

    * 创建并切换分支： git checkout -b iss53 (iss53为分支名)
    * 切换分支： git checkout master (master为主分支)
    * 分支合并： git merge iss53
    * 删除分支： git branch -d iss53
    * 查看分支： git branch
    * 推送分支到远程服务器： git push origin iss53
    * 删除远程分支： git push origin :iss53

更多操作请看这里： http://progit.org/book/zh/
目录

结构：

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

    * apps 应用都存放在这个目录中，每添加一个新的目录（应用），需要在 settings.py 添加相同名称的应用。
    * templates 为模板存放处，目录名称与 apps 中目录所使用的名称相同。

South数据库变更工具

在Django中，当 models.py 中的字段内容变更后，数据库内容不会发生变化，使用 south 可以让Model中的变化与数据库同步。

python manage.py schemamigration youappname --initial  # youappname目录下面创建一个migrations的子目录（注意！！就算有多个app，也只要initial一个就可以）

python manage.py syncdb                                #初始化数据表等


#以后每次对models更改后，可以运行以下两条命令同步到数据库

python manage.py schemamigration youappname --auto     #检测对models的更改

python manage.py migrate youappnam  #将更改反应到数据库（如果出现表已存在的错误，后面加 --fake）


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
pylogs, 一个单人的博客系统, 
http://code.google.com/p/pylogs/
http://pylogs.googlecode.com/svn/trunk/ 

tmitter, 一个类似twitter的python实现
http://code.google.com/p/tmitter/
http://tmitter.googlecode.com/svn/trunk/


另一个博客 youflog
http://youflog.googlecode.com/svn/trunk/youflog/

django 系列
http://www.danfi.cn/tag/django

Django学习笔记
http://zhoubo.sinaapp.com/?p=575

写第一个Django app 笔记(安装配置)
http://www.cnblogs.com/ubunoon/archive/2008/05/20/pythondjangoinstall.html

Python and django 系列
http://www.cnblogs.com/tenghoo/category/185556.html


django is python系列
http://xlp223.ycool.com 


The Django Book 中文版
 http://djangobook.py3k.cn/2.0/chapter01/

The Django Book 2.0 中文版 chm版本
http://www.ppurl.com/2011/04/the-django-book-2-0-%e4%b8%ad%e6%96%87%e7%89%88.html
 
  
A Django setup using Nginx and Gunicorn
 http://senko.net/en/django-nginx-gunicorn/
 
Django (web framework) on wikipedia
http://en.wikipedia.org/wiki/Django_%28web_framework%29