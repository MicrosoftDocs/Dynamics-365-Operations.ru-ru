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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7b8c782aff488a433c40a49ab7f4fe2d0e944e4
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041193"
---
# <span data-ttu-id="98b01-103"><a name="GUIDVALUE">Функция ER GUIDVALUE</a></span><span class="sxs-lookup"><span data-stu-id="98b01-103"><a name="GUIDVALUE">GUIDVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98b01-104">Функция `GUIDVALUE` преобразует заданный ввод типа *Строка* в элемент данных типа *GUID*.</span><span class="sxs-lookup"><span data-stu-id="98b01-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="98b01-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98b01-105">Syntax</span></span>

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="98b01-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="98b01-106">Arguments</span></span>

<span data-ttu-id="98b01-107">`input`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="98b01-107">`input`: *String*</span></span>

<span data-ttu-id="98b01-108">Действительный путь источника данных типа *Строка*.</span><span class="sxs-lookup"><span data-stu-id="98b01-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="98b01-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="98b01-109">Return values</span></span>

<span data-ttu-id="98b01-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="98b01-110">*GUID*</span></span>

<span data-ttu-id="98b01-111">Результирующе значение глобально уникального кода (GUID).</span><span class="sxs-lookup"><span data-stu-id="98b01-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="98b01-112">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="98b01-112">Usage notes</span></span>

<span data-ttu-id="98b01-113">Чтобы выполнить преобразование в обратном направлении (то есть, для преобразования указанного ввода с типом данных *GUID* в элемент данных с типом данных *Строка*), можно использовать функцию [TEXT](er-functions-text-text.md).</span><span class="sxs-lookup"><span data-stu-id="98b01-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="98b01-114">Пример</span><span class="sxs-lookup"><span data-stu-id="98b01-114">Example</span></span>

<span data-ttu-id="98b01-115">Определите следующие источники данных в соответствии вашей модели:</span><span class="sxs-lookup"><span data-stu-id="98b01-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="98b01-116">Источник данных **myID** типа *Вычисляемое поле*, содержащий выражение `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span><span class="sxs-lookup"><span data-stu-id="98b01-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="98b01-117">Источник данных **Users** типа *Записи таблицы*, который относится к таблице UserInfo</span><span class="sxs-lookup"><span data-stu-id="98b01-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="98b01-118">Затем можно использовать такое выражение, как `FILTER (Users, Users.objectId = myID)` для фильтрации таблицы UserInfo по полю **objectId** типа данных *GUID*.</span><span class="sxs-lookup"><span data-stu-id="98b01-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98b01-119">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="98b01-119">Additional resources</span></span>

[<span data-ttu-id="98b01-120">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="98b01-120">Text functions</span></span>](er-functions-category-text.md)
