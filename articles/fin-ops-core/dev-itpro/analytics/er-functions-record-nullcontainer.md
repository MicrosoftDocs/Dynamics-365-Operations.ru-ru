---
title: Функция ER NULLCONTAINER
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности NULLCONTAINER.
author: NickSelin
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: af6651ef3c62bd8d1285fa8179ac923d3c333ce7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746515"
---
# <a name="nullcontainer-er-function"></a><span data-ttu-id="8653e-103">Функция ER NULLCONTAINER</span><span class="sxs-lookup"><span data-stu-id="8653e-103">NULLCONTAINER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8653e-104">Функция `NULLCONTAINER` возвращает нулевое значение *Контейнер (запись)*, у которого такая же структура, что и у указанного списка записей или записи.</span><span class="sxs-lookup"><span data-stu-id="8653e-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="8653e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8653e-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="8653e-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="8653e-106">Arguments</span></span>

<span data-ttu-id="8653e-107">`list`: *Список записей* или *Контейнер (запись)*</span><span class="sxs-lookup"><span data-stu-id="8653e-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="8653e-108">Действительный путь источника данных типа *Список записей* или *Контейнер (запись)*.</span><span class="sxs-lookup"><span data-stu-id="8653e-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="8653e-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="8653e-109">Return values</span></span>

<span data-ttu-id="8653e-110">*Контейнер (запись)*</span><span class="sxs-lookup"><span data-stu-id="8653e-110">*Container (record)*</span></span>

<span data-ttu-id="8653e-111">Результирующее значение записи.</span><span class="sxs-lookup"><span data-stu-id="8653e-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8653e-112">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="8653e-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="8653e-113">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="8653e-113">This function is obsolete.</span></span> <span data-ttu-id="8653e-114">Вместо этого используйте функцию `EMPTYRECORD`.</span><span class="sxs-lookup"><span data-stu-id="8653e-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="8653e-115">Дополнительные сведения см. в разделе [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="8653e-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="8653e-116">Пример</span><span class="sxs-lookup"><span data-stu-id="8653e-116">Example</span></span>

<span data-ttu-id="8653e-117">`NULLCONTAINER (SPLIT ("abc", 1))` возвращает новую пустую запись, которая имеет такую же структуру, как список, который возвращен функцией `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="8653e-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="8653e-118">Дополнительные сведения см. в разделе [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="8653e-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8653e-119">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8653e-119">Additional resources</span></span>

[<span data-ttu-id="8653e-120">Функции для работы с записями</span><span class="sxs-lookup"><span data-stu-id="8653e-120">Record functions</span></span>](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]