---
title: updateReadMessagesContents
description: updateReadMessagesContents attributes, type and example
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: updateReadMessagesContents  
[Back to constructors index](index.md)



### Attributes:

| Name     |    Type       | Required |
|----------|---------------|----------|
|messages|Array of [int](../types/int.md) | Yes|
|pts|[int](../types/int.md) | Yes|
|pts\_count|[int](../types/int.md) | Yes|



### Type: [Update](../types/Update.md)


### Example:

```
$updateReadMessagesContents = ['_' => 'updateReadMessagesContents', 'messages' => [int, int], 'pts' => int, 'pts_count' => int];
```  

[PWRTelegram](https://pwrtelegram.xyz) json-encoded version:

```
{"_": "updateReadMessagesContents", "messages": [int], "pts": int, "pts_count": int}
```


Or, if you're into Lua:  


```
updateReadMessagesContents={_='updateReadMessagesContents', messages={int}, pts=int, pts_count=int}

```


