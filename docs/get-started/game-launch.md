---
sidebar_position: 2
---

# Game Launch

Available games - **`Avionix`**, **`Tower`**, **`Mines`**, **`Classic Dice`**, **`Hash Dice`**, **`Limbo`**, **`Wheel`**,

To launch a game, the following parameters needed;

```json
{
  "merchant": "The merchant id provided by us",
  "token": "The players's token from the merchant's side",
  "game": "avionix" | "tower"| "mines" | "classic-dice" | "hash-dice" | "limbo" | "wheel"
}
```

The above parameters are passed to the game's launch url as below;

```
  https://{game}.gameyetu.com/?merchant={merchant}&token={token}
```

Example launch url;

```
  https://avionix.gameyetu.com/?merchant=gameyetu&token=4512bb329301b0842eae1c4e5441d1909eb7108ee79a09a07f64ee86fa318e09
```
