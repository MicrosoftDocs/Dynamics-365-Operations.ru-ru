---
title: Функция ER TEXT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности TEXT
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 20313133ce29b8d5048814ff78ce4ea4f5c54d4a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743696"
---
# <a name="text-er-function"></a><span data-ttu-id="97273-103">Функция ER TEXT</span><span class="sxs-lookup"><span data-stu-id="97273-103">TEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97273-104">Функция `TEXT` возвращает указанное число в качестве *строкового* значения после его преобразования в текстовую строку, которая отформатирована в соответствии с параметрами языкового стандарта сервера текущего экземпляра приложения.</span><span class="sxs-lookup"><span data-stu-id="97273-104">The `TEXT` function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="97273-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97273-105">Syntax</span></span>

```vb
TEXT (number)
```

## <a name="arguments"></a><span data-ttu-id="97273-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="97273-106">Arguments</span></span>

<span data-ttu-id="97273-107">`number`: *Целочисленный* или *Вещественный*</span><span class="sxs-lookup"><span data-stu-id="97273-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="97273-108">Число, которое должно быть преобразовано в текстовую строку.</span><span class="sxs-lookup"><span data-stu-id="97273-108">A number that must be converted to a text string.</span></span>

## <a name="return-values"></a><span data-ttu-id="97273-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="97273-109">Return values</span></span>

<span data-ttu-id="97273-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="97273-110">*String*</span></span>

<span data-ttu-id="97273-111">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="97273-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="97273-112">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="97273-112">Usage notes</span></span>

<span data-ttu-id="97273-113">Для значений типа *Вещественный* преобразование строки ограничено до двух десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="97273-113">For values of the *Real* type, the string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="97273-114">Пример</span><span class="sxs-lookup"><span data-stu-id="97273-114">Example</span></span>

<span data-ttu-id="97273-115">Если языковой стандарт экземпляра сервера Microsoft Dynamics 365 Finance определен как **EN-US**, `TEXT (NOW ())` возвращает текущую дату сеанса Finance, 17 декабря 2015, как текстовую строку **"12/17/2015 07:59:23 AM"**.</span><span class="sxs-lookup"><span data-stu-id="97273-115">If the server locale of the Microsoft Dynamics 365 Finance instance is defined as **EN-US**, `TEXT (NOW ())` returns the current Finance session date, December 17, 2015, as the text string **"12/17/2015 07:59:23 AM"**.</span></span> <span data-ttu-id="97273-116">`TEXT (1/3)` возвращает **"0,33"**.</span><span class="sxs-lookup"><span data-stu-id="97273-116">`TEXT (1/3)` returns **"0.33"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="97273-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="97273-117">Additional resources</span></span>

[<span data-ttu-id="97273-118">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="97273-118">Text functions</span></span>](er-functions-category-text.md)
