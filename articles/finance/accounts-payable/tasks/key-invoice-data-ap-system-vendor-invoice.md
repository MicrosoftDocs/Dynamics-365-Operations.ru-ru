---
title: Ключевые сведения по накладной в системе расчетов с поставщиками с использованием накладной поставщика
description: Этот проводник по задаче поможет вам создать накладную поставщика из заказа на покупку и просмотреть результаты сопоставления заказа на покупку, поступления и накладной (трехстороннее сопоставление).
author: abruer
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5d3f9fc1fb7724632dbc9c4c3e1e28c6e85eaf61
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827802"
---
# <a name="key-invoice-data-in-ap-using-a-vendor-invoice"></a><span data-ttu-id="05f2b-103">Ключевые сведения по накладной в системе расчетов с поставщиками с использованием накладной поставщика</span><span class="sxs-lookup"><span data-stu-id="05f2b-103">Key invoice data in AP using a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="05f2b-104">Этот проводник по задаче поможет вам создать накладную поставщика из заказа на покупку и просмотреть результаты сопоставления заказа на покупку, поступления и накладной (трехстороннее сопоставление).</span><span class="sxs-lookup"><span data-stu-id="05f2b-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="05f2b-105">Создание заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="05f2b-105">Create a purchase order</span></span>
1. <span data-ttu-id="05f2b-106">В области перехода перейдите к **Модули > Расчеты с поставщиками > Заказы на покупку > Все заказы на покупку**.</span><span class="sxs-lookup"><span data-stu-id="05f2b-106">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="05f2b-107">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="05f2b-107">Click **New**.</span></span>
3. <span data-ttu-id="05f2b-108">В поле **Счет поставщика** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="05f2b-108">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="05f2b-109">Найдите поставщика для выбора.</span><span class="sxs-lookup"><span data-stu-id="05f2b-109">Find a vendor to select.</span></span> <span data-ttu-id="05f2b-110">Например, прокрутите вниз до US-104.</span><span class="sxs-lookup"><span data-stu-id="05f2b-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="05f2b-111">Выберите поставщика US-104.</span><span class="sxs-lookup"><span data-stu-id="05f2b-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="05f2b-112">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="05f2b-112">Click **OK**.</span></span>
7. <span data-ttu-id="05f2b-113">В поле **Код номенклатуры** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="05f2b-113">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="05f2b-114">Выберите складируемую номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="05f2b-114">Select an inventory item.</span></span> <span data-ttu-id="05f2b-115">Например, выберите код номенклатуры 1000.</span><span class="sxs-lookup"><span data-stu-id="05f2b-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="05f2b-116">Разверните экспресс-вкладку **Сведения о строке**.</span><span class="sxs-lookup"><span data-stu-id="05f2b-116">Expand the **Line details** fastTab.</span></span>
10. <span data-ttu-id="05f2b-117">Нажмите вкладку **Настройка**. Вы можете переопределить политику проверки соответствия, чтобы использовать двухстороннее сопоставление, трехстороннее сопоставление или полностью отключить сопоставление.</span><span class="sxs-lookup"><span data-stu-id="05f2b-117">Click the **Setup** tab. You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="05f2b-118">В области действий щелкните **Покупка**.</span><span class="sxs-lookup"><span data-stu-id="05f2b-118">On the Action Pane, click **Purchase**.</span></span>
12. <span data-ttu-id="05f2b-119">Нажмите кнопку **Подтвердить**.</span><span class="sxs-lookup"><span data-stu-id="05f2b-119">Click **Confirm**.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="05f2b-120">Получение продукции</span><span class="sxs-lookup"><span data-stu-id="05f2b-120">Receive the products</span></span>
1. <span data-ttu-id="05f2b-121">В области действий щелкните **Получить**.</span><span class="sxs-lookup"><span data-stu-id="05f2b-121">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="05f2b-122">Щелкните **Поступление продуктов**.</span><span class="sxs-lookup"><span data-stu-id="05f2b-122">Click **Product receipt**.</span></span>
3. <span data-ttu-id="05f2b-123">В поле **Поступление продуктов** введите номер поступления продуктов.</span><span class="sxs-lookup"><span data-stu-id="05f2b-123">In the **Product receipt** field, enter the product receipt number.</span></span> <span data-ttu-id="05f2b-124">Например, введите "PR123".</span><span class="sxs-lookup"><span data-stu-id="05f2b-124">For example, enter PR123.</span></span>
4. <span data-ttu-id="05f2b-125">Щелкните **ОК**, чтобы выполнить разноску поступления продуктов.</span><span class="sxs-lookup"><span data-stu-id="05f2b-125">Click **OK** to post the product receipt.</span></span>
5. <span data-ttu-id="05f2b-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="05f2b-126">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="05f2b-127">Создание накладной поставщика</span><span class="sxs-lookup"><span data-stu-id="05f2b-127">Create a vendor invoice</span></span>
1. <span data-ttu-id="05f2b-128">В области перехода перейдите к **Модули > Расчеты с поставщиками > Заказы на покупку > Полученные, но не оприходованные заказы на покупку**.</span><span class="sxs-lookup"><span data-stu-id="05f2b-128">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders received but not invoiced**.</span></span>
2. <span data-ttu-id="05f2b-129">Выберите созданный заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="05f2b-129">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="05f2b-130">На панели операций щелкните **Счет**.</span><span class="sxs-lookup"><span data-stu-id="05f2b-130">On the Action Pane, click **Invoice**.</span></span>
4. <span data-ttu-id="05f2b-131">Щелкните **Счет**.</span><span class="sxs-lookup"><span data-stu-id="05f2b-131">Click **Invoice**.</span></span>
5. <span data-ttu-id="05f2b-132">В поле **Номер** введите номер накладной.</span><span class="sxs-lookup"><span data-stu-id="05f2b-132">In the **Number** field, enter the invoice number.</span></span>
6. <span data-ttu-id="05f2b-133">В поле **Описание счета** введите значение.</span><span class="sxs-lookup"><span data-stu-id="05f2b-133">In the **Invoice description** field, type a value.</span></span>
7. <span data-ttu-id="05f2b-134">В поле **Дата счета** введите дату.</span><span class="sxs-lookup"><span data-stu-id="05f2b-134">In the **Invoice date** field, enter a date.</span></span>
8. <span data-ttu-id="05f2b-135">В поле **Цена за единицу** введите 1200.</span><span class="sxs-lookup"><span data-stu-id="05f2b-135">In the **Unit price** field, enter 1200.</span></span>
9. <span data-ttu-id="05f2b-136">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="05f2b-136">Click **Add line**.</span></span>
10. <span data-ttu-id="05f2b-137">В поле **Код номенклатуры** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="05f2b-137">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="05f2b-138">В списке найдите код номенклатуры накладных расходов на установку.</span><span class="sxs-lookup"><span data-stu-id="05f2b-138">In the list, find the installation charge item number.</span></span> <span data-ttu-id="05f2b-139">Например, S0001.</span><span class="sxs-lookup"><span data-stu-id="05f2b-139">For example, S0001</span></span>
12. <span data-ttu-id="05f2b-140">Выберите код номенклатуры накладных расходов на установку.</span><span class="sxs-lookup"><span data-stu-id="05f2b-140">Select the installation charge item number.</span></span> <span data-ttu-id="05f2b-141">Обратите внимание, что сопоставление не выполнялось с момента внесения изменений.</span><span class="sxs-lookup"><span data-stu-id="05f2b-141">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="05f2b-142">Щелкните **Обновить статус сопоставления**.</span><span class="sxs-lookup"><span data-stu-id="05f2b-142">Click **Update match status**.</span></span>
14. <span data-ttu-id="05f2b-143">В области действий щелкните **Просмотр**.</span><span class="sxs-lookup"><span data-stu-id="05f2b-143">On the Action Pane, click **Review**.</span></span>
15. <span data-ttu-id="05f2b-144">Щелкните **Сведения о сопоставлении**.</span><span class="sxs-lookup"><span data-stu-id="05f2b-144">Click **Matching details**.</span></span> <span data-ttu-id="05f2b-145">Новую строку со службами не требуется сопоставлять, поэтому статус останется прежним: "Не выполнено".</span><span class="sxs-lookup"><span data-stu-id="05f2b-145">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="05f2b-146">Выберите поступление продуктов для полученной складируемой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="05f2b-146">Select the product receipt for the inventory item that you received.</span></span> <span data-ttu-id="05f2b-147">Строка с поступлением продуктов была сопоставлена, но имеется расхождение в количестве или цене, поэтому появляется ошибка.</span><span class="sxs-lookup"><span data-stu-id="05f2b-147">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="05f2b-148">В поле **Цена за единицу** введите число.</span><span class="sxs-lookup"><span data-stu-id="05f2b-148">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="05f2b-149">Теперь, когда цена за единицу совпадает, статус обновится до значения "Выполнено".</span><span class="sxs-lookup"><span data-stu-id="05f2b-149">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="05f2b-150">Если политика допускает расхождения или если результатом сопоставления является лишь предупреждение, накладную все равно можно разнести.</span><span class="sxs-lookup"><span data-stu-id="05f2b-150">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="05f2b-151">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="05f2b-151">Close the page.</span></span>
19. <span data-ttu-id="05f2b-152">Щелкните **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="05f2b-152">Click **Post**.</span></span>
20. <span data-ttu-id="05f2b-153">Закройте форму.</span><span class="sxs-lookup"><span data-stu-id="05f2b-153">Close the form.</span></span> <span data-ttu-id="05f2b-154">Обратите внимание, что заказ на покупку больше не указан как полученный, но без выставления в накладных.</span><span class="sxs-lookup"><span data-stu-id="05f2b-154">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]