---
title: "第 12 课 - 使用 GitHub Pages 部署网站"
description: "使用 GitHub Copilot 应用配置 Pages 工作流、审查拉取请求，并确认 Space Quiz 已上线。"
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

部署 Space Quiz，让所有人都能试用。Copilot 可以准备工作流并指导部署，但你仍需审查更改并确认网站已上线。

本课将完成以下任务：

- 请求 Copilot 配置 GitHub Pages 部署。
- 在合并前审查工作流和拉取请求。
- 跟踪部署并验证已发布的网站。

## 场景

Space Quiz 已经位于 GitHub 仓库中，但用户仍需要一种简单的试用方式。使用 GitHub Pages 发布这个单文件网站后，用户便可通过公共 URL 访问，无需添加服务器或运行时依赖项。

## 请求 Copilot 部署网站

在 `space-quiz` 的 Copilot 应用会话中发送以下提示：

```plaintext
Enable GitHub Pages for this repository. Create a GitHub Actions workflow that builds the website if needed and deploys it to GitHub Pages. Add a README describing the app and how to run it locally if one does not already exist. Create a pull request with these changes and merge it after required checks pass. Monitor the deployment until it succeeds, then report the final URL of the live website. If you lack permission to enable Pages or merge, tell me exactly what I need to approve or do; do not report success until the site is live.
```

![三阶段示意图：已合并的 space-quiz 拉取请求；成功运行的 GitHub Actions Deploy website 工作流，其中包含 Build website、Upload artifact 和 Deploy to Pages 步骤；以及在 yourname.github.io/space-quiz/ 上线的 Space Quiz。](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> 此提示要求代理创建并合并拉取请求，以及更改仓库的 Pages 设置。继续之前，请审查差异、部署权限以及 GitHub 的任何审批提示。

## 审查工作流并验证部署

1. 确认仅当仓库尚无 README 时才添加 README。
2. 审查拉取请求中的更改，包括工作流的构建和部署步骤。
3. 仅在拉取请求的必需检查通过后才合并。
4. 跟踪 GitHub Actions 部署运行，直到其成功。
5. 打开报告中的 URL，确认 Space Quiz 已加载。

如果代理无权启用 Pages 或合并拉取请求，请按照其提供的具体说明操作。在部署成功且线上网站可以加载之前，不要将任务视为已完成。

## 总结和后续步骤

Space Quiz 现已作为在线网站提供，并且你已亲自验证部署，而不是只依赖代理的报告。继续学习[第 13 课：回顾与后续步骤][next-lesson]。

[next-lesson]: ../13-review/
