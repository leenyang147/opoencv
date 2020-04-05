git config --list  查看git的信息
git config user.name ''
git config user.email ''

本地repository与github仓库关联
git remote add origin ".git"

添加    可能需要添加用户名和密码
git push -u origin master


untracked file 值的是那些 添加到工作区 但是没有提交到暂存区的文件
git reset HEAD <file> 暂存区恢复到上一次状态
git checkout -- <file> 将暂存区中的文件覆盖工作区的文件 有风险
git log 查看历史提交记录

git reset [] HEAD~ ~2 
[] 1 --mixed reposiory和暂存区回滚
   2 --soft  reposiory回滚
   3 --hard  repository和暂存区和工作区回滚  有风险
 
 回滚指定快照 git reset ID
 
 回滚个别文件 git reset ID <file>   此时指针不会移动
 
 版本对比
 git diff 比较暂存区和工作区的区别
 j 一行一行的往下移动 k 一行一行的往上移动
 f 一页一页的往下移动 b 一页一页的往上移动
 搜索 \关键词
 
 git diff 版本号1 版本号2 比较俩个不同版本的repository快照
 
 git diff 版本号 比较repository当前工作目录的快照区别
 
 git diff --cached [快照ID] 比较暂存区域和git的repository的区别
 
 修改最后一次提交
 git commit --amend 不算一次新的提交
 
 如何在git中删除文件
 git rm <> 
 注意此命令 只是删除了 文件在工作区 和 暂存区的文件 对于repository的部分需要回滚
 git rm --cached <file> 只删除暂存区域而保留工作区域
 
 重命名文件
 git mv <old> <new>
 
 
 