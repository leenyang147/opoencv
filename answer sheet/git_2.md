git的分支 分支既指针
支持分支 对于版本控制而言非常重要。git的每一个节点 都是一个拷贝的副本 因此只要改变分支指向的指针就可以进行拷贝。不需要因为
创建一个新的版本而拷贝所有的源代码。
创建分支
git branch 分支名
切换分支
git checkout 分支名
git checkout -b 分支名 创建并且切换分支

git log --decorate --oneline （显示提交记录精简版）
git log --decorate --oneline --graph --all（显示提交记录精简版图形版）

合并分支  无论什么
git merge 分支名

删除分支 删除分支 只是删除指针不删除快照
git branch -d 分支名

匿名分支
git checkout HEAD~ 会在head指针之前的那个commit那里创建一个新的匿名分支。

checkout 命令
1 指定的提交中 拷贝文件到工作区和暂存区
git checkout <file> HEAD~

git checkout -- <file> 直接用暂存区覆盖到工作区。
加-的原因是 仿真文件名和分支 混淆

git 恢复文件 并没有改变指针 和reset命令类似

checkout 与 reset的区别
在恢复文件方面 reset 只允许改变暂存区 默认为mixed 而不会改变工作区
而checkout 命令则同时改变暂存区域工作区 因此reset更加安全

在改变快照方面 reset是回到故去 会删分支和快照 而 checkout只是改变head指针。