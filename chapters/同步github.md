# 将gitbook中的项目与github同步 [参考来源](https://help.gitbook.com/github/can-i-host-on-github.html)

通过简单的设置，使gitbook的项目与github同步，github每次提交就会自动更新gitbook项目。

总共分3步：

- 设置github的权限（只用设置一次）
- 连接在github上的项目地址（每次创建gitbook项目都需要设置）
- 设置钩子（webhook）（每次创建gitbook项目都需要设置）

--------------------------------------------------------------------------------

1. 设置github的权限

  - 进入gitbook的设置页面`https://www.gitbook.com/@{{UserName}}/settings`

  - 找到"GitHub"的面板（往下拉倒数第三个）选择"with access to publich repositories"。

  - 回到页面顶部，点击左侧"Save"按钮保存。

2. 连接github上的项目地址（前提是已经在github上创建了相应的项目）

  - 进入github对应项目的设置页面`https://www.gitbook.com/book/l{{UserName}}/{{Book}}/settings/github`

  - 在"GitHub Repository"面板中填入`UserName/repo`。UserName为github用户名；rep为需要同步到github上的项目。比如在github上也创建了一个名为"try-gitbook"的项目，我的用户名为"lovedlyl"，这里就应该天`lovedlyl/try-gitbook`。

3. 设置钩子（webhook）

  - 紧挨下面有一个"Integration"面板，点击"Add webhook"。回到页面顶部，点击"Save"按钮保存即可。

  - 下次直接使用`git push origin master`就可同时更新gitbook上的相应项目。
