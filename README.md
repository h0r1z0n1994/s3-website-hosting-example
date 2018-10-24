S3 WebSite Hosting Sample
====

ハンズオン用S3Webサイトホスティングのチュートリアル

## 静的ウェブサイトをセットアップする

AWS マネジメントコンソール にサインインし、Amazon S3 コンソール (https://console.aws.amazon.com/s3/) を開きます。

### ステップ1: バケットの作成とウェブサイトとしての設定

+ バケットを作成します。
ここではバケット名を一定の規則に統一するために、「性.名.seminar」とします。
例) horizono.yoshihiro.seminar

リージョンは「アジアパシフィック（東京）」を指定

+ Webサイトの設定
バケットの 「プロパティ」 ペインを開き、「Static Website Hosting」 を選択して、次の操作を行います。
「このバケットを使用してウェブサイトをホストする」 を選択します。

「インデックスドキュメント」 ボックスに、「index.html」と入力
「保存」を選択してウェブサイトの設定を保存します。

「エンドポイント」の内容を書き留めます。
※上記手順で作成している場合は「http://[lastname].[firstname].seminar.s3-website-ap-northeast-1.amazonaws.com」となるはず

### ステップ2: バケットのコンテンツを公開するバケットポリシーの追加

+ バケットの 「アクセス権限」ペインで、「バケットポリシー」 を選択します。

+ バケットポリシーエディターにbacket-policy.txtの内容をコピー＆ペーストします。

+ example-bucket を自身のバケット名に置き換えます

+ 「保存」を選択して設定を保存します。

### ステップ3: インデックスドキュメントのアップロード

+ コンソールを使用して、index.htmlをバケットにアップロードします。

### ステップ4: ウェブサイトのテスト

+ ステップ1で書き留めた「エンドポイント」の内容をブラウザのURL欄に入力します。

+ ブラウザにindex.htmlページが表示されれば、ウェブサイトのデプロイが成功しています。
