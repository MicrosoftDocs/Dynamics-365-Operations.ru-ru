---
title: Функция ER SPLITLISTBYLIMIT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности SPLITLISTBYLIMIT.
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
ms.openlocfilehash: 54c78f36c93e1bdb472b84fc7ca6428d20088bad
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041868"
---
# <span data-ttu-id="d06ef-103"><a name="SPLITLISTBYLIMIT">Функция ER SPLITLISTBYLIMIT</a></span><span class="sxs-lookup"><span data-stu-id="d06ef-103"><a name="SPLITLISTBYLIMIT">SPLITLISTBYLIMIT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d06ef-104">Функция `SPLITLISTBYLIMIT` разделяет указанный список на новый список подсписков (пакетов).</span><span class="sxs-lookup"><span data-stu-id="d06ef-104">The `SPLITLISTBYLIMIT` function splits the specified list into a new list of sublists (batches).</span></span> <span data-ttu-id="d06ef-105">Количество записей в каждом пакете рассчитывается динамически.</span><span class="sxs-lookup"><span data-stu-id="d06ef-105">The number of records in each batch is dynamically calculated.</span></span> <span data-ttu-id="d06ef-106">Затем функция возвращает результат в качестве нового значения *Список записей*, которое состоит из пакетов.</span><span class="sxs-lookup"><span data-stu-id="d06ef-106">The function then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="d06ef-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d06ef-107">Syntax</span></span>

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a><span data-ttu-id="d06ef-108">Аргументы</span><span class="sxs-lookup"><span data-stu-id="d06ef-108">Arguments</span></span>

<span data-ttu-id="d06ef-109">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="d06ef-109">`list`: *Record list*</span></span>

<span data-ttu-id="d06ef-110">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="d06ef-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="d06ef-111">`limit value`: *Целочисленный* или *Вещественный*</span><span class="sxs-lookup"><span data-stu-id="d06ef-111">`limit value`: *Integer* or *Real*</span></span>

<span data-ttu-id="d06ef-112">Максимальное значение лимита, используемого для разделения исходного списка на пакеты.</span><span class="sxs-lookup"><span data-stu-id="d06ef-112">The maximum value of the limit that is used to split the original list into batches.</span></span>

<span data-ttu-id="d06ef-113">`limit source`: *Поле*</span><span class="sxs-lookup"><span data-stu-id="d06ef-113">`limit source`: *Field*</span></span>

<span data-ttu-id="d06ef-114">Действительный путь поля типа *Целочисленный* или *Вещественный* в указанном списке.</span><span class="sxs-lookup"><span data-stu-id="d06ef-114">The valid path of a field of the *Integer* or *Real* type in the specified list.</span></span> <span data-ttu-id="d06ef-115">Значение этого поля определяет шаг, на который увеличивается общая сумма.</span><span class="sxs-lookup"><span data-stu-id="d06ef-115">The value of this field defines the step that the total sum is increased on.</span></span>

## <a name="return-values"></a><span data-ttu-id="d06ef-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="d06ef-116">Return values</span></span>

<span data-ttu-id="d06ef-117">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="d06ef-117">*Record list*</span></span>

<span data-ttu-id="d06ef-118">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="d06ef-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d06ef-119">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="d06ef-119">Usage notes</span></span>

<span data-ttu-id="d06ef-120">Возвращаемый список пакетов содержит следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="d06ef-120">The list of batches that is returned contains the following elements:</span></span>

- <span data-ttu-id="d06ef-121">**Значение**: *Список*</span><span class="sxs-lookup"><span data-stu-id="d06ef-121">**Value**: *List*</span></span>

    <span data-ttu-id="d06ef-122">Список записей, относящихся к текущему пакету.</span><span class="sxs-lookup"><span data-stu-id="d06ef-122">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="d06ef-123">**BatchNumber**: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="d06ef-123">**BatchNumber**: *Integer*</span></span>

    <span data-ttu-id="d06ef-124">Номер текущего пакета в возвращенном списке.</span><span class="sxs-lookup"><span data-stu-id="d06ef-124">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="d06ef-125">Предел не применяется к одному элементу исходного списка, если источник предела превышает заданный предел.</span><span class="sxs-lookup"><span data-stu-id="d06ef-125">The limit isn't applied to a single item of the original list if the limit source exceeds the defined limit.</span></span>

## <a name="example"></a><span data-ttu-id="d06ef-126">Пример</span><span class="sxs-lookup"><span data-stu-id="d06ef-126">Example</span></span>

<span data-ttu-id="d06ef-127">На следующем рисунке показан формат электронной отчетности (ER).</span><span class="sxs-lookup"><span data-stu-id="d06ef-127">The following illustration shows an Electronic reporting (ER) format.</span></span>

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

<span data-ttu-id="d06ef-128">На следующих рисунках показаны источники данных, которые используются для формата.</span><span class="sxs-lookup"><span data-stu-id="d06ef-128">The following illustration shows the data sources that are used for the format.</span></span>

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

<span data-ttu-id="d06ef-129">На следующем рисунке показан результат выполнения формата.</span><span class="sxs-lookup"><span data-stu-id="d06ef-129">The following illustration shows the result when the format is run.</span></span> <span data-ttu-id="d06ef-130">В этом случае выводится плоский список товарных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="d06ef-130">In this case, the output is a flat list of commodity items.</span></span>

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

<span data-ttu-id="d06ef-131">На следующих рисунках этот же формат был скорректирован для представления списка товарных номенклатур в партиях, когда одна партия может содержать товары с общим весом, который не должен превышать 9.</span><span class="sxs-lookup"><span data-stu-id="d06ef-131">In the following illustrations, the same format has been adjusted so that it presents the list of commodity items in batches if a single batch must include commodities and the total weight should not exceed a limit of 9.</span></span>

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

<span data-ttu-id="d06ef-132">На следующем рисунке показан результат выполнения скорректированного формата.</span><span class="sxs-lookup"><span data-stu-id="d06ef-132">The following illustration shows the result when the adjusted format is run.</span></span>

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> <span data-ttu-id="d06ef-133">Предел не применяется к последнему элементу исходного списка, так как значение (**11**) источника предела (**вес**) превышает заданный предел (**9**).</span><span class="sxs-lookup"><span data-stu-id="d06ef-133">The limit isn't applied to the last item of the original list, because the value (**11**) of the limit source (**weight**) exceeds the defined limit (**9**).</span></span> <span data-ttu-id="d06ef-134">Чтобы игнорировать подсписки во время создания отчета, используйте функцию `WHERE` или выражение **Включено** соответствующего элемента формата по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="d06ef-134">To ignore sublists during report generation, use either the `WHERE` function or the **Enabled** expression of the corresponding format element, as you require.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d06ef-135">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d06ef-135">Additional resources</span></span>

[<span data-ttu-id="d06ef-136">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="d06ef-136">List functions</span></span>](er-functions-category-list.md)
