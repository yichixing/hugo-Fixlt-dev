# Github配置：2 Github Pull 与 Github Push，pull对分支后才能用push



[0 检查当前分支的跟踪关系]
	<命令：git status；因为如果追踪错误，那么我想要push推送到我想要的分支很可能失败，因为追踪错误的缘故，pull的是其它的分支，因此我想要的分支就没法push了>

[1 取消本地 main 分支对 所有分支 的跟踪]
	<命令：git branch --unset-upstream>

[[[[2 指定pull拉取main的分支（为了push到main，只能强制指定要拉取main分支）]
	《命令：git pull origin main》

[[[[3 pull拉取了main分支后 就能push推送到main分支了]
	<命令：git push -u origin main>

---

> Author:   
> URL: /posts/github%E9%87%8D%E8%A6%81%E8%AE%A4%E7%9F%A5/github%E9%85%8D%E7%BD%AE-github-pull-%E4%B8%8E-github-pushpull%E5%AF%B9%E5%88%86%E6%94%AF%E5%90%8E%E6%89%8D%E8%83%BD%E7%94%A8push/  

