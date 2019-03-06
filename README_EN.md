# git remote add origin https://github.com/wuxiumu/luthier-ci.meiyoufan.git

```
删除 commit，重置到某个 commit

确保当前分支为主分支 master

// 本地新建一个分支 old_master
1. git branch old_master

// 推送本地的当前分支到远程的 old_master 分支 --> 远程不存在会自动新建 old_master 分支
2. git push origin old_master

// 本地当前分支回退到指定提交 --> xxx 为 commit 的 SHA 值
3. git reset --hard xxxxx

4. 操作远程，修改默认分支为 old_master。即主分支修改为 old_master

// 删除远程的 master 分支。master 已经不是主分支了
5. git push origin --delete master

// 推送本地当前分支到远程 master 分支 --> 远程不存在会自动新建 master 分支
6. git push origin master

7. 操作远程，修改默认分支为 master 。即主分支修改为 master

// 删除远程 old_master 分支。old_master 已经不是主分支了
8. git push origin --delete old_master

```