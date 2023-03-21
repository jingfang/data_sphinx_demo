# attachments
添付ファイルテーブル:

「添付ファイル」テーブルは、ユーザーがアップロードしたファイル（ドキュメント、画像、その他のファイルタイプ）を保存・管理するために使用されます。このテーブルには、元のファイル名、一意の識別トークン、実際のファイルデータ、ファイルが所属するチーム、作成・更新のタイムスタンプ、コンテンツタイプ、ファイルサイズなどのメタデータを格納するためのさまざまな列が含まれています。このテーブルの目的は、アプリケーション内のユーザーやチームのファイル管理、検証、取得を容易にすることです。

| Column name | type | PK | FK | required | description | code_reference |
| --- | --- | --- | --- | --- | --- | --- |
| id | uuid | True | False | True | <br><br>「No input provided. Please provide a concise summary to develop a comprehensive column description.」は、入力がない場合に表示されるエラーメッセージです。要約すると、このメッセージは、コラムの説明を開発するために簡潔な要約を提供するように求めていることを示しています。 | [link](../references/attachments_id.md) |
| filename | string | False | False | True | <br><br>「filename」列は、アップロードされたファイルの元のファイル名を保存し、添付ファイルを識別するために使用されます。この列は、新しいAttachmentオブジェクトを作成し、ファイル名の存在を検証し、GraphQL AttachmentTypeの「filename」フィールドを定義するために使用されます。また、「token_with_ext」メソッドでファイル拡張子と組み合わせて一意のトークンを生成するために使用されます。 | [link](../references/attachments_filename.md) |
| token | string | False | False | True | <br><br>「トークン」列は、添付ファイルのテーブルにおいて、一意の識別子を生成するために「has_secure_token」メソッドによって使用されます。これは、ファイル名を一意にし、ファイル形式を検証し、重複ファイルを防止するために使用されます。また、ユーザーのファイルダウンロードを認証するためにも使用されます。GraphQLの「AttachmentType」オブジェクトにおいて、非nullフィールドとして定義され、データベーススキーマには一意のインデックス制約が設定されています。 | [link](../references/attachments_token.md) |
| data | binary | False | False | True | <br><br>「attachments」テーブルの「data」列は、実際のファイルデータを保存し、検証に必要です。この列は、ファイルをアップロードする際にファイルデータを保存し、表示アクションでファイルデータを返すために使用されます。また、「post_mutation」メソッドの「team」フィールドと関連付けられており、データの取得に必要な場合があります。 | [link](../references/attachments_data.md) |
| team_id | uuid | False | True | True | <br><br>「attachments」テーブルの「team_id」列は、添付ファイルが属するチームを示すために使用されます。これは、「teams」テーブルの「id」列を参照する外部キーとして機能します。この「team_id」列は、RecordLoaderを使用して対応する「Team」オブジェクトをロードし、「ScoreboardType」の「team」フィールドとして設定するために使用されます。また、関係を表すインデックスに含まれ、GraphQLフィールドとして「AttachmentType」で定義されています。 | [link](../references/attachments_team_id.md) |
| created_at | datetime | False | False | True | <br><br>「created_at」カラムは、「attachments」テーブルにおいてファイルがアップロードされた日時を保存し、ファイルの順序を決定するために使用されます。このカラムは、チームにアクセス可能なすべての添付ファイルを取得し、日付に基づいてペナルティをフィルタリングし、添付ファイルの作成日を「AttachmentType」フィールドに表示するために使用されます。 | [link](../references/attachments_created_at.md) |
| updated_at | datetime | False | False | True | <br><br>「updated_at」カラムは、アタッチメントテーブル内のレコードが最後に更新された日時を示すものであり、ActiveRecordのタイムスタンプ機能によって自動的に更新されます。このカラムは、最新のアップロードされた添付ファイルを追跡するために使用され、また「TeamType」オブジェクトに関連する添付ファイルを取得するための「has_many」関連付けに使用されます。 | [link](../references/attachments_updated_at.md) |
| content_type | string | False | False | True | <br><br>「content_type」列は、アップロードされたファイルのMIMEタイプを表します。この列は、レスポンスのContent-Typeヘッダーを設定し、画像をインライン表示し、バリデーションを通じて値の存在を確認するために使用されます。 | [link](../references/attachments_content_type.md) |
| size | integer | False | False | True | <br><br>この場合、出力は以下のようになります：<br>カラムの目的：「attachments」テーブルの「size」カラムは、アップロードされたファイルのサイズを格納し、検証および表示目的に使用されます。<br>使用法：「size」カラムは、アップロードされたファイルが20MB以下であることを検証し、GraphQLフィールドとして表示され、また「team」モデルに関連付けられます。 | [link](../references/attachments_size.md) |
