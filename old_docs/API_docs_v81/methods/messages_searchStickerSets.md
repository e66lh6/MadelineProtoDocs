---
title: messages.searchStickerSets
description: Find a sticker set
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Method: messages.searchStickerSets  
[Back to methods index](index.md)


Find a sticker set

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|exclude\_featured|[Bool](../types/Bool.md) | Exclude featured sticker sets from the search? | Optional|
|q|[string](../types/string.md) | The search query | Yes|
|hash|Array of [int](../types/int.md) | The IDs of stickersets you already fetched | Optional|


### Return type: [messages\_FoundStickerSets](../types/messages_FoundStickerSets.md)

### Can bots use this method: **YES**


### MadelineProto Example:


```
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$messages_FoundStickerSets = $MadelineProto->messages->searchStickerSets(['exclude_featured' => Bool, 'q' => 'string', 'hash' => [int, int], ]);
```

### [PWRTelegram HTTP API](https://pwrtelegram.xyz) example (NOT FOR MadelineProto):

### As a bot:

POST/GET to `https://api.pwrtelegram.xyz/botTOKEN/madeline`

Parameters:

* method - messages.searchStickerSets
* params - `{"exclude_featured": Bool, "q": "string", "hash": [int], }`



### As a user:

POST/GET to `https://api.pwrtelegram.xyz/userTOKEN/messages.searchStickerSets`

Parameters:

exclude_featured - Json encoded Bool

q - Json encoded string

hash - Json encoded  array of int




Or, if you're into Lua:

```
messages_FoundStickerSets = messages.searchStickerSets({exclude_featured=Bool, q='string', hash={int}, })
```

