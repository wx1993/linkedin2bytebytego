# Payment System
> Today is Cyber Monday. Here is how money moves when you click the Buy button on Amazon or any of your favorite shopping websites. 

```js
const is_pc = false
const platform = is_pc ? 'pc' : 'mobile'
```

<img src="/system-design/payment.jpeg" width="500" />

I posted the same diagram last week for an overview and a few people asked me about the detailed steps, so here you go: 

1. When a user clicks the “Buy” button, a payment event is generated and sent to the payment service.

2. The payment service stores the payment event in the database.

3. Sometimes a single payment event may contain several payment orders. For example, you may select products from multiple sellers in a single checkout process. The payment service will call the payment executor for each payment order.
