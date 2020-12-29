---
title: Функция ER TABLENAME2ID
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности TABLENAME2ID
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
ms.openlocfilehash: a68a8e1f4afa378ab446eae12bc90cdb3aba8b19
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681166"
---
# <a name="tablename2id-er-function"></a><span data-ttu-id="8fc3e-103">Функция ER TABLENAME2ID</span><span class="sxs-lookup"><span data-stu-id="8fc3e-103">TABLENAME2ID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8fc3e-104">Функция `TABLENAME2ID` возвращает числовое представление идентификатора таблицы для указанного имени таблицы в качестве *целочисленного* значения.</span><span class="sxs-lookup"><span data-stu-id="8fc3e-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fc3e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8fc3e-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="8fc3e-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="8fc3e-106">Arguments</span></span>

<span data-ttu-id="8fc3e-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="8fc3e-107">`text`: *String*</span></span>

<span data-ttu-id="8fc3e-108">Текстовое значение, представляющее действительное имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="8fc3e-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="8fc3e-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="8fc3e-109">Return values</span></span>

<span data-ttu-id="8fc3e-110">*Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="8fc3e-110">*Integer*</span></span>

<span data-ttu-id="8fc3e-111">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="8fc3e-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8fc3e-112">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="8fc3e-112">Usage notes</span></span>

<span data-ttu-id="8fc3e-113">Выполнение этой функции может привести к различным результатам в разных экземплярах Microsoft Dynamics 365 Finance, даже если используется одно и то же название компании.</span><span class="sxs-lookup"><span data-stu-id="8fc3e-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="8fc3e-114">Пример</span><span class="sxs-lookup"><span data-stu-id="8fc3e-114">Example</span></span>

<span data-ttu-id="8fc3e-115">`TABLENAME2ID ("Intrastat")` возвращает **1510**.</span><span class="sxs-lookup"><span data-stu-id="8fc3e-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8fc3e-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8fc3e-116">Additional resources</span></span>

[<span data-ttu-id="8fc3e-117">Другие функции (характерные для конкретных бизнес-доменов)</span><span class="sxs-lookup"><span data-stu-id="8fc3e-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
