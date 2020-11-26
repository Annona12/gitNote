### Git的使用

------

1. 安装Git

   - 在Git官方网站下载程序， 然后按照步骤安装即可，然后右击鼠标可以出现 Git Bash,点击出现命令行窗口就说明安装成功了；
   
2. 在我们的电脑本地创建版本库

   - 创建本地版本库的步骤

     ```
     //1、创建（也可以直接在一个我们需要与远程仓库关联的目录里面直接开始git init）
     mkdir 版本库文件名
     cd 版本库文件名
     pwd查看文件路径
     
     //2、把版本库变成Git可以管理的仓库
     git init
     
     //把文件添加到版本库里面
     git add 需要添加的文件名字
     git commit -m “提交描述”
     
     //git add其实就是我们修改了的文件或是新增的文件添加到暂存区
     //git commit把暂存区的所有内容提交到当前的分支
     Git的版本库里存了很多东西，其中最重要的就是称为stage（或者叫index）的暂存区，还有Git为我们自动创建的第一个分支master，以及指向master的一个指针叫HEAD。
     
     
     我们在创建git版本库时Git自动为我们创建了一个唯一的分支master,所以最开始的时候我们commit的时候就是将修改的内容提交到master分支上
     
     ```

     ![image-20201114144048711](C:\Users\cheng\AppData\Roaming\Typora\typora-user-images\image-20201114144048711.png)

   - 远程仓库的创建

     - 在GitHub创建一个新的仓库

     - 关联步骤

       ```
       //1、vueOriginshishenm?
       git remote add vueOrigin git@github.com:Annona12/vuedemo.git(这个是我们在远程仓库创建的仓库的SSH的链接)
       
       //先要将文件进行提交，git add /git commit
       
       //2、把本地仓库的所有的内容推送到远程仓库中
       git push -u vueOrigin master
       
       //3、下次再进行推送的时候只需要输入
       git push vueOrigin master
       ```

       

   - 分支的创建和使用？？？？

     ```
     分支里面的HEAD，其实是指向当前的分支，然后的话
     分支管理的作用和意义：
     首先Git代码管理仓库可以创建很多很多的分支，Git在最开始的时候默认的拆个年间了一个master的分支，然后的话，我们在需要开发一个新的功能的时候或是在需要开发一个新的模块的时候，我们就可以在创建一个新的分支，然后我们新的分支和其他人工作的分支互不干扰，就算我们开发的这一个分支存在错误没有开发完成也可以将代码进行提交保存，在我们开发完成这一个新的模块之后再进行合并，合并完成之后我们可以切换会主分支，然后删除不需要的分支
     
     第一种方法
     //1、创建分支并且换分支
     $ git checkout -b dev
     //2、切换分支
     $ git branch dev
     $ git checkout dev
     //3、合并分支
     $ git merge dev
     //4、删除分支
     $ git branch -d dev
     
     第二种方法
     $ git switch -c dev
     
     $ git switch master
     
     ```

     

   - 

3. 常用的命令

   ```
   $ git init
   $ git add
   $ git commit -m "description"
   $ git log 
   $ git log --pretty=oneline
   $ git reset --hard HEAD^
   $ git reset --hard 1094a
   $ git reflog
   $ git status
   $ git diff HEAD -- readme.txt 
   $ git checkout -- readme.txt  可以丢弃工作区的修改：总之，就是让这个文件回到最近一次git commit或git add时的状态。
   $ rm test.txt
   $ git remote add origin git@github.com:michaelliao/learngit.git
   $ git push -u origin master
   $ git push origin master
   $ git clone git@github.com:michaelliao/gitskills.git
   ```

   

4. 

   