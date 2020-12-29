---
title: Функция ER GUIDVALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности GUIDVALUE.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb6f301cf7a39208aa23337401a9684fb5b3a73d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685963"
---
# <a name="guidvalue-er-function"></a><span data-ttu-id="f5700-103">Функция ER GUIDVALUE</span><span class="sxs-lookup"><span data-stu-id="f5700-103">GUIDVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5700-104">Функция `GUIDVALUE` преобразует заданный ввод типа *Строка* в элемент данных типа *GUID*.</span><span class="sxs-lookup"><span data-stu-id="f5700-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5700-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5700-105">Syntax</span></span>

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="f5700-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="f5700-106">Arguments</span></span>

<span data-ttu-id="f5700-107">`input`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="f5700-107">`input`: *String*</span></span>

<span data-ttu-id="f5700-108">Действительный путь источника данных типа *Строка*.</span><span class="sxs-lookup"><span data-stu-id="f5700-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f5700-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f5700-109">Return values</span></span>

<span data-ttu-id="f5700-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f5700-110">*GUID*</span></span>

<span data-ttu-id="f5700-111">Результирующе значение глобально уникального кода (GUID).</span><span class="sxs-lookup"><span data-stu-id="f5700-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f5700-112">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="f5700-112">Usage notes</span></span>

<span data-ttu-id="f5700-113">Чтобы выполнить преобразование в обратном направлении (то есть, для преобразования указанного ввода с типом данных *GUID* в элемент данных с типом данных *Строка*), можно использовать функцию [TEXT](er-functions-text-text.md).</span><span class="sxs-lookup"><span data-stu-id="f5700-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="f5700-114">Пример</span><span class="sxs-lookup"><span data-stu-id="f5700-114">Example</span></span>

<span data-ttu-id="f5700-115">Определите следующие источники данных в соответствии вашей модели:</span><span class="sxs-lookup"><span data-stu-id="f5700-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="f5700-116">Источник данных **myID** типа *Вычисляемое поле*, содержащий выражение `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span><span class="sxs-lookup"><span data-stu-id="f5700-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="f5700-117">Источник данных **Users** типа *Записи таблицы*, который относится к таблице UserInfo</span><span class="sxs-lookup"><span data-stu-id="f5700-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="f5700-118">Затем можно использовать такое выражение, как `FILTER (Users, Users.objectId = myID)` для фильтрации таблицы UserInfo по полю **objectId** типа данных *GUID*.</span><span class="sxs-lookup"><span data-stu-id="f5700-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f5700-119">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f5700-119">Additional resources</span></span>

[<span data-ttu-id="f5700-120">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="f5700-120">Text functions</span></span>](er-functions-category-text.md)
