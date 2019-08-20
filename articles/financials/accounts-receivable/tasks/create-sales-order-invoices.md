---
title: Создание накладных по заказам на продажу
description: В этом руководстве по задаче описывается процесс выставления накладных по заказу на продажу, включая объединения накладных и пакетную обработку.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba8e0f02f2d1eb12cecc2c434fbca1e198cddbe9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842961"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="e6d24-103">Создание накладных по заказам на продажу</span><span class="sxs-lookup"><span data-stu-id="e6d24-103">Create sales order invoices</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e6d24-104">В этом руководстве по задаче описывается процесс выставления накладных по заказу на продажу, включая объединения накладных и пакетную обработку.</span><span class="sxs-lookup"><span data-stu-id="e6d24-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="e6d24-105">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="e6d24-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="e6d24-106">Создание накладной из заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="e6d24-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="e6d24-107">Перейдите в раздел "Расчеты с клиентами" > "Заказы" > "Отправленные заказы на продажу, для которых не получены накладные".</span><span class="sxs-lookup"><span data-stu-id="e6d24-107">Go to Accounts receivable > Orders > Shipped but not invoiced sales orders.</span></span>
2. <span data-ttu-id="e6d24-108">Выберите заказ на продажу в списке.</span><span class="sxs-lookup"><span data-stu-id="e6d24-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="e6d24-109">В области действий щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="e6d24-109">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="e6d24-110">Щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="e6d24-110">Click Invoice.</span></span>
    * <span data-ttu-id="e6d24-111">Обратите внимание, что этот заказ на продажу имеет несколько отборочных накладных, связанных с ним.</span><span class="sxs-lookup"><span data-stu-id="e6d24-111">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="e6d24-112">Будет отображаться только слово <multiple> вместо числа отборочных накладных.</span><span class="sxs-lookup"><span data-stu-id="e6d24-112">It will only show the word <multiple> instead of the packing slip number.</span></span>  
5. <span data-ttu-id="e6d24-113">Разверните раздел "Параметры".</span><span class="sxs-lookup"><span data-stu-id="e6d24-113">Expand the Parameters section.</span></span>
    * <span data-ttu-id="e6d24-114">Для разноски необходимо установить значение "Да", чтобы разнести накладную.</span><span class="sxs-lookup"><span data-stu-id="e6d24-114">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="e6d24-115">Также можно отключить разноску и просто напечатать накладную.</span><span class="sxs-lookup"><span data-stu-id="e6d24-115">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="e6d24-116">Однако этот же результат можно получить, создав проформу вместо накладной.</span><span class="sxs-lookup"><span data-stu-id="e6d24-116">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    * <span data-ttu-id="e6d24-117">Этот параметр используется для пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="e6d24-117">This option is used for batch jobs.</span></span> <span data-ttu-id="e6d24-118">Запрос выполняется при выполнении пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="e6d24-118">The query is run when the batch job is run.</span></span>    
6. <span data-ttu-id="e6d24-119">В поле "Печать" выберите "После".</span><span class="sxs-lookup"><span data-stu-id="e6d24-119">In the Print field, select 'After'.</span></span>
7. <span data-ttu-id="e6d24-120">Выберите значение "Да" для параметра "Печать накладной".</span><span class="sxs-lookup"><span data-stu-id="e6d24-120">Select Yes for Print invoice.</span></span>
    * <span data-ttu-id="e6d24-121">С помощью функции управления печатью можно напечатать несколько копий накладной, а также отправить накладную по электронной почте в формате PDF.</span><span class="sxs-lookup"><span data-stu-id="e6d24-121">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
8. <span data-ttu-id="e6d24-122">В поле "Печать расходов" выберите значение "Суммировать".</span><span class="sxs-lookup"><span data-stu-id="e6d24-122">In the Print charges field, select 'Summarize'.</span></span>
9. <span data-ttu-id="e6d24-123">В поле "Проверка кредитного лимита" выберите значение "Сальдо".</span><span class="sxs-lookup"><span data-stu-id="e6d24-123">In the Check credit limit field, select 'Balance'.</span></span>
10. <span data-ttu-id="e6d24-124">Щелкните "Отмена".</span><span class="sxs-lookup"><span data-stu-id="e6d24-124">Click Cancel.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="e6d24-125">Объединение заказов в одну накладную</span><span class="sxs-lookup"><span data-stu-id="e6d24-125">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="e6d24-126">Перейдите в раздел "Расчеты с клиентами" > "Заказы" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="e6d24-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="e6d24-127">Найдите клиента, для которого открыто несколько накладных.</span><span class="sxs-lookup"><span data-stu-id="e6d24-127">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="e6d24-128">Выберите открытый заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="e6d24-128">Select an open sales order.</span></span>
4. <span data-ttu-id="e6d24-129">Выберите другой открытый заказов на продажу для этого же клиента.</span><span class="sxs-lookup"><span data-stu-id="e6d24-129">Select another open sales order for the same customer.</span></span>
5. <span data-ttu-id="e6d24-130">В области действий щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="e6d24-130">On the Action Pane, click Invoice.</span></span>
6. <span data-ttu-id="e6d24-131">Щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="e6d24-131">Click Invoice.</span></span>
7. <span data-ttu-id="e6d24-132">Разверните раздел "Параметры".</span><span class="sxs-lookup"><span data-stu-id="e6d24-132">Expand the Parameters section.</span></span>
8. <span data-ttu-id="e6d24-133">В поле "Количество" выберите значение "Все".</span><span class="sxs-lookup"><span data-stu-id="e6d24-133">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="e6d24-134">Обратите внимание, что в разделе обзора представлено две накладные.</span><span class="sxs-lookup"><span data-stu-id="e6d24-134">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="e6d24-135">Объединим их в одну накладную.</span><span class="sxs-lookup"><span data-stu-id="e6d24-135">Now let's merge them into a single invoice.</span></span>  
9. <span data-ttu-id="e6d24-136">В поле "Суммарная обработка" выберите значение "Счет в накладной".</span><span class="sxs-lookup"><span data-stu-id="e6d24-136">In the Summary update for field, select 'Invoice account'.</span></span>
10. <span data-ttu-id="e6d24-137">Щелкните "Упорядочить", чтобы объединить заказы на продажу в одну накладную.</span><span class="sxs-lookup"><span data-stu-id="e6d24-137">Click Arrange to merge the sales orders into a single invoice.</span></span>
    * <span data-ttu-id="e6d24-138">Два заказа на продажу объединены в одну накладную.</span><span class="sxs-lookup"><span data-stu-id="e6d24-138">The two sales orders are now merged into a single invoice.</span></span>   
11. <span data-ttu-id="e6d24-139">Щелкните "Отмена".</span><span class="sxs-lookup"><span data-stu-id="e6d24-139">Click Cancel.</span></span>
12. <span data-ttu-id="e6d24-140">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="e6d24-140">Click Yes.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="e6d24-141">Разноска накладных в партии</span><span class="sxs-lookup"><span data-stu-id="e6d24-141">Post invoices in a batch</span></span>
1. <span data-ttu-id="e6d24-142">Перейдите в раздел "Расчеты с клиентами" > "Накладные" > "Пакетное выставление накладных" > "Накладная".</span><span class="sxs-lookup"><span data-stu-id="e6d24-142">Go to Accounts receivable > Invoices > Batch invoicing > Invoice.</span></span>
2. <span data-ttu-id="e6d24-143">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="e6d24-143">Click Select.</span></span>
3. <span data-ttu-id="e6d24-144">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e6d24-144">Click OK.</span></span>
4. <span data-ttu-id="e6d24-145">Щелкните "Партия".</span><span class="sxs-lookup"><span data-stu-id="e6d24-145">Click Batch.</span></span>
5. <span data-ttu-id="e6d24-146">Щелкните "Да", чтобы включить пакетную обработку.</span><span class="sxs-lookup"><span data-stu-id="e6d24-146">Click on Yes to turn on batch processing.</span></span>
6. <span data-ttu-id="e6d24-147">Щелкните "Повторение".</span><span class="sxs-lookup"><span data-stu-id="e6d24-147">Click Recurrence.</span></span>
7. <span data-ttu-id="e6d24-148">Выбор дней</span><span class="sxs-lookup"><span data-stu-id="e6d24-148">Select Days</span></span>
8. <span data-ttu-id="e6d24-149">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e6d24-149">Click OK.</span></span>
9. <span data-ttu-id="e6d24-150">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e6d24-150">Click OK.</span></span>
10. <span data-ttu-id="e6d24-151">Щелкните "Отмена".</span><span class="sxs-lookup"><span data-stu-id="e6d24-151">Click Cancel.</span></span>
11. <span data-ttu-id="e6d24-152">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="e6d24-152">Click Yes.</span></span>

