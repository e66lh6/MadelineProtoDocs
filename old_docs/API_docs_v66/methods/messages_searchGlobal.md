---
title: messages.searchGlobal
description: Global message search
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Method: messages.searchGlobal  
[Back to methods index](index.md)


Global message search

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|q|[string](../types/string.md) | The query | Yes|
|offset\_date|[int](../types/int.md) | 0 or the date offset | Yes|
|offset\_peer|[Username, chat ID, Update, Message or InputPeer](../types/InputPeer.md) | 0 or the peer offset | Optional|
|offset\_id|[int](../types/int.md) | 0 or the message ID offset | Yes|
|limit|[int](../types/int.md) | The number of results to return | Yes|


### Return type: [messages\_Messages](../types/messages_Messages.md)

### Can bots use this method: **NO**


### MadelineProto Example:


```
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$messages_Messages = $MadelineProto->messages->searchGlobal(['q' => 'string', 'offset_date' => int, 'offset_peer' => InputPeer, 'offset_id' => int, 'limit' => int, ]);
```

### [PWRTelegram HTTP API](https://pwrtelegram.xyz) example (NOT FOR MadelineProto):



### As a user:

POST/GET to `https://api.pwrtelegram.xyz/userTOKEN/messages.searchGlobal`

Parameters:

q - Json encoded string

offset_date - Json encoded int

offset_peer - Json encoded InputPeer

offset_id - Json encoded int

limit - Json encoded int




Or, if you're into Lua:

```
messages_Messages = messages.searchGlobal({q='string', offset_date=int, offset_peer=InputPeer, offset_id=int, limit=int, })
```

### Errors this method can return:

| Error    | Description   |
|----------|---------------|
|SEARCH_QUERY_EMPTY|The search query is empty|


