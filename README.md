# Amazon RDS+EC2+PGroonga+ロジカルレプリケーションを使った低コスト高速全文検索

PostgreSQL で使用できる全文検索の拡張に PGroonga という高速で高性能な拡張があります。 PGroonga は、全言語対応の超高速全文検索機能を PostgreSQL で使えるようにする拡張で、 安定して高速で、かつ高機能（同義語、表記ゆれや異字体への対応、類似文書検索などが使えます）です。

Amazon RDS は Amazon がクラウド上で提供する RDBS サービスで、データベースのインストールや パッチ適用、スケールアウト、バックアップなどを Amazon が面倒をみてくれるため、 運用上の手間を大幅に減らすことができます。

Amazon RDS は、とても便利なのですが、拡張機能を自由にインストールすることができません。 以下の URL の一覧にある拡張しか使えません。
https://docs.aws.amazon.com/ja_jp/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html#PostgreSQL.Concepts.General.FeatureSupport.Extensions.11x

PGroonga も使えないため、日本語を始めとする多言語対応の超高速全文検索機能を Amazon RDS では使うことができません。

そこで、PostgreSQL 10 から使えるようになった、ロジカルレプリケーションと Amazon EC2 上にインストールした PostgreSQL と PGroonga を使って RDS のメリットである、 運用の負担を少なくしつつ、PGroonga を使用して高速で高機能な全文検索ができるような構成を考えました。

本発表では、どのような構成で Amazon RDS のメリットを活かしつつ、Amazon EC2 上で PGroonga を使った全文検索ができるのかを紹介します。

## ライセンス

### スライド

CC BY-SA 4.0

原著作者：堀本泰弘

### Groonga・PGroonga・Mroonga・Rroongaのロゴ

CC BY 3.0

原著作者：Groongaプロジェクト

### クリアコードのロゴ

CC BY-SA 4.0

原著作者：株式会社クリアコード

### PostgreSQL Elephant ロゴ

The PostgreSQL Licence

原著作者：The PostgreSQL Community Association of Canada

## 作者向け

### 表示

    rake

### 公開

    rake publish

## 閲覧者向け

### インストール

    gem install rabbit-slide-komainu8-postgresql-conference-japan-2019

### 表示

    rabbit rabbit-slide-komainu8-postgresql-conference-japan-2019.gem

