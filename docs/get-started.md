---
sidebar_position: 1
---

## Avionix Integration guide

**Game launch process**

To launch the game, the following parameters are needed

```json
{
  "merchant": "The merchant id provided by us",
  "token": "The user's token from the merchant's side"
}
```

The above parameters are appended to the game launch url as below;

```mdx
https://avionix.gameyetu.com/?merchant={merchant}&token={token}
```
