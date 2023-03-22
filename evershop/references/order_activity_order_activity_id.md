| path | summary | is relevant |
| --- | --- | --- |
| [packages/evershop/src/modules/checkout/migration/Version-1.0.0.js](https://github.com/evershopcommerce/evershop/blob/4f1f4947f95e03b9cf64486a42b1669d484cba61/packages/evershop/src/modules/checkout/migration/Version-1.0.0.js) | <br><br>テーブルorder_activityのカラムorder_activity_idは、主キーとして使用されています。また、テーブルorder_activityの外部キーであるorder_activity_order_idとの関連付けにも使用されています。具体的には、order_activity_order_idは、テーブルorderのorder_idと関連付けられており、order_activityテーブルのorder_activity_idは、order_activity_order_idとの関連付けに使用されています。 | True |
| [packages/evershop/src/modules/checkout/graphql/types/Order/Order.resolvers.js](https://github.com/evershopcommerce/evershop/blob/47620ae98869cea2f1d7bf2a46af54b0a43a64fa/packages/evershop/src/modules/checkout/graphql/types/Order/Order.resolvers.js) | このコードの中で、テーブルorder_activityのカラムorder_activity_idは、activitiesフィールドのクエリで使用されています。具体的には、order_activityテーブルからorderIdが一致するレコードを取得し、order_activity_idで降順に並べ替えています。そして、取得したレコードをcamelCase関数を使って変換し、activitiesフィールドの値として返しています。 | True |
| [packages/evershop/src/modules/checkout/migration/Version-1.0.1.js](https://github.com/evershopcommerce/evershop/blob/4f1f4947f95e03b9cf64486a42b1669d484cba61/packages/evershop/src/modules/checkout/migration/Version-1.0.1.js) | このコードの中では、テーブルorder_activityのカラムorder_activity_idは使用されていません。ただし、テーブルorder_activityに新しいカラムuuidが追加され、一意キー制約が設定されています。また、既存のuuidが空の場合は、新しいuuidが生成されます。 | False |
[Back to order_activity](../tables/order_activity.md)