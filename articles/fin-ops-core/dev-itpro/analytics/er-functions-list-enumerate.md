---
title: Функция ER ENUMERATE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ENUMERATE.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 0827fe33a548970c7673ac2ab830bb22d367c8cc
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567876"
---
# <a name="enumerate-er-function"></a><span data-ttu-id="17e48-103">Функция ER ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="17e48-103">ENUMERATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17e48-104">Функция `ENUMERATE` возвращает новое значение *Список записей*, состоящее из перечисленных записей указанного списка.</span><span class="sxs-lookup"><span data-stu-id="17e48-104">The `ENUMERATE` function returns a new *Record list* value that consists of enumerated records of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="17e48-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17e48-105">Syntax</span></span>

```vb
ENUMERATE (list)
```

## <a name="arguments"></a><span data-ttu-id="17e48-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="17e48-106">Arguments</span></span>

<span data-ttu-id="17e48-107">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="17e48-107">`list`: *Record list*</span></span>

<span data-ttu-id="17e48-108">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="17e48-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="17e48-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="17e48-109">Return values</span></span>

<span data-ttu-id="17e48-110">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="17e48-110">*Record list*</span></span>

<span data-ttu-id="17e48-111">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="17e48-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="17e48-112">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="17e48-112">Usage notes</span></span>

<span data-ttu-id="17e48-113">Список перечисленных записей, которые возвращаются, открывает следующие дополнительные элементы:</span><span class="sxs-lookup"><span data-stu-id="17e48-113">The list of enumerated records that is returned exposes the following additional elements:</span></span>

- <span data-ttu-id="17e48-114">Запись полей (компонент **Значение**)</span><span class="sxs-lookup"><span data-stu-id="17e48-114">The record of fields (**Value** component)</span></span>
- <span data-ttu-id="17e48-115">Индекс текущей записи (**Номер** компонента)</span><span class="sxs-lookup"><span data-stu-id="17e48-115">The current record index (**Number** component)</span></span>

## <a name="example"></a><span data-ttu-id="17e48-116">Пример</span><span class="sxs-lookup"><span data-stu-id="17e48-116">Example</span></span>

<span data-ttu-id="17e48-117">На следующем рисунке источник данных **Enumerated** создается как нумерованный список записей поставщика из источника данных **Vendors**, который ссылается на таблицу VendTable.</span><span class="sxs-lookup"><span data-stu-id="17e48-117">In the following illustration, an **Enumerated** data source is created as an enumerated list of vendor records from the **Vendors** data source that refers to the VendTable table.</span></span>

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

<span data-ttu-id="17e48-118">На следующем рисунке показан формат электронной отчетности (ER).</span><span class="sxs-lookup"><span data-stu-id="17e48-118">The following illustration shows the Electronic reporting (ER) format.</span></span> <span data-ttu-id="17e48-119">В этом формате привязки данных создаются для создания выходных данных в формате XML.</span><span class="sxs-lookup"><span data-stu-id="17e48-119">In this format, data bindings are created to generate output in XML format.</span></span> <span data-ttu-id="17e48-120">Эти выходные данные представляют отдельных поставщиков как перечислимые узлы.</span><span class="sxs-lookup"><span data-stu-id="17e48-120">This output presents individual vendors as enumerated nodes.</span></span>

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

<span data-ttu-id="17e48-121">На следующем рисунке показан результат выполнения созданного формата.</span><span class="sxs-lookup"><span data-stu-id="17e48-121">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a><span data-ttu-id="17e48-122">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="17e48-122">Additional resources</span></span>

[<span data-ttu-id="17e48-123">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="17e48-123">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]