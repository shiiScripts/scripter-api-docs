---
weight: 16
title: Get a Specific Kitten
---
# Inventory Commands

## interactItem()

> Overloads:

```java
utils.inventory.interactItem(int itemId, String action);
utils.inventory.interactItem(String name, boolean exactName, String action);
```

> Examples:

```java
utils.inventory.interactItem(ItemID.SPADE, "Dig");
utils.inventory.interactItem("Spade", true, "Dig");
```

Interacts with an item via the specified menu option.

<aside class="notice">You should use exact names where possible to avoid bugs!</aside>

<!-- <aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside> -->

<!-- ### HTTP Request

`GET http://example.com/api/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve -->

## itemOnItem()

> Overloads:

```java
utils.inventory.itemOnItem(int itemId, int targetItemId);
```

> Examples:

```java
utils.inventory.itemOnItem(ItemID.KNIFE, ItemID.LOGS);
```

Uses an item on the target item.

<aside class="notice">The <code>ItemID</code> class contains a list of item IDs for commonly used items.</aside>

## itemOnNpc()

> Overloads:

```java
utils.inventory.itemOnNpc(int itemId, int targetNpcId);
```

> Examples:

```java
utils.inventory.itemOnNpc(ItemID.GRIMY_SNAPDRAGON, NpcID.LEPRECHAUN);
```

Uses an item on the target npc.

<aside class="notice">The <code>ItemID</code> and <code>NpcID</code> classes contain lists of commonly used IDs.</aside>

## itemOnObject()

> Overloads:

```java
utils.inventory.itemOnObject(int itemId, int targetObjectId);
```

> Examples:

```java
utils.inventory.itemOnObject(ItemID.BRONZE_KEY, ObjectID.GATE);
```

Uses an item on the target object.

<aside class="notice">The <code>ItemID</code> and <code>ObjectID</code> classes contain lists of commonly used IDs.</aside>