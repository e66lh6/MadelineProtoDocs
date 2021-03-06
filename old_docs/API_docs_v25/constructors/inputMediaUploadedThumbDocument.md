---
title: inputMediaUploadedThumbDocument
description: inputMediaUploadedThumbDocument attributes, type and example
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: inputMediaUploadedThumbDocument  
[Back to constructors index](index.md)



### Attributes:

| Name     |    Type       | Required |
|----------|---------------|----------|
|file|[File path or InputFile](../types/InputFile.md) | Yes|
|thumb|[File path or InputFile](../types/InputFile.md) | Yes|
|mime\_type|[string](../types/string.md) | Optional|
|attributes|Array of [DocumentAttribute](../types/DocumentAttribute.md) | Yes|



### Type: [InputMedia](../types/InputMedia.md)


### Example:

```
$inputMediaUploadedThumbDocument = ['_' => 'inputMediaUploadedThumbDocument', 'file' => InputFile, 'thumb' => InputFile, 'mime_type' => 'string', 'attributes' => [DocumentAttribute, DocumentAttribute]];
```  

[PWRTelegram](https://pwrtelegram.xyz) json-encoded version:

```
{"_": "inputMediaUploadedThumbDocument", "file": InputFile, "thumb": InputFile, "mime_type": "string", "attributes": [DocumentAttribute]}
```


Or, if you're into Lua:  


```
inputMediaUploadedThumbDocument={_='inputMediaUploadedThumbDocument', file=InputFile, thumb=InputFile, mime_type='string', attributes={DocumentAttribute}}

```


