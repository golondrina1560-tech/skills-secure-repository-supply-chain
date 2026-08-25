## Step 2: Dependabot alerts を有効にして確認する

_よくできました！ :tada: Dependency graph を使って依存関係を追加し、確認できました。_

リポジトリが使う依存関係の数を考えると、管理は自動化する必要があります。コードを安全に保つことは最優先なので、まずやるべきは、使っている依存関係が脆弱だったりマルウェアだったりしたときに通知を受け取る仕組みを作ることです。Dependabot alerts を有効にすれば実現できます。

**Dependabot alerts とは**

Dependabot alerts は、コードが安全でないパッケージに依存していることを知らせます。Dependabot alerts は [GitHub Advisory Database](https://github.com/advisories) を参照しています。データベースには既知のセキュリティ脆弱性とマルウェアの一覧が、**GitHub reviewed advisories** と **unreviewed advisories** の 2 種類に分けて収録されています。

セキュリティ脆弱性のあるパッケージにコードが依存していると、プロジェクトや利用者にさまざまな問題を引き起こす可能性があります。できるだけ早く安全なバージョンにアップグレードしてください。コードがマルウェアを使っている場合は、安全な代替パッケージに置き換える必要があります。

いま追加した `follow-redirects` 依存関係で試してみましょう。

### :keyboard: やること 2.1: GitHub Advisory Database でセキュリティアドバイザリを見る

1. [GitHub Advisory Database](https://github.com/advisories) を開きます。
1. アドバイザリの検索ボックスに `follow-redirects` と入力または貼り付けます。
1. 見つかったアドバイザリのどれかをクリックして、詳しい情報を見ます。
1. アドバイザリの packages、impact、patches、workaround、references が表示されます。

`follow-redirects` にアドバイザリが長く並んでいることに気づいたでしょうか。怖く見えますが、実はよいことです。活発にメンテナンスされ、脆弱性を取り除くパッチが公開されているということだからです。Dependabot alerts を有効にしておけば、依存関係を更新すべきときにアラートを受け取り、すぐに対応できます。

では、リポジトリで Dependabot alerts を有効にしましょう。

### :keyboard: やること 2.2: Dependabot alerts を有効にする

1. **Settings** タブを開きます。
1. **Advanced Security**（アカウントによっては **Code security**）の設定を表示します。
1. Dependabot alerts を **Enable** にします。
1. **Dependabot がアラートを確認するまで 60 秒ほど待ちます。**
1. **Security** タブを開きます。
1. サイドバーの「Vulnerability alerts」の下で **Dependabot** を選び、既定ブランチの Dependabot alerts の一覧を表示します。

Dependabot が、使っている依存関係の脆弱性を知らせてくれました。さらに Dependabot には、依存関係を安全なバージョンに更新する pull request を作らせて、脆弱性への対処を助けてもらうこともできます。

アラートの 1 つについて、Dependabot に pull request を作らせて動きを見てみましょう。

### :keyboard: やること 2.3: Dependabot alert から pull request を作る

1. Dependabot alerts の一覧で「Prototype Pollution in minimist」をクリックし、詳しい情報を表示します。
1. **Create Dependabot security update** ボタンをクリックして、依存関係を更新する pull request を作ります。作成には最大 2 分ほどかかることがあります。
1. pull request が作られると、アラートのページに **Review security update** ボタンが表示されます。
1. **Review security update** ボタンをクリックして pull request を表示します。
   - pull request と **Files changed** タブで更新内容を確認できます。
1. **Conversation** タブに戻り、pull request をマージします。
1. pull request をマージしたので、Mona が作業を確認しています。少し待って、コメントを見てください。進捗と次の Step が投稿されます。
