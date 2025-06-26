---
sidebar_position: 6
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

# Rollback

This request is used to add a given amount to a player's wallet when a given game action that had deducted the same amount from the wallet, fails.

| path    | **`/rollback`** |
| ------- | --------------- |
| method  | **`POST`**      |
| headers | **`x-api-key`** |

### Request

<Tabs>
  <TabItem value="parameters" label="Parameters">
    | Parameter   | Description                                                                 |
    | ----------- | --------------------------------------------------------------------------- |
    | token       | **String** - Player's token on the merchant's side                          |
    | amount      | **Number** - Amount to be added to the player's wallet                 |
  </TabItem>
  
  <TabItem value="example" label="Example">

    ```json
    {
      "token": "0ae4b6385b4a5966a5849c0d8b50202a",
      "amount": 100,
    }

    ```

  </TabItem>

</Tabs>

### Response

<Tabs>
  <TabItem value="parameters" label="Parameters">

    | Parameter | Description                                                                                         |
    | --------- | --------------------------------------------------------------------------------------------------- |
    | code      | **Number** - response status code                                                                       |
    | message   | **String** - response explanation                                                                       |
    | data      | **Object** <ul><li>id - ***String*** player id</li><li>name - ***String*** player name</li><li>balance - ***Number*** player balance</li></ul> |

  </TabItem>

  <TabItem value="success" label="Success Example">

    ```json
    {
        "code": 200,
        "message": "ok",
        "data": {
            "id": "12345",
            "name": "johndoe",
            "balance": 1000
        }
    }
    ```

  </TabItem>

  <TabItem value="error" label="Error Example">

    ```json
    {
        "code": 401,
        "message": "Invalid token",
        "data": {}
    }
    ```

  </TabItem>
</Tabs>
