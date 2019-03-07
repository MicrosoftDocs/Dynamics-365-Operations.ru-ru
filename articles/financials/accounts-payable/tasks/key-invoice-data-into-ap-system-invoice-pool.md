---
title: Ввод данных счета в модуль расчетов с поставщиками с использованием кластера накладных
description: В этом руководстве по задаче показано, как использовать регистр накладных для создания накладных.
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b4e9a52a383d4acc0bf2adc669fd88c0c0f7402
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "357458"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="2b2d0-103">Ввод данных счета в модуль расчетов с поставщиками с использованием кластера накладных</span><span class="sxs-lookup"><span data-stu-id="2b2d0-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2b2d0-104">В этом руководстве по задаче показано, как использовать регистр накладных для создания накладных.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-104">This task guide will show you how to use the invoice register to create invoices.</span></span>  <span data-ttu-id="2b2d0-105">Затем используйте кластер накладных для сопоставления накладной с заказом на покупку и завершения оформления расходов на странице накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="2b2d0-106">Создание заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="2b2d0-106">Create a purchase order</span></span>
1. <span data-ttu-id="2b2d0-107">Перейдите в раздел "Расчеты с поставщиками" > "Заказы на покупку" > "Заказы на покупку".</span><span class="sxs-lookup"><span data-stu-id="2b2d0-107">Go to Accounts payable > Purchase orders > Purchase orders.</span></span>
2. <span data-ttu-id="2b2d0-108">Щелкните "Создать", чтобы создать заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-108">Click New to create a purchase order.</span></span>
3. <span data-ttu-id="2b2d0-109">В поле "Счет поставщика" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-109">In the Vendor account field, click the drop down button to open the lookup.</span></span>
4. <span data-ttu-id="2b2d0-110">Выберите поставщика в списке.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-110">Select the vendor from the list.</span></span> <span data-ttu-id="2b2d0-111">Например, выберите поставщика 1001.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-111">For example, vendor 1001.</span></span>
5. <span data-ttu-id="2b2d0-112">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-112">Click OK.</span></span>
6. <span data-ttu-id="2b2d0-113">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-113">In the Item number field, click the drop down button to open the lookup.</span></span>
7. <span data-ttu-id="2b2d0-114">Найдите код номенклатуры обслуживания в списке.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-114">Find the services item number in the list.</span></span> <span data-ttu-id="2b2d0-115">Например, выберите S0001.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-115">For example, select S0001.</span></span>
8. <span data-ttu-id="2b2d0-116">Щелкните код номенклатуры, чтобы выбрать его.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-116">Click on the item number and select it.</span></span>
    * <span data-ttu-id="2b2d0-117">Чистая сумма равна 75,00.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-117">The net amount is 75.00.</span></span>  <span data-ttu-id="2b2d0-118">Это сумма, которая ожидается в накладной.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-118">That is the amount that we will expect on the invoice.</span></span>  
9. <span data-ttu-id="2b2d0-119">В области действий щелкните "Покупка".</span><span class="sxs-lookup"><span data-stu-id="2b2d0-119">On the action pane, click Purchase.</span></span>
10. <span data-ttu-id="2b2d0-120">Нажмите кнопку "Подтвердить".</span><span class="sxs-lookup"><span data-stu-id="2b2d0-120">Click Confirm.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="2b2d0-121">Создание и разноска накладной</span><span class="sxs-lookup"><span data-stu-id="2b2d0-121">Create and post and invoice</span></span>
1. <span data-ttu-id="2b2d0-122">Перейдите в раздел "Расчеты с поставщиками" > "Накладные" > "Регистр накладных".</span><span class="sxs-lookup"><span data-stu-id="2b2d0-122">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="2b2d0-123">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="2b2d0-123">Click New.</span></span>
3. <span data-ttu-id="2b2d0-124">Откройте поиск, чтобы выбрать имя регистра накладных для использования.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-124">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="2b2d0-125">Выберите имя регистра накладных для использования.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-125">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="2b2d0-126">Щелкните "Строки", чтобы открыть регистр и ввести строки расходов.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-126">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="2b2d0-127">В окне поиска выберите поставщика.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-127">In the lookup, select a vendor.</span></span> <span data-ttu-id="2b2d0-128">Например, выберите поставщика 1001.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-128">For example, click on vendor 1001.</span></span>
7. <span data-ttu-id="2b2d0-129">В поле Накладная введите номер накладной.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-129">In the Invoice field, enter the invoice number.</span></span>
8. <span data-ttu-id="2b2d0-130">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-130">In the Description field, type a value.</span></span>
9. <span data-ttu-id="2b2d0-131">В поле "Кредит" введите число.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-131">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="2b2d0-132">В поле "Заказ на покупку" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-132">In the Purchase order field, click the drop down button to open the lookup.</span></span>
11. <span data-ttu-id="2b2d0-133">Выберите заказ на покупку, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-133">Select the purchase order that you created earlier.</span></span>
12. <span data-ttu-id="2b2d0-134">В поле "Кем утверждено" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-134">In the Approved by field, click the drop down button to open the lookup.</span></span>
13. <span data-ttu-id="2b2d0-135">Выделите утверждающее лицо и нажмите кнопку "Выбрать", чтобы выбрать его.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-135">Highlight an approver and click Select to select that approver.</span></span>
14. <span data-ttu-id="2b2d0-136">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="2b2d0-136">Click Post.</span></span>
15. <span data-ttu-id="2b2d0-137">Закройте форму.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-137">Close the form.</span></span>
16. <span data-ttu-id="2b2d0-138">Закройте форму.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-138">Close the form.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="2b2d0-139">Открытие накладной из кластера и сопоставление накладной с заказом на покупку для завершения процесса накладной</span><span class="sxs-lookup"><span data-stu-id="2b2d0-139">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="2b2d0-140">Перейдите в раздел "Расчеты с поставщиками" > "Накладные" > "Кластер накладных".</span><span class="sxs-lookup"><span data-stu-id="2b2d0-140">Go to Accounts payable > Invoices > Invoice pool.</span></span>
2. <span data-ttu-id="2b2d0-141">Щелкните "Заказ на покупку", чтобы создать накладную поставщика из накладной в кластере.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-141">Click Purchase order to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="2b2d0-142">Выберите накладную, которую требуется просмотреть.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-142">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="2b2d0-143">Щелкните "Обновить статус сопоставления", чтобы завершить сопоставление.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-143">Click Update match status to complete the matching.</span></span>
5. <span data-ttu-id="2b2d0-144">В области действий щелкните "Параметры".</span><span class="sxs-lookup"><span data-stu-id="2b2d0-144">On the action pane, click Options.</span></span>
6. <span data-ttu-id="2b2d0-145">Щелкните "Изменить режим просмотра".</span><span class="sxs-lookup"><span data-stu-id="2b2d0-145">Click Change view.</span></span>
7. <span data-ttu-id="2b2d0-146">Щелкните "Представление сетки".</span><span class="sxs-lookup"><span data-stu-id="2b2d0-146">Click Grid view.</span></span>
8. <span data-ttu-id="2b2d0-147">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="2b2d0-147">Click Post.</span></span>
9. <span data-ttu-id="2b2d0-148">Закройте форму.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-148">Close the form.</span></span>
10. <span data-ttu-id="2b2d0-149">Перейдите в раздел "Расчеты с поставщиками" > "Поставщики" > "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="2b2d0-149">Go to Accounts payable > Vendors > Vendors.</span></span>
11. <span data-ttu-id="2b2d0-150">Выберите поставщика, указанного в заказе на покупку.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-150">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="2b2d0-151">Например, выберите поставщика 1001.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-151">For example, select vendor 1001.</span></span>
12. <span data-ttu-id="2b2d0-152">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-152">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="2b2d0-153">В области действий щелкните "Поставщик".</span><span class="sxs-lookup"><span data-stu-id="2b2d0-153">On the action pane, click Vendor.</span></span>
14. <span data-ttu-id="2b2d0-154">Щелкните "Проводки".</span><span class="sxs-lookup"><span data-stu-id="2b2d0-154">Click Transactions.</span></span>
15. <span data-ttu-id="2b2d0-155">Выберите созданную накладную.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-155">Select the invoice that you created.</span></span>
    * <span data-ttu-id="2b2d0-156">Начисление регистра накладных было реверсировано и разнесено на соответствующий счет расходов.</span><span class="sxs-lookup"><span data-stu-id="2b2d0-156">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  

