---
permalink: /docs/message-storage/uuid-encoding/
title: Message Repository Table Schema
published_at: 2021-08-24
updated_at: 2021-08-24
---

[![Packagist Version](https://img.shields.io/packagist/v/eventsauce/uuid-encoding.svg?style=flat-square)](https://packagist.org/packages/eventsauce/uuid-encoding)

```bash
composer require eventsauce/uuid-encoding
```

The UUID Encoding package allows customizing how the UUIDs used for the event ID and the
aggregate root ID are converted to string when written to the database.

### Binary UUID Encoder

`UuidBinaryEncoder` encodes the UUID using `$uuid->getBytes()` to generate a binary
text version of the UUID, which should be used when the database does not have a
native `uuid` type.

### String UUID Encoder

`UuidStringEncoder` encodes the UUID using `$uuid->toString()` to generate a plain
text version of the UUID, which should be used when the database has a `uuid` type.

### Custom Implementations

Custom implementations of `UuidEncoder` can be used to optimize UUID storage as needed.
