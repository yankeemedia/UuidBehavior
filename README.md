UuidBehavior
============

Forked  from (https://github.com/badlamer/UuidBehavior)

Helps you add UUID for propel ActiveRecord

### Difference with badlamer/UuidBehavior

Added support for primaryKey, the builder will add primaryKey to the column if no other field is configured as primaryKey

### Requirements

This behavior requires Propel >= 1.6.0 and Ramsey\Uuid for PHP >= 5.4

### Installation

Get the code by cloning this repository, or by using Composer (recommended):

```javascript
{
    "repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/yankeemedia/UuidBehavior"
        }
    ],

    "require": {
        "yankee/propel-uuid-behavior": "dev-master"
    }
}
```

Then, if you don't use Composer, or an autoloader in your application, add the
following configuration to your `build.properties` or `propel.ini` file:

```ini
propel.behavior.uuid.class = vendor.yankee.propel-uuid-behavior.src.UuidBehavior
```

> Note: `vendor.yankee.propel-uuid-behavior.src.UuidBehavior` is the path to access the `UuidBehavior` class in "dot-path" notation.


Then declare the behavior in your `schema.xml`:

```xml
<table name="person">
  <behavior name="uuid">
    <parameter name="name" value="uuid_column" />
  </behavior>
</table>
```
