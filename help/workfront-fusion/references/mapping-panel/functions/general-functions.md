---
title: General functions
description: The following general functions are available in the Adobe Workfront Fusion mapping panel.
author: Becky
feature: Workfront Fusion
exl-id: 6d4b8801-aa7e-47d4-80b3-aceac10c073f
TQID: 'https://experienceleague.adobe.com/1IX25ZtrWVizi5gZJfFw-acnW5eIuXpGgcXgXW0T-Hw'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
---
# General functions

## Variables

You can use these general variables to identify details about an execution:

* `executionId`: the ID of this scenario execution
* `scenarioId`: the ID of the currently opened scenario
* `scenarioName`: the name of the currently running scenario
* `scenarioUrl`: a link to the current scenario in the Fusion user interface
* `executionUrl`: a link to the current scenario execution in the Fusion user interface
* `scenarioApiUrl`: the Fusion API URL for the current scenario
* `executionApiUrl`: the Fusion API URL for the details of the current execution
* `teamId`: the ID of the Fusion team that owns the current scenario
* `organizationId`: the ID of the Fusion organization associated with the current execution. This is not an Adobe IMS organization ID.
* `triggerTimestamp`: The time at which this execution was triggered
* `operationsConsumed`: the number of operations used at that point in the scenario.

Variable names are case-sensitive. For example, use `scenarioUrl`, not `scenarioURL`.

You can use these variables in mapped fields without building URLs or hardcoding team and organization IDs. For example, you can include the following in a mapped text field in a notification:

<pre><code>
Scenario: &#123;&#123;scenarioName&#125;&#125;
Open scenario: &#123;&#123;scenarioUrl&#125;&#125;
Open execution: &#123;&#123;executionUrl&#125;&#125;
Team: &#123;&#123;teamId&#125;&#125;
Organization: &#123;&#123;organizationId&#125;&#125;
</code></pre>

Keep the following in mind when you use these variables:

* The values are resolved when the scenario runs. The mapping panel lists the variables, but it does not preview their values.
* `scenarioUrl` and `executionUrl` link to the scenario and to the execution in the Fusion user interface. `scenarioApiUrl` and `executionApiUrl` are API endpoint URLs, not links to Fusion pages.
* The API URL variables return text only. They do not make a request or provide authentication credentials. Normal API authentication and permissions still apply.
* Links do not grant additional access. Normal Fusion permissions apply.
* `executionUrl` is not generated for runs that are not saved to execution history, such as sandbox runs or runs with history synchronization turned off. A generated link does not guarantee that the execution details are available at the moment you use it.
* `scenarioUrl` cannot be generated for a template or an unsaved scenario.
* If a URL cannot be generated, the variable has no value.

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

