# Secure your repository's supply chain（日本語版）

_サプライチェーンを保護し、環境内の依存関係を把握し、依存関係の脆弱性を知って、パッチを当てる。_

> このリポジトリは GitHub Skills「[Secure your Repository Supply Chain](https://github.com/skills/secure-repository-supply-chain)」（MIT License）の日本語版です。
> 演習の進め方と自動チェックの仕組みは原本と同じで、Issue に投稿される手順の本文だけを日本語にしています。

## ようこそ

GitHub は、環境内の依存関係を把握することから、依存関係の脆弱性を知り、パッチを当てるところまで、サプライチェーンの保護を支援します。

- **対象**: 開発者、DevOps エンジニア、SRE、セキュリティ担当者
- **学ぶこと**: リポジトリの依存関係の見方、Dependabot alerts の見方、Dependabot security updates と version updates の有効化
- **作るもの**: リポジトリの依存関係、Dependabot alerts、依存関係を修正する pull request、バージョン更新
- **前提**: なし
- **所要時間**: 1 時間以内

この演習で扱うもの:

1. Dependency graph
2. Dependency alerts
3. Dependency security updates
4. Dependency versions updates

### 演習の始め方

演習を自分のアカウントにコピーし、Octocat（Mona）が最初のレッスンを準備するまで **20 秒ほど**待ってから、**ページを再読み込み**してください。

[![](https://img.shields.io/badge/Copy%20Exercise-%E2%86%92-1f883d?style=for-the-badge&logo=github&labelColor=197935)](https://github.com/new?template_owner=mamezou&template_name=skills-ja-secure-repository-supply-chain&owner=%40me&name=skills-secure-repository-supply-chain&description=Exercise:+Secure+your+Repository+Supply+Chain&visibility=public)

<details>
<summary>うまくいかないとき 🤷</summary><br/>

演習をコピーするときは、次の設定を推奨します。

- Owner は自分の個人アカウント（または演習を置く Organization）を選ぶ。

- private リポジトリは Actions の実行時間を消費するため、public リポジトリを推奨します。

20 秒待っても演習が始まらないときは、[Actions](../../actions) タブを確認してください。

- ジョブが実行中かどうかを見る。少し長くかかることがあります。

- ジョブが失敗している場合は、講師に知らせてください。

</details>

---

&copy; 2025 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)
