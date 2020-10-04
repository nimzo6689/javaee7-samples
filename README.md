# Java EE 7 サンプル集

このワークスペースは、Java EE 7 のサンプルとユニットテストで構成されています。  
これらは、各技術/JSR ごとに異なるディレクトリに分類しています。

## 実行方法

サンプルは、Arquillian エコシステムを使用して、Payara でテストされています。

- Payara

  - `payara-ci-managed`

    このプロファイルは、サンプルごとに Payara サーバーをインストールし、サーバーを起動します。
    CI サーバに便利です。使用する Payara のバージョンは、`payara.version`プロパティで設定できます。
    これはデフォルトのプロファイルであり、明示的に指定する必要はありません。

**コンソールで実行するには、次のようにします。**:

1. ターミナルで、トップレベルのディレクトリで `mvn test --fail-at-end` を実行し、デフォルトプロファイルのテストを開始します。

**トップレベルのディレクトリで行うテストのサブセットのみを実行するには**:

1. トップレベルプロジェクト飲みをビルドする。: `mvn clean install -pl "test-utils,util" --also-make`
1. cd でテストしたいサブディレクトリに移動する。 （例）: `cd jaspic`
1. Maven でテストを実施。 （例）: `mvn clean test`

### 主なコーディング規約

- 新しいソースファイルを作成する際には、ライセンスヘッダを付けたりコピーしたりしないでください。
- jboss/ide-config](https://github.com/jboss/ide-config#readme) リポジトリで定義されている JBoss Community のコードフォーマットプロファイルに従ってください。
  詳細はそこで説明されており、Eclipse、IntelliJ、NetBeans 用の設定もあります。

### Small Git tips

- [fork](https://help.github.com/articles/fork-a-repo) から最新を取り込む場合、`git pull upstream master` を実行するだけで、その準備ができます。
