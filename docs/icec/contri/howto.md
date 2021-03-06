欢迎电协的每一位同学加入到这个 Wiki 的编辑中来，让大家的知识更加集中。

## 前提

你需要注册一个 GitHub 账号，[注册新 GitHub 帐户 - GitHub Docs](https://docs.github.com/cn/github/getting-started-with-github/signing-up-for-a-new-github-account).

## 修改编辑

在参与 Wiki 的编写 **需要** 一个 GitHub 账号，**但不需要** 高超的 GitHub 技巧。

假如我想要修改一个页面内容，应该怎么操作呢？

1. 在 **ICEC Wiki** 网站上找到对应页面；
2. 点击正文右上方、目录左侧的 **“编辑此页”** *edit* 按钮；
3. 在编辑框里编写你想修改的内容。另外，由于 **ICEC Wiki** 使用 Markdown 进行编写，如果想进行一些比较大的更改（比如扩充页面内容），你需要掌握一些 [Markdown 语法](https://markdown.tw/)；
4. 写好了之后点下方的绿色按钮 Propose changes 提交修改。但是，GitHub 可能会提示你没有权限。不必担心！GitHub 会自动帮你将 **ICEC Wiki** 的所有文件复制一份，放到你的仓库中（fork）并创建申请合并更改的请求 (Pull Request)；
5. 之后，点上方的绿色按钮 (Create pull request) 后，GitHub 会跳转到一个新的页面 Open a pull request。删掉方框里的文字，简单写写你做的修改，然后再点一下下面的绿色按钮 (Create pull request)；
6. 不出意外的话，你的 PR 就顺利提交到仓库，等待合并了。之后，你就可以等待项目组合并你的分支，或者指出还要修改的地方。当然，你也可以给他人的 PR 提出修改意见，或者只是点赞/踩。如果有消息，会有邮件通知和/或出现在网页右上角的提醒（取决于你个人 Settings 中的设置）。

## 加入维护队伍（选取一小块内容负责管理）

联系当前网站管理：[钟弋辰](https://github.com/ActivePeter)，[谭丰伟](https://github.com/tfx2001)，我们会将你加入到仓库的开发者中。

## 文章中涉及图片

这里的话，有两种方式：

1. 将图片放入 `_static/images` 中，这种方式需要将项目 clone 下来，具体看 [clone 到本地编辑](#clone)；

2. [使用 Gitee 图床](../../tool/note/markdown/markdown_picbed.md)。

   为了确保稳定性请不要使用其余图床，并且保证你的仓库标记清楚，不会过段时间忘了把它删掉。

## clone 到本地编辑

把项目 **clone** 下来可以更灵活的编辑内容，如 **图片，目录结构，新增文章** 等。

考虑到有不熟悉或不了解 Git 的同学，我们将给出一套 **最容易入门，不容易出错** 的完整方案。

### 1. 安装 Git

[Git 简介](../../tool/manage/git.md)。

### 2. 安装新手友好的图形化 Git 界面 - Sourcetree

[Sourcetree 简介](../../tool/manage/sourcetree.md)。

### 3. 克隆 Wiki 仓库

先在本地选择好存放 **项目文件夹** 的路径，然后在该文件夹内右键，点击 `Git Bash Here` ，然后输入以下命令：

```sh
git clone https://hub.fastgit.org/cuit-icec/cuit-icec.github.io.git
```

执行完后，项目就已经克隆到你的本地了，**如果感觉放的位置不对，迁移这个文件夹也是可以的**。

然后去 Sourcetree 中打开这个文件夹，可以看到内容的 **提交记录**：

![image-20210204002813871](https://gitee.com/zhongyichen33/testtupian/raw/master/20210204002813.png)

还有顶栏里的 **常用操作**：

![image-20210204002909114](https://gitee.com/zhongyichen33/testtupian/raw/master/20210204002909.png)

### 4. 安装 Typora

 [Typora 简介](../../tool/note/markdown/typora.md)。

### 5. 编写文章

使用 Typora 打开项目根目录中的 `README.md`，

![image-20210204005619174](https://gitee.com/zhongyichen33/testtupian/raw/master/20210204005619.png)

大概看到的界面是这样的，然后就可以 **开始编写** 了，如果侧边栏不是树形结构，建议 **切换成树形结构**，在侧边栏底部的右边：

![image-20210204005754508](https://gitee.com/zhongyichen33/testtupian/raw/master/20210204005754.png)

**关于内容要求**：（后续完善格式手册）。

### 5. 安装 Visual Studio Code

[Visual Studio Code 简介](../../tool/software/code_editor/visual_studio_code.md)。

### 6. 变动目录结构，添加文章

1. 使用 VS Code 打开我们的项目文件夹（右键文件夹空白处 -> 通过 VS Code 打开，或 VS Code -> 文件 -> 打开文件夹）

   选择 **mkdocs.yml** , 我们需要通过 **修改这个文件** 来进行目录的变更还有文章的添加，格式很简单，其实看文件现有的内容就大概能明白。例如：

   ```yaml
   nav:
     - 简介:
       - Home: index.md
       - 参与 Wiki 的贡献: 
         - 如何参与贡献: icec/contri/howto.md
         - 当前人员分配: icec/contri/member.md
       - 成员: icec/members.md
   ```

   其中：`- Home: index.md` 对应网页侧边栏直接指向一个文章页面，Home 对应的栏目名称，`index.md` 对应的在 `/docs` 文件夹中的相对路径。

   上述配置生成的目录如下：

   ![image-20210204015002101](https://gitee.com/zhongyichen33/testtupian/raw/master/20210204015002.png)

   **注意：**
   
   1. 只写一句 `- 参与 Wiki 的贡献: ` 而后面既不跟文件名，又不跟二级目录 **是不行的，会报错的**！
   2. **横线** 后面需要有 **空格**，然后如果是指向文件 **冒号** 后面需要有 **空格**；
   3. 新建 Markdown 文件的名称 **必须是英文**，单词之间使用 `-` 连接，不要使用 `_`。

### 7. 在本地预览效果

这一步是用来确认 **效果是否符合预期** 和 **排查问题** 的，可以 [跳到下一步](#8)。

### 8. 提交文章

打开 Sourcetree，左边侧边栏点选到 **文件状态**，我们可以看到改动的文件会罗列在为暂存文件夹中

![image-20210204022132477](https://gitee.com/zhongyichen33/testtupian/raw/master/20210204022132.png)

点击 **暂存所有**，在下放栏目中写上 **简略的注释**（TODO：注释规范），点击 **提交**；

![image-20210204022403436](https://gitee.com/zhongyichen33/testtupian/raw/master/20210204022403.png)

一般来说当前是 **最新的分支状态** 的话，直接就顺利提交了。

有些时候可能会提交不成功，因为不是最新的，![image-20210204022617940](https://gitee.com/zhongyichen33/testtupian/raw/master/20210204022618.png) 有数字，那么我们需要 **先拉取** 一下，以同步最新的 commit，然后提交。一般来说，没有 **冲突** 的话，这一步就顺利提交了。

最坏的一种情况，出现了**冲突**（本地的改动和最新的 commit 的改动在同一个地方进行了修改）

如图：

这种时候我个人觉得最方便的解决办法是打开 **VS Code** ，然后查看冲突文件（ VS Code 会把 **冲突文件** 标记成 **<span style="color:purple;">紫色</span>** 的。

然后会在 **冲突的位置** 显示出两个版本的内容，我们 **根据内容进行选取** 就行，如果暂时无法确定舍弃哪一部分，就选择 **两者都保留**，

这样操作之后，回到 Sourcetree 里，保存未暂存文件，会发现里面的冲突不见了，下面的描述框里面会有一大段英文描述自动帮你写好了，然后我们进行一次提交和推送，冲突解决，提交成功。

### 9. 等待 Github Actions 部署

去 Github [查看部署进度](https://github.com/cuit-icec/cuit-icec.github.io/actions)，部署完成后刷新对应的页面就能看到变更啦～

## 存在文章中未提到的问题

请及时反馈到该文章对应的 [issue](https://github.com/cuit-icec/cuit-icec.github.io/issues/5) 中。

