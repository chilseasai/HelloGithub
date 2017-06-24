## 如何用命令行在 github 新建一个项目
#### 新建项目分2种情况：(无论是哪种情况，都得先在github新建一个项目的仓库)
1.代码从零开始

2.本地已经存在项目代码，只想放到github上开源或存放

#### 代码从零开始
> 你可以在本地创建一个空白的文件夹，然后克隆刚刚创建的项目(ps: clone url 在项目主页的右下方位置可以找到)本地，然后添加代码再上传。

````
mkdir emptyFolder
cd emptyFodler
git clone https://github.com/youraccount/yourproject.git
````
#### 本地已经存在代码
> 在你的项目文件目录先执行命令git init，使之成为一个git仓库。

> 将项目里所有文件加到本地的仓库，使用以下命令：
````
  git add .  //注意还有一个小圆点
  git commit -m "some message for this project."
````
> 然后将github上的项目pull下来
````
  git pull https://github.com/youraccount/yourproject.git
````
> 为版本库添加名为origin的远程版本库。
````
  git remote add origin https://github.com/youraccount/yourproject.git
````
> 执行推送命令，完成GitHub版本库的初始化。注意命令行中的-u参数，在推送成功后自动建立本地分支与远程版本库分支的追踪
````
  git push -u origin master
````
##### Reference
http://www.jianshu.com/p/df7ce9f3a5cb