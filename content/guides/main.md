---
weight: 10
title: API Reference
---

# Introduction

Shismo Scripter is a plugin which reads and executes code based on both Shismo's and RuneLite's inbuilt APIs. You can create your own completely customisable automated scripts written in Java/Groovy.

**How do I use this documentation?**

To your left, there is a table of contents and search bar that will take you to a specific section.

Once you have found what you want, have a read on what the functions do and view the code examples in the dark area to the right.

# Guides

<!-- > Code Example:

```java
System.out.println("The code examples are here!");
``` -->
## Getting Started
First, enable the Shismo Scripter plugin and navigate to the white pencil icon on the right. Once this panel is open, there are multiple options to choose from.


![Scripter Image](/images/scripter.png)

## Functions
> Query:

```java
boolean isBankOpen = utils.bank.isOpen();
if(utils.bank.isOpen()){
	//Do stuff
}

WorldPoint playerLocation = utils.player.getWorldLocation();
utils.walk.walkTo(playerLocation);
```

> Command:

```java
utils.bank.openBank();
```

> Event:

```java
utils.bank.addLog("Waiting up to 10 seconds for Mr Hans to spawn.");
if(utils.event.npcSpawned(NpcID.HANS, 10000)) {
	utils.bank.addLog("Mr Hans spawned in under 10 seconds.");
} else {
	utils.bank.addLog("Mr Hans did not spawn in under 10 seconds.");
}

utils.bank.addLog("Waiting forever until Mr Hans spawns.");
utils.event.npcSpawned(NpcID.HANS);
utils.bank.addLog("This will only run if Mr Hans spawns, otherwise it will never run.");
```

Shismo Scripter has **three** main types of functions:

- **Queries:** Returns a value of some type when called.

- **Commands:** Executes an action with no return value.

- **Events:** Waits for an event to occur and pauses script execution. Can also return a boolean if a timeout is specified.

<aside class="warning">
Events can pause script execution forever if the condition is never satisfied, keep that in mind.
</aside>

## Code Editor
The inbuilt code editor comes with auto code completion. This is accessible via pressing `ctrl + click`.

<aside class="notice">
Error logs are posted to the in-built script logger. You can access the logger via the button in the Scripter panel.
</aside>

# Bindings

## Client

You have access to all common classes in `net.runelite.api` like `WorldPoint`, `Client` etc. 

You can find out more via the official [RuneLite documentation](https://static.runelite.net/api/runelite-api/net/runelite/api/package-summary.html).

> Examples:
```java
new WorldPoint(420, 69, 0);

client.getEnergy();

ItemID.KNIFE();

NpcID.HANS();

ObjectID.ALTAR();
```


### ItemID
Enum class for in game ItemIDs.
### NpcID
Enum class for in game NpcIDs.
### ObjectID
Enum class for in game ObjectIDs.

## Utils

A set of common utilities that link to our very own Shismo Utils.

> Examples:
```java
utils.bank.function();
utils.debug.function();
utils.event.function();
utils.inventory.function();
utils.npc.function();
utils.object.function();
utils.player.function();
utils.prayer.function();
utils.walk.function();
utils.widget.function();
```