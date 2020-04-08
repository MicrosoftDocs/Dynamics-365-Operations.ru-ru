---
title: Регистрация комиссий продаж
description: В этой теме объясняется, как рассчитываются и регистрируются комиссии за продажу.
author: omulvad
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8f9cb895f733442e95cd7008c63942463bbd2cba
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148534"
---
# <a name="register-sales-commissions"></a><span data-ttu-id="89570-103">Регистрация комиссий продаж</span><span class="sxs-lookup"><span data-stu-id="89570-103">Register sales commissions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="89570-104">В этой теме объясняется, как рассчитываются и регистрируются комиссии за продажу.</span><span class="sxs-lookup"><span data-stu-id="89570-104">This topic explains how sales commissions are calculated and registered.</span></span> <span data-ttu-id="89570-105">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="89570-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="89570-106">Перед началом этого руководства выполните руководство "Настройка правил комиссии за продажу", чтобы гарантировать, что выполнена вся настройка расчета комиссии.</span><span class="sxs-lookup"><span data-stu-id="89570-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="89570-107">Обратите внимание на номера клиента и номенклатуры, выбранные для процесса комиссии, и используйте их при создании заказа на продажу в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="89570-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="89570-108">Выставление накладной по заказу на продажу, разрешающему комиссию для продавца</span><span class="sxs-lookup"><span data-stu-id="89570-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="89570-109">В области переходов выберите **Модули > Продажи и маркетинг > Заказы на продажу > Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="89570-109">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="89570-110">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="89570-110">Select **New**.</span></span>
3. <span data-ttu-id="89570-111">В поле **Счет клиента** выберите требуемую запись из раскрывающегося меню.</span><span class="sxs-lookup"><span data-stu-id="89570-111">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="89570-112">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="89570-112">Select **OK**.</span></span>
5. <span data-ttu-id="89570-113">В области панели операций выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="89570-113">On the Action Pane, select **Options**.</span></span>
6. <span data-ttu-id="89570-114">Выберите **Изменить режим просмотра**.</span><span class="sxs-lookup"><span data-stu-id="89570-114">Select **Change view**.</span></span>
7. <span data-ttu-id="89570-115">Выберите **Представление заголовка**.</span><span class="sxs-lookup"><span data-stu-id="89570-115">Select **Header view**.</span></span>
8. <span data-ttu-id="89570-116">Разверните раздел **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="89570-116">Expand the **Setup** section.</span></span>

    - <span data-ttu-id="89570-117">Значение в поле **Группа продаж** соответствует группе с одним или несколькими торговыми представителями, назначенными для нее.</span><span class="sxs-lookup"><span data-stu-id="89570-117">The value in the **Sales group** field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="89570-118">Люди в группе получат комиссии, когда по заказу выставляется счет в соответствии с ранее заданными ставками и распределением.</span><span class="sxs-lookup"><span data-stu-id="89570-118">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   
    - <span data-ttu-id="89570-119">Значение копируется из карты клиента, но его можно изменить, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="89570-119">The value is copied from the Customer card, but you can change it if you wish.</span></span>  
    - <span data-ttu-id="89570-120">Группа продаж также копируется в строку заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="89570-120">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="89570-121">Это можно изменять так, чтобы это отличалось от указанного в заголовке и/или между строками.</span><span class="sxs-lookup"><span data-stu-id="89570-121">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    - <span data-ttu-id="89570-122">Значение в поле **Группа комиссий** представляет собой группу, созданную для одного или нескольких клиентов с целью отслеживания комиссии.</span><span class="sxs-lookup"><span data-stu-id="89570-122">The value in the **Commission group** field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   
    - <span data-ttu-id="89570-123">Значение копируется из карты клиента, но его можно изменить, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="89570-123">The value is copied from the Customer card, but you can change it if you wish.</span></span>   

9. <span data-ttu-id="89570-124">В области панели операций выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="89570-124">On the Action Pane, select **Options**.</span></span>
10. <span data-ttu-id="89570-125">Выберите **Изменить режим просмотра**.</span><span class="sxs-lookup"><span data-stu-id="89570-125">Select **Change view**.</span></span>
11. <span data-ttu-id="89570-126">Выберите **Представление строки**.</span><span class="sxs-lookup"><span data-stu-id="89570-126">Select **Line view**.</span></span>
12. <span data-ttu-id="89570-127">В раскрывающемся меню в поле **Код номенклатуры** выберите номенклатуру, настроенную для комиссионных.</span><span class="sxs-lookup"><span data-stu-id="89570-127">In the drop down menu of the **Item number** field, select the item you have set up for commissions.</span></span> 
13. <span data-ttu-id="89570-128">В поле **Количество** введите число.</span><span class="sxs-lookup"><span data-stu-id="89570-128">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="89570-129">Обратите внимание на строку "Чистая сумма".</span><span class="sxs-lookup"><span data-stu-id="89570-129">Take note of the line's Net amount.</span></span> <span data-ttu-id="89570-130">Она предоставляет собой выручку с продаж, которая в этом примере лежит в основе расчета комиссии.</span><span class="sxs-lookup"><span data-stu-id="89570-130">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
14. <span data-ttu-id="89570-131">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="89570-131">Select **Save**.</span></span>
15. <span data-ttu-id="89570-132">На панели операций выберите **Накладная**.</span><span class="sxs-lookup"><span data-stu-id="89570-132">On the Action Pane, select **Invoice**.</span></span>
16. <span data-ttu-id="89570-133">Выберите **Накладная**.</span><span class="sxs-lookup"><span data-stu-id="89570-133">Select **Invoice**.</span></span>
17. <span data-ttu-id="89570-134">Разверните раздел **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="89570-134">Expand the **Parameters** section.</span></span>
18. <span data-ttu-id="89570-135">В поле **Количество** выберите значение **Все**.</span><span class="sxs-lookup"><span data-stu-id="89570-135">In the **Quantity** field, select **All**.</span></span>
19. <span data-ttu-id="89570-136">Выберите значение **Да** в поле **Разноска**.</span><span class="sxs-lookup"><span data-stu-id="89570-136">Select **Yes** in the **Posting** field.</span></span>
20. <span data-ttu-id="89570-137">Выберите **ОК**, затем выберите **ОК** в следующей области.</span><span class="sxs-lookup"><span data-stu-id="89570-137">Select **OK**, then select **OK** in the next pane.</span></span> <span data-ttu-id="89570-138">Разноска проводок может занять около минуты.</span><span class="sxs-lookup"><span data-stu-id="89570-138">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="89570-139">Разрешите обработку для завершения и не закрывайте страницу.</span><span class="sxs-lookup"><span data-stu-id="89570-139">Allow the processing to complete and don't close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="89570-140">Просмотр зарегистрированных комиссий за продажу</span><span class="sxs-lookup"><span data-stu-id="89570-140">Review the registered sales commissions</span></span>
1. <span data-ttu-id="89570-141">В области действий выберите **Накладная**, затем снова выберите **Накладная**.</span><span class="sxs-lookup"><span data-stu-id="89570-141">On the Action Pane, select **Invoice**, then select **Invoice** again.</span></span>
2. <span data-ttu-id="89570-142">В области действий выберите **Накладная**, затем выберите **Проводки по комиссии**.</span><span class="sxs-lookup"><span data-stu-id="89570-142">On the Action Pane, select **Invoice**, then select **Commission transactions**.</span></span>

    - <span data-ttu-id="89570-143">На вкладке **Обзор** показаны строки, представляющие суммы комиссии, подлежащие оплате торговым представителям, которые связаны с заказом на продажу, по которому выставлены накладные.</span><span class="sxs-lookup"><span data-stu-id="89570-143">The **Overview** tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="89570-144">Рассмотрим подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="89570-144">Let's review the details.</span></span>  
    - <span data-ttu-id="89570-145">Если вы использовали руководство "Настройка правил комиссии за продажу" для настройки группы **Комиссии за продажу**, имеется два торговых представителя для получения комиссий за продажу и комиссия делится поровну между ними.</span><span class="sxs-lookup"><span data-stu-id="89570-145">If you used the "Set up sales commission rules" guide to set up the **Commission sales** group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    - <span data-ttu-id="89570-146">В этом примере общая сумма комиссии рассчитывается как процент от выручки с продаж (чистая сумма строки заказа).</span><span class="sxs-lookup"><span data-stu-id="89570-146">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>  
3. <span data-ttu-id="89570-147">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="89570-147">Close the page.</span></span>
4. <span data-ttu-id="89570-148">Выберите **Ваучер**.</span><span class="sxs-lookup"><span data-stu-id="89570-148">Select **Voucher**.</span></span> <span data-ttu-id="89570-149">Можно просматривать проводки по ваучеру для сумм комиссий, разнесенных в предопределенный расход комиссии и счетам, подлежащим оплате комиссии.</span><span class="sxs-lookup"><span data-stu-id="89570-149">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  

