---
title: createNewSecretChat
description: Creates new secret chat, returns created chat
---
## Method: createNewSecretChat  
[Back to methods index](index.md)


Creates new secret chat, returns created chat

### Params:

| Name     |    Type       | Required | Description |
|----------|:-------------:|:--------:|------------:|
|user\_id|[int](../types/int.md) | Yes|Identifier of a user to create secret chat with|


### Return type: [Chat](../types/Chat.md)

### Example:


```
$MadelineProto = new \danog\MadelineProto\API();
if (isset($token)) { // Login as a bot
    $this->bot_login($token);
}
if (isset($number)) { // Login as a user
    $sentCode = $MadelineProto->phone_login($number);
    echo 'Enter the code you received: ';
    $code = '';
    for ($x = 0; $x < $sentCode['type']['length']; $x++) {
        $code .= fgetc(STDIN);
    }
    $MadelineProto->complete_phone_login($code);
}

$Chat = $MadelineProto->createNewSecretChat(['user_id' => int, ]);
```

Or, if you're into Lua:

```
Chat = createNewSecretChat({user_id=int, })
```

