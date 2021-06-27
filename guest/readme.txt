签到系统部署步骤：
1. 复制guest目录到d盘根目录.

2. 使用命令安装如下包: 
pip install django==1.10.3   
pip install django-bootstrap3==11.0.0

3. 进入guest目录下，修改配置文件guest\settings.py，将其中的mysql数据库密码，改成自己系统的数据库密码后保存即可，
另外若端口号不是默认的3306,则改成你自己修改后的端口号.

4. 使用navicat连接mysql数据库，连接成功后创建一个名为guest_dev的数据库, 创建后双击打开它，再选中它，点击右键菜单中的执行sql文件，
弹出弹窗后，进入guest目录下的sql目录，选中guest.sql文件，点击执行后，出现含有“successfully”的提示后，
关闭弹窗，打开guest_dev数据库，选中表，右键菜单点击刷新，即可看到表已导入进数据库.

5. 启动服务，命令行进入项目目录guest下，若系统就一个python3版本，输入命令： 
python manange.py runserver
否则输入： 
python3 manage.py runserver

6.服务正常启动后，就可在浏览器中输入地址： http://127.0.0.1:8000/, 若出现登录页面，
用户名：
admin
密码:
123456Ok
完成登录后就可正常使用系统.

