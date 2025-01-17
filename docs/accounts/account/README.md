---
description: >-
  An account in the wallet. An account is associated with one AccountKey,
  containing a View keypair and a Spend keypair.
---

# Account

## Attributes

| Name | Type | Description |
| :--- | :--- | :--- |
| `object` | String, value is "account" | String representing the object's type. Objects of the same type share the same value. |
| `account_id` | String | The unique identifier for the account. |
| `name` | String | The display name for the account. |
| `main_address` | String | The b58 address code for the account's main address. The main address is determined by the seed subaddress. It is not assigned to a single recipient and should be considered a free-for-all address. |
| `next_subaddress_index` | String \(uint64\) | This index represents the next subaddress to be assigned as an address. This is useful information in case the account is imported elsewhere. |
| `recovery_mode` | Boolean | A flag that indicates this imported account is attempting to un-orphan found TXOs. It is recommended to move all MOB to another account after recovery if the user is unsure of the assigned addresses. |

## Example

```text
{
  "object": "account",
  "account_id": "gdc3fd37f1903aec5a12b12a580eb837e14f87e5936f92a0af4794219f00691d",
  "name": "I love MobileCoin",
  "main_address": "8vbEtknX7zNtmN5epTYU95do3fDfsmecDu9kUbW66XGkKBX87n8AyqiiH9CMrueo5H7yiBEPXPoQHhEBLFHZJLcB2g7DZJ3tUZ9ArVgBu3a",
  "next_subaddress_index": "3",
  "first_block_index": "3500",
  "recovery_mode": false
}
```

