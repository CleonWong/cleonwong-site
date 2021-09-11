---
layout: post
title: "Order Book"
date: 2021-07-07 14:54:00 +0800
tags: finance
categories: my-notes
pretext:
thanks:
---

_Note:_

- "Markets" here refer to centralised markets (as opposed to decentralised markets).
- "Order book" here refers to limit order book (as opposed to [other types of order books](https://www.stocksbaazigar.com/types-of-order-books/))

_What you should know:_

- It pays to know what an [Order] is when trying to understand order books.

<br />

---

##### What is an "order book"

An **order book** is a list of buy and sell orders for an asset sorted by price level.

Specifically, buy orders are sorted with the highest bid price at the top of the book, while sell orders are sorted with the lowest ask price at the top of the book. This is a visual representation of the **price-time priority** that is typically used to **match** orders.

Buy orders with the highest bid price has the highest priority, while sell orders with the lowest ask price has the highest priority. This method of matching and filling orders seek to maximise allocative efficiency, as the trader with the highest bid price values the asset the most (willing to pay the most money) while the trader with the lowest ask price values the asset the least (willing to accept the least money).

[This answer on Quora](https://www.quora.com/How-do-exchanges-match-limit-orders) gives a simple example on how a limit order is typically matched.

Another way I like to think about order books is that it shows _the best potential_ prices that buyers and sellers are willing to transact at. [This answer on StackExchange](https://money.stackexchange.com/questions/1063/can-someone-explain-a-stocks-bid-vs-ask-price-relative-to-current-price) provides an intuitive alternative explanation of what an order book is.

Generally, bid and ask prices on an order book never matches in any market at any one point in time because overlapping bids and asks are matched and filled, hence they are removed from the order book.

##### Examples of exchanges that use order books to settle orders

1. Traditional, high-volume, centralised stock exchanges like the New York Stock Exchange and NASDAQ.
2. Coinbase (still a centralised exchange but for cryptocurrencies).
3. Binance (still a centralised exchange but for cryptocurrencies).

<br />

---

##### What information does the order book reveal about the market for that asset?

###### Market depth

The **market depth** measures the volume of limit orders in real time. It determines the market’s ability to handle large market orders without the price of an asset being impacted too much. [This article on Bybit](https://blog.bybitglobal.com/en-us/learn/order-book-explained-for-beginners/) provides a simple illustration of the effects of market depth on asset price.

###### Spread

The **bid-ask spread (or spread)** is the difference between the highest price a buyer is willing to pay for an asset and the lowest price a seller is willing to accept for the asset.

The bid-ask spread helps us examine liquidity in underlying asset because it tells us how easy it is to buy and sell the asset (specifically, how easy it is to match buy and sell orders).

<br />

---

##### When is it good to use an order book to settle orders?

###### When the market for the asset is liquid

A liquid market means that there are many buyers (buy orders) and sellers (sell orders) present. With a large quantity of buy and sell orders, it becomes more possible to have bid and ask prices that closely match each other. This means transactions can take place easily (because orders are matched easily) and large transactions can happen with relatively low slippage.

<br />

---

##### When is it bad to use an order book to settle orders?

###### When the market for the asset is illiquid

An illiquid market means there are few buy and sell orders. It is then more likely to have a large bid-ask spread and that the bid and ask prices don't match (when the highest bid price is lower than the lowest ask price, transactions cannot happen). Depending on how the exchange deals with the large spread, transactions using this order book model can still happen but it usually results in more volatile prices of the asset.

###### When the asset has to be traded "on-chain" (e.g. cryptocurrencies)

<br />

---

##### Future food for thought

The **current** stock price you're referring to is actually the price of the _last trade_. It is a _historical_ price – but during market hours, that's usually mere seconds ago for very liquid stocks.
