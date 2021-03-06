---
title: auth.dropTempAuthKeys
description: Delete all temporary authorization keys except the ones provided
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Method: auth.dropTempAuthKeys  
[Back to methods index](index.md)


Delete all temporary authorization keys except the ones provided

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|except\_auth\_keys|Array of [long](../types/long.md) | The temporary authorization keys to keep | Yes|


### Return type: [Bool](../types/Bool.md)

### Can bots use this method: **YES**


### MadelineProto Example:


```
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$Bool = $MadelineProto->auth->dropTempAuthKeys(['except_auth_keys' => [long, long], ]);
```

### [PWRTelegram HTTP API](https://pwrtelegram.xyz) example (NOT FOR MadelineProto):

### As a bot:

POST/GET to `https://api.pwrtelegram.xyz/botTOKEN/madeline`

Parameters:

* method - auth.dropTempAuthKeys
* params - `{"except_auth_keys": [long], }`



### As a user:

POST/GET to `https://api.pwrtelegram.xyz/userTOKEN/auth.dropTempAuthKeys`

Parameters:

except_auth_keys - Json encoded  array of long




Or, if you're into Lua:

```
Bool = auth.dropTempAuthKeys({except_auth_keys={long}, })
```

