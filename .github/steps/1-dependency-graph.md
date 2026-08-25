## Step 1: dependency graph で依存関係を確認して追加する

**リポジトリのサプライチェーンを保護することが、なぜ重要なのか**: オープンソースの利用が加速し、ほとんどのプロジェクトが数百のオープンソース依存関係に頼っています。問題はセキュリティです。使っている依存関係に脆弱性があったらどうなるでしょうか。利用者をサプライチェーン攻撃の危険にさらすことになります。サプライチェーンを守るために最も大切なことの 1 つが、脆弱な依存関係にパッチを当て、マルウェアを置き換えることです。

GitHub には、環境内の依存関係を把握し、脆弱性を知り、パッチを当てるための機能がそろっています。GitHub のサプライチェーン機能は次のとおりです。

- Dependency graph
- Dependency review
- Dependabot alerts
- Dependabot updates
  - Dependabot security updates
  - Dependabot version updates

**dependency graph とは**: リポジトリに保存されたマニフェストファイルとロックファイル、および dependency submission API（ベータ）で登録された依存関係をまとめたものです。リポジトリごとに次を表示します。

- Dependencies（依存先）: リポジトリが依存しているエコシステムとパッケージ
- Dependents（依存元）: リポジトリに依存しているリポジトリとパッケージ

### :keyboard: やること 1.1: dependency graph が有効か確認する

**説明を開いたまま作業できるよう、ブラウザーで別のタブを開いて以下の操作を行うことをおすすめします。**

>[!NOTE]
> dependency graph は、新しいパブリックリポジトリでは既定で有効です。

1. **Settings** タブを開きます。
1. **Advanced Security**（アカウントによっては **Code security**）をクリックします。
1. **Dependency Graph** が **Enabled** になっていることを確認します。

### :keyboard: やること 1.2: 新しい依存関係を追加して dependency graph を見る

1. **Code** タブを開き、`code/src/AttendeeSite` フォルダーを探します。
1. 次の内容を、`package-lock.json` の `dependencies` マップの最後の項目として `main` ブランチにコミットします _(末尾から 3 番目の `}` の後ろ、最後の 2 つの括弧の前)_

    > 🪧 **注:** ファイルは github.com 上で直接編集してコミットできます。`.` キーを押して軽量エディターを開いて編集・コミットすることもできます。

    ```json
    ,
    "follow-redirects": {
      "version": "1.14.1",
      "resolved": "https://registry.npmjs.org/follow-redirects/-/follow-redirects-1.14.1.tgz",
      "integrity": "sha512-HWqDgT7ZEkqRzBvc2s64vSZ/hfOceEol3ac/7tKwzuvEyWx3/4UegXh5oBOIotkGsObyk3xznnSRVADBgWSQVg=="
    }
    ```

1. **Insights** タブを開きます。
1. サイドナビゲーションから **Dependency graph** を選びます。
1. **Dependencies** タブですべての依存関係を確認します。
1. `follow-redirects` を検索し、いま追加した依存関係を確認します。
   ![「follow-redirects」依存関係のスクリーンショット](https://user-images.githubusercontent.com/6351798/196288729-734e3319-c5d7-4f35-a19c-676c12f0e27d.png)
1. 依存関係を追加したので、Mona が作業を確認しています。少し待って、コメントを見てください。進捗と次の Step が投稿されます。
