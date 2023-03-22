# order_activity
「order_activity」テーブルは、データベース内の注文に関連するさまざまなアクティビティを保存・管理するために使用されます。注文関連のアクション（ステータス変更、コメント、顧客への通知など）を追跡する目的で、主キーと外部キー（「order_activity_id」や「order_activity_order_id」など）を使って注文とそれに対応するアクティビティ間の関係を確立します。また、「uuid」列を使って各レコードの一意の識別子を保存し、「created_at」と「updated_at」列を使って作成・更新のタイムスタンプを保存します。このテーブルは、注文アクティビティの履歴を維持し、注文処理や顧客とのやり取りに関する洞察を提供するために不可欠です。

| Column name | type | PK | FK | required | description | code_reference |
| --- | --- | --- | --- | --- | --- | --- |
| order_activity_id | int unsigned | True | False | True | <br><br>「order_activity_id」列は、主キーとして機能し、「order_activity_order_id」外部キーとの関係を確立するために「order_activity」テーブルで使用されます。この列は、一致する「orderId」に基づいて「order_activity」テーブルからレコードを取得するために使用され、クエリ結果の「activities」フィールド値として返される前に降順でソートされます。 | [link](../references/order_activity_order_activity_id.md) |
| uuid | varchar(36) | False | False | True | <br><br>「uuid」列は、注文活動テーブル内の各レコードに対して一意の識別子として機能します。この列は自動的に生成され、新しい行に割り当てられ、テーブル内のレコードやAPIリクエストで識別するために使用されます。NOT NULL制約と一意の制約があります。 | [link](../references/order_activity_uuid.md) |
| order_activity_order_id | int unsigned | False | True | True | <br><br>「order_activity」テーブルの「order_activity_order_id」列は、外部キー制約として機能し、2つのテーブル間の関係を確立するために「order」テーブルの「order_id」列を参照します。この列は、各アクティビティログに関連する特定の注文を識別するために使用され、コードベース全体でさまざまなクエリや挿入に使用されます。 | [link](../references/order_activity_order_activity_order_id.md) |
| comment | text | False | False | True | <br><br>「order_activity」テーブルの「comment」列は、注文に関連するさまざまなアクティビティに関するコメントを格納するために使用されます。この列は、各アクティビティのコメントを表示し、日ごとにアクティビティをグループ化し、注文ステータスの変更に関連するコメントを格納し、顧客が使用した支払い方法を示すために使用されます。 | [link](../references/order_activity_comment.md) |
| customer_notified | smallint unsigned | False | False | True | <br><br>「customer_notified」列は、注文アクティビティテーブルで顧客が通知されたかどうかを示すフラグとして機能します。この列は、注文アクティビティを保存し、顧客が通知されたかどうかを示すために使用されます。デフォルトでは値が0に設定され、将来のSendGrid設定に基づいて変更できます。 | [link](../references/order_activity_customer_notified.md) |
| created_at | timestamp | False | False | True | <br><br>「created_at」カラムは、「order_activity」テーブルにおいて、新しい注文アクティビティが作成された日時と更新された日時を記録するために使用されます。このカラムは、データベース内の注文アクティビティの作成と更新のタイムスタンプを追跡するために使用されます。 | [link](../references/order_activity_created_at.md) |
| updated_at | timestamp | False | False | True | <br><br>「order_activity」テーブルの「updated_at」列は、行が最後に更新された日時を示すためのものです。この列は、行が更新されるたびに自動的に更新され、最新の更新のタイムスタンプとして機能します。 | [link](../references/order_activity_updated_at.md) |
