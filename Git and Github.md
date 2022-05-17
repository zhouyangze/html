## Git and Github

#### 写在前面:

作为一个非科班选手，为了使得自己看起来比较的专业，学会使用github是必不可少的了，此外由于有多台电脑，每台电脑之间的文件同步也十分的头疼，于是学会github和git势在必行

如何注册一个github和建立github仓库此处不多赘述，和普通的网站注册并无太多不同，也有很多教程

#### 美化Git的界面：

#### 如何链接github 和git：

铺垫工作在知乎这篇文章中有十分详细的介绍，但是在时间过程中会出现一点问题，在clone和push之前的步骤都是没有问题的。

https://www.zhihu.com/people/wu-ming-shi-lue-lue-lue

步骤:

新建文件夹和仓库

git init

git add

git commit -m "XXX"

git remote add origin  ssh://git@github.com/zhouyangze/html.git

然后即可push

在push 和 clone 会遇到的一些问题：

关于clone的时候报错显示无法链接的时候，把http改为git即可解决

![image-20220207162840793](C:\Users\22365\AppData\Roaming\Typora\typora-user-images\image-20220207162840793.png)

当 git push origin branch_name时遇到报错如下：

![image-20220207163100016](C:\Users\22365\AppData\Roaming\Typora\typora-user-images\image-20220207163100016.png)

解决方案为:

输入**git remote –v**如果没有如何的反馈说明![image-20220207163244449](C:\Users\22365\AppData\Roaming\Typora\typora-user-images\image-20220207163244449.png)

说明与上游已断开链接，无法拉取代码，则需要重新remote链接

![image-20220207164551166](C:\Users\22365\AppData\Roaming\Typora\typora-user-images\image-20220207164551166.png)

链接之后即可push:![image-20220207164639948](C:\Users\22365\AppData\Roaming\Typora\typora-user-images\image-20220207164639948.png)

但是可能会出现以下的报错，解决办法如下：

![image-20220207184826460](C:\Users\22365\AppData\Roaming\Typora\typora-user-images\image-20220207184826460.png)

但是git 执行git pull –rebase报错误如下：

error: Cannot pull with rebase: You have unstaged changes.
error: Additionally, your index contains uncommitted changes.

原因：如果有未提交的更改，是不能git pull的

解决：
先执行git stash，再执行git pull –rebase，最后再执行git stash pop，之后即可push。其中git stash可用来暂存当前正在进行的工作，git stash pop从Git栈中读取最近一次保存的内容

在克隆的时候可能还会遇到问题

![image-20220517114546280](C:\Users\22365\AppData\Roaming\Typora\typora-user-images\image-20220517114546280.png)

解决方法为![image-20220517114617866](C:\Users\22365\AppData\Roaming\Typora\typora-user-images\image-20220517114617866.png)