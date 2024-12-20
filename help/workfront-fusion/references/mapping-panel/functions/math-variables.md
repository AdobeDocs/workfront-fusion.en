---
title: Math variables
description: The following math variables are available in the [!DNL Adobe Workfront Fusion mapping] panel.
author: Becky
feature: Workfront Fusion
exl-id: b309f035-4d46-473b-b915-6938587b0bcf
---
# Math variables

## pi

Represents the mathematical symbol $\pi$.

## [!UICONTROL random]

Returns a floating-point pseudo-random number in the range [`0`,`1`] (inclusive of `0`, but not `1`).

Use the following formula to generate an integer pseudo-random number in the range [`min`,`max`] (inclusive of both `min` and `max`):

![](assets/math-variable-random-350x61.png)

```
floor(random * (1.max - 1.min + 1)) + 1.min
```
