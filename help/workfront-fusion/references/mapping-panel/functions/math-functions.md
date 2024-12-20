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
