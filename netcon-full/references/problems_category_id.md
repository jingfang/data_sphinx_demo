| path | summary | is relevant |
| --- | --- | --- |
| [api/app/graphql/types/problem_type.rb](https://github.com/kei-mo/llm-demo-netcon-score-server/blob/fa851159fa03ab03b0a37fa9ccd3b122d7121109/api/app/graphql/types/problem_type.rb) | <br><br>このコードでは、テーブルproblemsのカラムcategory_idは、Types::ProblemTypeのcategoryというフィールドで参照されています。また、belongs_to :categoryというアソシエーションも定義されており、category_idを使用してcategoriesテーブルとの関連付けを行っています。具体的には、category_idがある問題が属するカテゴリーを取得するために使用されます。 | True |
| [api/db/schema.rb](https://github.com/kei-mo/llm-demo-netcon-score-server/blob/fa851159fa03ab03b0a37fa9ccd3b122d7121109/api/db/schema.rb) | <br><br>テーブルproblemsのカラムcategory_idは、問題が属するカテゴリーを示すために使用されます。このカラムは、categoriesテーブルのidと関連付けられており、問題がどのカテゴリーに属するかを示すために使用されます。 | True |
[Back to problems](../tables/problems.md)