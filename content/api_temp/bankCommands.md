---
weight: 12
title: Get a Specific Kitten
---
# Bank Commands

## openBank()

> Overloads:

```java
utils.bank.openBank();
```

> Examples:

```java
if(!utils.bank.isOpen()) {
    utils.bank.openBank();
}
```

Opens the bank interface for the player.

<aside class="notice">Does nothing if a bank cannot be found.</aside>

<!-- <aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside> -->

<!-- ### HTTP Request

`GET http://example.com/api/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve -->

## closeBank()

> Overloads:

```java
utils.bank.closeBank();
```

> Examples:

```java
if(!utils.bank.isOpen()) {
    utils.bank.closeBank();
}
```

Closes the bank interface for the player.

<aside class="notice">Does nothing if the bank isn't open.</aside>

## depositXOfItem()

> Overloads:

```java
utils.bank.depositXOfItem(int itemid, int quantity);
```

> Examples:

```java
utils.bank.depositXOfItem(1234, 10);
utils.bank.depositXOfItem(ItemID.KNIFE, 5);
```

Deposits a specified quantity of an item, identified by its item ID.

<aside class="notice">The <code>ItemID</code> class contains a list of item IDs for commonly used items.</aside>

## depositAllOfItems()

> Overloads:

```java
// The `...` means you can add as many params as you want
utils.bank.depositAllOfItems(int itemids...);
```

> Examples:

```java
utils.bank.depositAllOfItems(123, 456, 789);
utils.bank.depositAllOfItems(ItemID.CHARCOAL, ItemID.PAPYRUS, ItemID.ROPE, ItemID.CHAIR);
```

Deposits all items matching the provided item IDs.

<aside class="notice">The <code>ItemID</code> class contains a list of item IDs for commonly used items.</aside>

## withdrawXOfItem()

> Overloads:

```java
utils.bank.withdrawXOfItem(int itemid, int quantity);
```

> Examples:

```java
utils.bank.withdrawXOfItem(123, 2);
utils.bank.withdrawXOfItem(ItemID.KNIFE, 2);
```

Deposits all items matching the provided item IDs.

<aside class="notice">The <code>ItemID</code> class contains a list of item IDs for commonly used items.</aside>
