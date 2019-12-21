---
title: Translation project
teaser: An Intro to Git and GitHub for Beginners (Tutorial)
category: translation
tags: [translation, Github]

---

### 步骤6：在 GitHub上创建新的仓库

 

如果你只想在本地跟踪代码，则无需使用GitHub。 但是，如果你想与团队合作，则可以使用GitHub协同修改项目代码。

如果要在GitHub上创建新的仓库，请登录并转到GitHub主页。 你会看到一个绿色的“+ New repository ”按钮：

 ![Git_101_Screenshot1-2.png](https://product.hubspot.com/hs-fs/hubfs/Git_101_Screenshot1-2.png?width=671&height=141&name=Git_101_Screenshot1-2.png)

单击按钮后，GitHub将要求你命名仓库并提供简短描述：

![Git_101_Screenshot_2-1.png](https://product.hubspot.com/hs-fs/hubfs/Git_101_Screenshot_2-1.png?width=671&height=418&name=Git_101_Screenshot_2-1.png)

填写完信息后，请按“Create repository”按钮以创建新的仓库。

GitHub会询问你是否要从头开始创建新的仓库，或者是否要添加在本地创建的仓库。 在这种情况下，由于我们已经在本地创建了新的仓库，因此我们希望将其推送到GitHub上，因此请遵循 **“....或从命令行推送现有仓库”** 部分： 

### `mnelson:myproject mnelson$ git remote add origin https://github.com/cubeton/mynewrepository.git mnelson:myproject mnelson$ git push -u origin master Counting objects: 3, done. Writing objects: 100% (3/3), 263 bytes | 0 bytes/s, done. Total 3 (delta 0), reused 0 (delta 0) To https://github.com/cubeton/mynewrepository.git  * [new branch]      master -> master Branch master set up to track remote branch master from origin.`[view raw](https://gist.github.com/cubeton/3a2616c44e35ca68a6b0/raw/41e5758cfdbd7db8a1659c1adaba9346680097f9/addgithub.md)[addgithub.md](https://gist.github.com/cubeton/3a2616c44e35ca68a6b0#file-addgithub-md) hosted with ❤ by [GitHub](https://github.com)`mnelson:myproject mnelson$ git remote add origin https://github.com/cubeton/mynewrepository.git mnelson:myproject mnelson$ git push -u origin master Counting objects: 3, done. Writing objects: 100% (3/3), 263 bytes | 0 bytes/s, done. Total 3 (delta 0), reused 0 (delta 0) To https://github.com/cubeton/mynewrepository.git  * [new branch]      master -> master Branch master set up to track remote branch master from origin.`[view raw](https://gist.github.com/cubeton/3a2616c44e35ca68a6b0/raw/41e5758cfdbd7db8a1659c1adaba9346680097f9/addgithub.md)[addgithub.md](https://gist.github.com/cubeton/3a2616c44e35ca68a6b0#file-addgithub-md) hosted with ❤ by [GitHub](https://github.com/)

（由于你的GitHub用户名和仓库名称不同，因此你需要将第一个命令行中的URL更改为本节中GitHub列出的内容） 

### 步骤7：将分支推送到GitHub

 

现在，我们将分支中的提交**推送**到新的GitHub仓库。这使其他人可以看到你所做的更改。 如果它们是由仓库拥有者同意的，则可以将其更改合并到主分支中。

要将更改推送到GitHub上的新分支，你需要运行 `**git push origin yourbranchname**. ```GitHub将在远程仓库上自动为你创建分支： 

```
mnelson:myproject mnelson$ git push origin my-new-branch
Counting objects: 3, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 313 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/cubeton/mynewrepository.git
 * [new branch]      my-new-branch -> my-new-branch
```

[view raw](https://gist.github.com/cubeton/bf8274609c344b6d0e70/raw/4764e740cac9a48eefad341d9e34ceb09f89b73f/addnewbranchgithub.md)[addnewbranchgithub.md](https://gist.github.com/cubeton/bf8274609c344b6d0e70#file-addnewbranchgithub-md) hosted with ❤ by [GitHub](https://github.com)

```
mnelson:myproject mnelson$ git push origin my-new-branch
Counting objects: 3, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 313 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/cubeton/mynewrepository.git
 * [new branch]      my-new-branch -> my-new-branch
```

[view raw](https://gist.github.com/cubeton/bf8274609c344b6d0e70/raw/4764e740cac9a48eefad341d9e34ceb09f89b73f/addnewbranchgithub.md)[addnewbranchgithub.md](https://gist.github.com/cubeton/bf8274609c344b6d0e70#file-addnewbranchgithub-md) hosted with ❤ by [GitHub](https://github.com/)

你可能想知道上面命令中“origin”一词的含义。当你将远程仓库克隆到本地计算机时，git为你创建了一个**别名**。在几乎所有情况下，此别名都称为[**origin**](https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes) 。它实质上是远程仓库URL的简写。 因此，要将更改推送到远程仓库，可以使用以下命令： **git push git@github.com:git/git.git yourbranchname** 或者**git push origin yourbranchname**

（如果这是你第一次在本地使用GitHub，则可能会提示你使用GitHub用户名和密码登录。）

如果刷新GitHub页面，你会看到注释，说你的名字的分支刚刚被推送到仓库中。 你也可以单击”branches“链接以查看此处列出的分支。

![Git_101_Screenshot2.png](file:///C:/Users/lenovo/Desktop/xiaozhu/Final-Exam/%E9%99%84%E4%BB%B62%20translation%20project/An%20Intro%20to%20Git%20and%20GitHub%20for%20Beginners%20(Tutorial)_files/Git_101_Screenshot2.webp) 

现在，单击上方屏幕截屏中的绿色按钮。 我们将提出**发送请求**！

 

### 步骤8：创建发送请求（PR）

发送请求（或PR）是一种提醒仓库拥有者要更改其代码的方式。 它允许他们在将更改放在主分支上之前检查代码并确保它看起来很好。

这是PR页面在你提交之前的样子：

![Git_101_Screenshot_4.png](file:///C:/Users/lenovo/Desktop/xiaozhu/Final-Exam/%E9%99%84%E4%BB%B62%20translation%20project/An%20Intro%20to%20Git%20and%20GitHub%20for%20Beginners%20(Tutorial)_files/Git_101_Screenshot_4.webp) 

这就是你提交PR请求后的样子 ：

![Git_101_Screenshot_5.png](file:///C:/Users/lenovo/Desktop/xiaozhu/Final-Exam/%E9%99%84%E4%BB%B62%20translation%20project/An%20Intro%20to%20Git%20and%20GitHub%20for%20Beginners%20(Tutorial)_files/Git_101_Screenshot_5.webp) 

你可能会在底部看到一个绿色的大按钮，上面显示“Merge pull request”。 单击这意味着你将你的更改合并到主分支中。

请注意，此按钮并非总是绿色。 在某些情况下，它会是灰色的，这意味着你面临 **合并冲突**。这是当一个文件中的更改与另一个文件中的更改冲突时，git无法确定要使用的版本。你必须手动进入并告诉git使用哪个版本。

有时你将成为共同所有者或回购的唯一所有者，在这种情况下，你可能不需要创建PR来合并你的更改。但是，创建一个分支仍然是一个好主意，这样你可以保留更新的更完整历史记录，并确保在进行更改时始终创建一个新分支。

 

---

[^1]: 
    Such as footnotes.

[kd]: http://kramdown.gettalong.org/
[rd]: https://github.com/davidfstr/rdiscount
[rc]: https://github.com/vmg/redcarpet
[kds]: https://kramdown.gettalong.org/syntax.html
