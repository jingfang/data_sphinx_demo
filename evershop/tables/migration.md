# migration
テーブル移行とは、データベース内のテーブル構造やデータの変更を管理するプロセスです。移行テーブルは、各モジュールの移行状態や実行されたスクリプトのバージョンを追跡・記録し、データベースの変更履歴を管理できます。また、異なるコンポーネントやページでのステータス表現や、レコードの作成・更新日時の自動記録が可能で、データの整合性維持に役立ちます。

| Column name | type | PK | FK | required | description | code_reference |
| --- | --- | --- | --- | --- | --- | --- |
| migration_id | int unsigned | True | False | True | <br><br>'migration'テーブルの'migration_id'列は、自動増分のAUTO_INCREMENT属性を持つ主キーとして機能します。この列は、各移行レコードを一意に識別し、新しいレコードのために値を自動的に増分するために使用されます。 | [link](../references/migration_migration_id.md) |
| module | char(255) | False | False | True | <br><br>「migration」テーブルの「module」列は、アプリケーション内の各モジュールの移行状態を追跡するために使用されます。この列は、移行が実行されたときにモジュール名を保存し、指定されたモジュールの最新バージョンを取得するために使用されます。また、同じモジュールに対して複数の移行が行われるのを防止するためにも使用されます。 | [link](../references/migration_module.md) |
| version | char(255) | False | False | True | <br><br>「migration」テーブルの「version」列は、実行された移行スクリプトのバージョンを追跡するためのものです。この列は、各モジュールの移行の最新バージョンを挿入および更新し、すでに実行されたスクリプトをスキップするために使用されます。 | [link](../references/migration_version.md) |
| status | char(255) | False | False | True | <br><br>「migration」テーブルの「status」列は、異なるコンポーネントやページで様々なステータスを表すために使用されます。この列は、出荷ステータス、支払いステータス、顧客ステータス、カテゴリステータスなどの情報を表示するために、異なるコンポーネントでプロップとして使用されます。また、「product」テーブルでステータスが1の製品をフィルタリングするためにも使用されます。 | [link](../references/migration_status.md) |
| created_at | timestamp | False | False | True | <br><br>「created_at」カラムは、各テーブルの行が作成または挿入された日時を追跡するために使用されます。このカラムは、TIMESTAMP型として定義され、デフォルト値はcurrent_timestamp()です。各行の作成時間を自動的に記録するために使用され、さまざまなコンポーネントやクエリでレコードの作成時間をフィルタリングおよび表示するためにも使用されます。 | [link](../references/migration_created_at.md) |
| updated_at | timestamp | False | False | True | <br><br>「updated_at」カラムは、テーブル内のレコードが更新された日時を自動的に記録するために使用されます。カラムは、DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMPで設定され、レコードが更新されるたびに現在の日時に更新されます。これにより、データベース内の各レコードの最新の状態を追跡するのに役立ちます。 | [link](../references/migration_updated_at.md) |
