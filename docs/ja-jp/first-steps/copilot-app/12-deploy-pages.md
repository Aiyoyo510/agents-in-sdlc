---
title: "レッスン 12 - GitHub Pages でサイトを公開する"
description: "GitHub Copilot アプリで Pages ワークフローを構成し、プルリクエストを確認して、Space Quiz が公開されたことを確かめます。"
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Space Quiz を公開して、誰でも試せるようにします。Copilot はワークフローの準備とデプロイを支援しますが、変更を確認し、サイトが公開されたことを確かめる必要があります。

このレッスンでは、次のことを行います。

- GitHub Pages へのデプロイを構成するよう Copilot に依頼します。
- マージする前にワークフローとプルリクエストを確認します。
- デプロイの状況を追跡し、公開されたサイトを確認します。

## シナリオ

Space Quiz はすでに GitHub リポジトリにありますが、まだ簡単に試せる方法がありません。1 ファイルで構成されたサイトを GitHub Pages で公開すると、サーバーやランタイム依存関係を追加せずに、公開 URL からアクセスできるようになります。

## Copilot にサイトのデプロイを依頼する

`space-quiz` の Copilot アプリ セッションで、次のプロンプトを送信します。

```plaintext
Enable GitHub Pages for this repository. Create a GitHub Actions workflow that builds the website if needed and deploys it to GitHub Pages. Add a README describing the app and how to run it locally if one does not already exist. Create a pull request with these changes and merge it after required checks pass. Monitor the deployment until it succeeds, then report the final URL of the live website. If you lack permission to enable Pages or merge, tell me exactly what I need to approve or do; do not report success until the site is live.
```

![3 段階の図: マージ済みの space-quiz プルリクエスト、Build website、Upload artifact、Deploy to Pages の各手順が成功した GitHub Actions の Deploy website 実行、yourname.github.io/space-quiz/ で公開された Space Quiz。](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> このプロンプトでは、エージェントにプルリクエストの作成とマージ、およびリポジトリの Pages 設定の変更を依頼します。続行する前に、差分、デプロイの権限、GitHub の承認要求を確認してください。

## ワークフローを確認してデプロイを検証する

1. リポジトリに README がない場合に限り、README が追加されていることを確認します。
2. ワークフローのビルド手順とデプロイ手順を含め、プルリクエストの変更を確認します。
3. 必須のプルリクエスト チェックが成功してからマージします。
4. GitHub Actions のデプロイ実行が成功するまで追跡します。
5. 報告された URL を開き、Space Quiz が読み込まれることを確認します。

エージェントが Pages の有効化やプルリクエストのマージを実行できない場合は、提示された具体的な手順に従います。デプロイが成功し、公開サイトが読み込まれるまでは、完了と見なさないでください。

## まとめと次のステップ

エージェントの報告だけに頼らず、デプロイを確認したうえで Space Quiz を公開できました。[レッスン 13: 振り返りと次のステップ][next-lesson]に進みます。

[next-lesson]: ../13-review/
