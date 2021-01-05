# git-command
git command learning

## git commit -a -m "message"
-a 参数表示，可以将所有已跟踪文件中的执行修改或删除操作的文件都提交到本地仓库，即使它们没有经过git add添加到暂存区。
注意，新加的文件（即没有被git系统管理的文件）是不能被提交到本地仓库的。建议一般不要使用-a 参数，正常的提交还是使用git add先将要改动的文件添加到暂存区，再用git commit 提交到本地版本库。

### git add
git add .
不加参数默认为将修改操作的文件和未跟踪新添加的文件添加到git系统的暂存区，注意不包括删除。

git add -u .
-u 表示将已跟踪文件中的修改和删除的文件添加到暂存区，不包括新增加的文件，注意这些被删除的文件被加入到暂存区再被提交并推送到服务器的版本库之后这个文件就会从git系统中消失了。

git add -A .
-A 表示将所有的已跟踪的文件的修改与删除和新增的未跟踪的文件都添加到暂存区

## git checkout -b branchName

History，所有提交过的commit保存的位置，也就是说只要commit过，都是历史，可以回到过去。
Stage(index)，也就是当前git add过的但尚未commit的文件。
Work directory，就是当前正在改的代码了。
