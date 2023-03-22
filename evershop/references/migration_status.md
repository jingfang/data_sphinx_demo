| path | summary | is relevant |
| --- | --- | --- |
| [packages/evershop/src/components/admin/checkout/orderEdit/Shipment.js](https://github.com/evershopcommerce/evershop/blob/7d41ed3f57a1ac7d8b02cb86fd8b01508e77bcf6/packages/evershop/src/components/admin/checkout/orderEdit/Shipment.js) | <br><br>テーブルmigrationのカラムstatusは、Shipmentコンポーネントの中で、Areaコンポーネントのpropsとして渡され、Statusコンポーネントに渡されて表示されます。具体的には、shipmentStatusというプロパティがStatusコンポーネントのpropsとして渡され、その中のbadgeとnameがそれぞれステータスの色とテキストとして表示されます。また、Actionsコンポーネントでもstatusプロパティとして渡され、ステータスに応じて表示されるアクションが変化します。 | True |
| [packages/evershop/src/modules/customer/pages/admin/customerEdit%2BcustomerNew/General.js](https://github.com/evershopcommerce/evershop/blob/7d41ed3f57a1ac7d8b02cb86fd8b01508e77bcf6/packages/evershop/src/modules/customer/pages/admin/customerEdit%2BcustomerNew/General.js) | このコードの中で、テーブルmigrationのカラムstatusは、顧客のステータスを表示するために使用されています。具体的には、Statusコンポーネントで顧客のステータスが表示されます。顧客のステータスが1の場合は「Enabled」、それ以外の場合は「Disabled」と表示されます。ただし、PropTypesの定義に誤りがあり、statusの型がstringになっているため、正しくはnumber型であるべきです。 | True |
| [packages/evershop/src/components/admin/checkout/orderGrid/rows/PaymentStatus.js](https://github.com/evershopcommerce/evershop/blob/7d41ed3f57a1ac7d8b02cb86fd8b01508e77bcf6/packages/evershop/src/components/admin/checkout/orderGrid/rows/PaymentStatus.js) | <br><br>このコードでは、テーブルmigrationのカラムstatusが、PaymentStatusRowコンポーネントのpropsとして渡され、Badgeコンポーネントのtitle、variant、progressの値として使用されています。具体的には、status.nameがBadgeコンポーネントのtitleとして、status.badgeがBadgeコンポーネントのvariantとして、status.progressがBadgeコンポーネントのprogressとして使用されます。 | True |
| [packages/evershop/src/components/admin/checkout/orderGrid/rows/ShipmentStatus.js](https://github.com/evershopcommerce/evershop/blob/7d41ed3f57a1ac7d8b02cb86fd8b01508e77bcf6/packages/evershop/src/components/admin/checkout/orderGrid/rows/ShipmentStatus.js) | <br><br>このコードでは、テーブルmigrationのカラムstatusを受け取り、それを表示するために使用されています。具体的には、ShipmentStatusRowコンポーネントがレンダリングされる際に、statusプロパティが渡され、その値がBadgeコンポーネントのtitleプロパティとして使用されます。つまり、statusは出荷状況を表す文字列であり、Badgeコンポーネントによって表示されるバッジのタイトルとして使用されます。 | True |
| [packages/evershop/src/modules/catalog/pages/admin/categoryEdit%2BcategoryNew/Status.js](https://github.com/evershopcommerce/evershop/blob/7d41ed3f57a1ac7d8b02cb86fd8b01508e77bcf6/packages/evershop/src/modules/catalog/pages/admin/categoryEdit%2BcategoryNew/Status.js) | このコードの中では、テーブルmigrationのカラムstatusは、カテゴリーの状態を表すために使用されています。具体的には、カテゴリーの有効/無効の状態を示すために、Fieldコンポーネントのラジオボタンの値として使用されています。また、includeInNavというカラムも同様に、ストアメニューに含めるかどうかを示すために使用されています。 | True |
| [packages/evershop/src/modules/cms/pages/admin/cmsPageEdit%2BcmsPageNew/StatusAndLayout.js](https://github.com/evershopcommerce/evershop/blob/7d41ed3f57a1ac7d8b02cb86fd8b01508e77bcf6/packages/evershop/src/modules/cms/pages/admin/cmsPageEdit%2BcmsPageNew/StatusAndLayout.js) | <br><br>このコードの中では、テーブルmigrationのカラムstatusは、CMSページのステータスを表すために使用されています。具体的には、`<Field>`コンポーネントの`name`プロパティに`status`が指定されており、`cmsPage?.status`がその値として渡されています。また、`propTypes`にも`cmsPage`オブジェクトの`status`プロパティが定義されています。 | True |
| [packages/evershop/src/modules/checkout/api/addCartItem/addItemToCart.js](https://github.com/evershopcommerce/evershop/blob/bc7ee43cdadfb8a00e896c8f753da75938507854/packages/evershop/src/modules/checkout/api/addCartItem/addItemToCart.js) | <br><br>このコードの中では、テーブルmigrationのカラムstatusは、商品を取得する際に使用されています。具体的には、以下のように、商品のステータスが1である商品を取得するために使用されています。<br><br>```<br>const product = await select()<br>  .from('product')<br>  .where('sku', '=', sku)<br>  .and('status', '=', 1)<br>  .load(pool);<br>``` | True |
| [packages/evershop/src/modules/checkout/graphql/types/Status/Status.resolvers.js](https://github.com/evershopcommerce/evershop/blob/bc7ee43cdadfb8a00e896c8f753da75938507854/packages/evershop/src/modules/checkout/graphql/types/Status/Status.resolvers.js) | このコードの中では、テーブルmigrationのカラムstatusは直接使われていません。代わりに、`getConfig`関数を使用して、注文の出荷ステータスと支払いステータスのリストを取得し、それらのステータスのコード、名前、バッジ、進捗を返すために使用されています。したがって、このコードは、注文のステータスを管理するために、テーブルmigrationのカラムstatusを直接使用するのではなく、設定ファイルからステータスを取得する方法を提供しています。 | False |
| [packages/evershop/src/modules/checkout/graphql/types/Status/Status.graphql](https://github.com/evershopcommerce/evershop/blob/0e00f5a5fda1ecd14d16ff1143f53f5befbfe32b/packages/evershop/src/modules/checkout/graphql/types/Status/Status.graphql) | <br><br>このコードでは、テーブルmigrationのカラムstatusは直接使用されていません。ただし、`PaymentStatus`と`ShipmentStatus`タイプは、支払いや出荷の状態を表すために使用されるため、間接的にstatusと関連しています。また、`shipmentStatusList`と`paymentStatusList`クエリは、それぞれ出荷状況と支払い状況のリストを返すため、これらのクエリもstatusと関連しています。 | False |
| [packages/evershop/src/modules/checkout/pages/admin/orderGrid/Grid.js](https://github.com/evershopcommerce/evershop/blob/7d41ed3f57a1ac7d8b02cb86fd8b01508e77bcf6/packages/evershop/src/modules/checkout/pages/admin/orderGrid/Grid.js) | このコードの中で、テーブルmigrationのカラムstatusは使用されていません。 | False |
| [packages/evershop/src/modules/checkout/api/createShipment/createShipment.js](https://github.com/evershopcommerce/evershop/blob/bc7ee43cdadfb8a00e896c8f753da75938507854/packages/evershop/src/modules/checkout/api/createShipment/createShipment.js) | このコードの中で、テーブルmigrationのカラムstatusは使用されていません。 | False |
| [packages/evershop/src/lib/middleware/tests/unit/404page.handling.test.js](https://github.com/evershopcommerce/evershop/blob/0e00f5a5fda1ecd14d16ff1143f53f5befbfe32b/packages/evershop/src/lib/middleware/tests/unit/404page.handling.test.js) | このコードにはテーブルmigrationのカラムstatusに関する記述はありません。 | False |
| [packages/evershop/src/modules/checkout/pages/admin/orderEdit/ShipmentStatus.js](https://github.com/evershopcommerce/evershop/blob/7d41ed3f57a1ac7d8b02cb86fd8b01508e77bcf6/packages/evershop/src/modules/checkout/pages/admin/orderEdit/ShipmentStatus.js) | このコードの中では、テーブルmigrationのカラムstatusは使用されていません。コード内でshipmentStatusという名前のプロパティが使用されていますが、これはGraphQLクエリで取得されたオブジェクトのプロパティであり、テーブルmigrationのカラムstatusとは関係ありません。 | False |
| [packages/evershop/src/modules/checkout/pages/admin/orderEdit/PaymentStatus.js](https://github.com/evershopcommerce/evershop/blob/7d41ed3f57a1ac7d8b02cb86fd8b01508e77bcf6/packages/evershop/src/modules/checkout/pages/admin/orderEdit/PaymentStatus.js) | このコードの中では、テーブルmigrationのカラムstatusは使用されていません。コード内で使用されているのは、orderオブジェクトのpaymentStatusプロパティです。このプロパティは、GraphQLクエリで取得され、Badgeコンポーネントのpropsとして渡されています。 | False |
| [packages/evershop/src/modules/paypal/api/paypalAuthorizePayment/[bodyParser]authorize.js](https://github.com/evershopcommerce/evershop/blob/bc7ee43cdadfb8a00e896c8f753da75938507854/packages/evershop/src/modules/paypal/api/paypalAuthorizePayment/[bodyParser]authorize.js) | <br><br>このコードの中では、テーブルmigrationのカラムstatusは使用されていません。 | False |
| [packages/evershop/src/modules/base/api/global/[apiResponse]apiErrorHandler.js](https://github.com/evershopcommerce/evershop/blob/bc7ee43cdadfb8a00e896c8f753da75938507854/packages/evershop/src/modules/base/api/global/[apiResponse]apiErrorHandler.js) | このコードにはテーブルmigrationのカラムstatusに関する記述はありません。 | False |
| [packages/evershop/src/modules/catalog/pages/admin/productEdit%2BproductNew/Status.js](https://github.com/evershopcommerce/evershop/blob/7d41ed3f57a1ac7d8b02cb86fd8b01508e77bcf6/packages/evershop/src/modules/catalog/pages/admin/productEdit%2BproductNew/Status.js) | このコードの中で、テーブルmigrationのカラムstatusは直接使われていません。ただし、このコードは商品のステータスと可視性を管理するために、productオブジェクトのstatusとvisibilityプロパティを使用しています。これらのプロパティは、おそらくデータベースのproductテーブルのカラムと対応していますが、直接的にはテーブルmigrationのカラムstatusとは関係ありません。 | False |
| [packages/evershop/src/modules/catalog/api/createVariantGroup/[bodyParser]saveGroup.js](https://github.com/evershopcommerce/evershop/blob/bc7ee43cdadfb8a00e896c8f753da75938507854/packages/evershop/src/modules/catalog/api/createVariantGroup/[bodyParser]saveGroup.js) | このコードの中では、テーブルmigrationのカラムstatusは使用されていません。 | False |
| [packages/evershop/src/modules/catalog/api/updateAttribute/finish[apiResponse].js](https://github.com/evershopcommerce/evershop/blob/bc7ee43cdadfb8a00e896c8f753da75938507854/packages/evershop/src/modules/catalog/api/updateAttribute/finish[apiResponse].js) | このコードの中で、テーブルmigrationのカラムstatusは使用されていません。 | False |
| [packages/evershop/src/modules/paypal/api/paypalCapturePayment/[bodyParser]capture.js](https://github.com/evershopcommerce/evershop/blob/bc7ee43cdadfb8a00e896c8f753da75938507854/packages/evershop/src/modules/paypal/api/paypalCapturePayment/[bodyParser]capture.js) | <br><br>このコードの中で、テーブルmigrationのカラムstatusは使用されていません。 | False |
| [packages/evershop/src/modules/catalog/api/updateCategory/finish[apiResponse].js](https://github.com/evershopcommerce/evershop/blob/bc7ee43cdadfb8a00e896c8f753da75938507854/packages/evershop/src/modules/catalog/api/updateCategory/finish[apiResponse].js) | このコードの中で、テーブルmigrationのカラムstatusは使用されていません。 | False |
| [packages/evershop/src/modules/catalog/api/deleteAttributeGroup/deleteAttributeGroup.js](https://github.com/evershopcommerce/evershop/blob/bc7ee43cdadfb8a00e896c8f753da75938507854/packages/evershop/src/modules/catalog/api/deleteAttributeGroup/deleteAttributeGroup.js) | このコードの中では、テーブルmigrationのカラムstatusは使用されていません。 | False |
| [packages/evershop/src/modules/catalog/api/updateProduct/finish[apiResponse].js](https://github.com/evershopcommerce/evershop/blob/bc7ee43cdadfb8a00e896c8f753da75938507854/packages/evershop/src/modules/catalog/api/updateProduct/finish[apiResponse].js) | このコードの中で、テーブルmigrationのカラムstatusは使用されていません。 | False |
| [packages/evershop/src/modules/paypal/api/getPaymentMethods/registerPaypal[sendMethods].js](https://github.com/evershopcommerce/evershop/blob/bc7ee43cdadfb8a00e896c8f753da75938507854/packages/evershop/src/modules/paypal/api/getPaymentMethods/registerPaypal[sendMethods].js) | <br><br>このコードの中では、テーブルmigrationのカラムstatusは使用されていません。代わりに、getSetting関数を使用して、paypalPaymentStatusという名前の設定値を取得しています。この設定値は、Paypal支払いが有効になっているかどうかを示すために使用されます。 | False |
| [packages/evershop/src/modules/stripe/api/getPaymentMethods/registerStripe[sendMethods].js](https://github.com/evershopcommerce/evershop/blob/bc7ee43cdadfb8a00e896c8f753da75938507854/packages/evershop/src/modules/stripe/api/getPaymentMethods/registerStripe[sendMethods].js) | <br><br>このコードの中では、テーブルmigrationのカラムstatusは使用されていません。コード内で使用されているのは、別のテーブル（settingテーブル）のstripePaymentStatusカラムの値です。 | False |
| [packages/evershop/src/modules/cod/api/codCapturePayment/[bodyParser]capture.js](https://github.com/evershopcommerce/evershop/blob/bc7ee43cdadfb8a00e896c8f753da75938507854/packages/evershop/src/modules/cod/api/codCapturePayment/[bodyParser]capture.js) | <br><br>このコードの中で、テーブルmigrationのカラムstatusは使用されていません。 | False |
| [packages/evershop/src/lib/middleware/tests/unit/delegate.test.js](https://github.com/evershopcommerce/evershop/blob/0e00f5a5fda1ecd14d16ff1143f53f5befbfe32b/packages/evershop/src/lib/middleware/tests/unit/delegate.test.js) | このコードの中で、テーブルmigrationのカラムstatusは使用されていません。 | False |
| [packages/evershop/src/modules/checkout/api/updateShipment/updateShipment.js](https://github.com/evershopcommerce/evershop/blob/bc7ee43cdadfb8a00e896c8f753da75938507854/packages/evershop/src/modules/checkout/api/updateShipment/updateShipment.js) | このコードの中で、テーブルmigrationのカラムstatusは使用されていません。 | False |
| [packages/evershop/src/modules/cms/api/fileDelete/deleteFile.js](https://github.com/evershopcommerce/evershop/blob/bc7ee43cdadfb8a00e896c8f753da75938507854/packages/evershop/src/modules/cms/api/fileDelete/deleteFile.js) | このコードにはテーブルmigrationのカラムstatusに関する記述はありません。 | False |
| [packages/evershop/src/modules/promotion/api/deleteCoupon/deleteCoupon.js](https://github.com/evershopcommerce/evershop/blob/bc7ee43cdadfb8a00e896c8f753da75938507854/packages/evershop/src/modules/promotion/api/deleteCoupon/deleteCoupon.js) | <br><br>このコードの中では、テーブルmigrationのカラムstatusは使用されていません。 | False |
[Back to migration](../tables/migration.md)