git config --list

untracked file 值的是那些 添加到工作区 但是没有提交到暂存区的文件
git reset HEAD <file> 暂存区恢复到上一次状态
git checkout -- <file> 将暂存区中的文件覆盖工作区的文件 有风险
git log 查看历史提交记录

git reset <> HEAD~ ~2 
<> 1 --mixed reposiory和暂存区回滚
   2 --soft  reposiory回滚
   3 --hard  repository和暂存区和工作区回滚  有风险
 
 回滚指定快照 git reset ID
 
 回滚个别文件 git reset ID <file>   此时指针不会移动
 