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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1932116b67cef79622f0f6152b168b5961a72c7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683046"
---
# <a name="nullcontainer-er-function"></a><span data-ttu-id="119a8-103">Функция ER NULLCONTAINER</span><span class="sxs-lookup"><span data-stu-id="119a8-103">NULLCONTAINER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="119a8-104">Функция `NULLCONTAINER` возвращает нулевое значение *Контейнер (запись)*, у которого такая же структура, что и у указанного списка записей или записи.</span><span class="sxs-lookup"><span data-stu-id="119a8-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="119a8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="119a8-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="119a8-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="119a8-106">Arguments</span></span>

<span data-ttu-id="119a8-107">`list`: *Список записей* или *Контейнер (запись)*</span><span class="sxs-lookup"><span data-stu-id="119a8-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="119a8-108">Действительный путь источника данных типа *Список записей* или *Контейнер (запись)*.</span><span class="sxs-lookup"><span data-stu-id="119a8-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="119a8-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="119a8-109">Return values</span></span>

<span data-ttu-id="119a8-110">*Контейнер (запись)*</span><span class="sxs-lookup"><span data-stu-id="119a8-110">*Container (record)*</span></span>

<span data-ttu-id="119a8-111">Результирующее значение записи.</span><span class="sxs-lookup"><span data-stu-id="119a8-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="119a8-112">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="119a8-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="119a8-113">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="119a8-113">This function is obsolete.</span></span> <span data-ttu-id="119a8-114">Вместо этого используйте функцию `EMPTYRECORD`.</span><span class="sxs-lookup"><span data-stu-id="119a8-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="119a8-115">Дополнительные сведения см. в разделе [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="119a8-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="119a8-116">Пример</span><span class="sxs-lookup"><span data-stu-id="119a8-116">Example</span></span>

<span data-ttu-id="119a8-117">`NULLCONTAINER (SPLIT ("abc", 1))` возвращает новую пустую запись, которая имеет такую же структуру, как список, который возвращен функцией `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="119a8-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="119a8-118">Дополнительные сведения см. в разделе [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="119a8-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="119a8-119">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="119a8-119">Additional resources</span></span>

[<span data-ttu-id="119a8-120">Функции для работы с записями</span><span class="sxs-lookup"><span data-stu-id="119a8-120">Record functions</span></span>](er-functions-category-record.md)
