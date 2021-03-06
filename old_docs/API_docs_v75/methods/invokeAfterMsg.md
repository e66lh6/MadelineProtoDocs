---
title: invokeAfterMsg
description: Invokes a query after successfull completion of one of the previous queries.
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Method: invokeAfterMsg  
[Back to methods index](index.md)


Invokes a query after successfull completion of one of the previous queries.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|msg\_id|[long](../types/long.md) | Message identifier on which a current query depends | Yes|
|query|[!X](../types/!X.md) | The query itself | Yes|


### Return type: [X](../types/X.md)

### Can bots use this method: **YES**


### MadelineProto Example:


```
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$X = $MadelineProto->invokeAfterMsg(['msg_id' => long, 'query' => !X, ]);
```

### [PWRTelegram HTTP API](https://pwrtelegram.xyz) example (NOT FOR MadelineProto):

### As a bot:

POST/GET to `https://api.pwrtelegram.xyz/botTOKEN/madeline`

Parameters:

* method - invokeAfterMsg
* params - `{"msg_id": long, "query": !X, }`



### As a user:

POST/GET to `https://api.pwrtelegram.xyz/userTOKEN/invokeAfterMsg`

Parameters:

msg_id - Json encoded long

query - Json encoded !X




Or, if you're into Lua:

```
X = invokeAfterMsg({msg_id=long, query=!X, })
```

