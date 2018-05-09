--- 
title: "Утверждение поставщиков для определенных продуктов"
description: "В этой процедуре показано, как утвердить поставщиков для определенных продуктов."
author: mkirknel
manager: AnnBe
ms.date: 11/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a6db8ab41ab393cc92b4fea0435608eff110d58b
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---
# <a name="approve-vendors-for-specific-products"></a><span data-ttu-id="6f934-103">Утверждение поставщиков для определенных продуктов</span><span class="sxs-lookup"><span data-stu-id="6f934-103">Approve vendors for specific products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6f934-104">В этой процедуре показано, как утвердить поставщиков для определенных продуктов.</span><span class="sxs-lookup"><span data-stu-id="6f934-104">This procedure shows you how to approve vendors for specific products.</span></span> <span data-ttu-id="6f934-105">Это позволяет контролировать, каких поставщиков можно использовать при добавлении продукта в заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="6f934-105">This allows you to control which vendors can be used when the product is added to a purchase order.</span></span> <span data-ttu-id="6f934-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="6f934-106">You can use this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="6f934-107">Обычно эту задачу выполняет менеджер по закупкам.</span><span class="sxs-lookup"><span data-stu-id="6f934-107">This task would typically be carried out by a Purchasing manager.</span></span>

1. <span data-ttu-id="6f934-108">Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="6f934-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="6f934-109">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="6f934-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="6f934-110">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="6f934-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="6f934-111">Разверните раздел "Покупка".</span><span class="sxs-lookup"><span data-stu-id="6f934-111">Expand the Purchase section.</span></span>
    * <span data-ttu-id="6f934-112">Если в поле "Поставщик" отображается основной поставщик, необходимо добавить этого поставщика в качестве утвержденного поставщика на следующих шагах.</span><span class="sxs-lookup"><span data-stu-id="6f934-112">If there is a primary vendor shown in the Vendor field, then you need to add this vendor as an approved vendor in the following steps.</span></span> <span data-ttu-id="6f934-113">Запишите номер поставщика, если он отображается.</span><span class="sxs-lookup"><span data-stu-id="6f934-113">Make a note of the vendor number, if one is shown.</span></span>  
5. <span data-ttu-id="6f934-114">В области действий щелкните "Покупка".</span><span class="sxs-lookup"><span data-stu-id="6f934-114">On the Action Pane, click Purchase.</span></span>
6. <span data-ttu-id="6f934-115">Нажмите кнопку Настройка.</span><span class="sxs-lookup"><span data-stu-id="6f934-115">Click Setup.</span></span>
7. <span data-ttu-id="6f934-116">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="6f934-116">Click Add.</span></span>
8. <span data-ttu-id="6f934-117">В поле "Поставщик" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6f934-117">In the Vendor field, enter or select a value.</span></span>
    * <span data-ttu-id="6f934-118">Выберите утвержденного поставщика.</span><span class="sxs-lookup"><span data-stu-id="6f934-118">Select the approved vendor.</span></span> <span data-ttu-id="6f934-119">Хотя бы одна из строк должна быть основным поставщиком, если она присутствовала в записи продукта.</span><span class="sxs-lookup"><span data-stu-id="6f934-119">At least one of the lines has to be the primary vendor if there was one in the product record.</span></span> <span data-ttu-id="6f934-120">Если вы заполнили номер поставщика ранее, выберите его здесь.</span><span class="sxs-lookup"><span data-stu-id="6f934-120">If you made a note of the vendor number earlier, select it here.</span></span>  
9. <span data-ttu-id="6f934-121">В поле "Истечение срока" введите дату.</span><span class="sxs-lookup"><span data-stu-id="6f934-121">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="6f934-122">Выберите дату через несколько месяцев в будущем.</span><span class="sxs-lookup"><span data-stu-id="6f934-122">Choose a date a that is a few months ahead.</span></span>  
10. <span data-ttu-id="6f934-123">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="6f934-123">Click Add.</span></span>
11. <span data-ttu-id="6f934-124">В поле "Поставщик" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6f934-124">In the Vendor field, enter or select a value.</span></span>
12. <span data-ttu-id="6f934-125">В поле "Истечение срока" введите дату.</span><span class="sxs-lookup"><span data-stu-id="6f934-125">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="6f934-126">Выберите дату, отличную от предыдущей даты окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="6f934-126">Choose a date that is different than the previous expiration date.</span></span>  
13. <span data-ttu-id="6f934-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6f934-127">Close the page.</span></span>
14. <span data-ttu-id="6f934-128">Щелкните "Утвержденные поставщики".</span><span class="sxs-lookup"><span data-stu-id="6f934-128">Click Approved vendors.</span></span>
15. <span data-ttu-id="6f934-129">В поле "Истечение срока" введите дату.</span><span class="sxs-lookup"><span data-stu-id="6f934-129">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="6f934-130">Эта дата выступает в роли фильтра, чтобы можно было просмотреть, какие поставщики были утверждены до определенной даты.</span><span class="sxs-lookup"><span data-stu-id="6f934-130">This date acts as a filter so you can see who the approved vendors are, up to a certain date.</span></span>  
16. <span data-ttu-id="6f934-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6f934-131">Close the page.</span></span>
17. <span data-ttu-id="6f934-132">Щелкните "Период действия".</span><span class="sxs-lookup"><span data-stu-id="6f934-132">Click Effective period.</span></span>
18. <span data-ttu-id="6f934-133">В поле "Показать поставщиков, срок действия утверждения которых заканчивается до" введите дату.</span><span class="sxs-lookup"><span data-stu-id="6f934-133">In the Show vendors expired by field, enter a date.</span></span>
    * <span data-ttu-id="6f934-134">Эту страницу можно использовать для определения поставщиков, срок действия статуса утверждения которых заканчивается после определенной даты.</span><span class="sxs-lookup"><span data-stu-id="6f934-134">You can use this page to identify vendors where the approval status will expire after a certain date.</span></span>  
19. <span data-ttu-id="6f934-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6f934-135">Close the page.</span></span>
20. <span data-ttu-id="6f934-136">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="6f934-136">Click Edit.</span></span>
21. <span data-ttu-id="6f934-137">В поле "Способ проверки утвержденных поставщиков" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="6f934-137">In the Approved vendor check method field, select an option.</span></span>
    * <span data-ttu-id="6f934-138">Это поле позволяет выбрать политику в случае, если продукт добавляется к строке заказа на покупку, в которой поставщик не является утвержденным поставщиком.</span><span class="sxs-lookup"><span data-stu-id="6f934-138">This field allows you to select the policy for what should happen if the product is added to a purchase order line where the vendor is not an approved vendor.</span></span>  
22. <span data-ttu-id="6f934-139">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6f934-139">Click Save.</span></span>
23. <span data-ttu-id="6f934-140">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6f934-140">Close the page.</span></span>
24. <span data-ttu-id="6f934-141">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6f934-141">Close the page.</span></span>
25. <span data-ttu-id="6f934-142">Перейдите в раздел "Закупки и источники" > "Поставщики" > "Отношения поставщика и номенклатуры" > "Список утвержденных поставщиков по номенклатуре".</span><span class="sxs-lookup"><span data-stu-id="6f934-142">Go to Procurement and sourcing > Vendors > Vendor/item relations > Approved vendor list by item.</span></span>
    * <span data-ttu-id="6f934-143">На этой странице представлен обзор всех продуктов и утвержденных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="6f934-143">This page gives you an overview of all products and the approved vendors.</span></span>  
26. <span data-ttu-id="6f934-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6f934-144">Close the page.</span></span>
27. <span data-ttu-id="6f934-145">Перейдите в раздел "Закупки и источники" > "Поставщики" > "Все поставщики".</span><span class="sxs-lookup"><span data-stu-id="6f934-145">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
    * <span data-ttu-id="6f934-146">Также можно начать с поставщика, а затем перейти в список утвержденных продуктов для этого счета поставщика.</span><span class="sxs-lookup"><span data-stu-id="6f934-146">You can also start from a vendor and then go to the list of approved products for that vendor account.</span></span>  
28. <span data-ttu-id="6f934-147">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="6f934-147">In the list, find and select the desired record.</span></span>
29. <span data-ttu-id="6f934-148">В области действий щелкните "Закупки".</span><span class="sxs-lookup"><span data-stu-id="6f934-148">On the Action Pane, click Procurement.</span></span>
30. <span data-ttu-id="6f934-149">Щелкните "Список утвержденных поставщиков по поставщикам".</span><span class="sxs-lookup"><span data-stu-id="6f934-149">Click Approved vendor list by vendor.</span></span>
31. <span data-ttu-id="6f934-150">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6f934-150">Close the page.</span></span>
32. <span data-ttu-id="6f934-151">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6f934-151">Close the page.</span></span>


