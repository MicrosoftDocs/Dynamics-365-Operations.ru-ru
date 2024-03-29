---
title: Список функций ER в логической категории
description: В этой статье содержится информация о логических функциях, которые поддерживаются в электронной отчетности (ER).
author: kfend
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 1d011968d9cfa4125e7283ca36c3558e3e79b93a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291305"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>Список функций ER в логической категории

[!include [banner](../includes/banner.md)]

Логические функции электронной отчетности (ER) могут использоваться для работы с логическими значениями для выполнения более одного сравнения в одном выражении или для тестирования нескольких условий. В данной статье приводится краткое описание этих функций.

## <a name="list-of-supported-functions"></a>Список поддерживаемых функций

| Функция | Описание |
|----------|-------------|
| [И](er-functions-logical-and.md)                       | Эта функция возвращает *логическое* значение **TRUE**, если все указанные условия — true. В противном случае возвращает *логическое* значение **FALSE**. |
| [Обращение](er-functions-logical-case.md)                     | Эта функция оценивает значение указанного выражения по сравнению с указанными альтернативными вариантами и возвращает результат первого варианта, равного значению указанного выражения. В противном случае возвращает дополнительный результат по умолчанию, если результат по умолчанию указан в качестве последнего аргумента вызванной функции, которой не предшествует вариант. Возвращаемое значение может быть значением любого из поддерживаемых типов данных. |
| [Содержит](er-functions-logical-contains.md)             | Эта функция определяет, содержит ли заданный ввод заданный текст. Это возвращает *логическое* значение **TRUE**, если заданный ввод содержит заданный текст. В противном случае возвращает *логическое* значение **FALSE**. |
| [EndsWith](er-functions-logical-endswith.md)             | Эта функция определяет, содержит ли заданный ввод заканчивается заданным текстом. Это возвращает *логическое* значение **TRUE**, если заданный ввод заканчивается заданным текстом. В противном случае возвращает *логическое* значение **FALSE**. |
| [Если](er-functions-logical-if.md)                         | Эта функция возвращает первое указанное значение, если выполняется указанное условие. В противном случае возвращает второе указанное значение. Возвращаемое значение может быть значением любого из поддерживаемых типов данных. |
| [Не](er-functions-logical-not.md)                       | Эта функция возвращает обратное логическое значение указанного условия в качестве *логического* значения. |
| [Или](er-functions-logical-or.md)                         | Эта функция возвращает *логическое* значение **FALSE**, если все указанные условия — false. Если какое-либо указанное условие — true, эта функция возвращает *логическое* значение **TRUE**. |
| [StartsWith](er-functions-logical-startswith.md)         | Эта функция определяет, содержит ли заданный ввод начинается заданным текстом. Это возвращает *логическое* значение **TRUE**, если заданный ввод начинается заданным текстом. В противном случае возвращает *логическое* значение **FALSE**. |
| [ValueIn](er-functions-logical-valuein.md)               | Эта функция определяет, соответствует ли заданный ввод какому-либо значению указанного элемента в указанном списке. Она возвращает *логическое* значение **TRUE**, если указанный ввод совпадает с результатом выполнения указанного выражения по крайней мере для одной записи указанного списка. В противном случае возвращает *логическое* значение **FALSE**. |
| [ValueInLarge](er-functions-logical-valueinlarge.md)     | Эта функция определяет, соответствует ли заданный ввод типа *Int64* или *Integer* какому-либо значению указанного элемента в указанном списке. Она возвращает *логическое* значение **TRUE**, если указанный ввод совпадает с результатом выполнения указанного выражения по крайней мере для одной записи указанного списка. В противном случае возвращает *логическое* значение **FALSE**. |


## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор электронной отчетности](general-electronic-reporting.md)

[Конструктор формул в электронной отчетности](general-electronic-reporting-formula-designer.md)

[Язык формул электронной отчетности](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
