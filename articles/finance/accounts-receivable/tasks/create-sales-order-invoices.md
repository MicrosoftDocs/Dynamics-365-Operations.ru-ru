---
title: Создание накладных по заказам на продажу
description: В этом руководстве по задаче описывается процесс выставления накладных по заказу на продажу, включая объединения накладных и пакетную обработку.
author: ShivamPandey-msft
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 984bb482f357e35dcfa4c08597a6be9e39817b98
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837113"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="be2b1-103">Создание накладных по заказам на продажу</span><span class="sxs-lookup"><span data-stu-id="be2b1-103">Create sales order invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="be2b1-104">В этом руководстве по задаче описывается процесс выставления накладных по заказу на продажу, включая объединения накладных и пакетную обработку.</span><span class="sxs-lookup"><span data-stu-id="be2b1-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="be2b1-105">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="be2b1-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="be2b1-106">Создание накладной из заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="be2b1-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="be2b1-107">Перейдите к **Область перехода > Модули > Расчеты с клиентами > Заказы > Отправленные заказы на продажу, для которых не получены накладные**.</span><span class="sxs-lookup"><span data-stu-id="be2b1-107">Go to **Navigation pane > Modules > Accounts receivable > Orders > Shipped but not invoiced sales orders**.</span></span>
2. <span data-ttu-id="be2b1-108">Выберите заказ на продажу в списке.</span><span class="sxs-lookup"><span data-stu-id="be2b1-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="be2b1-109">В области **Панель операций** щелкните **Накладная > Создать > Накладная**.</span><span class="sxs-lookup"><span data-stu-id="be2b1-109">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span> <span data-ttu-id="be2b1-110">Обратите внимание, что этот заказ на продажу имеет несколько отборочных накладных, связанных с ним.</span><span class="sxs-lookup"><span data-stu-id="be2b1-110">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="be2b1-111">Будет отображаться только слово <multiple> вместо числа отборочных накладных.</span><span class="sxs-lookup"><span data-stu-id="be2b1-111">It will only show the word <multiple> instead of the packing slip number.</span></span>  
4. <span data-ttu-id="be2b1-112">Разверните раздел **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="be2b1-112">Expand the **Parameters** section.</span></span>
    - <span data-ttu-id="be2b1-113">Для разноски необходимо установить значение "Да", чтобы разнести накладную.</span><span class="sxs-lookup"><span data-stu-id="be2b1-113">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="be2b1-114">Также можно отключить разноску и просто напечатать накладную.</span><span class="sxs-lookup"><span data-stu-id="be2b1-114">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="be2b1-115">Однако этот же результат можно получить, создав проформу вместо накладной.</span><span class="sxs-lookup"><span data-stu-id="be2b1-115">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    - <span data-ttu-id="be2b1-116">Этот параметр используется для пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="be2b1-116">This option is used for batch jobs.</span></span> <span data-ttu-id="be2b1-117">Запрос выполняется при выполнении пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="be2b1-117">The query is run when the batch job is run.</span></span>
5. <span data-ttu-id="be2b1-118">В поле **Печать** выберите "После".</span><span class="sxs-lookup"><span data-stu-id="be2b1-118">In the **Print** field, select 'After'.</span></span>
6. <span data-ttu-id="be2b1-119">Выберите значение **Да** для параметра **Печать накладной**.</span><span class="sxs-lookup"><span data-stu-id="be2b1-119">Select **Yes** for **Print invoice**.</span></span> <span data-ttu-id="be2b1-120">С помощью функции управления печатью можно напечатать несколько копий накладной, а также отправить накладную по электронной почте в формате PDF.</span><span class="sxs-lookup"><span data-stu-id="be2b1-120">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
7. <span data-ttu-id="be2b1-121">В поле **Печать расходов** выберите значение "Суммировать".</span><span class="sxs-lookup"><span data-stu-id="be2b1-121">In the **Print charges** field, select 'Summarize'.</span></span>
8. <span data-ttu-id="be2b1-122">В поле **Проверка кредитного лимита** выберите значение "Сальдо".</span><span class="sxs-lookup"><span data-stu-id="be2b1-122">In the **Check credit limit** field, select 'Balance'.</span></span>
9. <span data-ttu-id="be2b1-123">Щелкните **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="be2b1-123">Click **Cancel**.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="be2b1-124">Объединение заказов в одну накладную</span><span class="sxs-lookup"><span data-stu-id="be2b1-124">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="be2b1-125">Перейдите к **Область перехода > Модули > Расчеты с клиентами > Заказы > Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="be2b1-125">Go to **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="be2b1-126">Найдите клиента, для которого открыто несколько накладных.</span><span class="sxs-lookup"><span data-stu-id="be2b1-126">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="be2b1-127">Выберите несколько открытых заказов на продажу для одного и того же клиента.</span><span class="sxs-lookup"><span data-stu-id="be2b1-127">Select multiple open sales orders from the same customer.</span></span>
4. <span data-ttu-id="be2b1-128">В области **Панель операций** щелкните **Накладная > Создать > Накладная**.</span><span class="sxs-lookup"><span data-stu-id="be2b1-128">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span>
5. <span data-ttu-id="be2b1-129">Разверните раздел **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="be2b1-129">Expand the **Parameters** section.</span></span>
6. <span data-ttu-id="be2b1-130">В поле **Количество** выберите значение "Все".</span><span class="sxs-lookup"><span data-stu-id="be2b1-130">In the **Quantity** field, select 'All'.</span></span> <span data-ttu-id="be2b1-131">Обратите внимание, что в разделе обзора представлено две накладные.</span><span class="sxs-lookup"><span data-stu-id="be2b1-131">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="be2b1-132">Объединим их в одну накладную.</span><span class="sxs-lookup"><span data-stu-id="be2b1-132">Now let's merge them into a single invoice.</span></span>  
7. <span data-ttu-id="be2b1-133">В поле **Суммарная обработка для** выберите значение "Счет в накладной".</span><span class="sxs-lookup"><span data-stu-id="be2b1-133">In the **Summary update for** field, select 'Invoice account'.</span></span>
8. <span data-ttu-id="be2b1-134">Щелкните **Упорядочить**, чтобы объединить заказы на продажу в одну накладную.</span><span class="sxs-lookup"><span data-stu-id="be2b1-134">Click **Arrange** to merge the sales orders into a single invoice.</span></span> <span data-ttu-id="be2b1-135">Два заказа на продажу объединены в одну накладную.</span><span class="sxs-lookup"><span data-stu-id="be2b1-135">The two sales orders are now merged into a single invoice.</span></span>   
9. <span data-ttu-id="be2b1-136">Щелкните **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="be2b1-136">Click **Cancel**.</span></span>
10. <span data-ttu-id="be2b1-137">Нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="be2b1-137">Click **Yes**.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="be2b1-138">Разноска накладных в партии</span><span class="sxs-lookup"><span data-stu-id="be2b1-138">Post invoices in a batch</span></span>
1. <span data-ttu-id="be2b1-139">Выберите **Область переходов > Модули > Расчеты с клиентами > Накладные > Пакетное выставление накладных > Накладная**.</span><span class="sxs-lookup"><span data-stu-id="be2b1-139">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Batch invoicing > Invoice**.</span></span>
2. <span data-ttu-id="be2b1-140">Щелкните **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="be2b1-140">Click **Select**.</span></span>
3. <span data-ttu-id="be2b1-141">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="be2b1-141">Click **OK**.</span></span>
4. <span data-ttu-id="be2b1-142">Щелкните **Партия**.</span><span class="sxs-lookup"><span data-stu-id="be2b1-142">Click **Batch**.</span></span>
5. <span data-ttu-id="be2b1-143">В поле **Пакетная обработка** выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="be2b1-143">Select **Yes** in **Batch processing**.</span></span>
6. <span data-ttu-id="be2b1-144">Щелкните **Повторение**.</span><span class="sxs-lookup"><span data-stu-id="be2b1-144">Click **Recurrence**.</span></span>
7. <span data-ttu-id="be2b1-145">Выберите **Дни**.</span><span class="sxs-lookup"><span data-stu-id="be2b1-145">Select **Days**.</span></span>
8. <span data-ttu-id="be2b1-146">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="be2b1-146">Click **OK**.</span></span>
9. <span data-ttu-id="be2b1-147">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="be2b1-147">Click **OK**.</span></span>
10. <span data-ttu-id="be2b1-148">Щелкните **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="be2b1-148">Click **Cancel**.</span></span>
11. <span data-ttu-id="be2b1-149">Нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="be2b1-149">Click **Yes**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]