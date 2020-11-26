#### Git的一些基本的操作

------

> ##### 从Git上克隆项目并与VSCode关联起来

1. 将项目从git上克隆下来

   ```
   git clone 项目的地址
   ```

2. 克隆完成后在我们的文件夹中新创建一个项目

   ```
   cd 新创建的文件的名字
   ```

3. 把git上面最新版本的项目分支chekout到我们创建的新文件夹里面

   ```
   git checkout 最新项目版本号
   ```

   ![](E:\fourth_nanjing\实习文件\实习学习文件\ThirDay\git操作.png)



#### GitPromble

1. Git GitHub GitLab的区别

   ```
   https://www.cnblogs.com/leeyongbard/p/9777498.html
   ```

2. 

#### GitOpteraation

1. 错误总结

   - first：$ git add firstFile

     ```
     fatal: pathspec 'readme.txt' did not match any files
     ```

     错误原因：说明文件夹里面没有匹配到该文件，我们只需要在相应的仓库里面添加该文件便可以

   - second:

     ```
     fatal: invalid --pretty format: online
     ```

     错误原因：

   - third：

     ![image-20201103165352692](C:\Users\cheng\AppData\Roaming\Typora\typora-user-images\image-20201103165352692.png)

     警告解决：

     问题解决地址：https://blog.csdn.net/weixin_44394753/article/details/91410463

   - 

2. Git知识难点

   - checkout的一般使用场景

     ```
     场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。
     
     场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD <file>，就回到了场景1，第二步按场景1操作。
     场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。
     
     ```
     
- 
  
3. Git代码和VSCode解决合并分支的冲突问题
   - 首先在VSCode里面会有现在的工作区域和远程仓库的相应文件出现冲突的对比，然后我们选择使用哪一个文件的修改，解决好冲突，然后再进行一次提交，就好了
4. 



