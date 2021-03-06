---
title: messages.messages
description: messages_messages attributes, type and example
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: messages.messages  
[Back to constructors index](index.md)



### Attributes:

| Name     |    Type       | Required |
|----------|---------------|----------|
|messages|Array of [Message](../types/Message.md) | Yes|
|chats|Array of [Chat](../types/Chat.md) | Yes|
|users|Array of [User](../types/User.md) | Yes|



### Type: [messages\_Messages](../types/messages_Messages.md)


### Example:

```
$messages_messages = ['_' => 'messages.messages', 'messages' => [Message, Message], 'chats' => [Chat, Chat], 'users' => [User, User]];
```  

[PWRTelegram](https://pwrtelegram.xyz) json-encoded version:

```
{"_": "messages.messages", "messages": [Message], "chats": [Chat], "users": [User]}
```


Or, if you're into Lua:  


```
messages_messages={_='messages.messages', messages={Message}, chats={Chat}, users={User}}

```


