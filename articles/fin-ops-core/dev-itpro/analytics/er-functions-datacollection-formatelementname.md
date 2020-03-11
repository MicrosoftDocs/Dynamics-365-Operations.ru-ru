---
title: Функция ER FORMATELEMENTNAME
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности FORMATELEMENTNAME.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 5f299a4bb697afce152a61ec35fcefab7157f356
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042535"
---
# <span data-ttu-id="c9052-103"><a name="FORMATELEMENTNAME">Функция ER FORMATELEMENTNAME</a></span><span class="sxs-lookup"><span data-stu-id="c9052-103"><a name="FORMATELEMENTNAME">FORMATELEMENTNAME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9052-104">Функция `FORMATELEMENTNAME` возвращает значение *строка*, представляющее имя элемента текущего формата электронной отчетности (ER).</span><span class="sxs-lookup"><span data-stu-id="c9052-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9052-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9052-105">Syntax</span></span>

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="c9052-106">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="c9052-106">Return values</span></span>

<span data-ttu-id="c9052-107">*Строка*</span><span class="sxs-lookup"><span data-stu-id="c9052-107">*String*</span></span>

<span data-ttu-id="c9052-108">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="c9052-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c9052-109">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="c9052-109">Usage notes</span></span>

<span data-ttu-id="c9052-110">Эта функция может вызываться в выражениях ER, настроенных для свойств **Имя ключа собранных данных** и **Значение ключа собранных данных** компонента формата УК из группы **Текст** в компоненте **Common\\File**, где включен параметр **Сбор сведений о результате**.</span><span class="sxs-lookup"><span data-stu-id="c9052-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="c9052-111">Пример</span><span class="sxs-lookup"><span data-stu-id="c9052-111">Example</span></span>

<span data-ttu-id="c9052-112">Для получения дополнительных сведений об использовании этой функции см. проводник по задаче [ER Использование выходных данных формата для инвентаризации и агрегирования](tasks/er-format-counting-summing-1.md), который является частью бизнес-процесса **Приобретение/разработка компонентов ИТ-услуг и решений**.</span><span class="sxs-lookup"><span data-stu-id="c9052-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c9052-113">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c9052-113">Additional resources</span></span>

[<span data-ttu-id="c9052-114">Функции сбора данных</span><span class="sxs-lookup"><span data-stu-id="c9052-114">Data collection functions</span></span>](er-functions-category-data-collection.md)
