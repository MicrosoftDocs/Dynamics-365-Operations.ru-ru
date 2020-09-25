---
title: Функция ER EMPTYRECORD
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности EMPTYRECORD.
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
ms.openlocfilehash: 2e46fcef3d53483b782ac39a0661fc0edc8d861c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743958"
---
# <a name="emptyrecord-er-function"></a><span data-ttu-id="ac086-103">Функция ER EMPTYRECORD</span><span class="sxs-lookup"><span data-stu-id="ac086-103">EMPTYRECORD ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac086-104">Функция `EMPTYRECORD` возвращает нулевое значение *Контейнер (запись)*, у которого такая же структура, что и у указанного списка записей или записи.</span><span class="sxs-lookup"><span data-stu-id="ac086-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac086-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac086-105">Syntax</span></span>

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="ac086-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="ac086-106">Arguments</span></span>

<span data-ttu-id="ac086-107">`list`: *Список записей* или *Контейнер (запись)*</span><span class="sxs-lookup"><span data-stu-id="ac086-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="ac086-108">Действительный путь источника данных типа *Список записей* или *Контейнер (запись)*.</span><span class="sxs-lookup"><span data-stu-id="ac086-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="ac086-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ac086-109">Return values</span></span>

<span data-ttu-id="ac086-110">*Контейнер (запись)*</span><span class="sxs-lookup"><span data-stu-id="ac086-110">*Container (record)*</span></span>

<span data-ttu-id="ac086-111">Результирующее значение записи.</span><span class="sxs-lookup"><span data-stu-id="ac086-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ac086-112">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="ac086-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="ac086-113">Запись null является записью, в которой все поля имеют пустое значение.</span><span class="sxs-lookup"><span data-stu-id="ac086-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="ac086-114">Пустое значения равно **0** (ноль) для чисел, пустой строке для строк и т. д.</span><span class="sxs-lookup"><span data-stu-id="ac086-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="ac086-115">Пример</span><span class="sxs-lookup"><span data-stu-id="ac086-115">Example</span></span>

<span data-ttu-id="ac086-116">`EMPTYRECORD (SPLIT ("abc", 1))` возвращает новую пустую запись, которая имеет такую же структуру, как список, который возвращен функцией `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="ac086-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="ac086-117">Дополнительные сведения см. в разделе [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="ac086-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ac086-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ac086-118">Additional resources</span></span>

[<span data-ttu-id="ac086-119">Функции для работы с записями</span><span class="sxs-lookup"><span data-stu-id="ac086-119">Record functions</span></span>](er-functions-category-record.md)
