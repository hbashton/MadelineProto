---
title: chat
description: chat attributes, type and example
---
## Constructor: chat  
[Back to constructors index](index.md)



### Attributes:

| Name     |    Type       | Required |
|----------|:-------------:|---------:|
|id|[int](../types/int.md) | Yes|
|title|[string](../types/string.md) | Yes|
|photo|[ChatPhoto](../types/ChatPhoto.md) | Yes|
|participants\_count|[int](../types/int.md) | Yes|
|date|[int](../types/int.md) | Yes|
|version|[int](../types/int.md) | Yes|



### Type: [Chat](../types/Chat.md)


### Example:

```
$chat = ['_' => 'chat', 'id' => int, 'title' => string, 'photo' => ChatPhoto, 'participants_count' => int, 'date' => int, 'version' => int, ];
```  

Or, if you're into Lua:  


```
chat={_='chat', id=int, title=string, photo=ChatPhoto, participants_count=int, date=int, version=int, }

```


