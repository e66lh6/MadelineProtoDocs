---
title: channels.getLeftChannels
description: Get all channels you left
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Method: channels.getLeftChannels  
[Back to methods index](index.md)


Get all channels you left

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|offset|[int](../types/int.md) | Offset | Yes|


### Return type: [messages\_Chats](../types/messages_Chats.md)

### Can bots use this method: **YES**


### MadelineProto Example:


```
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$messages_Chats = $MadelineProto->channels->getLeftChannels(['offset' => int, ]);
```

### [PWRTelegram HTTP API](https://pwrtelegram.xyz) example (NOT FOR MadelineProto):

### As a bot:

POST/GET to `https://api.pwrtelegram.xyz/botTOKEN/madeline`

Parameters:

* method - channels.getLeftChannels
* params - `{"offset": int, }`



### As a user:

POST/GET to `https://api.pwrtelegram.xyz/userTOKEN/channels.getLeftChannels`

Parameters:

offset - Json encoded int




Or, if you're into Lua:

```
messages_Chats = channels.getLeftChannels({offset=int, })
```

