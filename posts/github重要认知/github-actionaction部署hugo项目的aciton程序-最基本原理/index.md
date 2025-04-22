# Github Action：0 Action部署hugo项目的aciton程序 最基本原理


		[[[[在action环境安装项目包（hugo包）的两种做法（参考如何让AI写action程序）]
			《1 uses 关键字并指定一个像 别大大佬些好的aciton 比如peaceiris/actions-hugo@v3 这样的“动作 (Action)”时，你是在委托这个预先打包好的工具去完成安装和配置 Hugo 的任务》
			《2 直接用run字段亲自告诉那个临时的 Linux 系统具体怎么做才能把 Hugo 装好》

		[action部署hugo项目的aciton程序]
			<action部署hugo项目的aciton程序的核心：让action使用hugo命令，action环境需要hugo命令执行hugo博客>
			<1 有参考作用的使用uses参数的action程序的写法（参考如何让AI写action程序）>
			<2 有参考作用的使用run字段的action程序的写法 https://aistudio.google.com/prompts/1dv1SBgRsYgFBSgYe1Dseg0dyYouTZ3_P（参考如何让AI写action程序）>

		[aciton想部署hugo的核心就是用别人预先写好的东西]
			《hugo官方有提供官方action动作把仓库代码下载（检出） 到当前的虚拟运行环境中，它就是actions/checkout@v4，通过uses: actions/checkout@v4: 就能使用一个预先写好的、官方提供的“动作” (Action)》
		

---

> Author:   
> URL: https://yichixing.github.io/hugo-Fixlt-dev/posts/github%E9%87%8D%E8%A6%81%E8%AE%A4%E7%9F%A5/github-actionaction%E9%83%A8%E7%BD%B2hugo%E9%A1%B9%E7%9B%AE%E7%9A%84aciton%E7%A8%8B%E5%BA%8F-%E6%9C%80%E5%9F%BA%E6%9C%AC%E5%8E%9F%E7%90%86/  

