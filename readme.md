# 广东东软学院安卓实验报告三：“数据存储”

Android schoolwork entertainment app: imitating wechat

Software tips: for learning only. The phone number in the software is not my own number. If you think the software source code is useful, don’t forget to light up star for me

仅供学习交流使用, 软件内电话号码非本人号码。 如果你觉得该软件源码有用，不要忘记帮我点亮star✨

源：广东东软学院安卓实验报告三

软件设计的内容不一定全都是参照实验三的内容

©️ ChuanyangChen 传扬

Source code usage reminder ⏰： Remember to change more！！ not too much like my version of the software！

源代码使用提醒⏰：记得改多点，不要太像我这个版本的软件

How can I download the software source code?

我该如何下载软件源码？

Github下载直通车⏬ ：https://github.com/Ulrich2003/Part3---Android-schoolwork-entertainment-app-imitating-wechat

![image-20211127001234414](https://img-blog.csdnimg.cn/img_convert/7582a691e3ac0609292cb269d61f4e79.png)

#### 1.创建一个工程（本实验在实验二基础上加以改进）

实验二下载直通车⏬：https://blog.csdn.net/weixin_45525653/article/details/121574111?spm=1001.2014.3001.5501

![image-20211220202742248](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211220202742248.png)

#### 2.在注册Activity中将用户各种信息收录到SQLite中，并且将必要信息存入SharedPreferences中，实现「记住用户注册信息」，在登录页面中实现信息自动填充以便注册完成后快速登录。

![image-20211220204314775](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211220204314775.png)

##### SQLite数据的存入

在用户「注册成功」的时候，将注册数据存入SQLite数据库，其中包含用户的账号和密码，是「登录页面」数据比对的重要数据。

![image-20211220204949771](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211220204949771.png)

![image-20211220205311914](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211220205311914.png)

##### SQLite数据的读取

用户在「登录页面」输入完信息点击登录后，系统会从SQLite数据库中查询存在的账号密码，并一一进行比对，如果存在对应的账号及密码，则登录成功，否则提示用户登录失败。

![image-20211220205625677](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211220205625677.png)

![image-20211220204704049](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211220204704049.png)

在AndroidStudio中可以看到数据库文件在设备中的位置：

![image-20211220205857899](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211220205857899.png)

#### 3.通过SharedPreference实现注册后的用户快速登录

![image-20211220212829034](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211220212829034.png)

SharedPreferences在手机中存放的位置：

![image-20211220213155101](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211220213155101.png)

关键代码：

![image-20211220213244372](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211220213244372.png)

#### 4.使用文件存取数据

##### 使用文件方式完成数据的存入

在本实验中，我利用了文件存取来确保App首页的名称是最新登录的用户名名称，当然如果是首次使用，仅会显示一串电话号码

首次使用的效果：

![image-20211220210329381](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211220210329381.png)

登录新建的账号：

![image-20211220210646796](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211220210646796.png)

退出App重新进入主页面的样子：

![image-20211220210736336](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211220210736336.png)

关键代码：

![image-20211220210936455](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211220210936455.png)

##### 使用文件方式完成数据的读取

![image-20211220211048695](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211220211048695.png)

关键代码：

![image-20211220210957607](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211220210957607.png)

在AndroidStudio中可以看到文件在设备中的位置，并文件中的内容：

![image-20211220211221045](https://vichien-public.oss-cn-guangzhou.aliyuncs.com/typora/image-20211220211221045.png)

#### 



