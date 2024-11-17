---
weight: 14
title: Get a Specific Kitten
---
# Events

## npcSpawned()

> Overloads:

```java
utils.event.npcSpawned(int id, int timeoutMillis);
```

> Returns:

```java
boolean
```

> Examples:

```java
if(utils.event.npcSpawned(NpcID.HANS, 10)){
    utils.debug.sendLog("Hans spawned within 10 seconds");
} else {
    utils.debug.sendLog("Hans did not spawn within 10 seconds");
}
```

Returns a boolean indicating if the NPC with the specified ID spawned within the given timeout.

<aside class="warning">This is a blocking action, it will halt execution of your thread until the condition is satisfied.</aside>

<!-- <aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside> -->

<!-- ### HTTP Request

`GET http://example.com/api/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve -->

## gameTick()

> Overloads:

```java
utils.event.gameTick();
```

> Returns:

```java
boolean
```

> Examples:

```java
utils.debug.sendLog("Time from here:");
utils.event.gameTick();
utils.debug.sendLog("To here is most likely around 600ms~");
```

Returns a boolean indicating if the gametick happens within 1000ms.

<aside class="warning">This is a blocking action, it will halt execution of your thread until the condition is satisfied.</aside>

## sleep()

> Overloads:

```java
utils.event.sleep(int minMilli, int maxMilli);
```

> Examples:

```java
utils.debug.sendLog("Time from here:");
utils.event.sleep(1000, 1500);
utils.debug.sendLog("To here is between 1000 - 1500ms");
```

Sleeps for a duration between min and max milliseconds.

<aside class="warning">This is a blocking action, it will halt execution of your thread until the condition is satisfied.</aside>