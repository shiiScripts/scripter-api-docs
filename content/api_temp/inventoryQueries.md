---
weight: 15
title: Inventory
---

# Inventory Queries

## containsAll()

> Overloads:

```java
utils.inventory.containsAll(int... itemIds);
```

> Returns:

```java
boolean
```

> Examples:

```java
if (utils.inventory.containsAll(ItemID.KNIFE, ItemID.LOGS)) {
    //Perform actions when inventory contains all of the specified items
}
```

Checks if the inventory contains all of the specified items.

<aside class="success">
Remember — the `!` operator can be used to invert the condition!
</aside>

## containsAny()

> Overloads:

```java
utils.inventory.containsAny(int... itemIds);
```

> Returns:

```java
boolean
```

> Examples:

```java
if (utils.inventory.containsAny(ItemID.KNIFE, ItemID.LOGS)) {
    //Perform actions when inventory contains any of the specified items
}
```

Checks if the inventory contains any of the specified items.

<aside class="success">
Remember — the `!` operator can be used to invert the condition!
</aside>

## containsAmount()

> Overloads:

```java
utils.inventory.containsAmount(int itemId, int amount, boolean exactAmount);
```

> Returns:

```java
boolean
```

> Examples:

```java
if (utils.inventory.containsAmount(ItemID.LOGS, 2, false)) {
    //Perform actions when inventory contains 2 or more logs
}

if (utils.inventory.containsAmount(ItemID.LOGS, 2, true)) {
    //Perform actions when inventory contains exactly 2 logs
}
```

Checks if the inventory contains an exact amount or more of a specified item.

<aside class="success">
Remember — the `!` operator can be used to invert the condition!
</aside>


## isFull()

> Overloads:

```java
utils.inventory.isFull();
```

> Returns:

```java
boolean
```

> Examples:

```java
if (utils.inventory.isFull()) {
    //Perform actions when the inventory is full
}
```

Checks if the inventory is full.

<aside class="success">
Remember — the `!` operator can be used to invert the condition!
</aside>


## isEmpty()

> Overloads:

```java
utils.inventory.isEmpty();
```

> Returns:

```java
boolean
```

> Examples:

```java
if (utils.inventory.isEmpty()) {
    //Perform actions when the inventory is empty
}
```

Checks if the inventory is empty.

<aside class="success">
Remember — the `!` operator can be used to invert the condition!
</aside>

<!-- ### HTTP Request

`GET http://example.com/api/kittens`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted. -->


