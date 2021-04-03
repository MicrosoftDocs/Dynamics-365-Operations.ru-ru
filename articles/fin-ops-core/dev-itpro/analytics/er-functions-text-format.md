---
title: Функция ER FORMAT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности FORMAT.
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
ms.openlocfilehash: fc8b0d6e25e12165e2a89f11d3c577d5ba8c7706
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566158"
---
# <a name="format-er-function"></a><span data-ttu-id="2b4be-103">Функция ER FORMAT</span><span class="sxs-lookup"><span data-stu-id="2b4be-103">FORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b4be-104">Функция `FORMAT` возвращает указанную строку как *строковое* значение после ее форматирования путем замены любых вхождений **%N** с *n*-м аргументом.</span><span class="sxs-lookup"><span data-stu-id="2b4be-104">The `FORMAT` function returns the specified string as a *String* value after it has been formatted by substituting any occurrences of **%N** with the *N* th argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b4be-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b4be-105">Syntax</span></span>

```vb
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a><span data-ttu-id="2b4be-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="2b4be-106">Arguments</span></span>

<span data-ttu-id="2b4be-107">`string`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="2b4be-107">`string`: *String*</span></span>

<span data-ttu-id="2b4be-108">Ссылка на источник данных типа данных *Строка*, который должен быть отформатирован.</span><span class="sxs-lookup"><span data-stu-id="2b4be-108">A reference to a data source of the *String* type that must be formatted.</span></span> <span data-ttu-id="2b4be-109">Этот аргумент обязательный.</span><span class="sxs-lookup"><span data-stu-id="2b4be-109">This argument is required.</span></span>

<span data-ttu-id="2b4be-110">`argument 1`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="2b4be-110">`argument 1`: *String*</span></span>

<span data-ttu-id="2b4be-111">Первый аргумент, который используется для замены вхождений **%1**.</span><span class="sxs-lookup"><span data-stu-id="2b4be-111">The first argument, which is used to replace occurrences of **%1**.</span></span> <span data-ttu-id="2b4be-112">Этот аргумент обязательный.</span><span class="sxs-lookup"><span data-stu-id="2b4be-112">This argument is required.</span></span>

<span data-ttu-id="2b4be-113">`argument N`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="2b4be-113">`argument N`: *String*</span></span>

<span data-ttu-id="2b4be-114">*n*-й аргумент, который используется для замены вхождений **%2**, **%3** и т. д.</span><span class="sxs-lookup"><span data-stu-id="2b4be-114">The *N* th argument, which is used to replace occurrences of **%2**, **%3**, and so on.</span></span> <span data-ttu-id="2b4be-115">Эти дополнительные аргументы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="2b4be-115">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="2b4be-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="2b4be-116">Return values</span></span>

<span data-ttu-id="2b4be-117">*Строка*</span><span class="sxs-lookup"><span data-stu-id="2b4be-117">*String*</span></span>

<span data-ttu-id="2b4be-118">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="2b4be-118">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2b4be-119">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="2b4be-119">Usage notes</span></span>

<span data-ttu-id="2b4be-120">Если аргумент не предусмотрен для параметра, параметр возвращается как **"%N"** в строке.</span><span class="sxs-lookup"><span data-stu-id="2b4be-120">If an argument isn't provided for a parameter, the parameter is returned as **"%N"** in the string.</span></span> <span data-ttu-id="2b4be-121">Для значений типа *Вещественный* преобразование строки по умолчанию ограничено до двух десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="2b4be-121">For values of the *Real* type, the default string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="2b4be-122">Пример</span><span class="sxs-lookup"><span data-stu-id="2b4be-122">Example</span></span>

<span data-ttu-id="2b4be-123">В следующем примере источник данных **PaymentModel** возвращает список записей клиентов с помощью компонента **Клиент**.</span><span class="sxs-lookup"><span data-stu-id="2b4be-123">In the following illustration, the **PaymentModel** data source returns a list of customer records by using the **Customer** component.</span></span> <span data-ttu-id="2b4be-124">Он возвращает значение даты обработки с помощью поля **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="2b4be-124">It returns the processing date value by using the **ProcessingDate** field.</span></span>

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

<span data-ttu-id="2b4be-125">В формате электронной отчетности (ER), который создан для генерации электронного файла для выбранных клиентов, **PaymentModel** выбирается в качестве источника данных и управляет потоком операций.</span><span class="sxs-lookup"><span data-stu-id="2b4be-125">In the Electronic reporting (ER) format that is designed to generate an electronic file for selected customers, **PaymentModel** is selected as a data source, and it controls the process flow.</span></span> <span data-ttu-id="2b4be-126">Если выбранный клиент остановлен на дату обработки отчета, исключение создается для информирования пользователя.</span><span class="sxs-lookup"><span data-stu-id="2b4be-126">If a selected customer is stopped for the date when the report is processed, an exception is thrown to notify the user.</span></span> <span data-ttu-id="2b4be-127">Формула, которая предназначена для этого типа управления обработкой, может использовать следующие ресурсы:</span><span class="sxs-lookup"><span data-stu-id="2b4be-127">The formula that is designed for this type of processing control can use the following resources:</span></span>

- <span data-ttu-id="2b4be-128">Метка SYS70894, которая имеет следующий текст:</span><span class="sxs-lookup"><span data-stu-id="2b4be-128">Label SYS70894, which has the following text:</span></span>

    - <span data-ttu-id="2b4be-129">**Для языка EN-US:** "Nothing to print"</span><span class="sxs-lookup"><span data-stu-id="2b4be-129">**For the EN-US language:** "Nothing to print"</span></span>
    - <span data-ttu-id="2b4be-130">**Для языка DE:** "Nichts zu drucken"</span><span class="sxs-lookup"><span data-stu-id="2b4be-130">**For the DE language:** "Nichts zu drucken"</span></span>

- <span data-ttu-id="2b4be-131">Метка SYS18389, которая имеет следующий текст:</span><span class="sxs-lookup"><span data-stu-id="2b4be-131">Label SYS18389, which has the following text:</span></span>

    - <span data-ttu-id="2b4be-132">**Для языка EN-US:** "Customer %1 is stopped for %2."</span><span class="sxs-lookup"><span data-stu-id="2b4be-132">**For the EN-US language:** "Customer %1 is stopped for %2."</span></span>
    - <span data-ttu-id="2b4be-133">**Для языка DE:** "Debitor '%1' wird für %2 gesperrt."</span><span class="sxs-lookup"><span data-stu-id="2b4be-133">**For the DE language:** "Debitor '%1' wird für %2 gesperrt."</span></span>

<span data-ttu-id="2b4be-134">Вот выражение, которое можно разработать.</span><span class="sxs-lookup"><span data-stu-id="2b4be-134">Here is the expression that can be designed.</span></span>

```vb
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

<span data-ttu-id="2b4be-135">Если отчет обрабатывается для клиента **Litware Retail** 17 декабря 2015 г., в культуре **EN-US** и языке **EN-US**, эта формула возвращает следующий текст, который можно представить для пользователя в виде сообщения исключения:</span><span class="sxs-lookup"><span data-stu-id="2b4be-135">If a report is processed for the **Litware Retail** customer on December 17, 2015, in the **EN-US** culture and the **EN-US** language, this formula returns the following text, which can be presented to the user as an exception message:</span></span>

<span data-ttu-id="2b4be-136">*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*</span><span class="sxs-lookup"><span data-stu-id="2b4be-136">*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*</span></span>

<span data-ttu-id="2b4be-137">Если этот же отчет обрабатывается для клиента **Litware Retail** 17 декабря 2015 г. в культуре **DE** и языке **DE**, эта формула возвращает следующий текст, который использует другой формат даты:</span><span class="sxs-lookup"><span data-stu-id="2b4be-137">If the same report is processed for the **Litware Retail** customer on December 17, 2015, in the **DE** culture and the **DE** language, the formula returns the following text, which uses a different date format:</span></span>

<span data-ttu-id="2b4be-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span><span class="sxs-lookup"><span data-stu-id="2b4be-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span></span>

>[!NOTE]
> <span data-ttu-id="2b4be-139">Следующий синтаксис применяется в формулах ER для меток:</span><span class="sxs-lookup"><span data-stu-id="2b4be-139">The following syntax is applied in ER formulas for labels:</span></span>
>
> - <span data-ttu-id="2b4be-140">**Для меток из ресурсов в приложении Microsoft Dynamics 365 Finance:** **\@X**, где **Х** — идентификатор метки в репозитории прикладных объектов (AOT)</span><span class="sxs-lookup"><span data-stu-id="2b4be-140">**For labels from resources in the Microsoft Dynamics 365 Finance app:** **\@X**, where **X** is the label ID in the Application Object Tree (AOT)</span></span>
> - <span data-ttu-id="2b4be-141">**Для меток, которые находятся в конфигурациях ER:** **@"GER_LABEL:X"**, где **Х** — код метки в конфигурации ER</span><span class="sxs-lookup"><span data-stu-id="2b4be-141">**For labels that reside in ER configurations:** **@"GER_LABEL:X"**, where **X** is the label ID in the ER configuration</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2b4be-142">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2b4be-142">Additional resources</span></span>

[<span data-ttu-id="2b4be-143">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="2b4be-143">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]