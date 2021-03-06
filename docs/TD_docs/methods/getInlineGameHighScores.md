---
title: getInlineGameHighScores
description: Bots only. Returns game high scores and some part of the score table around of the specified user in the game
---
## Method: getInlineGameHighScores  
[Back to methods index](index.md)


Bots only. Returns game high scores and some part of the score table around of the specified user in the game

### Params:

| Name     |    Type       | Required | Description |
|----------|:-------------:|:--------:|------------:|
|inline\_message\_id|[string](../types/string.md) | Yes|Inline message identifier|
|user\_id|[int](../types/int.md) | Yes|User identifier|


### Return type: [GameHighScores](../types/GameHighScores.md)

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

$GameHighScores = $MadelineProto->getInlineGameHighScores(['inline_message_id' => string, 'user_id' => int, ]);
```

Or, if you're into Lua:

```
GameHighScores = getInlineGameHighScores({inline_message_id=string, user_id=int, })
```

