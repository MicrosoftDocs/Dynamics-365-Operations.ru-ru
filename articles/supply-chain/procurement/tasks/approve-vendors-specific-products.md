---
title: Утверждение поставщиков для определенных продуктов
description: В этой процедуре показано, как утвердить поставщиков для определенных продуктов.
author: RichardLuan
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cc7d8a93bdbdb5a1446fc34beff4b74aa9d11a0
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016661"
---
# <a name="approve-vendors-for-specific-products"></a><span data-ttu-id="84e49-103">Утверждение поставщиков для определенных продуктов</span><span class="sxs-lookup"><span data-stu-id="84e49-103">Approve vendors for specific products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="84e49-104">В этой процедуре показано, как утвердить поставщиков для определенных продуктов.</span><span class="sxs-lookup"><span data-stu-id="84e49-104">This procedure shows you how to approve vendors for specific products.</span></span> <span data-ttu-id="84e49-105">Это позволяет контролировать, каких поставщиков можно использовать при добавлении продукта в заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="84e49-105">This allows you to control which vendors can be used when the product is added to a purchase order.</span></span> <span data-ttu-id="84e49-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="84e49-106">You can use this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="84e49-107">Обычно эту задачу выполняет менеджер по закупкам.</span><span class="sxs-lookup"><span data-stu-id="84e49-107">This task would typically be carried out by a Purchasing manager.</span></span>

1. <span data-ttu-id="84e49-108">В области перехода выберите **Модули > Управление сведениями о продукте > Продукты > Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="84e49-108">In Navigation Pane, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="84e49-109">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="84e49-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="84e49-110">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="84e49-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="84e49-111">Разверните экспресс-вкладку **Покупка**.</span><span class="sxs-lookup"><span data-stu-id="84e49-111">Expand the **Purchase** fastTab.</span></span> <span data-ttu-id="84e49-112">Если в поле **Поставщик** отображается основной поставщик, необходимо добавить этого поставщика в качестве утвержденного поставщика на следующих шагах.</span><span class="sxs-lookup"><span data-stu-id="84e49-112">If there is a primary vendor shown in the **Vendor** field, then you need to add this vendor as an approved vendor in the following steps.</span></span> <span data-ttu-id="84e49-113">Запишите номер поставщика, если он отображается.</span><span class="sxs-lookup"><span data-stu-id="84e49-113">Make a note of the vendor number, if one is shown.</span></span>  
5. <span data-ttu-id="84e49-114">В области действий щелкните **Покупка**.</span><span class="sxs-lookup"><span data-stu-id="84e49-114">On the Action Pane, click **Purchase**.</span></span>
6. <span data-ttu-id="84e49-115">Щелкните **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="84e49-115">Click **Setup**.</span></span>
7. <span data-ttu-id="84e49-116">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="84e49-116">Click **Add**.</span></span>
8. <span data-ttu-id="84e49-117">В поле "Поставщик" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="84e49-117">In the Vendor field, enter or select a value.</span></span> <span data-ttu-id="84e49-118">Выберите утвержденного поставщика.</span><span class="sxs-lookup"><span data-stu-id="84e49-118">Select the approved vendor.</span></span> <span data-ttu-id="84e49-119">Хотя бы одна из строк должна быть основным поставщиком, если она присутствовала в записи продукта.</span><span class="sxs-lookup"><span data-stu-id="84e49-119">At least one of the lines has to be the primary vendor if there was one in the product record.</span></span> <span data-ttu-id="84e49-120">Если вы заполнили номер поставщика ранее, выберите его здесь.</span><span class="sxs-lookup"><span data-stu-id="84e49-120">If you made a note of the vendor number earlier, select it here.</span></span>  
9. <span data-ttu-id="84e49-121">В поле **Истечение срока** введите дату.</span><span class="sxs-lookup"><span data-stu-id="84e49-121">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="84e49-122">Выберите дату через несколько месяцев в будущем.</span><span class="sxs-lookup"><span data-stu-id="84e49-122">Choose a date a that is a few months ahead.</span></span>  
10. <span data-ttu-id="84e49-123">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="84e49-123">Click **Add**.</span></span>
11. <span data-ttu-id="84e49-124">В поле **Поставщик** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="84e49-124">In the **Vendor** field, enter or select a value.</span></span>
12. <span data-ttu-id="84e49-125">В поле **Истечение срока** введите дату.</span><span class="sxs-lookup"><span data-stu-id="84e49-125">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="84e49-126">Выберите дату, отличную от предыдущей даты окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="84e49-126">Choose a date that is different than the previous expiration date.</span></span>  
13. <span data-ttu-id="84e49-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="84e49-127">Close the page.</span></span>
14. <span data-ttu-id="84e49-128">На панели операций щелкните **Утвержденные поставщики**.</span><span class="sxs-lookup"><span data-stu-id="84e49-128">On the Action Pane, click **Approved vendors**.</span></span>
15. <span data-ttu-id="84e49-129">В поле **Истечение срока** введите дату.</span><span class="sxs-lookup"><span data-stu-id="84e49-129">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="84e49-130">Эта дата выступает в роли фильтра, чтобы можно было просмотреть, какие поставщики были утверждены до определенной даты.</span><span class="sxs-lookup"><span data-stu-id="84e49-130">This date acts as a filter so you can see who the approved vendors are, up to a certain date.</span></span>  
16. <span data-ttu-id="84e49-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="84e49-131">Close the page.</span></span>
17. <span data-ttu-id="84e49-132">На панели операций щелкните **Период действия**.</span><span class="sxs-lookup"><span data-stu-id="84e49-132">On the Action Pane, click **Effective period**.</span></span>
18. <span data-ttu-id="84e49-133">В поле **Показать поставщиков, срок действия утверждения которых заканчивается до** введите дату.</span><span class="sxs-lookup"><span data-stu-id="84e49-133">In the **Show vendors expired by** field, enter a date.</span></span> <span data-ttu-id="84e49-134">Эту страницу можно использовать для определения поставщиков, срок действия статуса утверждения которых заканчивается после определенной даты.</span><span class="sxs-lookup"><span data-stu-id="84e49-134">You can use this page to identify vendors where the approval status will expire after a certain date.</span></span>  
19. <span data-ttu-id="84e49-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="84e49-135">Close the page.</span></span>
20. <span data-ttu-id="84e49-136">Выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="84e49-136">Click **Edit**.</span></span>
21. <span data-ttu-id="84e49-137">В поле **Способ проверки утвержденных поставщиков** выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="84e49-137">In the **Approved vendor check method** field, select an option.</span></span> <span data-ttu-id="84e49-138">Это поле позволяет выбрать политику в случае, если продукт добавляется к строке заказа на покупку, в которой поставщик не является утвержденным поставщиком.</span><span class="sxs-lookup"><span data-stu-id="84e49-138">This field allows you to select the policy for what should happen if the product is added to a purchase order line where the vendor is not an approved vendor.</span></span>  
22. <span data-ttu-id="84e49-139">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="84e49-139">Click **Save**.</span></span>
23. <span data-ttu-id="84e49-140">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="84e49-140">Close the page.</span></span>
24. <span data-ttu-id="84e49-141">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="84e49-141">Close the page.</span></span>
25. <span data-ttu-id="84e49-142">В области перехода выберите **Модули > Закупки и источники > Поставщики > Отношения поставщика и номенклатуры > Список утвержденных поставщиков по номенклатуре**.</span><span class="sxs-lookup"><span data-stu-id="84e49-142">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > Vendor/item relations > Approved vendor list by item**.</span></span> <span data-ttu-id="84e49-143">На этой странице представлен обзор всех продуктов и утвержденных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="84e49-143">This page gives you an overview of all products and the approved vendors.</span></span>  
26. <span data-ttu-id="84e49-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="84e49-144">Close the page.</span></span>
27. <span data-ttu-id="84e49-145">В область переходов выберите **Модули > Закупки и источники > Поставщики > Все поставщики**.</span><span class="sxs-lookup"><span data-stu-id="84e49-145">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span> <span data-ttu-id="84e49-146">Также можно начать с поставщика, а затем перейти в список утвержденных продуктов для этого счета поставщика.</span><span class="sxs-lookup"><span data-stu-id="84e49-146">You can also start from a vendor and then go to the list of approved products for that vendor account.</span></span>  
28. <span data-ttu-id="84e49-147">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="84e49-147">In the list, find and select the desired record.</span></span>
29. <span data-ttu-id="84e49-148">На панели операций щелкните **Закупки**.</span><span class="sxs-lookup"><span data-stu-id="84e49-148">On the Action Pane, click **Procurement**.</span></span>
30. <span data-ttu-id="84e49-149">Щелкните **Список утвержденных поставщиков по поставщикам**.</span><span class="sxs-lookup"><span data-stu-id="84e49-149">Click **Approved vendor list by vendor**.</span></span>
31. <span data-ttu-id="84e49-150">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="84e49-150">Close the page.</span></span>
32. <span data-ttu-id="84e49-151">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="84e49-151">Close the page.</span></span>

