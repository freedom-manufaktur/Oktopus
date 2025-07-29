Documentation and examples for whoosh Oktopus functions
---
Version: `6.4.0` - `2025-07-29` \
Link: [Documentation on GitHub](https://github.com/freedom-manufaktur/Oktopus/blob/main/Documentation/Oktopus%20Functions.md)

# Language
whoosh Oktopus uses [Scriban](https://github.com/scriban/scriban) as scripting/templating engine.\
Check out the
- [Scriban language syntax](https://github.com/scriban/scriban/blob/master/doc/language.md) in a templating context (within `{{` and `}}`)
- [Scriban built-in functions](https://github.com/scriban/scriban/blob/master/doc/builtins.md), which proviede a broad set of base capabilities

for further information.

# Oktopus built-in functions
This document describes the built-in functions provided by whoosh Oktopus (in addition to [Scriban built-in functions](https://github.com/scriban/scriban/blob/master/doc/builtins.md)).

- [`array` functions](#array-functions)
- [`convert` functions](#convert-functions)
- [`dateOnly` functions](#dateonly-functions)
- [`globalVariable` functions](#globalvariable-functions)
- [`html` functions](#html-functions)
- [`json` functions](#json-functions)
- [`oktopus` functions](#oktopus-functions)
- [`step` functions](#step-functions)
- [`string` functions](#string-functions)
- [`timeonly` functions](#timeonly-functions)
- [`variable` functions](#variable-functions)
- [`workflow` functions](#workflow-functions)

## `array` functions
Array functions available through the object 'array' in whoosh Oktopus.

- [`array.isNullOrEmpty`](#arrayisnullorempty)
- [`array.hasItems`](#arrayhasitems)
- [`array.remove`](#arrayremove)

[🔝 Back to top](#oktopus-built-in-functions)

### `array.isNullOrEmpty`
```
array.isNullOrEmpty <list>
```

#### Description
Returns if an input `list` is null or empty. The shortcut `array.empty` can be used instead.

#### Arguments
- `list`: The input list

#### Returns
**true** if `list` is empty; otherwise **false**

#### Examples
> **input**
```oktopus-html
{{ array.isNullOrEmpty [] }}
{{ array.isNullOrEmpty [1, 2, 3]  }}
```
> **output**
```html
true
false
```
[🔝 Back to top](#oktopus-built-in-functions)

### `array.hasItems`
```
array.hasItems <list>
```

#### Description
Returns if an input `list` has elements.

#### Arguments
- `list`: The input list

#### Returns
**true** if `list` has elements; otherwise **false**

#### Examples
> **input**
```oktopus-html
{{ array.hasItems [1, 2, 3] }}
{{ array.hasItems [] }}
```
> **output**
```html
true
false
```
[🔝 Back to top](#oktopus-built-in-functions)

### `array.remove`
```
array.remove <list> <remove>
```

#### Description
Removes an element from an input `list`.

#### Arguments
- `list`: The input list
- `remove`: The element to remove from the `list`. Must be a scalar value

#### Returns
A new list with the element removed

#### Examples
> **input**
```oktopus-html
{{ array.remove [1, 2, 3] 1 }}
```
> **output**
```html
[2, 3]
```
[🔝 Back to top](#oktopus-built-in-functions)

## `convert` functions
Convert functions available through the object 'convert' in whoosh Oktopus.

- [`convert.toBase64`](#converttobase64)
- [`convert.toBase64URL`](#converttobase64url)
- [`convert.toCsv`](#converttocsv)
- [`convert.toCsvRows`](#converttocsvrows)
- [`convert.toDecimal`](#converttodecimal)
- [`convert.toDouble`](#converttodouble)
- [`convert.toInt`](#converttoint)
- [`convert.toLong`](#converttolong)
- [`convert.toText`](#converttotext)

[🔝 Back to top](#oktopus-built-in-functions)

### `convert.toBase64`
```
convert.toBase64 <value>
```

#### Description
Converts the input `value` to Base64. 

#### Arguments
- `value`: The input object

#### Returns
The input `value` converted to Base64

#### Examples
> **input**
```oktopus-html
{{ convert.toBase64 "Test" }}
{{ convert.toBase64 MyFileVar }}
```
> **output**
```html
VGVzdA==
77u/VGVzdENvbnRlbnQ=
```
[🔝 Back to top](#oktopus-built-in-functions)

### `convert.toBase64URL`
```
convert.toBase64Url <value>
```

#### Description
Converts the input `value` to Base64URL. Base64URL converts the special characters `/`, `=` and `+` from Base64 so it can be used for URL adresses and filenames.

#### Arguments
- `value`: The input object

#### Returns
The input `value` converted to Base64URL

#### Examples
> **input**
```oktopus-html
{{ convert.toBase64URL "Test" }}
{{ convert.toBase64URL MyFileVar }}
```
> **output**
```html
VGVzdA
77u_VGVzdENvbnRlbnQ
```
[🔝 Back to top](#oktopus-built-in-functions)

### `convert.toCsv`
```
convert.toCsv <value> <header>?
```

#### Description
Converts the input `value` to a CSV. An optional `header` can be passed to specify the CSV header.
If the `header` is not specified then the return will have no CSV header.

#### Arguments
- `value`: The input object
- `header`: An optional string of comma-separated values that represent the CSV header

#### Returns
The input `value` converted to a CSV

#### Examples
> **input**
```oktopus-html
{{ convert.toCsv {Id:1,Text:"Foo"} }}
{{ convert.toCsv {Id:1,Text:"Foo"} "Id,Text" }}
{{ convert.toCsv [{Id:1,Text:"Foo"},{Id:2,Text:"Bar"}] "Id,Text" }}
```
> **output**
```html
1,Foo
Id,Text
1,Foo
Id,Text
"{Id: 1, Text: ""Foo""}","{Id: 2, Text: ""Bar""}"
```
[🔝 Back to top](#oktopus-built-in-functions)

### `convert.toCsvRows`
```
convert.toCsvRows <value> <header>?
```

#### Description
Converts the input `value` to a CSV rows. An optional `header` can be passed to specify the CSV header.
If the `header` is not specified then the return will have no CSV header.

#### Arguments
- `value`: The input object
- `header`: An optional string of comma-separated values that represent the CSV header

#### Returns
The input `value` converted to CSV rows

#### Examples
> **input**
```oktopus-html
{{ convert.toCsvRows {Id:1,Text:"Foo"} }}
{{ convert.toCsvRows {Id:1,Text:"Foo"} "Id,Text" }}
{{ convert.toCsvRows [{Id:1,Text:"Foo"},{Id:2,Text:"Bar"}] "Id,Text" }}
```
> **output**
```html
1,Foo

Id,Text
1,Foo

Id,Text
1,Foo
2,Bar
```
[🔝 Back to top](#oktopus-built-in-functions)

### `convert.toDecimal`
```
convert.toDecimal <value> <culture>?
```

#### Description
Converts the input `value` to a 128 bit decimal. An optional `culture` can be passed to specify the format of the `value`.
If the `culture` is not specified then the default will be used.

#### Arguments
- `value`: The input object
- `culture`: An optional string of the culture format

#### Returns
The input `value` converted to a 128 bit decimal

#### Examples
> **input**
```oktopus-html
{{ convert.toDecimal "1.337,01" "de" }}
{{ convert.toDecimal "1,337.01" "en" }}
```
> **output**
```html
1337.01
1337.01
```
[🔝 Back to top](#oktopus-built-in-functions)

### `convert.toDouble`

```
convert.toDouble <value> <culture>?
```

#### Description

Converts the input `value` to a 64 bit double. An optional `culture` can be passed to specify the format of the `value`.
If the `culture` is not specified then the default will be used.

#### Arguments

- `value`: The input object
- `culture`: An optional string of the culture format

#### Returns

The input `value` converted to a 64 bit double

#### Examples

> **input**
```oktopus-html
{{ convert.toDouble "1,337" "de" }}
{{ convert.toDouble "1,337" "en" }}
```
> **output**
```html
1.337
1337
```
[🔝 Back to top](#oktopus-built-in-functions)
### `convert.toInt`

```
convert.toInt <value> <culture>?
```

#### Description

Converts the input `value` to a 32 bit integer. An optional `culture` can be passed to specify the format of the `value`.
If the `culture` is not specified then the default will be used.

#### Arguments

- `value`: The input object
- `culture`: An optional string of the culture format

#### Returns

The input `value` converted to a 32 bit integer

#### Examples

> **input**
```oktopus-html
{{ convert.toInt "1,337" }}
{{ convert.toInt "1337" }}
```
> **output**
```html
1337
1337
```
[🔝 Back to top](#oktopus-built-in-functions)
### `convert.toLong`

```
convert.toLong <value> <culture>?
```

#### Description

Converts the input `value` to a 64 bit integer. An optional `culture` can be passed to specify the format of the `value`.
If the `culture` is not specified then the default will be used.

#### Arguments

- `value`: The input object
- `culture`:  An optional string of the culture format

#### Returns

The input `value` converted to a 64 bit integer

#### Examples

> **input**
```oktopus-html
{{ convert.toLong "1,337" }}
{{ convert.toLong "1337" }}
```
> **output**
```html
1337
1337
```
[🔝 Back to top](#oktopus-built-in-functions)
### `convert.toText`

```
convert.toText <value>
```

#### Description

Converts the input `value` to a string. The shortcut `convert.toString` can be used instead.

#### Arguments

- `value`: The input object

#### Returns

The input `value` converted to a string

#### Examples

> **input**
```oktopus-html
{{ convert.toText 1.337 }}
{{ convert.toText 1337 }}
```
> **output**
```html
"1.337"
1337
```
[🔝 Back to top](#oktopus-built-in-functions)

## `dateOnly` functions

DateOnly functions available through the object 'dateOnly' in whoosh Oktopus.

- [`dateOnly.from`](#dateonlyfrom)
- [`dateOnly.now`](#dateonlynow)
- [`dateOnly.parse`](#dateonlyparse)
- [`dateOnly.today`](#dateonlytoday)

[🔝 Back to top](#oktopus-built-in-functions)
### `dateOnly.from`

```
dateOnly.from <dateTime>
```

#### Description

Returns the date string of an input `dateTime`.

#### Arguments

- `dateTime`: The input datetime object

#### Returns

The date string of the `dateTime` input

#### Examples

> **input**
```oktopus-html
{{ dateOnly.from date.now }}
{{ dateTime = date.parse "2024/12/31 13:37:00Z"; dateOnly.from dateTime  }}
```
> **output**
```html
2024-01-01
2024-12-31
```
[🔝 Back to top](#oktopus-built-in-functions)
### `dateOnly.now`

```
dateOnly.now
```

#### Description

Returns a date string of the current time.

#### Arguments


#### Returns


#### Examples

> **input**
```oktopus-html
{{ dateOnly.now }}
```
> **output**
```html
2024-01-01
```
[🔝 Back to top](#oktopus-built-in-functions)
### `dateOnly.parse`

```
dateOnly.parse <dateString> <culture>?
```

#### Description

Returns a date string of an input date string. An optional `culture` can be passed to specify the format of the `dateString`.
If the `culture` is not specified then the default will be used.

#### Arguments

- `dateString`: The input date string
- `culture`:  An optional string of the culture format

#### Returns

A date string of the input `dateString`

#### Examples

> **input**
```oktopus-html
{{ dateOnly.parse "2024-01-01" }}
{{ dateOnly.parse "2024/12/31" }}
{{ (dateOnly.parse "2024-12-31") | object.format "m" }}
{{ dateOnly.parse "31-12-2024" "de" }}
```
> **output**
```html
2024-01-01
2024-12-31
December 31
2024-12-31
```
[🔝 Back to top](#oktopus-built-in-functions)
### `dateOnly.today`

```
dateOnly.today
```

#### Description

Returns a date string of the current time.

#### Arguments


#### Returns


#### Examples

> **input**
```oktopus-html
{{ dateOnly.today }}
```
> **output**
```html
2024-01-01
```
[🔝 Back to top](#oktopus-built-in-functions)

## `globalVariable` functions

Global variable functions available through the object 'globalVariable' in whoosh Oktopus.

- [`globalVariable.load`](#globalvariableload)
- [`globalVariable.store`](#globalvariablestore)

[🔝 Back to top](#oktopus-built-in-functions)
### `globalVariable.load`

```
globalVariable.load <globalVariableName>
```

#### Description

Returns the value of a global variable. Global variables have to be set with a name and a value under `Global variables`

#### Arguments

- `globalVariableName`: The name of the global variable

#### Returns

The value of the input `globalVariableName`

#### Examples

> **input**
```oktopus-html
{{ globalVariable.load "MyGlobalVariable" }}
```
> **output**
```html
"MyValue"
```
[🔝 Back to top](#oktopus-built-in-functions)
### `globalVariable.store`

```
globalVariable.store <value> <globalVariableName>
```

#### Description

Stores a global variable of an input `value`. If the `globalVariableName` already exists then the new `value` will be stored, otherwise the new `globalVariableName` and the `value` will be added under `Global variables`. The shortcut `globalVariable.set` can be used instead.

#### Arguments

- `value`: The input object
- `globalVariableName`: The name of the global variable

#### Returns


#### Examples

> **input**
```oktopus-html
{{ globalVariable.store "MyValue" "MyGlobalVariable" }}
```
> **output**
```html
Storing global variable 'MyGlobalVariable'='MyValue'
```
[🔝 Back to top](#oktopus-built-in-functions)


## `html` functions
HTML functions available through the object 'html' in whoosh Oktopus.

- [`html.GetBody`](#htmlgetbody)
- [`html.removeAllAttributes`](#htmlremoveallattributes)
- [`html.removeAttributes`](#htmlremoveattributes)

[🔝 Back to top](#oktopus-built-in-functions)


### `html.GetBody`
```
html.GetBody <text>
```

#### Description
Extracts the body of an arbitrary HTML input `text`.

#### Arguments
- `text`: The input HTML string

#### Returns
A new HTML string with the body.

#### Examples
> **input**
```oktopus-html
{{ html.GetBody "<html><head></head><body><p>Foo</p></body></html>" }}
{{ html.GetBody "<p>Bar</p>" }}
```
> **output**
```html
<p>Foo</p>
<p>Bar</p>
```

[🔝 Back to top](#oktopus-built-in-functions)


### `html.removeAllAttributes`
```
html.removeAllAttributes <text>
```

#### Description
Removes all attributes of the input `text`.

#### Arguments
- `text`: The input HTML string

#### Returns
A new HTML string with all attributes removed

#### Examples
> **input**
```oktopus-html
{{ html.removeAllAttributes "<html><head></head><body><p src='FooBar'>FooBar</p></body></html>" }}
```
> **output**
```html
<html><head></head><body><p>FooBar</p></body></html>
```

[🔝 Back to top](#oktopus-built-in-functions)


### `html.removeAttributes`
```
html.removeAttributes <text>
```

#### Description

Removes the attributes of the input `text`. XML namespaces, src and href are not removed by this function, if you want to remove all attributes then use [`html.RemoveAllAttributes`](#htmlremoveallattributes).

#### Arguments

- `text`: The input HTML string

#### Returns

A new HTML string with the attributes removed

#### Examples

> **input**
```oktopus-html
{{ html.removeAttributes "<html><head></head><body><p title='FooBar'>FooBar</p></body></html>" }}
```
> **output**
```html
<html><head></head><body><p>FooBar</p></body></html>
```
[🔝 Back to top](#oktopus-built-in-functions)

## `json` functions

JSON functions available through the object 'json' in whoosh Oktopus.

- [`json.deserialize`](#jsondeserialize)
- [`json.format`](#jsonformat)
- [`json.serialize`](#jsonserialize)

[🔝 Back to top](#oktopus-built-in-functions)
### `json.deserialize`

```
json.deserialize <jsonString>
```

#### Description

Deserializes the input `jsonString`. The shortcut `json.parse` can be used instead.

#### Arguments

- `jsonString`: The input JSON string

#### Returns

A new JSON object

#### Examples

> **input**
```oktopus-html
{{ json.deserialize '{"Foo":"Bar"}' }}
```
> **output**
```html
{Foo: "Bar"}
```
[🔝 Back to top](#oktopus-built-in-functions)
### `json.format`

```
json.format <jsonString>
```

#### Description

Indents the input `jsonString`.

#### Arguments

- `jsonString`: The input JSON string

#### Returns

A new formatted JSON string

#### Examples

> **input**
```oktopus-html
{{ json.format '{"Foo":"Bar"}' }}
```
> **output**
```html
{
 "Foo":"Bar"
}
```
[🔝 Back to top](#oktopus-built-in-functions)
### `json.serialize`

```
json.serialize <json> <options>?
```

#### Description

Serializes the input `json`. If `options` is set to "Indented" then the resulting JSON string will be intended.

#### Arguments

- `json`: The input JSON object
- `options`: An optional string that can be set to "Indented"

#### Returns

A new JSON string

#### Examples

> **input**
```ruby
{{ json.serialize {Foo:"Bar"} }}
{{ json.serialize {Foo:"Bar"} "Indented" }}
```
> **output**
```json
{"Foo":"Bar"}

{
 "Foo":"Bar"
}
```
[🔝 Back to top](#oktopus-built-in-functions)


## `oktopus` functions
Oktopus information functions available through the object `oktopus` in whoosh Oktopus.

- [`oktopus.server`](#oktopusserver)

[🔝 Back to top](#oktopus-built-in-functions)


### `oktopus.server`
```ruby
oktopus.server
```

#### Description
Returns an object with relevant information of the current whoosh Oktopus instance.

#### Examples
> **input**
```ruby
{{ oktopus.server }}
{{ oktopus.server.uptime | object.format "%d" }}
```
> **output**
```json
{"MachineName":"TESTDEV","Uptime":"1.33:07:00.1337000","Version":"5.9.0","EnvironmentName":"Test Environment"}'
1
```
[🔝 Back to top](#oktopus-built-in-functions)

## `step` functions

Oktopus step functions available through the object 'step' in whoosh Oktopus. These functions can be set to control the workflow to enable branching in steps or enable advanced error handling.

- [`step.errorMessage`](#steperrormessage)
- [`step.item`](#stepitem)
- [`step.retry`](#stepretry)
- [`step.retryIn`](#stepretryin)
- [`step.skip`](#stepskip)
- [`step.skipIf`](#stepskipif)
- [`step.skipIfEmpty`](#stepskipifempty)
- [`step.skipIfNull`](#stepskipifnull)
- [`step.wait`](#stepwait)

[🔝 Back to top](#oktopus-built-in-functions)
### `step.errorMessage`

```
step.errorMessage
```

#### Description

Returns the error message of when a step fails. This is typically used under `Advanced Settings` in the `Error handling script`.

#### Arguments


#### Returns


#### Examples

> **input**
```oktopus-html
if (step.errorMessage | string.contains "temporarily unavailable") step.retryIn (timespan.from_seconds 5) end
```
> **output**
```html
<input>(1,1): Waiting for 5000ms...
Error handling script decided to retry step [...]
```
[🔝 Back to top](#oktopus-built-in-functions)
### `step.item`

```
step.item
```

#### Description

Returns the item set in the current step context. This can be used in certain steps like `Create or update Business Object(s)` in the `Ivanti Service Manager` technology by using an item, like a JSON, in the `Items (mass upsert)` field. In other fields set in the current step you can iterate over the item by using `step.item` and a key that is set in the item.

#### Arguments


#### Returns


#### Examples

> **input**
```oktopus-html
{{ step.item.id }}
{{ step.item.name | convert.toCsv }}
```
> **output**
```html

```
[🔝 Back to top](#oktopus-built-in-functions)
### `step.retry`

```
step.retry
```

#### Description

Retries a step if it fails. This is typically used under `Advanced Settings` in the `Error handling script`.

#### Arguments


#### Returns


#### Examples

> **input**
```oktopus-html
{{ step.retry }}
```
> **output**
```html
Error handling script decided to retry step [...]
```
[🔝 Back to top](#oktopus-built-in-functions)
### `step.retryIn`

```
step.retryIn <timespan>
```

#### Description

Waits for a given `timespan` ( set in milliseconds ) and then retries a step if it fails . This is typically used under `Advanced Settings` in the `Error handling script`.

#### Arguments

- `timespan`: The input timespan object

#### Returns


#### Examples

> **input**
```oktopus-html
{{ step.retryIn (timespan.from_seconds 5) }}
```
> **output**
```html
<input>(1,1): Waiting for 5000ms...
Error handling script decided to retry step [...]
```
[🔝 Back to top](#oktopus-built-in-functions)
### `step.skip`

```
step.skip
```

#### Description

Skips the current step. This is typically used under `Advanced Settings` in the `Error handling script`.

#### Arguments


#### Returns


#### Examples

> **input**
```oktopus-html
{{ step.skip }}
```
> **output**
```html
Skipping step [...]
```
[🔝 Back to top](#oktopus-built-in-functions)
### `step.skipIf`

```
step.skipIf <value>
```

#### Description

Skips the current step if the input `value` evaluates to true.

#### Arguments

- `value`: The input object

#### Returns


#### Examples

> **input**
```oktopus-html
{{ step.skipIf true }}
{{ step.skipIf false }}
```
> **output**
```html
Skipping step [...]
Successfully executed step [...]
```
[🔝 Back to top](#oktopus-built-in-functions)
### `step.skipIfEmpty`

```
step.skipIfEmpty <value>
```

#### Description

Skips the current step if the input `value` is null or is an empty string.

#### Arguments

- `value`: The input object

#### Returns


#### Examples

> **input**
```oktopus-html
{{ step.skipIfEmpty null }}
{{ step.skipIfEmpty "" }}
{{ step.skipIfEmpty {} }}
```
> **output**
```html
Skipping step [...]
Skipping step [...]
Successfully executed step [...]
```
[🔝 Back to top](#oktopus-built-in-functions)
### `step.skipIfNull`

```
step.skipIfNull <value>
```

#### Description

Skips the current step if the input `value` is null.

#### Arguments

- `value`: The input object

#### Returns


#### Examples

> **input**
```oktopus-html
{{ step.skipIfNull null }}
{{ step.skipIfNull {} }}
```
> **output**
```html
Skipping step [...]
Successfully executed step [...]
```
[🔝 Back to top](#oktopus-built-in-functions)
### `step.wait`

```
step.wait <timespan>
```

#### Description

Waits for a given `timespan` ( set in milliseconds ). This is typically used under `Advanced Settings` in the `Error handling script`.

#### Arguments

- `timespan`: The input timespan object

#### Returns


#### Examples

> **input**
```oktopus-html
{{ step.wait (timespan.from_seconds 5) }}
{{ step.wait 5) }}
```
> **output**
```html
<input>(1,1): Waiting for 5000ms...
<input>(1,1): Waiting for 5ms...
```
[🔝 Back to top](#oktopus-built-in-functions)

## `string` functions

String functions available through the object 'step' in whoosh Oktopus.

- [`string.getFileName`](#stringgetfilename)
- [`string.hasContent`](#stringhascontent)
- [`string.isNullOrEmpty`](#stringisnullorempty)
- [`string.TruncateSmart`](#stringtruncatesmart)

[🔝 Back to top](#oktopus-built-in-functions)
### `string.getFileName`

```
string.getFileName <name> <extension> <fallbackName>?
```

#### Description

Returns the file name of of the input `name` and `extension`. The optional `fallbackName` will be used if `name` contains invalid characters, like `/`, `\`, `<`, `>`, `|`, `:`, `*`, `?` or `"`.

#### Arguments

- `name`: The input string of the resulting file name
- `extension`: The input string of the resulting file name extension
- `fallbackName`: An optional string that is used instead of `name`

#### Returns

A new string of file name

#### Examples

> **input**
```oktopus-html
string.GetFileName "Test" "eml" "Email"
string.GetFileName "<>" "eml" "Email"
```
> **output**
```html
Test.eml
Email.eml
```
[🔝 Back to top](#oktopus-built-in-functions)
### `string.hasContent`

```
string.hasContent <value>
```

#### Description

Returns if an input `value` has content.

#### Arguments

- `value`: The input string

#### Returns

**true** if `value` has content; otherwise **false**

#### Examples

> **input**
```oktopus-html
{{ string.hasContent "Test" }}
{{ string.hasContent "" }}
```
> **output**
```html
true
false
```
### `string.isNullOrEmpty`

```
string.isNullOrEmpty <value>
```

#### Description

Returns if an input `value` is null or empty.

#### Arguments

- `value`: The input string

#### Returns

**true** if `value` is empty; otherwise **false**

#### Examples

> **input**
```oktopus-html
{{ string.isNullOrEmpty "" }}
{{ string.isNullOrEmpty "Test" }}
```
> **output**
```html
true
false
```
[🔝 Back to top](#oktopus-built-in-functions)

### `string.TruncateSmart`
```
string.TruncateSmart <text> <maxLength> <ellipsis>? <averageWordLength>?
```

#### Description
Truncates the `text` when it's too long.\
The algorithm tries to be smart and truncate directly after a word (when reasonable).

#### Arguments
- `text`: The input string
- `maxLength`: The maximum number of characters to return (includes the `ellipsis`).
- `ellipsis`: The ellipsis to use when the text is truncated. Default: `...`
- `averageWordLength`: The average length of a word. Default: `10`

#### Returns
The original or truncated text.

#### Examples
> **input**
```oktopus-html
{{ string.TruncateSmart "Lorem ipsum, consetetur elitr." 20 }}
{{ string.TruncateSmart "Lorem ipsum, consetetur elitr." 20 averageWordLength: 5 }}
{{ string.TruncateSmart "Lorem ipsum, consetetur elitr." 20 "---" }}
```
> **output**
```html
Lorem ipsum,...
Lorem ipsum, cons...
Lorem ipsum,---
```
[🔝 Back to top](#oktopus-built-in-functions)

## `timeOnly` functions

TimeOnly functions available through the object 'timeOnly' in whoosh Oktopus.

- [`timeOnly.from`](#timeonlyfrom)
- [`timeOnly.now`](#timeonlynow)
- [`timeOnly.parse`](#timeonlyparse)

[🔝 Back to top](#oktopus-built-in-functions)
### `timeOnly.from`

```
timeOnly.from <dateTime>
```

#### Description

Returns a time object of an input `dateTime`.

#### Arguments

- `dateTime`: The input datetime object

#### Returns

A new time object of the `dateTime` input.

#### Examples

> **input**
```oktopus-html
{{ timeOnly.from date.now }}
{{ dateTime = date.parse "2024/12/31 13:37:00Z"; timeOnly.from dateTime  }}
```
> **output**
```html
13:37:00.0000000
14:37:00.0000000
```
[🔝 Back to top](#oktopus-built-in-functions)
### `timeOnly.now`

```
timeOnly.now
```

#### Description

Returns a new time object of the current time.

#### Arguments


#### Returns


#### Examples

> **input**
```oktopus-html
{{ timeOnly.now }}
```
> **output**
```html
13:37:00.0000000
```
[🔝 Back to top](#oktopus-built-in-functions)
### `timeOnly.parse`

```
timeOnly.parse <timeString> <culture>?
```

#### Description

Returns a time object of an input time string. An optional `culture` can be passed to specify the format of the `timeString`.
If the `culture` is not specified then the default will be used.

#### Arguments

- `timeString`: The input time string
- `culture`:  An optional string of the culture format

#### Returns

A new time object of the input `dateString`

#### Examples

> **input**
```oktopus-html
{{ timeOnly.parse "13:37:00" }}
{{ (timeOnly.parse "13:37:00") | object.format "HH" }}
{{ timeOnly.parse "1:37 PM" }}
```
> **output**
```html
13:37:00.0000000
13
13:37:00.0000000
```
[🔝 Back to top](#oktopus-built-in-functions)

## `variable` functions

Variable functions available through the object 'variable' in whoosh Oktopus.

- [`variable.skip`](#variableskip)
- [`variable.skipIf`](#variableskipif)
- [`variable.skipIfEmpty`](#variableskipifempty)
- [`variable.skipIfNotEmpty`](#variableskipifnotempty)
- [`variable.skipIfNotNull`](#variableskipifnotnull)
- [`variable.skipIfNull`](#variableskipifnull)
- [`variable.store`](#variablestore)
- [`variable.useNull`](#variableusenull)

[🔝 Back to top](#oktopus-built-in-functions)
### `variable.skip`

```
variable.skip
```

#### Description

Skips the variable of a step.

#### Arguments


#### Returns


#### Examples

> **input**
```oktopus-html
{{ variable.skip }}
```
> **output**
```html
Ignoring [...]
```
[🔝 Back to top](#oktopus-built-in-functions)
### `variable.skipIf`

```
variable.skipIf <value>
```

#### Description

Skips the variable of a step if the input `value` evaluates to true.

#### Arguments

- `value`: The input object

#### Returns


#### Examples

> **input**
```oktopus-html
{{ variable.skipIf true }}
{{ variable.skipIf false }}
```
> **output**
```html
Ignoring [...]
Successfully executed step [...]
```
[🔝 Back to top](#oktopus-built-in-functions)
### `variable.skipIfEmpty`

```
variable.skipIfEmpty <value>
```

#### Description

Skips the variable of a step if the input `value` is null or is an empty string. The shortcut `variable.skipEmpty` can be used instead.

#### Arguments

- `value`: The input object

#### Returns


#### Examples

> **input**
```oktopus-html
{{ variable.skipIfEmpty null }}
{{ variable.skipIfEmpty "" }}
{{ variable.skipIfEmpty {} }}
```
> **output**
```html
Ignoring [...]
Ignoring [...]
Successfully executed step [...]
```
[🔝 Back to top](#oktopus-built-in-functions)
### `variable.skipIfNotEmpty`

```
variable.skipIfNotEmpty <value>
```

#### Description

Skips the variable of a step if the input `value` is not an empty string. The shortcut `variable.skipNotEmpty` can be used instead.

#### Arguments

- `value`: The input object

#### Returns


#### Examples

> **input**
```oktopus-html
{{ variable.skipIfNotEmpty null }}
{{ variable.skipIfNotEmpty "" }}
{{ variable.skipIfNotEmpty "{}" }}
```
> **output**
```html
Successfully executed step [...]
Successfully executed step [...]
Ignoring [...]
```
[🔝 Back to top](#oktopus-built-in-functions)
### `variable.skipIfNotNull`

```
variable.skipIfNotNull <value>
```

#### Description

Skips the variable of a step if the input `value` is not null. The shortcut `variable.skipNotNull` can be used instead.

#### Arguments

- `value`: The input object

#### Returns


#### Examples

> **input**
```oktopus-html
{{ variable.skipIfNotNull {} }}
{{ variable.skipIfNotNull null }}
```
> **output**
```html
Ignoring [...]
Successfully executed step [...]
```
[🔝 Back to top](#oktopus-built-in-functions)
### `variable.skipIfNull`

```
variable.skipIfNull <value>
```

#### Description

Skips the variable of a step if the input `value` is null. The shortcut `variable.skipNull` can be used instead.

#### Arguments

- `value`: The input object

#### Returns


#### Examples

> **input**
```oktopus-html
{{ variable.skipIfNull null }}
{{ variable.skipIfNull {} }}
```
> **output**
```html
Ignoring [...]
Successfully executed step [...]
```
[🔝 Back to top](#oktopus-built-in-functions)
### `variable.store`

```
variable.store <value> <variableName>
```

#### Description

Stores the input `value` with a `variableName` in the current workflow context. To use the variable just call the `variableName` in any step after the variable was stored.

#### Arguments

- `value`: The input object
- `variableName`: The string for the variable name

#### Returns


#### Examples

> **input**
```oktopus-html
{{ variable.store "Bar" "Foo" }}
{{ variable.store {Foo:"Bar"} "FooBar" }}
```
> **output**
```html
Storing variable 'Foo'='Bar'
Storing variable 'FooBar'='{"Foo":"Bar"}'
```
[🔝 Back to top](#oktopus-built-in-functions)
### `variable.useNull`

```
variable.useNull
```

#### Description

Forces `null` to be used as a variable instead of an empty string.

#### Arguments


#### Returns


#### Examples

> **input**
```oktopus-html
{{ variable.useNull }}
```
> **output**
```html
Text = <null>
```
[🔝 Back to top](#oktopus-built-in-functions)

## `workflow` functions

Workflow functions available through the object 'workflow' in whoosh Oktopus.

- [`workflow.fail`](#workflowfail)
- [`workflow.hideSecret`](#workflowhideSecret)
- [`workflow.log`](#workflowlog)
- [`workflow.stop`](#workflowstop)
- [`workflow.stopIf`](#workflowstopIf)
- [`workflow.stopIfEmpty`](#workflowstopIfEmpty)
- [`workflow.stopIfNull`](#workflowstopIfNull)

[🔝 Back to top](#oktopus-built-in-functions)
### `workflow.fail`

```
workflow.fail <reason>?
```

#### Description

Fails the current workflow. An optional `reason` string can be used to display a message why the workflow failed.

#### Arguments

- `reason`: An optional message string

#### Returns


#### Examples

> **input**
```oktopus-html
{{ workflow.fail }}
{{ if MyVariable == "Fail"; workflow.fail "Workflow failed."; end }}
```
> **output**
```html
Failed to execute step [...]
Failed to execute step [...] 'Fail (Workflow failed.)']
```
[🔝 Back to top](#oktopus-built-in-functions)
### `workflow.hideSecret`

```
workflow.hideSecret <value>
```

#### Description

Prevent logging the clear text of the `value`.

#### Arguments


#### Returns


#### Examples

> **input**
```oktopus-html
{{ workflow.hideSecret user.password }}
```
> **output**
```html
```
[🔝 Back to top](#oktopus-built-in-functions)
### `workflow.log`

```
workflow.log <value> <logLevel>?
```

#### Description

Logs the `value` under "Protocol" after the step was executed where the function was called. An optional `logLevel` string ( "[Success | Warning | Error]" ) can be used for advanced logging.

#### Arguments


#### Returns


#### Examples

> **input**
```oktopus-html
{{ workflow.log "FooBar" }}
{{ workflow.log "FooBar" "Success" }}
```
> **output**
```html
🛈FooBar
✅FooBar
```
[🔝 Back to top](#oktopus-built-in-functions)
### `workflow.stop`

```
workflow.stop <reason>?
```

#### Description

Stops the current workflow. An optional `reason` string can be used to display a message why the workflow stopped.

#### Arguments

- `reason`: An optional message string

#### Returns


#### Examples

> **input**
```oktopus-html
{{ workflow.stop }}
{{ if MyVariable == "Abort"; workflow.stop "Stopping workflow now."; end }}
```
> **output**
```html
Stopping workflow at step [...]
Stopping workflow at step [...] 'Stopping workflow now.'
```
[🔝 Back to top](#oktopus-built-in-functions)
### `workflow.stopIf`

```
workflow.stopIf <value> <reason>?
```

#### Description

Stops the current workflow if the input `value` evaluates to true. An optional `reason` string can be used to display a message why the workflow stopped.

#### Arguments

- `value`: The input object
- `reason`: An optional message string

#### Returns


#### Examples

> **input**
```oktopus-html
{{ workflow.stopIf true }}
{{ workflow.stopIf MyVariable == "Abort" "Stopping workflow now." }}
{{ workflow.stopIf false }}
```
> **output**
```html
Stopping workflow at step [...]
Stopping workflow at step [...] 'Stopping workflow now.'
Successfully executed step [...]
```
[🔝 Back to top](#oktopus-built-in-functions)
### `workflow.stopIfEmpty`

```
workflow.stopIfEmpty <value> <reason>?
```

#### Description

Stops the workflow if the input `value` is null or is an empty string. An optional `reason` string can be used to display a message why the workflow stopped.

#### Arguments

- `value`: The input object
- `reason`: An optional message string

#### Returns


#### Examples

> **input**
```oktopus-html
{{ workflow.stopIfEmpty null }}
{{ workflow.stopIfEmpty "" "Stopping workflow now." }}
{{ workflow.stopIfEmpty {} }}
```
> **output**
```html
Stopping workflow at step [...]
Stopping workflow at step [...] 'Stopping workflow now.'
Successfully executed step [...]
```
[🔝 Back to top](#oktopus-built-in-functions)

### `workflow.stopIfNull`
```
workflow.stopIfNull <value> <reason>?
```

#### Description
Stops the current workflow if the input `value` is null. An optional `reason` string can be used to display a message why the workflow stopped.

#### Arguments
- `value`: The input object
- `reason`: An optional message string

#### Returns


#### Examples
> **input**
```oktopus-html
{{ workflow.stopIfNull null }}
{{ workflow.stopIfNull null "Stopping workflow now." }}
{{ workflow.stopIfNull {} }}
```
> **output**
```html
Stopping workflow at step [...]
Stopping workflow at step [...] 'Stopping workflow now.'
Successfully executed step [...]
```

[🔝 Back to top](#oktopus-built-in-functions)
