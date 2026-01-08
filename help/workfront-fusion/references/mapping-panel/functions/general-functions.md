---
title: General functions
description: The following general functions are available in the Adobe Workfront Fusion mapping panel.
author: Becky
feature: Workfront Fusion
exl-id: 6d4b8801-aa7e-47d4-80b3-aceac10c073f
---
# General functions

## Variables

You can use these general variables to identify details about an execution:

* `executionID`: the ID of this scenario execution
* `triggerTimestamp`: The time at which this execution was triggered
* `scenarioID`: the ID of the currently opened scenario
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
