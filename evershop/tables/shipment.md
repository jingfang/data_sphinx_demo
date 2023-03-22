# shipment
「shipment」テーブルは、出荷情報を管理するデータベーステーブルで、出荷識別や注文との関連付け、キャリア名、追跡番号、作成日時、更新日時などの情報を格納します。このテーブルは、出荷情報の追跡や分析を可能にし、顧客が注文を追跡できるようにするためや、出荷プロセスの効率化に役立てられます。

| Column name | type | PK | FK | required | description | code_reference |
| --- | --- | --- | --- | --- | --- | --- |
| shipment_id | int unsigned | True | False | True | <br><br>「shipment」テーブルの「shipment_id」列は、特定の出荷を識別するための主キーとして機能し、また「order」テーブルに外部キーとしてリンクされ、注文の出荷情報を追跡するために使用されます。このパラメータは、URLパスに含まれ、'/orders/:order_id/shipments/:shipment_id'エンドポイントで特定の注文の出荷を更新するために使用されます。また、新しく挿入された出荷レコードを取得するためのクエリでも使用されます。 | [link](../references/shipment_shipment_id.md) |
| uuid | varchar(36) | False | False | True | <br><br>「shipment」テーブルの「uuid」列は、各出荷レコードの一意の識別子として機能します。この列は、varchar（36）データ型で定義され、NOT NULL制約とDEFAULT制約が設定されています。DEFAULT制約は、replace（uuid（）、'-''）関数を使用してランダムなUUIDを生成します。また、重複値を防止するために、UNIQUE KEYとして設定されています。APIリクエストのshipment_idパラメータに基づいて出荷レコードを取得および更新するために「uuid」列が使用され、Orderタイプのshipmentフィールドで対応する出荷レコードを取得するためにも使用されます。 | [link](../references/shipment_uuid.md) |
| shipment_order_id | int unsigned | False | True | True | <br><br>「shipment」テーブルの「shipment_order_id」列は、出荷情報を特定の注文に関連付けるために使用されます。これは、外部キーとして「order」テーブルの「order_id」列を参照します。この列は、特定の注文に関連する出荷情報を取得または挿入し、注文のステータスを「履行済み」に更新し、'updateShipment'および'Order'クエリで'order_id'に一致する出荷を検索するために使用されます。 | [link](../references/shipment_shipment_order_id.md) |
| carrier_name | varchar(255) | False | False | False | <br><br>「carrier_name」列は、出荷に使用されたキャリアの名前を格納する「shipment」テーブルの列です。この列は、対応するレコードの値を更新し、新しいレコードを挿入し、出荷を追加または完了するためのフォームで選択可能なオプションとして表示するために使用されます。また、出荷情報を表すJSONオブジェクトの文字列プロパティとして定義されています。 | [link](../references/shipment_carrier_name.md) |
| tracking_number | varchar(255) | False | False | False | <br><br>「shipment」テーブルの「tracking_number」列は、各出荷のキャリアの追跡番号を格納するためのものです。この列は、出荷テーブル内の出荷の追跡番号を更新するために使用され、顧客が注文を追跡することを可能にするためにも使用されます。 | [link](../references/shipment_tracking_number.md) |
| created_at | timestamp | False | False | True | <br><br>「created_at」カラムは、新しい出荷が作成されたときに自動的にタイムスタンプを挿入し、出荷が更新されたときに更新されます。これにより、出荷の作成日と更新日を追跡することができます。このカラムは、出荷データの追跡と分析を可能にするために使用されます。 | [link](../references/shipment_created_at.md) |
| updated_at | timestamp | False | False | True | <br><br>「updated_at」カラムは、「shipment」テーブル内のレコードが更新された日時を記録するために使用されます。このカラムは、配送情報が更新された日時を示すために特に使用されます。 | [link](../references/shipment_updated_at.md) |
