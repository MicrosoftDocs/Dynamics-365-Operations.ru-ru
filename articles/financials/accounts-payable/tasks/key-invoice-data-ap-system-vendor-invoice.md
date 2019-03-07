---
title: Ключевые сведения по накладной в системе расчетов с поставщиками с использованием накладной поставщика
description: Этот проводник по задаче поможет вам создать накладную поставщика из заказа на покупку и просмотреть результаты сопоставления заказа на покупку, поступления и накладной (трехстороннее сопоставление).
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1d2e31a5de7cefd20996c18bf4771296a587997
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "359114"
---
# <a name="key-invoice-data-in-ap-system-using-vendor-invoice"></a><span data-ttu-id="f6df2-103">Ключевые сведения по накладной в системе расчетов с поставщиками с использованием накладной поставщика</span><span class="sxs-lookup"><span data-stu-id="f6df2-103">Key invoice data in AP system using vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f6df2-104">Этот проводник по задаче поможет вам создать накладную поставщика из заказа на покупку и просмотреть результаты сопоставления заказа на покупку, поступления и накладной (трехстороннее сопоставление).</span><span class="sxs-lookup"><span data-stu-id="f6df2-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="f6df2-105">Создание заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="f6df2-105">Create a purchase order</span></span>
1. <span data-ttu-id="f6df2-106">Перейдите в раздел "Расчеты с поставщиками" > "Заказы на покупку" > "Все заказы на покупку".</span><span class="sxs-lookup"><span data-stu-id="f6df2-106">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="f6df2-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="f6df2-107">Click New.</span></span>
3. <span data-ttu-id="f6df2-108">В поле "Счет поставщика" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f6df2-108">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f6df2-109">Найдите поставщика для выбора.</span><span class="sxs-lookup"><span data-stu-id="f6df2-109">Find a vendor to select.</span></span> <span data-ttu-id="f6df2-110">Например, прокрутите вниз до US-104.</span><span class="sxs-lookup"><span data-stu-id="f6df2-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="f6df2-111">Выберите поставщика US-104.</span><span class="sxs-lookup"><span data-stu-id="f6df2-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="f6df2-112">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="f6df2-112">Click OK.</span></span>
7. <span data-ttu-id="f6df2-113">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f6df2-113">In the Item number field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="f6df2-114">Выберите складируемую номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="f6df2-114">Select an inventory item.</span></span> <span data-ttu-id="f6df2-115">Например, выберите код номенклатуры 1000.</span><span class="sxs-lookup"><span data-stu-id="f6df2-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="f6df2-116">Разверните или сверните раздел "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="f6df2-116">Expand or collapse the Line details section.</span></span>
10. <span data-ttu-id="f6df2-117">Перейдите на вкладку "Настройка".</span><span class="sxs-lookup"><span data-stu-id="f6df2-117">Click the Setup tab.</span></span>
    * <span data-ttu-id="f6df2-118">Вы можете переопределить политику проверки соответствия, чтобы использовать двухстороннее сопоставление, трехстороннее сопоставление или полностью отключить сопоставление.</span><span class="sxs-lookup"><span data-stu-id="f6df2-118">You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="f6df2-119">Разверните или сверните раздел "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="f6df2-119">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="f6df2-120">В области действий щелкните "Покупка".</span><span class="sxs-lookup"><span data-stu-id="f6df2-120">On the Action Pane, click Purchase.</span></span>
13. <span data-ttu-id="f6df2-121">Нажмите кнопку "Подтвердить".</span><span class="sxs-lookup"><span data-stu-id="f6df2-121">Click Confirm.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="f6df2-122">Получение продукции</span><span class="sxs-lookup"><span data-stu-id="f6df2-122">Receive the products</span></span>
1. <span data-ttu-id="f6df2-123">В области действий щелкните "Получение".</span><span class="sxs-lookup"><span data-stu-id="f6df2-123">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="f6df2-124">Щелкните "Поступление продуктов".</span><span class="sxs-lookup"><span data-stu-id="f6df2-124">Click Product receipt.</span></span>
3. <span data-ttu-id="f6df2-125">В поле "Поступление продуктов" введите номер поступления продуктов.</span><span class="sxs-lookup"><span data-stu-id="f6df2-125">In the Product receipt field, enter the product receipt number.</span></span> <span data-ttu-id="f6df2-126">Например, введите "PR123".</span><span class="sxs-lookup"><span data-stu-id="f6df2-126">For example, enter PR123.</span></span>
4. <span data-ttu-id="f6df2-127">Щелкните "ОК", чтобы выполнить разноску поступления продуктов.</span><span class="sxs-lookup"><span data-stu-id="f6df2-127">Click OK to post the product receipt.</span></span>
5. <span data-ttu-id="f6df2-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f6df2-128">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="f6df2-129">Создание накладной поставщика</span><span class="sxs-lookup"><span data-stu-id="f6df2-129">Create a vendor invoice</span></span>
1. <span data-ttu-id="f6df2-130">Перейдите в раздел "Расчеты с поставщиками" > "Заказы на покупку" > "Полученные заказы на покупку без выставленных накладных".</span><span class="sxs-lookup"><span data-stu-id="f6df2-130">Go to Accounts payable > Purchase orders > Purchase orders received but not invoiced.</span></span>
2. <span data-ttu-id="f6df2-131">Выберите созданный заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="f6df2-131">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="f6df2-132">В области действий щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="f6df2-132">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="f6df2-133">Щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="f6df2-133">Click Invoice.</span></span>
5. <span data-ttu-id="f6df2-134">В поле "Номер" введите номер накладной.</span><span class="sxs-lookup"><span data-stu-id="f6df2-134">In the Number field, enter the invoice number.</span></span>
6. <span data-ttu-id="f6df2-135">В поле "Описание накладной" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f6df2-135">In the Invoice description field, type a value.</span></span>
7. <span data-ttu-id="f6df2-136">В поле "Дата накладной" введите дату.</span><span class="sxs-lookup"><span data-stu-id="f6df2-136">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="f6df2-137">В поле "Цена за единицу" введите 1200.</span><span class="sxs-lookup"><span data-stu-id="f6df2-137">In the Unit price field, enter 1200.</span></span>
9. <span data-ttu-id="f6df2-138">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="f6df2-138">Click Add line.</span></span>
10. <span data-ttu-id="f6df2-139">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f6df2-139">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="f6df2-140">В списке найдите код номенклатуры накладных расходов на установку.</span><span class="sxs-lookup"><span data-stu-id="f6df2-140">In the list, find the installation charge item number.</span></span> <span data-ttu-id="f6df2-141">Например, S0001.</span><span class="sxs-lookup"><span data-stu-id="f6df2-141">For example, S0001</span></span>
12. <span data-ttu-id="f6df2-142">Выберите код номенклатуры накладных расходов на установку.</span><span class="sxs-lookup"><span data-stu-id="f6df2-142">Select the installation charge item number.</span></span>
    * <span data-ttu-id="f6df2-143">Обратите внимание, что сопоставление не выполнялось с момента внесения изменений.</span><span class="sxs-lookup"><span data-stu-id="f6df2-143">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="f6df2-144">Щелкните "Обновить статус сопоставления".</span><span class="sxs-lookup"><span data-stu-id="f6df2-144">Click Update match status.</span></span>
14. <span data-ttu-id="f6df2-145">В области действий щелкните "Просмотр".</span><span class="sxs-lookup"><span data-stu-id="f6df2-145">On the Action Pane, click Review.</span></span>
15. <span data-ttu-id="f6df2-146">Щелкните "Сведения о сопоставлении".</span><span class="sxs-lookup"><span data-stu-id="f6df2-146">Click Matching details.</span></span>
    * <span data-ttu-id="f6df2-147">Новую строку со службами не требуется сопоставлять, поэтому статус останется прежним: "Не выполнено".</span><span class="sxs-lookup"><span data-stu-id="f6df2-147">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="f6df2-148">Выберите поступление продуктов для полученной складируемой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="f6df2-148">Select the product receipt for the inventory item that you received.</span></span>
    * <span data-ttu-id="f6df2-149">Строка с поступлением продуктов была сопоставлена, но имеется расхождение в количестве или цене, поэтому появляется ошибка.</span><span class="sxs-lookup"><span data-stu-id="f6df2-149">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="f6df2-150">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="f6df2-150">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="f6df2-151">Теперь, когда цена за единицу совпадает, статус обновится до значения "Выполнено".</span><span class="sxs-lookup"><span data-stu-id="f6df2-151">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="f6df2-152">Если политика допускает расхождения или если результатом сопоставления является лишь предупреждение, накладную все равно можно разнести.</span><span class="sxs-lookup"><span data-stu-id="f6df2-152">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="f6df2-153">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f6df2-153">Close the page.</span></span>
19. <span data-ttu-id="f6df2-154">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="f6df2-154">Click Post.</span></span>
20. <span data-ttu-id="f6df2-155">Закройте форму.</span><span class="sxs-lookup"><span data-stu-id="f6df2-155">Close the form.</span></span>
    * <span data-ttu-id="f6df2-156">Обратите внимание, что заказ на покупку больше не указан как полученный, но без выставления в накладных.</span><span class="sxs-lookup"><span data-stu-id="f6df2-156">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  

