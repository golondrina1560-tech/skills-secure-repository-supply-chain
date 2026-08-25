## Step 3: Dependabot security updates を有効にして動かす

_Dependabot alerts の有効化・確認・作成、よくできました :sparkles:_

リポジトリで Dependabot alerts を有効にしたのは、コードのセキュリティを高める大きな一歩でした。とはいえ、アラートを自分で選び、pull request を作る操作も自分で行う必要がありました。依存関係の更新と管理を、もっと自動化できるとよいですね。Dependabot security updates を使えば自動化できます。

**Dependabot security updates とは**

機能を有効にすると、Dependabot が脆弱な依存関係を検出する*だけでなく*、Dependabot alerts を解決する pull request を自動で作成して修正します。

「Prototype Pollution in minimist」のアラートは手動で pull request を作って直しましたが、今後のアラートに向けて Dependabot security updates を有効にし、同じ流れを自動化しましょう。

### :keyboard: やること 3.1: Dependabot security updates を有効にして動かす

1. **Settings** タブを開き、**Advanced Security**（アカウントによっては **Code security**）を選びます。
1. **Dependabot security updates** を有効にします。新しい pull request が現れるまで 30〜60 秒待つ必要があるかもしれません。
1. リポジトリの **Pull requests** タブを開き、Dependabot が見つけたものを確認します。
1. **axios** 依存関係にパッチを当てる新しい pull request を探します。
1. pull request を確認してマージします。
1. pull request をマージしたので、Mona が作業を確認しています。少し待って、コメントを見てください。進捗と次の Step が投稿されます。
