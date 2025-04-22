# Github Action：2 Github Action部署项目原理：github Action是将项目部署到其它仓库，不是部署到自己的仓库

(08:41-10:19) ***4.4: 配置 Repository Secret***
-  ♈ **目的**：将生成的 Token 安全地提供给 **GitHub Actions workflow** 使用。**不应该**直接将 Token 字符串写入 YAML 文件。
-   **操作路径**：回到♎♐**存放 Hugo 源代码**的仓库（即 `hugo-main`），进入该仓库的 `Settings` -> 左侧菜单 `Security` 下的 `Secrets and variables` -> `Actions`。
-   ♈**操作**：点击 `New repository secret` 按钮。
-   **配置 Secret**：
    *   `Name`：输入 **Secret 的名称**。这个名称**必须**与 workflow YAML 文件中 `secrets.` 后面引用的名称**完全一致**。作者在这里将其命名为 `TOKEN`。
    *   `Secret`：将刚才**复制并保存**的**完整 Token 字符串**粘贴到这里。
-   **保存**：点击 `Add secret`。
-   ♈**优点**：使用 **Secrets** 可以**隐藏**敏感信息，workflow 运行时会安全地注入该值，比硬编码在代码中**安全**得多


[[[[[使用aciton后将分源代码仓库和静态页面仓库 ]https://aistudio.google.com/prompts/1dv1SBgRsYgFBSgYe1Dseg0dyYouTZ3_P
	《《《hugo-main 仓库 (源代码仓库)，专门用来提交项目源码的仓库，以及用来运行action的仓库，不需要开启github page的功能，所以hugo-main仓库不需要公开，也不需要把静态资源上传到这仓库上》
	《《《hugo-dev 仓库 (部署目标/静态页面仓库)，hugo-main运行action后生成的静态资源文件所推送到的仓库，是存放最终网站文件并对外提供访问的地方，它是自动化流程的终点/发布目标，因此我们在仓库开启github page功能》
		《《《aciton中的参数 EXTERNAL_REPOSITORY: letere-gz/hugo-dev 就是用来 明确指定了main仓库部署的目标是这个dev仓库。》

---

> Author:   
> URL: https://hugo-fixlt-dev.tcapital.top/posts/github%E9%87%8D%E8%A6%81%E8%AE%A4%E7%9F%A5/github-actiongithub-action%E9%83%A8%E7%BD%B2%E9%A1%B9%E7%9B%AE%E5%8E%9F%E7%90%86github-action%E6%98%AF%E5%B0%86%E9%A1%B9%E7%9B%AE%E9%83%A8%E7%BD%B2%E5%88%B0%E5%85%B6%E5%AE%83%E4%BB%93%E5%BA%93%E4%B8%8D%E6%98%AF%E9%83%A8%E7%BD%B2%E5%88%B0%E8%87%AA%E5%B7%B1%E7%9A%84%E4%BB%93%E5%BA%93/  

