| path | summary | is relevant |
| --- | --- | --- |
| [packages/evershop/src/modules/checkout/migration/Version-1.0.0.js](https://github.com/evershopcommerce/evershop/blob/4f1f4947f95e03b9cf64486a42b1669d484cba61/packages/evershop/src/modules/checkout/migration/Version-1.0.0.js) | <br><br>テーブルshipmentのカラムcreated_atは、新しい出荷が作成されたときに自動的にタイムスタンプが挿入されます。また、このカラムは、出荷が更新されたときにも自動的に更新されます。これにより、出荷の作成日時と更新日時が記録され、必要に応じて追跡できるようになります。 | True |
| [packages/evershop/src/modules/auth/migration/Version-1.0.0.js](https://github.com/evershopcommerce/evershop/blob/4f1f4947f95e03b9cf64486a42b1669d484cba61/packages/evershop/src/modules/auth/migration/Version-1.0.0.js) | このコードには、テーブルshipmentが含まれていないため、カラムcreated_atは使用されていません。 | False |
| [packages/evershop/src/modules/checkout/api/salestatistic/loadData.js](https://github.com/evershopcommerce/evershop/blob/bc7ee43cdadfb8a00e896c8f753da75938507854/packages/evershop/src/modules/checkout/api/salestatistic/loadData.js) | <br><br>このコードの中では、テーブルshipmentのカラムcreated_atは使用されていません。代わりに、テーブルorderのカラムcreated_atが使用されています。具体的には、各期間の開始日時と終了日時を計算するために使用されています。 | False |
| [packages/evershop/src/modules/customer/migration/Version-1.0.0.js](https://github.com/evershopcommerce/evershop/blob/4f1f4947f95e03b9cf64486a42b1669d484cba61/packages/evershop/src/modules/customer/migration/Version-1.0.0.js) | このコードにはテーブルshipmentが含まれておらず、カラムcreated_atも使用されていません。したがって、このコードの中でテーブルshipmentのカラムcreated_atは使用されていません。 | False |
| [packages/evershop/bin/install/createMigrationTable.js](https://github.com/evershopcommerce/evershop/blob/0e00f5a5fda1ecd14d16ff1143f53f5befbfe32b/packages/evershop/bin/install/createMigrationTable.js) | <br><br>このコードの中では、テーブルshipmentのカラムcreated_atは使用されていません。代わりに、migrationテーブルのカラムcreated_atが使用されています。 | False |
| [extensions/productComment/migration/Version-1.0.0.js](https://github.com/evershopcommerce/evershop/blob/4d620e55db5fe1ba1ecc21112381198aaf40bbf0/extensions/productComment/migration/Version-1.0.0.js) | <br><br>このコードの中では、テーブルshipmentのカラムcreated_atは使用されていません。代わりに、テーブルproduct_commentのカラムcreated_atが使用されています。このカラムは、コメントが作成された日時を示すために使用されます。 | False |
| [packages/evershop/src/modules/catalog/migration/Version-1.0.0.js](https://github.com/evershopcommerce/evershop/blob/4f1f4947f95e03b9cf64486a42b1669d484cba61/packages/evershop/src/modules/catalog/migration/Version-1.0.0.js) | このコードには、テーブルshipmentやカラムcreated_atに関する記述はありません。したがって、このコードの中でテーブルshipmentのカラムcreated_atは使用されていません。 | False |
| [packages/evershop/src/modules/checkout/graphql/types/Order/Order.resolvers.js](https://github.com/evershopcommerce/evershop/blob/47620ae98869cea2f1d7bf2a46af54b0a43a64fa/packages/evershop/src/modules/checkout/graphql/types/Order/Order.resolvers.js) | このコードの中で、テーブルshipmentのカラムcreated_atは使用されていません。 | False |
| [packages/evershop/src/modules/cms/migration/Version-1.0.0.js](https://github.com/evershopcommerce/evershop/blob/4f1f4947f95e03b9cf64486a42b1669d484cba61/packages/evershop/src/modules/cms/migration/Version-1.0.0.js) | このコードには、テーブルshipmentやcreated_atというカラムは含まれていません。したがって、created_atは使用されていません。 | False |
| [packages/evershop/src/modules/promotion/migration/Version-1.0.0.js](https://github.com/evershopcommerce/evershop/blob/4f1f4947f95e03b9cf64486a42b1669d484cba61/packages/evershop/src/modules/promotion/migration/Version-1.0.0.js) | このコードにはテーブルshipmentが含まれておらず、カラムcreated_atも使用されていません。したがって、このコードの中でテーブルshipmentのカラムcreated_atは使用されていません。 | False |
| [packages/evershop/src/modules/customer/pages/admin/customerGrid/Grid.js](https://github.com/evershopcommerce/evershop/blob/7d41ed3f57a1ac7d8b02cb86fd8b01508e77bcf6/packages/evershop/src/modules/customer/pages/admin/customerGrid/Grid.js) | <br><br>このコードの中には、テーブルshipmentのカラムcreated_atは含まれていません。したがって、このコードではcreated_atを使用していません。 | False |
[Back to shipment](../tables/shipment.md)