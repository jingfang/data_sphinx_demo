| path | summary | is relevant |
| --- | --- | --- |
| [packages/evershop/src/modules/checkout/migration/Version-1.0.0.js](https://github.com/evershopcommerce/evershop/blob/4f1f4947f95e03b9cf64486a42b1669d484cba61/packages/evershop/src/modules/checkout/migration/Version-1.0.0.js) | <br><br>このコードの中で、テーブルpayment_transactionのカラムparent_transaction_idは、支払いトランザクションの親トランザクションIDを格納するために使用されます。このカラムは、支払いトランザクションが親トランザクションに関連している場合にのみ使用されます。例えば、支払いトランザクションが返金トランザクションである場合、親トランザクションIDは元の支払いトランザクションのIDになります。 | True |
[Back to payment_transaction](../tables/payment_transaction.md)