---
title: Функция ER TABLENAME2ID
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности TABLENAME2ID
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
ms.openlocfilehash: 49370af4ebb7552dd3aff4512890fd93fa67c72d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563278"
---
# <a name="tablename2id-er-function"></a><span data-ttu-id="3e1ca-103">Функция ER TABLENAME2ID</span><span class="sxs-lookup"><span data-stu-id="3e1ca-103">TABLENAME2ID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e1ca-104">Функция `TABLENAME2ID` возвращает числовое представление идентификатора таблицы для указанного имени таблицы в качестве *целочисленного* значения.</span><span class="sxs-lookup"><span data-stu-id="3e1ca-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e1ca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e1ca-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="3e1ca-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="3e1ca-106">Arguments</span></span>

<span data-ttu-id="3e1ca-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="3e1ca-107">`text`: *String*</span></span>

<span data-ttu-id="3e1ca-108">Текстовое значение, представляющее действительное имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="3e1ca-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="3e1ca-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3e1ca-109">Return values</span></span>

<span data-ttu-id="3e1ca-110">*Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="3e1ca-110">*Integer*</span></span>

<span data-ttu-id="3e1ca-111">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="3e1ca-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3e1ca-112">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="3e1ca-112">Usage notes</span></span>

<span data-ttu-id="3e1ca-113">Выполнение этой функции может привести к различным результатам в разных экземплярах Microsoft Dynamics 365 Finance, даже если используется одно и то же название компании.</span><span class="sxs-lookup"><span data-stu-id="3e1ca-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="3e1ca-114">Пример</span><span class="sxs-lookup"><span data-stu-id="3e1ca-114">Example</span></span>

<span data-ttu-id="3e1ca-115">`TABLENAME2ID ("Intrastat")` возвращает **1510**.</span><span class="sxs-lookup"><span data-stu-id="3e1ca-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3e1ca-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3e1ca-116">Additional resources</span></span>

[<span data-ttu-id="3e1ca-117">Другие функции (характерные для конкретных бизнес-доменов)</span><span class="sxs-lookup"><span data-stu-id="3e1ca-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]