---
sidebar_position: 2
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

## Authentication

This request is sent to merchant's callback url to authenticate the user in the game

### Request

| Path   | `/auth` |
| ------ | ------- |
| Method | `Post`  |

```json
{
  "token": "0ae4b6385b4a5966a5849c0d8b50202a"
}
```

### Response

<Tabs>
  <TabItem value="json" label="Success">

    ```json
    {
        "code": 200,
        "message": "ok",
        "data": {
            "id": "12345",
            "name": "user_name",
            "balance": 1000
        }
    }
    ```

</TabItem>

  <TabItem value="error" label="Error">

    ```json
    {
        "code": 401,
        "message": "Invalid user token",
        "data": {}
    }
    ```

</TabItem>
</Tabs>
