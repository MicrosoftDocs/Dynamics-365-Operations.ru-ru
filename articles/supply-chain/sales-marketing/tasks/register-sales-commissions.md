--- 
title: "Регистрация комиссий продаж"
description: "В этой процедуре показано, как рассчитываются и регистрируются комиссии за продажу."
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 23ab5f9885983f2409794fc7f51a727a97f40ff4
ms.contentlocale: ru-ru
ms.lasthandoff: 09/11/2018

---
# <a name="register-sales-commissions"></a><span data-ttu-id="89a97-103">Регистрация комиссий продаж</span><span class="sxs-lookup"><span data-stu-id="89a97-103">Register sales commissions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="89a97-104">В этой процедуре показано, как рассчитываются и регистрируются комиссии за продажу.</span><span class="sxs-lookup"><span data-stu-id="89a97-104">This procedure shows you how sales commissions are calculated and registered.</span></span> <span data-ttu-id="89a97-105">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="89a97-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="89a97-106">Перед началом этого руководства выполните руководство "Настройка правил комиссии за продажу", чтобы гарантировать, что выполнена вся настройка расчета комиссии.</span><span class="sxs-lookup"><span data-stu-id="89a97-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="89a97-107">Обратите внимание на номера клиента и номенклатуры, выбранные для процесса комиссии, и используйте их при создании заказа на продажу в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="89a97-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="89a97-108">Выставление накладной по заказу на продажу, разрешающему комиссию для продавца</span><span class="sxs-lookup"><span data-stu-id="89a97-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="89a97-109">Перейдите в раздел "Продажи и маркетинг" > "Заказы на продажу" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="89a97-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="89a97-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="89a97-110">Click New.</span></span>
3. <span data-ttu-id="89a97-111">В поле "Счет клиента" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="89a97-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="89a97-112">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="89a97-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="89a97-113">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="89a97-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="89a97-114">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="89a97-114">Click OK.</span></span>
7. <span data-ttu-id="89a97-115">В области действий щелкните "Параметры".</span><span class="sxs-lookup"><span data-stu-id="89a97-115">On the Action Pane, click Options.</span></span>
8. <span data-ttu-id="89a97-116">Щелкните "Изменить режим просмотра".</span><span class="sxs-lookup"><span data-stu-id="89a97-116">Click Change view.</span></span>
9. <span data-ttu-id="89a97-117">Щелкните Вид заголовка.</span><span class="sxs-lookup"><span data-stu-id="89a97-117">Click Header view.</span></span>
10. <span data-ttu-id="89a97-118">Разверните раздел "Настройка".</span><span class="sxs-lookup"><span data-stu-id="89a97-118">Expand the Setup section.</span></span>
    * <span data-ttu-id="89a97-119">Значение в поле группы продаж соответствует группе с одним или несколькими торговыми представителями, назначенными для нее.</span><span class="sxs-lookup"><span data-stu-id="89a97-119">The value in the Sales group field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="89a97-120">Люди в группе получат комиссии, когда по заказу выставляется счет в соответствии с ранее заданными ставками и распределением.</span><span class="sxs-lookup"><span data-stu-id="89a97-120">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   <span data-ttu-id="89a97-121">Значение копируется из карты клиента, но его можно изменить, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="89a97-121">The value is copied from the Customer card, but you can change it if you wish.</span></span>  <span data-ttu-id="89a97-122">Группа продаж также копируется в строку заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="89a97-122">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="89a97-123">Это можно изменять так, чтобы это отличалось от указанного в заголовке и/или между строками.</span><span class="sxs-lookup"><span data-stu-id="89a97-123">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    * <span data-ttu-id="89a97-124">Значение в поле группы комиссий представляет собой группу, созданную для одного или нескольких клиентов с целью отслеживания комиссии.</span><span class="sxs-lookup"><span data-stu-id="89a97-124">The value in the Commission group field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   <span data-ttu-id="89a97-125">Значение копируется из карты клиента, но его можно изменить, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="89a97-125">The value is copied from the Customer card, but you can change it if you wish.</span></span>   
11. <span data-ttu-id="89a97-126">В области действий щелкните "Параметры".</span><span class="sxs-lookup"><span data-stu-id="89a97-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="89a97-127">Щелкните "Изменить режим просмотра".</span><span class="sxs-lookup"><span data-stu-id="89a97-127">Click Change view.</span></span>
13. <span data-ttu-id="89a97-128">Щелкните Линейное представление.</span><span class="sxs-lookup"><span data-stu-id="89a97-128">Click Line view.</span></span>
14. <span data-ttu-id="89a97-129">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="89a97-129">In the Item number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="89a97-130">В списке выберите номенклатуру, которая настроена для комиссий.</span><span class="sxs-lookup"><span data-stu-id="89a97-130">In the list, select the item you have set up for commissions.</span></span> 
16. <span data-ttu-id="89a97-131">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="89a97-131">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="89a97-132">Обратите внимание на строку "Чистая сумма".</span><span class="sxs-lookup"><span data-stu-id="89a97-132">Take note of the line's Net amount.</span></span> <span data-ttu-id="89a97-133">Она предоставляет собой выручку с продаж, которая в этом примере лежит в основе расчета комиссии.</span><span class="sxs-lookup"><span data-stu-id="89a97-133">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
17. <span data-ttu-id="89a97-134">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="89a97-134">Click Save.</span></span>
18. <span data-ttu-id="89a97-135">В области действий щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="89a97-135">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="89a97-136">Щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="89a97-136">Click Invoice.</span></span>
20. <span data-ttu-id="89a97-137">Разверните раздел "Параметры".</span><span class="sxs-lookup"><span data-stu-id="89a97-137">Expand the Parameters section.</span></span>
21. <span data-ttu-id="89a97-138">В поле "Количество" выберите значение "Все".</span><span class="sxs-lookup"><span data-stu-id="89a97-138">In the Quantity field, select 'All'.</span></span>
22. <span data-ttu-id="89a97-139">Выберите значение "Да" в поле "Разноска".</span><span class="sxs-lookup"><span data-stu-id="89a97-139">Select Yes in the Posting field.</span></span>
23. <span data-ttu-id="89a97-140">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="89a97-140">Click OK.</span></span>
24. <span data-ttu-id="89a97-141">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="89a97-141">Click OK.</span></span>
    * <span data-ttu-id="89a97-142">Разноска проводок может занять около минуты.</span><span class="sxs-lookup"><span data-stu-id="89a97-142">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="89a97-143">Разрешите обработку для завершения и не закрывайте страницу.</span><span class="sxs-lookup"><span data-stu-id="89a97-143">Allow the processing to complete and don’t close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="89a97-144">Просмотр зарегистрированных комиссий за продажу</span><span class="sxs-lookup"><span data-stu-id="89a97-144">Review the registered sales commissions</span></span>
1. <span data-ttu-id="89a97-145">В области действий щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="89a97-145">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="89a97-146">Щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="89a97-146">Click Invoice.</span></span>
3. <span data-ttu-id="89a97-147">В области действий щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="89a97-147">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="89a97-148">Щелкните "Проводки по комиссии".</span><span class="sxs-lookup"><span data-stu-id="89a97-148">Click Commission transactions.</span></span>
    * <span data-ttu-id="89a97-149">На вкладке "Обзор" показаны строки, представляющие суммы комиссии, подлежащие оплате торговым представителям, которые связаны с заказом на продажу, по которому выставлены накладные.</span><span class="sxs-lookup"><span data-stu-id="89a97-149">The Overview tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="89a97-150">Рассмотрим подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="89a97-150">Let's review the details.</span></span>     
    * <span data-ttu-id="89a97-151">Если вы использовали руководство "Настройка правил комиссии за продажу" для настройки группы комиссий за продажу, имеется два торговых представителя для получения комиссий за продажу и комиссия делится поровну между ними.</span><span class="sxs-lookup"><span data-stu-id="89a97-151">If you used the "Set up sales commission rules" guide to set up the Commission sales group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    * <span data-ttu-id="89a97-152">В этом примере общая сумма комиссии рассчитывается как процент от выручки с продаж (чистая сумма строки заказа).</span><span class="sxs-lookup"><span data-stu-id="89a97-152">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>   
5. <span data-ttu-id="89a97-153">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="89a97-153">Close the page.</span></span>
6. <span data-ttu-id="89a97-154">Щелкните "Операция".</span><span class="sxs-lookup"><span data-stu-id="89a97-154">Click Voucher.</span></span>
    * <span data-ttu-id="89a97-155">Можно просматривать проводки по ваучеру для сумм комиссий, разнесенных в предопределенный расход комиссии и счетам, подлежащим оплате комиссии.</span><span class="sxs-lookup"><span data-stu-id="89a97-155">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  


