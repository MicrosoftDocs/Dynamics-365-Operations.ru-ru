---
title: Функция ER NULLCONTAINER
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности NULLCONTAINER.
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
ms.openlocfilehash: 1dde102acf18e451cb895b51b28d22102f38936c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915794"
---
# <span data-ttu-id="89d20-103"><a name="NULLCONTAINER">Функция ER NULLCONTAINER</a></span><span class="sxs-lookup"><span data-stu-id="89d20-103"><a name="NULLCONTAINER">NULLCONTAINER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89d20-104">Функция `NULLCONTAINER` возвращает нулевое значение *Контейнер (запись)*, у которого такая же структура, что и у указанного списка записей или записи.</span><span class="sxs-lookup"><span data-stu-id="89d20-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="89d20-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89d20-105">Syntax</span></span>

```
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="89d20-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="89d20-106">Arguments</span></span>

<span data-ttu-id="89d20-107">`list`: *Список записей* или *Контейнер (запись)*</span><span class="sxs-lookup"><span data-stu-id="89d20-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="89d20-108">Действительный путь источника данных типа *Список записей* или *Контейнер (запись)*.</span><span class="sxs-lookup"><span data-stu-id="89d20-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="89d20-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="89d20-109">Return values</span></span>

<span data-ttu-id="89d20-110">*Контейнер (запись)*</span><span class="sxs-lookup"><span data-stu-id="89d20-110">*Container (record)*</span></span>

<span data-ttu-id="89d20-111">Результирующее значение записи.</span><span class="sxs-lookup"><span data-stu-id="89d20-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="89d20-112">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="89d20-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="89d20-113">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="89d20-113">This function is obsolete.</span></span> <span data-ttu-id="89d20-114">Вместо этого используйте функцию `EMPTYRECORD`.</span><span class="sxs-lookup"><span data-stu-id="89d20-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="89d20-115">Дополнительные сведения см. в разделе [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="89d20-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="89d20-116">Пример</span><span class="sxs-lookup"><span data-stu-id="89d20-116">Example</span></span>

<span data-ttu-id="89d20-117">`NULLCONTAINER (SPLIT ("abc", 1))` возвращает новую пустую запись, которая имеет такую же структуру, как список, который возвращен функцией `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="89d20-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="89d20-118">Дополнительные сведения см. в разделе [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="89d20-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="89d20-119">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="89d20-119">Additional resources</span></span>

[<span data-ttu-id="89d20-120">Функции для работы с записями</span><span class="sxs-lookup"><span data-stu-id="89d20-120">Record functions</span></span>](er-functions-category-record.md)
