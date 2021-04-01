---
title: Создание накладных по заказам на продажу
description: В этом руководстве по задаче описывается процесс выставления накладных по заказу на продажу, включая объединения накладных и пакетную обработку.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d2e1dd552f529d09756c1ddeec39fc54a1f073a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241594"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="ae1f8-103">Создание накладных по заказам на продажу</span><span class="sxs-lookup"><span data-stu-id="ae1f8-103">Create sales order invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ae1f8-104">В этом руководстве по задаче описывается процесс выставления накладных по заказу на продажу, включая объединения накладных и пакетную обработку.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="ae1f8-105">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="ae1f8-106">Создание накладной из заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="ae1f8-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="ae1f8-107">Перейдите к **Область перехода > Модули > Расчеты с клиентами > Заказы > Отправленные заказы на продажу, для которых не получены накладные**.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-107">Go to **Navigation pane > Modules > Accounts receivable > Orders > Shipped but not invoiced sales orders**.</span></span>
2. <span data-ttu-id="ae1f8-108">Выберите заказ на продажу в списке.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="ae1f8-109">В области **Панель операций** щелкните **Накладная > Создать > Накладная**.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-109">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span> <span data-ttu-id="ae1f8-110">Обратите внимание, что этот заказ на продажу имеет несколько отборочных накладных, связанных с ним.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-110">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="ae1f8-111">Будет отображаться только слово <multiple> вместо числа отборочных накладных.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-111">It will only show the word <multiple> instead of the packing slip number.</span></span>  
4. <span data-ttu-id="ae1f8-112">Разверните раздел **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-112">Expand the **Parameters** section.</span></span>
    - <span data-ttu-id="ae1f8-113">Для разноски необходимо установить значение "Да", чтобы разнести накладную.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-113">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="ae1f8-114">Также можно отключить разноску и просто напечатать накладную.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-114">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="ae1f8-115">Однако этот же результат можно получить, создав проформу вместо накладной.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-115">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    - <span data-ttu-id="ae1f8-116">Этот параметр используется для пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-116">This option is used for batch jobs.</span></span> <span data-ttu-id="ae1f8-117">Запрос выполняется при выполнении пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-117">The query is run when the batch job is run.</span></span>
5. <span data-ttu-id="ae1f8-118">В поле **Печать** выберите "После".</span><span class="sxs-lookup"><span data-stu-id="ae1f8-118">In the **Print** field, select 'After'.</span></span>
6. <span data-ttu-id="ae1f8-119">Выберите значение **Да** для параметра **Печать накладной**.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-119">Select **Yes** for **Print invoice**.</span></span> <span data-ttu-id="ae1f8-120">С помощью функции управления печатью можно напечатать несколько копий накладной, а также отправить накладную по электронной почте в формате PDF.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-120">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
7. <span data-ttu-id="ae1f8-121">В поле **Печать расходов** выберите значение "Суммировать".</span><span class="sxs-lookup"><span data-stu-id="ae1f8-121">In the **Print charges** field, select 'Summarize'.</span></span>
8. <span data-ttu-id="ae1f8-122">В поле **Проверка кредитного лимита** выберите значение "Сальдо".</span><span class="sxs-lookup"><span data-stu-id="ae1f8-122">In the **Check credit limit** field, select 'Balance'.</span></span>
9. <span data-ttu-id="ae1f8-123">Щелкните **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-123">Click **Cancel**.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="ae1f8-124">Объединение заказов в одну накладную</span><span class="sxs-lookup"><span data-stu-id="ae1f8-124">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="ae1f8-125">Перейдите к **Область перехода > Модули > Расчеты с клиентами > Заказы > Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-125">Go to **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="ae1f8-126">Найдите клиента, для которого открыто несколько накладных.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-126">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="ae1f8-127">Выберите несколько открытых заказов на продажу для одного и того же клиента.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-127">Select multiple open sales orders from the same customer.</span></span>
4. <span data-ttu-id="ae1f8-128">В области **Панель операций** щелкните **Накладная > Создать > Накладная**.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-128">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span>
5. <span data-ttu-id="ae1f8-129">Разверните раздел **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-129">Expand the **Parameters** section.</span></span>
6. <span data-ttu-id="ae1f8-130">В поле **Количество** выберите значение "Все".</span><span class="sxs-lookup"><span data-stu-id="ae1f8-130">In the **Quantity** field, select 'All'.</span></span> <span data-ttu-id="ae1f8-131">Обратите внимание, что в разделе обзора представлено две накладные.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-131">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="ae1f8-132">Объединим их в одну накладную.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-132">Now let's merge them into a single invoice.</span></span>  
7. <span data-ttu-id="ae1f8-133">В поле **Суммарная обработка для** выберите значение "Счет в накладной".</span><span class="sxs-lookup"><span data-stu-id="ae1f8-133">In the **Summary update for** field, select 'Invoice account'.</span></span>
8. <span data-ttu-id="ae1f8-134">Щелкните **Упорядочить**, чтобы объединить заказы на продажу в одну накладную.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-134">Click **Arrange** to merge the sales orders into a single invoice.</span></span> <span data-ttu-id="ae1f8-135">Два заказа на продажу объединены в одну накладную.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-135">The two sales orders are now merged into a single invoice.</span></span>   
9. <span data-ttu-id="ae1f8-136">Щелкните **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-136">Click **Cancel**.</span></span>
10. <span data-ttu-id="ae1f8-137">Нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-137">Click **Yes**.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="ae1f8-138">Разноска накладных в партии</span><span class="sxs-lookup"><span data-stu-id="ae1f8-138">Post invoices in a batch</span></span>
1. <span data-ttu-id="ae1f8-139">Выберите **Область переходов > Модули > Расчеты с клиентами > Накладные > Пакетное выставление накладных > Накладная**.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-139">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Batch invoicing > Invoice**.</span></span>
2. <span data-ttu-id="ae1f8-140">Щелкните **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-140">Click **Select**.</span></span>
3. <span data-ttu-id="ae1f8-141">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-141">Click **OK**.</span></span>
4. <span data-ttu-id="ae1f8-142">Щелкните **Партия**.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-142">Click **Batch**.</span></span>
5. <span data-ttu-id="ae1f8-143">В поле **Пакетная обработка** выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-143">Select **Yes** in **Batch processing**.</span></span>
6. <span data-ttu-id="ae1f8-144">Щелкните **Повторение**.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-144">Click **Recurrence**.</span></span>
7. <span data-ttu-id="ae1f8-145">Выберите **Дни**.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-145">Select **Days**.</span></span>
8. <span data-ttu-id="ae1f8-146">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-146">Click **OK**.</span></span>
9. <span data-ttu-id="ae1f8-147">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-147">Click **OK**.</span></span>
10. <span data-ttu-id="ae1f8-148">Щелкните **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-148">Click **Cancel**.</span></span>
11. <span data-ttu-id="ae1f8-149">Нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="ae1f8-149">Click **Yes**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]