# 项目架构简单介绍及开发建议
- 推荐在 VSCode 进行开发

- lalc_frontend，前端，初始化时用 flutter create，构建应用 flutter run windows。推荐下载插件 Flutter Intl 来方便国际化，这样一来只要编辑 arb 文件就能自动生成国际化配置代码。

- lalc_backend，后端，初始化时用 uv sync 来配置环境（uv 是一个 python 虚拟环境的工具，不了解的话请自行搜索下载使用）；由于涉及到平级目录互相调用，建议用 uv pip install -e . 来模块化项目。

- 项目整体的打包用根目录的 packup_release.bat 文件，打包环境为 windows

# Git commit message 建议
- fork 到自己仓库后，建议自己另建一个分支（branch）开发，完成后先把新分支 push 到自己仓库，然后前往 [pr](https://github.com/HSLix/LixAssistantLimbusCompany/compare) 来新建自己的 pr，把你的分支合进来。
- git commit 时，建议带上 feat: fix: chores: docs:，等前缀标明本次 commit 的类型，遵循 [conventionalcommits](https://www.conventionalcommits.org/en/v1.0.0/) 的规范要求来做的话，自动发版才会正常工作。