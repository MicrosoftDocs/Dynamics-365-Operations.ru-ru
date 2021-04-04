---
title: Функция ER LISTOFFIRSTITEM
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности LISTOFFIRSTITEM.
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
ms.openlocfilehash: f2e1f7e55c61f883aebb9d5a522a883a9a9de694
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569848"
---
# <a name="listoffirstitem-er-function"></a><span data-ttu-id="ae302-103">Функция ER LISTOFFIRSTITEM</span><span class="sxs-lookup"><span data-stu-id="ae302-103">LISTOFFIRSTITEM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae302-104">Функция `LISTOFFIRSTITEM` возвращает значение *Список записей*, состоящее только из первой записи указанного списка.</span><span class="sxs-lookup"><span data-stu-id="ae302-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae302-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae302-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="ae302-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="ae302-106">Arguments</span></span>

<span data-ttu-id="ae302-107">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="ae302-107">`list`: *Record list*</span></span>

<span data-ttu-id="ae302-108">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="ae302-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="ae302-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae302-109">Return values</span></span>

<span data-ttu-id="ae302-110">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="ae302-110">*Record list*</span></span>

<span data-ttu-id="ae302-111">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="ae302-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="ae302-112">Пример</span><span class="sxs-lookup"><span data-stu-id="ae302-112">Example</span></span>

<span data-ttu-id="ae302-113">Выражение `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` возвращает значение текста **"A"**.</span><span class="sxs-lookup"><span data-stu-id="ae302-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ae302-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ae302-114">Additional resources</span></span>

[<span data-ttu-id="ae302-115">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="ae302-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]