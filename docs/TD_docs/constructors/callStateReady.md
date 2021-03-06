---
title: callStateReady
description: Call is ready to use
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: callStateReady  
[Back to constructors index](index.md)



Call is ready to use

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|protocol|[callProtocol](../constructors/callProtocol.md) | Yes|Call protocols supported by the peer|
|connections|Array of [callConnection](../constructors/callConnection.md) | Yes|Available UDP reflectors|
|config|[string](../types/string.md) | Yes|JSON-encoded call config|
|encryption\_key|[bytes](../types/bytes.md) | Yes|Call encryption key|
|emojis|Array of [string](../types/string.md) | Yes|Encryption key emojis fingerprint|



### Type: [CallState](../types/CallState.md)


