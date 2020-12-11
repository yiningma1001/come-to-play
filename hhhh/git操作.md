### **提交pr**
 - fork别人的仓库
 - 将代码clone到本地
 - 修改代码到自己的仓库
 - 提交pr
 -  ** main**
### **操作**
   - Git add. 添加所有未跟踪的文件
   - Git commit -m “ “
   - it push origin main 本地的master分支推送到远程的主机（可以通过git remote查询远程主机的别名）
   - Git remote rm[别名]删除一个存在的remote alias
   - Git status. 查询repo的状态
   - Git branch:列出所有的分支 
   - Git branch(branchname)创建新的分支
   - Git checkout(branchname)切换到新的分支
   - Git cinfig -l:查看config的信息
   - git pull --ff upstream main
### **远程仓库和github上自己的仓库不同步**
   - 使用fetch命令 先将远程upstream的内容同步到本地
再将本地内提交到github上自己的仓库
   - git remote(如果没有upstream）Git remote add upstream git@github.（URL）添加远程仓库的地址 )
   - 在本地创建一个新的分支 git checkout -b branch-name
     - 修改代码
     - Git add.
     - Git commit -m””
   - 将本地仓库内容会与上游仓库内容进行同步
     - Git fetch upstream main将远程仓库的内容拉到本地 并不自动合并
     - Git rebase upstream/main重新设置基线
     - **有冲突时**
       - 手动删除<<<<< =====>>>>>
       - git add .
       - git rebase --continue
   -  个人分支推送到github
     - Git push -f origin branch-name
   -  merge之后的清理（本地仓库的master和远程仓库的maste一致 删除本地仓库和自己github库中的分支）
      -  git push origin --delete branch-name删除自己github库中的分支
      -  git checkout mian -f 切换到maste分支
      -  git branch -D brach-name删除本地分支
      -  git pull --ff upstream main


