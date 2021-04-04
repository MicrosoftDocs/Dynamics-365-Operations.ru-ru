---
title: Функция LISTDISTINCT ER
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности LISTDISTINCT.
author: NickSelin
manager: kfend
ms.date: 7/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: f20565d73cea8d0cc1361bd03cda86a79a97955e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563832"
---
# <a name="listdistinct-er-function"></a><span data-ttu-id="c1c14-103">Функция LISTDISTINCT ER</span><span class="sxs-lookup"><span data-stu-id="c1c14-103">LISTDISTINCT ER Function</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="c1c14-104">Функция `LISTDISTINCT` вычисляет указанное выражение в качестве селектора для каждой записи указанного списка.</span><span class="sxs-lookup"><span data-stu-id="c1c14-104">The `LISTDISTINCT` function calculates the specified expression as a selector for every record of the specified list.</span></span> <span data-ttu-id="c1c14-105">Оно возвращает новое значение *списка записей*, содержащее одну запись для каждого уникального значения селектора.</span><span class="sxs-lookup"><span data-stu-id="c1c14-105">It returns a new *Record list* value that contains a single record for each unique selector value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1c14-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1c14-106">Syntax</span></span>

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a><span data-ttu-id="c1c14-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="c1c14-107">Arguments</span></span>

<span data-ttu-id="c1c14-108">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="c1c14-108">`list`: *Record list*</span></span>

<span data-ttu-id="c1c14-109">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="c1c14-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="c1c14-110">`selector`: *Примитивный тип данных*</span><span class="sxs-lookup"><span data-stu-id="c1c14-110">`selector`: *Primitive data type*</span></span>

<span data-ttu-id="c1c14-111">Допустимое выражение, используемое для расчета значения селектора для каждой записи в указанном списке.</span><span class="sxs-lookup"><span data-stu-id="c1c14-111">A valid expression that is used to calculate a selector value for every record in the specified list.</span></span>

<span data-ttu-id="c1c14-112">Для этого параметра поддерживаются следующие типы данных:</span><span class="sxs-lookup"><span data-stu-id="c1c14-112">The following data types are supported for this parameter:</span></span>

- <span data-ttu-id="c1c14-113">Логический</span><span class="sxs-lookup"><span data-stu-id="c1c14-113">Boolean</span></span>
- <span data-ttu-id="c1c14-114">Дата</span><span class="sxs-lookup"><span data-stu-id="c1c14-114">Date</span></span>
- <span data-ttu-id="c1c14-115">DateTime</span><span class="sxs-lookup"><span data-stu-id="c1c14-115">DateTime</span></span>
- <span data-ttu-id="c1c14-116">GUID</span><span class="sxs-lookup"><span data-stu-id="c1c14-116">GUID</span></span>
- <span data-ttu-id="c1c14-117">Целое число</span><span class="sxs-lookup"><span data-stu-id="c1c14-117">Integer</span></span>
- <span data-ttu-id="c1c14-118">Int64</span><span class="sxs-lookup"><span data-stu-id="c1c14-118">Int64</span></span>
- <span data-ttu-id="c1c14-119">Действующий</span><span class="sxs-lookup"><span data-stu-id="c1c14-119">Real</span></span>
- <span data-ttu-id="c1c14-120">Строка</span><span class="sxs-lookup"><span data-stu-id="c1c14-120">String</span></span>

## <a name="return-values"></a><span data-ttu-id="c1c14-121">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="c1c14-121">Return values</span></span>

<span data-ttu-id="c1c14-122">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="c1c14-122">*Record list*</span></span>

<span data-ttu-id="c1c14-123">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="c1c14-123">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c1c14-124">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="c1c14-124">Usage notes</span></span>

<span data-ttu-id="c1c14-125">Созданная структура списка совпадает со структурой указанного списка.</span><span class="sxs-lookup"><span data-stu-id="c1c14-125">The structure of the list that is created matches the structure of the specified list.</span></span>

<span data-ttu-id="c1c14-126">Для нескольких записей в указанном списке может быть рассчитано одно и то же значение селектора.</span><span class="sxs-lookup"><span data-stu-id="c1c14-126">The same selector value might be calculated for multiple records in the specified list.</span></span> <span data-ttu-id="c1c14-127">В этом случае значения полей соответствующей записи в созданном списке равны значениям первой записи из указанного списка, для которого рассчитывается значение селектора.</span><span class="sxs-lookup"><span data-stu-id="c1c14-127">In this case, field values of the corresponding record in the created list equal the values of the first record from the specified list that the selector value is calculated for.</span></span>

<span data-ttu-id="c1c14-128">Выполнение этой функции выполняется в любом источнике данных [электронной отчетности (ER)](general-electronic-reporting.md) типа *списка записей*, присутствующего в памяти.</span><span class="sxs-lookup"><span data-stu-id="c1c14-128">The execution of this function is done on any [Electronic reporting (ER)](general-electronic-reporting.md) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="c1c14-129">Источник данных **GROUPBY** также можно использовать для создания списка записей, для которых рассчитывается селектор с различными значениями.</span><span class="sxs-lookup"><span data-stu-id="c1c14-129">The **GROUPBY** data source can also be used to generate the list of records that the selector that has distinct values is calculated for.</span></span> <span data-ttu-id="c1c14-130">Однако с точки зрения производительности и потребления памяти лучше использовать функцию `LISTDISTINCT`, чем источник данных **GROUPBY**, так как выполнение функции в происходит памяти.</span><span class="sxs-lookup"><span data-stu-id="c1c14-130">However, from a performance and memory consumption perspective, it's better to use the `LISTDISTINCT` function than the **GROUPBY** data source, because the execution of the function is done in memory.</span></span>

## <a name="example"></a><span data-ttu-id="c1c14-131">Пример</span><span class="sxs-lookup"><span data-stu-id="c1c14-131">Example</span></span>

<span data-ttu-id="c1c14-132">В следующем примере показано, как можно получить список уникальных номеров счетов клиентов, для которых в течение определенного периода была создана по крайней мере одна накладная по продаже или накладная по проекту.</span><span class="sxs-lookup"><span data-stu-id="c1c14-132">The following example shows how you can get the list of unique customer account numbers that at least one sales invoice or project invoice has been issued to during a specific period.</span></span>

1. <span data-ttu-id="c1c14-133">Введите источник данных **SalesInvoice** типа `Record list`, относящийся к таблице приложения **CustInvoiceJour** и фильтрующий накладные по продаже для указанных периодов.</span><span class="sxs-lookup"><span data-stu-id="c1c14-133">Enter the **SalesInvoice** data source of the `Record list` type that refers to the **CustInvoiceJour** application table and filters sales invoices for specific periods.</span></span>

    <span data-ttu-id="c1c14-134">Поле `InvoiceAccount` этого источника данных возвращает номер счета клиента, по которому выставлена накладная.</span><span class="sxs-lookup"><span data-stu-id="c1c14-134">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

2. <span data-ttu-id="c1c14-135">Введите источник данных **ProjectInvoice** типа `Record list`, относящийся к таблице приложения **ProjInvoiceJour** и фильтрующий накладные по проекту для указанных периодов.</span><span class="sxs-lookup"><span data-stu-id="c1c14-135">Enter the **ProjectInvoice** data source of the `Record list` type that refers to the **ProjInvoiceJour** application table and filters project invoices for specific periods.</span></span>

    <span data-ttu-id="c1c14-136">Поле `InvoiceAccount` этого источника данных возвращает номер счета клиента, по которому выставлена накладная.</span><span class="sxs-lookup"><span data-stu-id="c1c14-136">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

3. <span data-ttu-id="c1c14-137">Настройте источник данных **AllInvoices** типа `Calculated field`, содержащий выражение `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span><span class="sxs-lookup"><span data-stu-id="c1c14-137">Configure the **AllInvoices** data source of the `Calculated field` type that contains the expression `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span></span>

    <span data-ttu-id="c1c14-138">Этот источник данных возвращает объединенный список накладных по продаже и накладных по проекту.</span><span class="sxs-lookup"><span data-stu-id="c1c14-138">This data source returns the joined list of sales invoices and project invoices.</span></span>

4. <span data-ttu-id="c1c14-139">Настройте источник данных **InvoicedCustomer** типа `Record list`, содержащий выражение `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span><span class="sxs-lookup"><span data-stu-id="c1c14-139">Configure the **InvoicedCustomer** data source of the `Record list` type that contains the expression `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span></span>

    <span data-ttu-id="c1c14-140">Этот источник данных возвращает новый список, содержащий одну запись для каждого уникального клиента, по которому была выставлена накладная в течение определенного периода времени.</span><span class="sxs-lookup"><span data-stu-id="c1c14-140">This data source returns a new list that contains a single record for every unique customer that has been invoiced during the defined period.</span></span> <span data-ttu-id="c1c14-141">Поле `InvoiceAccount` этого списка содержит номер счета клиента.</span><span class="sxs-lookup"><span data-stu-id="c1c14-141">The `InvoiceAccount` field of this list contains a customer account number.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c1c14-142">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c1c14-142">Additional resources</span></span>

[<span data-ttu-id="c1c14-143">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="c1c14-143">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]