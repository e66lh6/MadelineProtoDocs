---
title: channels.getAdminLog
description: Get admin log of a channel/supergroup
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Method: channels.getAdminLog  
[Back to methods index](index.md)


Get admin log of a channel/supergroup

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|channel|[Username, chat ID, Update, Message or InputChannel](../types/InputChannel.md) | The channel/supergroup | Optional|
|q|[string](../types/string.md) | Search query | Yes|
|events\_filter|[ChannelAdminLogEventsFilter](../types/ChannelAdminLogEventsFilter.md) | Event filter | Optional|
|admins|Array of [Username, chat ID, Update, Message or InputUser](../types/InputUser.md) | Fetch only actions from these admins | Optional|
|max\_id|[long](../types/long.md) | Maximum message ID to fetch | Yes|
|min\_id|[long](../types/long.md) | Minimum message ID to fetch | Yes|
|limit|[int](../types/int.md) | Number of results to fetch | Yes|


### Return type: [channels\_AdminLogResults](../types/channels_AdminLogResults.md)

### Can bots use this method: **NO**


### MadelineProto Example:


```
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$channels_AdminLogResults = $MadelineProto->channels->getAdminLog(['channel' => InputChannel, 'q' => 'string', 'events_filter' => ChannelAdminLogEventsFilter, 'admins' => [InputUser, InputUser], 'max_id' => long, 'min_id' => long, 'limit' => int, ]);
```

### [PWRTelegram HTTP API](https://pwrtelegram.xyz) example (NOT FOR MadelineProto):



### As a user:

POST/GET to `https://api.pwrtelegram.xyz/userTOKEN/channels.getAdminLog`

Parameters:

channel - Json encoded InputChannel

q - Json encoded string

events_filter - Json encoded ChannelAdminLogEventsFilter

admins - Json encoded  array of InputUser

max_id - Json encoded long

min_id - Json encoded long

limit - Json encoded int




Or, if you're into Lua:

```
channels_AdminLogResults = channels.getAdminLog({channel=InputChannel, q='string', events_filter=ChannelAdminLogEventsFilter, admins={InputUser}, max_id=long, min_id=long, limit=int, })
```

### Errors this method can return:

| Error    | Description   |
|----------|---------------|
|CHANNEL_INVALID|The provided channel is invalid|
|CHANNEL_PRIVATE|You haven't joined this channel/supergroup|
|CHAT_ADMIN_REQUIRED|You must be an admin in this chat to do this|


