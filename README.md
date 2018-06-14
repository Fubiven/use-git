# use-git
关于如何使用github管理项目（本文指针对window操作系统）

一、注册Github账号：
    进入 https://github.com/ 官网注册账号并登陆，注意记住以下信息：
    github-username —— 账号
    github-email —— 关联邮箱
    github-password —— 密码

二、git安装：
    下载git windows版并正确安装
    
三、设置个人Git信息：
    1、打开 Git Bash
    2、执行如下代码关联账号、邮箱信息
        git config --global user.name "git-username" —— 关联账号 git-username 为GitHub 注册账号
        git config --global user.email "git-email"   —— 关联邮箱 git-username 为GitHub 账号绑定邮箱
        
四、ssh-key配置(本地Git仓库和GitHub仓库之间的传输是通过SSH加密的)：  
    1、Windows下打开Git Bash，执行 ssh-keygen -t rsa -C "git-email"  创建SSH Key, 按提示输入密码，
         可以不填密码一路回车。
    2、然后用户主目录/.ssh/下会生成两个文件，id_rsa是私钥，不能泄露出去，id_rsa.pub是公钥，可以放心地告诉任何人。
         id_rsa.pub文件里面的内容就是key的内容
    3、登录GitHub，打开"Settibgs-> SSH Keys"页面，然后，点“Add SSH Key”，填上任意Title，
         在Key文本框里粘贴id_rsa.pub文件的内容,add key 完成添加
         
五、Github中创建仓库：
   1、登录账号后点击官网右上角 加号 - "new repository"
   2、填写仓库名称
   3、选填描述信息
   4、选择公开/私有（收费） 情况
   5、选择添加初始化自述文件（README）
   6、create repository 完成创建
   
六、创建本地仓库关联Github远程仓库：
  1、本地新建文件夹，确保路径不包含中文字符
  2、右键所创文件夹，点击Git bash here 打开git命令行
  3、命令行中执行 git init，使文件夹加入git管理
  2、执行git add “文件/文件夹名”，将所需内容添加到git,文件夹全部内容添加到git。
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
