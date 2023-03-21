# categories
「categories」テーブルは、問題カテゴリの管理に使用されるデータベーステーブルです。各カテゴリのID、コード、タイトル、説明、表示順序、作成日時、更新日時が格納されており、問題のカテゴリ関連付けや管理に役立ちます。また、問題のソートやカテゴリの順序設定にも使用され、ユーザーは関連する問題の作成日や更新日にアクセスできます。

| Column name | type | PK | FK | required | description | code_reference |
| --- | --- | --- | --- | --- | --- | --- |
| id | uuid | True | False | True | <br><br>「categories」テーブルの「id」列はUUIDタイプであり、各カテゴリーの一意の識別子として機能します。この列は、他のテーブルとカテゴリーを関連付けるために使用されます。また、「problems」テーブルで外部キーとして使用され、問題をそれぞれのカテゴリーに関連付けるために使用されます。さらに、さまざまなクエリやモデルでカテゴリー情報を取得し、関係を定義するために使用されます。 | [link](../references/categories_id.md) |
| code | string | False | False | True | <br><br>「code」列は、カテゴリごとに一意の識別子として機能する「categories」テーブルの列です。この列は、新しいレコードの作成、検証、検索、問題のカテゴリの特定、スタッフがカテゴリを特定するために使用されます。 | [link](../references/categories_code.md) |
| title | string | False | False | True | <br><br>「categories」テーブルの「title」列は、問題が属するカテゴリのタイトルを格納するための列です。この列は、Categoryモデルのフィールドとして文字列データ型を定義し、Categoryインスタンスのタイトルプロパティにアクセスし、Categoryモデルデータをデータベースに保存するために使用されます。また、問題クエリのカテゴリフィールドでも使用され、カテゴリオブジェクトのタイトル値を表します。 | [link](../references/categories_title.md) |
| description | string | False | False | True | <br><br>「categories」テーブルの「description」列は、各カテゴリの説明を保存するために使用されます。この列は、カテゴリの作成や更新時に説明を保存および更新するために使用され、さまざまなUIコンポーネントでカテゴリの説明を表示するために使用されます。また、テスト目的でランダムな説明を生成するためにも使用されます。 | [link](../references/categories_description.md) |
| order | integer | False | False | True | <br><br>「categories」テーブルの「order」列は、カテゴリやアイテムの表示順序を決定するために使用されます。この列は、問題をカテゴリや順序でソートするために使用され、カテゴリやアイテムを順序でソートするために使用され、カテゴリやアイテムの順序を設定するために使用され、カテゴリの順序をランダムに設定するために使用されます。 | [link](../references/categories_order.md) |
| created_at | datetime | False | False | True | <br><br>「categories」テーブルの「created_at」列は、各レコードが作成されたタイムスタンプを格納するためのものです。この列は、ActiveRecordのタイムスタンプ機能によって自動的に更新され、CategoryTypeオブジェクトのフィールドとして定義されています。これにより、ユーザーはカテゴリーと関連する問題の作成日をアクセスできます。 | [link](../references/categories_created_at.md) |
| updated_at | datetime | False | False | True | <br><br>「categories」テーブルの「updated_at」列は、レコードが最後に更新された時刻を示すタイムスタンプとして機能します。この列は、ActiveRecordのタイムスタンプ機能によって自動的に更新されます。CategoryTypeオブジェクトでは、「updated_at」フィールドがこの列にマップされ、カテゴリの更新時間を表します。このフィールドは「null: false」に設定されており、常に値が存在する必要があります。 | [link](../references/categories_updated_at.md) |
