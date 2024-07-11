###Instruments Shop

## Overview

This DAML project was based on a music instruments store.
The customer can request orders to the shop.
The store will then propose a quote for the order.
After the customer accepts the quote, the store can mark it as complete.


## Main flow:

1. Customer creates an order request. ( choice CreateOrderRequest )
3. Store accepts the order request and creates an order quote. ( choice AceptedOrderAndQuote )
4. Customer accepts the quote. ( choice AceptOrderQuote )
5. Store marks teh quote as completed. ( choice CompleteOrderQuote )


## Other choices:

1. Customer may cancel their order request. ( choice CancelOrderRequest )
2. Customer may update the instruments in their order request. ( choice UpdateOrderRequestInstruments )
3. Store may reject the order request. ( choice RejectOrderRequest )
4. Customer may reject the order quote. ( choice RejectOrderQuote )
5. Store may check the record for existing quotes. ( nonconsuming choice CheckQuotes )


## Compiling and testing:

To initialize the sandbox and start navigator: 
$ daml start

Test scripts were written in the Test.daml file.
