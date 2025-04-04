---
title: String functions
description: The following string functions are available in the Adobe Workfront Fusion mapping panel.
author: Becky
feature: Workfront Fusion
exl-id: d3e49fce-85bc-4ee6-9a94-497a306e0c74
---
# String functions

## [!UICONTROL length (text or buffer)]

Returns the length of text string (number of characters) or binary buffer (buffer size in bytes).

>[!BEGINSHADEBOX]

**Example:** 

`length( hello )`  

Returns: 5

>[!ENDSHADEBOX]

## [!UICONTROL lower (text)]

Converts all alphabetical characters in a text string to lowercase.

>[!BEGINSHADEBOX]

**Example:** 

`lower( Hello )`

Returns: hello

>[!ENDSHADEBOX]

## [!UICONTROL capitalize (text)]

Converts the first character in a text string to uppercase.

>[!BEGINSHADEBOX]

**Example:** 

`capitalize( workfront )`

Returns: [!DNL Workfront]  

>[!ENDSHADEBOX]

## [!UICONTROL startcase (text)]

Capitalizes the first letter of every word and lower cases all other letters.

>[!BEGINSHADEBOX]

**Example:** 
`startcase( hello WORLD )`

Returns: [!UICONTROL Hello World]

>[!ENDSHADEBOX]

## [!UICONTROL ascii (text; [remove diacritics])]

Removes all non-ascii characters from a text string.

>[!BEGINSHADEBOX]

**Examples:**

* `ascii(` `Wěošrčkřfžrýoáníté` `)`

Returns: [!DNL Workfront]

* `ascii(` `ěščřž` `;` `true` `)`

Returns: [!UICONTROL escrz]

>[!ENDSHADEBOX]

## [!UICONTROL replace (text;search string; replacement string)]

Replaces the search string with the new string.

>[!BEGINSHADEBOX]

**Example:** 

`replace( Hello World ; Hello ; Hi )`

Returns: [!UICONTROL Hi World]  

>[!ENDSHADEBOX]

Regular expressions (enclosed in `/.../`) can be used as search string with a combination of flags (such as `g`, `i`, `m`) appended:

>[!BEGINSHADEBOX]

**Example:**  

![Replace](assets/replace---1-350x31.png)

All of these numbers X X X X are replaced with X  

>[!ENDSHADEBOX]

The replacement string can include the following special replacement patterns:

* `$&` Inserts the matched substring.
* `$n` Where n is a positive integer less than 100, inserts the nth parenthesized submatch string. This is 1-indexed.

>[!BEGINSHADEBOX]

**Examples:**  

![Variable value](assets/variable-value-350x63.png)

Returns: Phone number `+420777111222`

![Variable return](assets/variable-value---2-350x55.png)

Returns: Phone number: `+420777111222`

>[!CAUTION]
>
>Do not use named capture groups such as `/ is (?<number>\d+)/` in the replacement string argument. Doing so results in an error.


>[!ENDSHADEBOX]

For more information on regular expressions, see [Text parser](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/text-parser.md).

## [!UICONTROL trim (text)]

Removes space characters at the start or end of the text.

## [!UICONTROL upper (text)]

Converts all alphabetical characters in a text string to uppercase.

>[!BEGINSHADEBOX]

**Example:** 

`upper( Hello )`

Returns: [!UICONTROL HELLO] 

>[!ENDSHADEBOX]

## [!UICONTROL substring (text; start;end)]

Returns a portion of a text string between the "start" position and "end" position.

>[!BEGINSHADEBOX]

**Examples:**

* `substring( Hello ; 0 ; 3)`

   Returns: Hel

* `substring( Hello ; 1 ; 3 )`

   Returns: el

>[!ENDSHADEBOX]

## [!DNL indexOf (string; value; [start])]

Returns the position of the first occurrence of a specified value in a string. This method returns '-1' if the value that is searched for is not there. The start value indicates where in the string the search should begin.

>[!BEGINSHADEBOX]

**Examples:**

* `indexOf( Workfront ; o )`

   Returns: 1

* `indexOf( Workfront ; x )`

   Returns: -1

* `indexOf( Workfront ; o ; 3 )`

   Returns: 6

>[!ENDSHADEBOX]

## [!UICONTROL toBinary (value)]

Converts any value to binary data.

You can also specify encoding as a second argument to apply binary conversions from hex or base64 to binary data.

>[!BEGINSHADEBOX]

**Examples:**

* `toBinary( Workfront )`

   Returns: 57 6f 72 6b 66 72 6f 6e 74

* `toBinary( V29ya2Zyb250 ; base64 )`

   Returns: 57 6f 72 6b 66 72 6f 6e 74

>[!ENDSHADEBOX]

## [!UICONTROL toString (value)]

Converts any value to a string.

## [!UICONTROL encodeURL (text)]

Encodes special characters in some text to a valid URL address.

## [!UICONTROL decodeURL (text)]

Decodes special characters in a URL to text.

>[!BEGINSHADEBOX]

**Example:** 
`decodeURL( Automate%20your%20workflow )`

Returns: [!UICONTROL Automate your workflow]  

>[!ENDSHADEBOX]

## [!UICONTROL escapeHTML (text)]

Escapes all HTML tags in text.

>[!BEGINSHADEBOX]

**Example:** 

`escapeHTML( <b>Hello</b> )`

 Returns: `&lt;b&gt;Hello&lt;/b&gt;`

>[!ENDSHADEBOX]

## [!UICONTROL escapeMarkdown(text)]

Escapes all Markdown tags in text.

>[!BEGINSHADEBOX]

**Example:** 

`escapeMarkdown( # Header )`

Returns: `&#35; Header`

>[!ENDSHADEBOX]

## [!UICONTROL stripHTML (text)]

Removes all HTML tags from text.

>[!BEGINSHADEBOX]

**Example:** 

`stripHTML( <b>Hello</b> )`

Returns: Hello

>[!ENDSHADEBOX]

## contains (text; search string)

Verifies whether text contains the search string.

>[!BEGINSHADEBOX]

**Examples:**

* `contains( Hello World ; Hello )`

   Returns: [!UICONTROL true]

* `contains( Hello World ; Bye )`

   Returns: [!UICONTROL false]

>[!ENDSHADEBOX]

## [!UICONTROL split (text; separator)]

Splits a string into an array of strings by separating the string into substrings.

>[!BEGINSHADEBOX]

**Example:** 

`split( John, George, Paul ; , )`

>[!ENDSHADEBOX]

## [!UICONTROL md5 (text)]

Calculates the md5 hash of a string.

>[!BEGINSHADEBOX]

**Example:** 

`md5( Workfront )`

Returns: `1448bbbeaa7a9b8091d426999f1f666b`

>[!ENDSHADEBOX]

## [!UICONTROL sha1 (text; [encoding]; [key])]

Calculates the sha1 hash of a string. If the key argument is specified, sha1 HMAC hash is returned instead. Supported encodings: "hex" (default), "base64" or "latin1."

>[!BEGINSHADEBOX]

**Example:** 

`sha1( workfront )`

Returns: b2b30b8ae1f9e5b40fbb0696eaabdbfd8d0c087f  

>[!ENDSHADEBOX]

## [!UICONTROL sha256 (text; [encoding]; [key])]

Calculates the sha256 hash of a string. If the key argument is specified, sha256 HMAC hash is returned instead. Supported encodings: "hex" (default), "base64" or "latin1".>

>[!BEGINSHADEBOX]

**Example:**

`sha256( workfront )`

Returns: ed3d7397eec7b94453035b67ba4468c883ee3bedeb57137f7371f2e0cf5e2bbc  

>[!ENDSHADEBOX]

## [!UICONTROL sha512 (text; [output encoding]; [key]; [key encoding])]

Calculates the sha512 hash of a string. If the key argument is specified, sha512 HMAC hash is returned instead.

Supported encodings:

* "[!UICONTROL hex]" (default)
* "[!UICONTROL base64]"
* "[!UICONTROL latin1]"

Supported key encodings:

* "[!UICONTROL text]" (default)
* "[!UICONTROL hex]"
* "[!UICONTROL base64]" or "[!UICONTROL binary]"

When using "[!UICONTROL binary]" key encoding, a key must be a buffer, not a string.

>[!BEGINSHADEBOX]

**Example:** 

`sha512(workfront)`

Returns: 789ae41b9456357e4f27c6a09956a767abbb8d80b206003ffdd1e94dbc687cd119b85e1e19db58bb44b234493af35fd431639c0345aadf2cf7ec26e9f4a7fb19 

>[!ENDSHADEBOX]

## [!UICONTROL base64 (text)]

Transforms text to base64.

>[!BEGINSHADEBOX]

**Example:** 

`base64( workfront )`

Returns: d29ya2Zyb250==  

>[!ENDSHADEBOX]
