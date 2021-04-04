---
title: Функция ER TEXT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности TEXT
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 5da7375020be827f432ba97740da37abe48962fc
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560069"
---
# <a name="text-er-function"></a><span data-ttu-id="7bbde-103">Функция ER TEXT</span><span class="sxs-lookup"><span data-stu-id="7bbde-103">TEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7bbde-104">Функция `TEXT` возвращает указанное число в качестве *строкового* значения после его преобразования в текстовую строку, которая отформатирована в соответствии с параметрами языкового стандарта сервера текущего экземпляра приложения.</span><span class="sxs-lookup"><span data-stu-id="7bbde-104">The `TEXT` function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bbde-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7bbde-105">Syntax</span></span>

```vb
TEXT (number)
```

## <a name="arguments"></a><span data-ttu-id="7bbde-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="7bbde-106">Arguments</span></span>

<span data-ttu-id="7bbde-107">`number`: *Целочисленный* или *Вещественный*</span><span class="sxs-lookup"><span data-stu-id="7bbde-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="7bbde-108">Число, которое должно быть преобразовано в текстовую строку.</span><span class="sxs-lookup"><span data-stu-id="7bbde-108">A number that must be converted to a text string.</span></span>

## <a name="return-values"></a><span data-ttu-id="7bbde-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="7bbde-109">Return values</span></span>

<span data-ttu-id="7bbde-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="7bbde-110">*String*</span></span>

<span data-ttu-id="7bbde-111">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="7bbde-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7bbde-112">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="7bbde-112">Usage notes</span></span>

<span data-ttu-id="7bbde-113">Для значений типа *Вещественный* преобразование строки ограничено до двух десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="7bbde-113">For values of the *Real* type, the string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="7bbde-114">Пример</span><span class="sxs-lookup"><span data-stu-id="7bbde-114">Example</span></span>

<span data-ttu-id="7bbde-115">Если языковой стандарт экземпляра сервера Microsoft Dynamics 365 Finance определен как **EN-US**, `TEXT (NOW ())` возвращает текущую дату сеанса Finance, 17 декабря 2015, как текстовую строку **"12/17/2015 07:59:23 AM"**.</span><span class="sxs-lookup"><span data-stu-id="7bbde-115">If the server locale of the Microsoft Dynamics 365 Finance instance is defined as **EN-US**, `TEXT (NOW ())` returns the current Finance session date, December 17, 2015, as the text string **"12/17/2015 07:59:23 AM"**.</span></span> <span data-ttu-id="7bbde-116">`TEXT (1/3)` возвращает **"0,33"**.</span><span class="sxs-lookup"><span data-stu-id="7bbde-116">`TEXT (1/3)` returns **"0.33"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7bbde-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7bbde-117">Additional resources</span></span>

[<span data-ttu-id="7bbde-118">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="7bbde-118">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]