# answers
「answers」テーブルは、問題への回答を格納・追跡するデータベーステーブルで、回答の一意の識別子や内容、確認フラグ、問題ID、チームID、作成日時、更新日時などを保管します。これらの情報は、回答の検索や更新、採点、検証、スコアボード表示、チーム別の回答追跡に利用され、回答の確認状況やチームと問題の組み合わせごとの一意の回答を保証します。

| Column name | type | PK | FK | required | description | code_reference |
| --- | --- | --- | --- | --- | --- | --- |
| id | uuid | True | False | True | <br><br>「answers」テーブルの「id」列は、各回答レコードの一意の識別子として機能します。この列は主キーとして使用され、回答レコードの検索や更新、他のテーブルとの結合、およびクライアントに最新の回答IDを返すために使用されます。 | [link](../references/answers_id.md) |
| bodies | json | False | False | True | <br><br>「answers」テーブルの「bodies」列は、問題の回答を表すテキストまたはテキストの配列を格納するためのものであり、採点や検証の目的にも使用されます。この列は、回答内容を一時的に保存し、採点のために正解と比較し、回答の形式と内容を検証するために使用されます。また、回答内容をさまざまなコンポーネントで表示するためにも使用され、JSON形式で回答に関連する追加情報を格納するためにも使用されます。 | [link](../references/answers_bodies.md) |
| confirming | boolean | False | False | True | <br><br>「answers」テーブルの「confirming」列は、回答が確認されたかどうかを示すフラグとして機能します。この列は、引数として渡された値に基づいてフラグを更新し、確認された回答をフィルタリングして表示し、回答が確認されたかどうかを追跡するために使用されます。 | [link](../references/answers_confirming.md) |
| problem_id | uuid | False | True | True | <br><br>「answers」テーブルの「problem_id」列は、回答が属する問題を識別するために使用されます。この列は、新しいレコードを検索および作成するために使用され、更新するレコードを識別するためにも使用されます。また、回答を対応する問題に関連付けるために、さまざまなミューテーションやモデルで使用されます。 | [link](../references/answers_problem_id.md) |
| team_id | uuid | False | True | True | <br><br>「answers」テーブルの「team_id」列は、与えられた回答がどのチームに属するかを示し、一意のインデックスとして使用され、チームと問題の組み合わせごとに1つの回答を保証します。この「team_id」列は、スコア集計のためにチームごとに回答をグループ化し、さまざまなモデルでチームごとに回答を検索し、新しい回答がどのチームに属するかを判断するために使用されます。 | [link](../references/answers_team_id.md) |
| created_at | datetime | False | False | True | <br><br>「answers」テーブルの「created_at」列は、回答が作成された日時を示します。この列は、問題ID、チームID、作成日時とのユニークなインデックスの一部として使用され、スコアボードの表示、遅延フィルタリング、検証、回答の優先順位の決定にも使用されます。 | [link](../references/answers_created_at.md) |
| updated_at | datetime | False | False | True | <br><br>「answers」テーブルの「updated_at」列は、回答が最後に更新された日時を示します。この列はActive Recordのタイムスタンプ機能によって自動的に更新され、同じ問題とチームの組み合わせに対して複数の回答がないように一意のインデックスに含まれています。回答の更新を追跡することができます。 | [link](../references/answers_updated_at.md) |
