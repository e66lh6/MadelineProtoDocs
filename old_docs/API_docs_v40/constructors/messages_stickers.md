---
title: messages.stickers
description: messages_stickers attributes, type and example
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: messages.stickers  
[Back to constructors index](index.md)



### Attributes:

| Name     |    Type       | Required |
|----------|---------------|----------|
|hash|[string](../types/string.md) | Yes|
|stickers|Array of [Document](../types/Document.md) | Yes|



### Type: [messages\_Stickers](../types/messages_Stickers.md)


### Example:

```
$messages_stickers = ['_' => 'messages.stickers', 'hash' => 'string', 'stickers' => [Document, Document]];
```  

[PWRTelegram](https://pwrtelegram.xyz) json-encoded version:

```
{"_": "messages.stickers", "hash": "string", "stickers": [Document]}
```


Or, if you're into Lua:  


```
messages_stickers={_='messages.stickers', hash='string', stickers={Document}}

```


