---
layout: page  # Or any layout defined in your theme
title: "Example Page"
permalink: /scripter-api-docs/bank/  # URL path for the page
---

# Bank Utilities (`utils.bank`)

## Overview
The `bank` utilities in the `Utils` class provide a set of methods for interacting with the in-game bank. These utilities simplify tasks like opening, closing, depositing, and withdrawing items from the bank.

## Methods

### `utils.bank.openBank()`
Opens the bank interface for the player.

---

### `utils.bank.closeBank()`
Closes the bank interface.

---

### `utils.bank.isOpen()`
Checks if the bank is currently open.

- **Returns**: `true` if the bank is open, otherwise `false`.

---

### `utils.bank.depositXOfItem(int itemId, int quantity)`
Deposits a specified quantity of an item, identified by its item ID.

- **Parameters**:
  - `itemId` (int): The ID of the item to deposit.
  - `quantity` (int): The number of items to deposit.

---

### `utils.bank.depositAllOfItems(int... itemIds)`
Deposits all items matching the provided item IDs.

- **Parameters**:
  - `itemIds` (int...): A list of item IDs to deposit.

---

### `utils.bank.withdrawXOfItem(int itemId, int quantity)`
Withdraws a specified quantity of an item, identified by its item ID.

- **Parameters**:
  - `itemId` (int): The ID of the item to withdraw.
  - `quantity` (int): The number of items to withdraw.

---

## Usage Example

```java
// Example usage of utils.bank methods
utils.bank.openBank();

if (utils.bank.isOpen()) {
    utils.bank.depositXOfItem(12345, 10); // Deposit 10 items of ID 12345
    utils.bank.withdrawXOfItem(67890, 5); // Withdraw 5 items of ID 67890
}

utils.bank.closeBank();