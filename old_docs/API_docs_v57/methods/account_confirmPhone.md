---
title: account.confirmPhone
description: Confirm this phone number is associated to this account, obtain phone_code_hash from sendConfirmPhoneCode
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Method: account.confirmPhone  
[Back to methods index](index.md)


Confirm this phone number is associated to this account, obtain phone_code_hash from sendConfirmPhoneCode

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|phone\_code\_hash|[string](../types/string.md) | obtain phone_code_hash from sendConfirmPhoneCode | Yes|
|phone\_code|[string](../types/string.md) | The code sent by sendConfirmPhoneCode | Yes|


### Return type: [Bool](../types/Bool.md)

### Can bots use this method: **NO**


### MadelineProto Example:


```
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$Bool = $MadelineProto->account->confirmPhone(['phone_code_hash' => 'string', 'phone_code' => 'string', ]);
```

### [PWRTelegram HTTP API](https://pwrtelegram.xyz) example (NOT FOR MadelineProto):



### As a user:

POST/GET to `https://api.pwrtelegram.xyz/userTOKEN/account.confirmPhone`

Parameters:

phone_code_hash - Json encoded string

phone_code - Json encoded string




Or, if you're into Lua:

```
Bool = account.confirmPhone({phone_code_hash='string', phone_code='string', })
```

### Errors this method can return:

| Error    | Description   |
|----------|---------------|
|CODE_HASH_INVALID|Code hash invalid|
|PHONE_CODE_EMPTY|phone_code is missing|


