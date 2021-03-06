---
title: botInlineMessageMediaVenue
description: botInlineMessageMediaVenue attributes, type and example
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: botInlineMessageMediaVenue  
[Back to constructors index](index.md)



### Attributes:

| Name     |    Type       | Required |
|----------|---------------|----------|
|geo|[GeoPoint](../types/GeoPoint.md) | Optional|
|title|[string](../types/string.md) | Yes|
|address|[string](../types/string.md) | Yes|
|provider|[string](../types/string.md) | Yes|
|venue\_id|[string](../types/string.md) | Yes|
|venue\_type|[string](../types/string.md) | Yes|
|reply\_markup|[ReplyMarkup](../types/ReplyMarkup.md) | Optional|



### Type: [BotInlineMessage](../types/BotInlineMessage.md)


### Example:

```
$botInlineMessageMediaVenue = ['_' => 'botInlineMessageMediaVenue', 'geo' => GeoPoint, 'title' => 'string', 'address' => 'string', 'provider' => 'string', 'venue_id' => 'string', 'venue_type' => 'string', 'reply_markup' => ReplyMarkup];
```  

[PWRTelegram](https://pwrtelegram.xyz) json-encoded version:

```
{"_": "botInlineMessageMediaVenue", "geo": GeoPoint, "title": "string", "address": "string", "provider": "string", "venue_id": "string", "venue_type": "string", "reply_markup": ReplyMarkup}
```


Or, if you're into Lua:  


```
botInlineMessageMediaVenue={_='botInlineMessageMediaVenue', geo=GeoPoint, title='string', address='string', provider='string', venue_id='string', venue_type='string', reply_markup=ReplyMarkup}

```



## Usage of reply_markup

You can provide bot API reply_markup objects here.  


