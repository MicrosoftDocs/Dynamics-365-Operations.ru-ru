---
title: Функция ER FIRST
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности FIRST.
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
ms.openlocfilehash: d30c8481866ccf3f7080197b37586a0460a4ad2c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746587"
---
# <a name="first-er-function"></a><span data-ttu-id="71622-103">Функция ER FIRST</span><span class="sxs-lookup"><span data-stu-id="71622-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71622-104">Функция `FIRST` возвращает первую запись указанного списка в виде значения *Контейнер (запись)*, если этот список не пуст.</span><span class="sxs-lookup"><span data-stu-id="71622-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="71622-105">Если список пуст, эта функция выдает исключение.</span><span class="sxs-lookup"><span data-stu-id="71622-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="71622-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71622-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="71622-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="71622-107">Arguments</span></span>

<span data-ttu-id="71622-108">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="71622-108">`list`: *Record list*</span></span>

<span data-ttu-id="71622-109">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="71622-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="71622-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="71622-110">Return values</span></span>

<span data-ttu-id="71622-111">*Контейнер (запись)*</span><span class="sxs-lookup"><span data-stu-id="71622-111">*Container (record)*</span></span>

<span data-ttu-id="71622-112">Результирующее значение записи.</span><span class="sxs-lookup"><span data-stu-id="71622-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="71622-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="71622-113">Example 1</span></span>

<span data-ttu-id="71622-114">Выражение `FIRST(SPLIT("ABC",1)).Value` возвращает значение текста **"A"**.</span><span class="sxs-lookup"><span data-stu-id="71622-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="71622-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="71622-115">Example 2</span></span>

<span data-ttu-id="71622-116">Выражение `FIRST(SPLIT("",1)).Value` выдает исключение во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="71622-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71622-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="71622-117">Additional resources</span></span>

[<span data-ttu-id="71622-118">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="71622-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]