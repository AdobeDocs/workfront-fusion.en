---
title: Math functions
description: The following math functions are available in the Adobe Workfront Fusion mapping panel.
author: Becky
feature: Workfront Fusion
exl-id: 3d08b09d-b395-4226-b7e3-d5650c428a59
---
# Math functions

## [!UICONTROL average ([array of values]) average(value1; [value2], ...)]

Returns the average value of the numeric values in a specific array, or the average value of numerical values entered individually.

## [!UICONTROL ceil (number)]

Returns the smallest integer greater than or equal to a specified number.

>[!BEGINSHADEBOX]

**Examples:** 

* `ceil(` `1.2` `)`

   Returns 2

* `ceil(` `4` `)`

   Returns 4

>[!ENDSHADEBOX]

## [!UICONTROL floor (number)]

Returns the largest integer less than or equal to a specified number.

>[!BEGINSHADEBOX]

**Examples:** 

* `floor(` `1.2` `)`

   Returns 1

* `floor(` `1.9` `)`

   Returns 1

* `floor(` `4` `)`

   Returns 4

>[!ENDSHADEBOX]

## [!UICONTROL max ([array of values]), max(value1;value2; ...)]

Returns the largest number in a specified array or the largest number among numbers entered individually.

## [!UICONTROL min ([array of values]), min(value1; value2; ...)]

Returns the smallest number in a specified array or the smallest number among numbers entered individually.

## [!UICONTROL round (number)]

Rounds a numeric value to the nearest integer.

>[!BEGINSHADEBOX]

**Examples:** 

* `round(` `1.2` `)`

   Returns 1

* `round(` `1.5` `)`

   Returns 2

* `round(` `1.7` `)`

   Returns 2
 
* `round(` `2` `)`

   Returns 2

>[!ENDSHADEBOX]

## [!UICONTROL sum ([array of values]), sum(value1; value2; ...)]

Returns the sum of the values in a specified array or the sum of numbers entered individually.

## [!UICONTROL parseNumber (number; decimal separator)]

Parses a string with a number and returns the number. For example, parseNumber(1 756,456;,)

## [!UICONTROL formatNumber (number; decimalPOINTS; [decimalSeparator]; [thousandsSeparator])]

Returns a number in requested format. By default, the decimal point is a comma (,) and the thousands separator is a period (.).

>[!BEGINSHADEBOX]

**Example:** 

`formatNumber( 123456789 ; 3 ; , ; . )`

Returns 123.456.789,000

>[!ENDSHADEBOX]

### [!UICONTROL abs(number)]

[!BADGE New!]{type=Informative}

Returns the absolute value of a number.

>[!BEGINSHADEBOX]

**Example:** 

* `abs(-3.14)`

   Returns 3.14
* `abs(3.14)`

   Returns 3.14


### [!UICONTROL div(number1; number2; ...)]

[!BADGE New!]{type=Informative}

Divides all the numbers in the order provided.

>[!BEGINSHADEBOX]

**Example:** 

* `div(10; 2)`

   Returns 5
* `div(100; 5; 4)`

   Returns 5


### [!UICONTROL ln(number)]

[!BADGE New!]{type=Informative}

Returns the natural logarithm of the number.


>[!BEGINSHADEBOX]

**Example:** 

* `ln(1)`

   Returns 0
* `ln(2.718281828)`

   Returns 1


### [!UICONTROL log(number1; number2)]

[!BADGE New!]{type=Informative}

Returns the logarithm of `number2` to the base `number1`.

>[!BEGINSHADEBOX]

**Example:** 

* `log(10; 100)`

   Returns 2
* `log(2; 8)`

   Returns 3


### [!UICONTROL number(string)]

[!BADGE New!]{type=Informative}

Converts a string to a number.

>[!BEGINSHADEBOX]

**Example:** 

* `number("3.14")`

   Returns 3.14
* `number("42")`

   Returns 42


### [!UICONTROL power(number; power)]

[!BADGE New!]{type=Informative}

Returns a number raised to the specified power.

>[!BEGINSHADEBOX]

**Example:** 

* `power(2; 3)`

   Returns 8
* `power(4; 0.5)`

   Returns 2


### [!UICONTROL prod(number1; number2; ...)]

[!BADGE New!]{type=Informative}

Multiplies all the provided numbers together.

>[!BEGINSHADEBOX]

**Example:** 

* `prod(2; 3; 4)`

   Returns 24
* `prod(5; 5)`

   Returns 25


### [!UICONTROL sortAscNum(number1; number2; ...)]

[!BADGE New!]{type=Informative}

Returns the provided numbers sorted in ascending order.

>[!BEGINSHADEBOX]

**Example:** 

* `sortAscNum(3; 1; 2)`

   Returns \[1, 2, 3]
* `sortAscNum(5; 3; 4)`

   Returns \[3, 4, 5]


### [!UICONTROL sortDescNum(number1; number2; ...)]

[!BADGE New!]{type=Informative}

Returns the provided numbers sorted in descending order.

>[!BEGINSHADEBOX]

**Example:** 

* `sortDescNum(3; 1; 2)`

   Returns \[3, 2, 1]
* `sortDescNum(5; 3; 4)`

   Returns \[5, 4, 3]


### [!UICONTROL sqrt(number)]

[!BADGE New!]{type=Informative}

Returns the square root of a number.

>[!BEGINSHADEBOX]

**Example:** 

* `sqrt(9)`

   Returns 3
* `sqrt(4)`

   Returns 2


### [!UICONTROL sub(number1; number2; ...)]

[!BADGE New!]{type=Informative}

Subtracts all numbers in the order provided.

>[!BEGINSHADEBOX]

**Example:** 

* `sub(10; 3; 2)`

   Returns 5
* `sub(20; 5)`

   Returns 15
