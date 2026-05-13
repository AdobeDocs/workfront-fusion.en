---
title: General functions
description: The following general functions are available in the Adobe Workfront Fusion mapping panel.
author: Becky
feature: Workfront Fusion
exl-id: 6d4b8801-aa7e-47d4-80b3-aceac10c073f
TQID: https://experienceleague.adobe.com/1IX25ZtrWVizi5gZJfFw-acnW5eIuXpGgcXgXW0T-Hw
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
---
# General functions

## Variables

You can use these general variables to identify details about an execution:

* `executionID`: the ID of this scenario execution
* `triggerTimestamp`: The time at which this execution was triggered
* `scenarioID`: the ID of the currently opened scenario
* `scenarioName`: the name of the currently running scenario
* `operationsConsumed`: the number of operations used at that point in the scenario.

## [!UICONTROL get (object or array; path)]

Returns the value path of an object or array. To access nested objects, use dot notation. The first item in an array is index 1.

>[!BEGINSHADEBOX]

**Examples:** 

* `get( array ; 1 + 1 )`
* `get( array ; 5.raw_name )`
* `get( object ; raw_name )`
* `get( object ; raw_name.sub_raw_name )`

>[!ENDSHADEBOX]

## [!UICONTROL if (expression; value1; value2)]

Returns the `value1` if the expression is evaluated to true; otherwise it returns the `value2`.

To create an if statement that returns a value only if two or more expressions are evaluated to true, use the `and` keyword. 

To combine `if` statements, use the `and` and `or` operators.

![and operator](assets/and-in-if-statement.png)

>[!BEGINSHADEBOX]

**Examples:** 

* `if( 1 = 1 ; A ; B )`

    Returns A

* `if( 1 = 2 ; A ; B )`

   Returns B

* `if( 1 = 2 and 1 = 2 ; A ; B )`

    Returns B

>[!ENDSHADEBOX]

## [!UICONTROL ifempty (value1; value2)]

Returns the `value1` if this value is not empty; otherwise it returns the `value2`.

>[!BEGINSHADEBOX]

**Examples:** 

* `ifempty(` `A` `;` `B` )

   Returns A

* `ifempty(` `unknown` `;` `B` )

   Returns B

* `ifempty(` `""` `;` `B` )

   Returns B

>[!ENDSHADEBOX]

## [!UICONTROL switch (expression; value1; result1; [value2; result2; ...]; [else])]

Evaluates one value (called the expression) against a list of values; returns the result corresponding to the first matching value. To include an  `else` value, add it after the final expression or value.

>[!BEGINSHADEBOX]

**Examples:** 

* `switch( B ; A ; 1 ; B ; 2 ; C ; 3 )`

   Returns 2

* `switch( C ; A ; 1 ; B ; 2 ; C ; 3 )`

   Returns 3

* `switch( X ; A ; 1 ; B ; 2 ; C ; 3 ; 4 )`

   Returns 4
   
   In this function, 4 is the value to be returned if no expressions apply (the `else` value).

>[!ENDSHADEBOX]

## [!UICONTROL omit(object; key1; [key2; ...])]

Omits the given keys of the object and returns the rest.

>[!BEGINSHADEBOX]

**Example:**

`omit(` User `;` password `)`

Returns a collection of the user's information, excluding the password.

>[!ENDSHADEBOX]

## [!UICONTROL pick(object; key1; [key2; ...])]

Picks only the given keys from the object.

>[!BEGINSHADEBOX]

**Example:** 

`pick(` User `;` password `;` email `)`

Returns a collection of only the user's password and email address.

>[!ENDSHADEBOX]

## mergeCollections(collection1; collection2)

Merges two collections by combining their key-value pairs. If both collections contain the same key, the value from the second collection overwrites that value from the first collection.

### [!UICONTROL isBlank(value)]

Returns `true` if the value is `null` or an empty string, otherwise returns `false`. Unlike `ifEmpty`, this function does not treat the number `0` or whitespace-only strings as blank.

>[!BEGINSHADEBOX]

**Example:** 

* `isBlank("")     `

   Returns  true
* `isBlank(null)   `

   Returns  true
* `isBlank("Hello")`

   Returns  false
* `isBlank(0)      `

   Returns  false
* `isBlank(" ")    `

   Returns  false

>[!ENDSHADEBOX]


### [!UICONTROL in(value; value1; value2; ...)]

Returns `true` if the value equals one of the provided values (strict equality, no type coercion).

>[!BEGINSHADEBOX]

**Example:** 

* `in("B"; "A"; "B"; "C")`

   Returns  true
* `in("D"; "A"; "B"; "C")`

   Returns  false
* `in(2; 1; 2; 3)        `

   Returns  true
* `in("2"; 1; 2; 3)      `

   Returns  false

>[!ENDSHADEBOX]

### [!UICONTROL ifin(value; value1; value2; ...; trueExpression; falseExpression)]

Returns `trueExpression` if the value matches any of the provided match values, otherwise returns `falseExpression`. Requires at least 3 arguments (value, one match value, and trueExpression + falseExpression).

>[!BEGINSHADEBOX]

**Example:** 

* `ifin("B"; "A"; "B"; "yes"; "no")`

   Returns  yes
* `ifin("D"; "A"; "B"; "yes"; "no")`

   Returns  no
* `ifin("X"; "X"; "found"; "not found")`

   Returns  found

>[!ENDSHADEBOX]

### [!UICONTROL case(indexNumber; value1; value2; ...)]

Returns the value at the position specified by the index number (1-based). Returns `null` if the index is out of bounds or is 0.

>[!BEGINSHADEBOX]

**Example:** 

* `case(1; "Sun"; "Mon"; "Tue")`

   Returns  Sun
* `case(2; "Sun"; "Mon"; "Tue")`

   Returns  Mon
* `case(3; "Sun"; "Mon"; "Tue")`

   Returns  Tue
* `case(5; "a"; "b")           `

   Returns  null

>[!NOTE]
>
>We recommend using this to get day name from a date:
>`case(dayOfWeek(date); "Sun"; "Mon"; "Tue"; "Wed"; "Thu"; "Fri"; "Sat")`

>[!ENDSHADEBOX]

