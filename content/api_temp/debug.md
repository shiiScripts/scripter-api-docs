---
weight: 13
title: Get a Specific Kitten
---
# Debug Commands

## sendLog()

> Overloads:

```java
utils.debug.sendLog(Object message);
```

> Examples:

```java
utils.debug.sendLog("Opening the bank.");
utils.bank.openBank();

if(utils.bank.isOpen()){
    utils.debug.sendLog("The bank is open.");
}

```

Sends a debug message to the Scripter Logger.

<aside class="notice">Will attempt to invoke toString() if what is passed isn't a String.</aside>

<!-- <aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside> -->

<!-- ### HTTP Request

`GET http://example.com/api/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve -->

## sendRedGameMessage()

> Overloads:

```java
utils.debug.sendRedGameMessage(Object message, String scriptName);
```

> Examples:

```java
utils.debug.sendRedGameMessage("Opening the bank.", "Bank Opener");
utils.bank.openBank();

if(utils.bank.isOpen()){
    utils.debug.sendRedGameMessage("The bank is open.", "Bank Opener");
}

```

Sends a red debug message to the in game chat.

<aside class="notice">Will attempt to invoke toString() if what is passed isn't a String.</aside>

## sendGreenGameMessage()

> Overloads:

```java
utils.debug.sendGreenGameMessage(Object message, String scriptName);
```

> Examples:

```java
utils.debug.sendGreenGameMessage("Opening the bank.", "Bank Opener");
utils.bank.openBank();

if(utils.bank.isOpen()){
    utils.debug.sendGreenGameMessage("The bank is open.", "Bank Opener");
}

```

Sends a red debug message to the in game chat.

<aside class="notice">Will attempt to invoke toString() if what is passed isn't a String.</aside>

## updateOverlayState()

> Overloads:

```java
utils.debug.updateOverlayState(Object message);
```

> Examples:

```js
utils.updateOverlayState(getState());

function getState(){
    if(!utils.bank.isOpen()){
        return BANKING;
    }
    return DOING_NOTHING;
}

var State = {
    DOING_NOTHING: "DOING_NOTHING",
    BANKING: "BANKING"
}
```

Updates the overlay with your state.

<aside class="notice">Will attempt to invoke toString() if what is passed isn't a String.</aside>
