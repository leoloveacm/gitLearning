# git 是一个版本控制的软件

### chapter 0 the used knowledge
git 是一个版本的控制软件
当我们的文件由于协同合作而导致文件副本太多的时候，我们的git就出现了，帮我们的软件的版本可以有很多的版本，并且版本之间我可以不断的切换，保证由于版本的缘故我并不会因为丢失或者修改代码而找不到代码的位置

github是一个非常好的代码托管网站
leoloveacm geekorange
并且可以自己搭建博客和其的的功能在上面

下面就开始git的学习吧！

### chapter 1 the basic

准确的说，git的本地仓库是git给你维护的三棵树
 * 工作目录 ---- 拥有实际文件实体
 * 暂存区(index) ----- 临时保存文件的改动
 * 最后是一个head ----- 指向我最后一次提交的结果

这个是在本地的情况，我们实际上还需要一个和github交互的过程，这个就是很多的pr操作,pull request操作

### chapter 2 the action
下面我们开始学习一些简单的指令，建议不要直接用vscode的GUI功能，(虽然win下面也有客户端，但是为了以后熟练使用，还是最好不要在一开始的时候偷懒)
下面的副标题是对于指令的分类

##### CREATE REPOSITORIES
> git init [project-name]<br>
这个指令是创建一个本地的代码库

> git clone [url]<br>
我们一般使用这个代码来从github上面下载一个本地的代码分支


##### MAKE CHANGES
> git status<br>
这个指令非常智能，可以给出当前的存储区的情况和对于你的一些建议，一个好的习惯是，在每次上传的代码的时候都要查看一下git status，并检查一些代码细节和关键

> git diff<br>
diff操作是将会比较我们的暂存区的代码和目前在文件夹中没有上传的代码，一般也是在上传或者下载之后开始使用的
    * git diff head:将目前的和在push的最新版本进行比较
    * git diff head^ head:比较前一次和前前一次的版本的变化
    * 除此之外,git diff 还可以比较分支的情况，这个我们后面再继续说

> git add [file]<br>
这一步是将一个文件加到我们的暂存区中