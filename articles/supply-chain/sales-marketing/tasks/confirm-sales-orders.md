---
title: Подтверждение заказов на продажу
description: В этой процедуре демонстрируется, как подтверждать заказы на продажу.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db475cf967bebec2d442aaa864800d920cf0ab81
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "323993"
---
# <a name="confirm-sales-orders"></a><span data-ttu-id="c1e2c-103">Подтверждение заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="c1e2c-103">Confirm sales orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c1e2c-104">В этой процедуре демонстрируется, как подтверждать заказы на продажу.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-104">This procedure demonstrates how to confirm sales orders.</span></span> <span data-ttu-id="c1e2c-105">Вы увидите, как подтвердить один заказ, а также подтвердить несколько заказов сразу.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-105">You’ll be shown how to confirm a single order, and how to confirm multiple orders at once.</span></span> <span data-ttu-id="c1e2c-106">Эти задачи обычно выполняются обработчиком заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-106">These tasks would typically be carried out by a sales order processor.</span></span> <span data-ttu-id="c1e2c-107">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="c1e2c-108">Прежде чем начать, убедитесь, что у вас есть несколько открытых заказов на продажу для одного и того же клиента.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-108">Before you start, make sure there are several open sales orders for the same customer.</span></span> <span data-ttu-id="c1e2c-109">При использовании USMF можно использовать клиента US-027.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-109">If you’re using USMF, you can use customer US-027.</span></span>


## <a name="confirm-a-single-sales-order"></a><span data-ttu-id="c1e2c-110">Подтверждение одного заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="c1e2c-110">Confirm a single sales order</span></span>
1. <span data-ttu-id="c1e2c-111">Перейдите в раздел "Продажи и маркетинг" > "Заказы на продажу" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-111">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="c1e2c-112">Найдите в списке и выберите заказ, который требуется подтвердить.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-112">In the list, find and select the order that you want to confirm.</span></span>
3. <span data-ttu-id="c1e2c-113">Щелкните ссылку в номере заказа на продажу, чтобы открыть выбранный заказ.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-113">Click the link on the sales order number to open the selected order.</span></span>
4. <span data-ttu-id="c1e2c-114">В области действий щелкните "Продажа".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-114">On the Action Pane, click Sell.</span></span>
5. <span data-ttu-id="c1e2c-115">Щелкните "Подтверждение заказа на продажу".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-115">Click Confirm sales order.</span></span>
6. <span data-ttu-id="c1e2c-116">Разверните или сверните раздел "Параметры".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-116">Expand or collapse the Parameters section.</span></span>
    * <span data-ttu-id="c1e2c-117">Убедитесь, что поле "Разноска" = "Да" активно.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-117">Make sure that the Posting Yes field is active.</span></span>  
7. <span data-ttu-id="c1e2c-118">Установите параметр "Печать подтверждения" в значение "Да".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-118">Set the Print confirmation option to Yes.</span></span>
    * <span data-ttu-id="c1e2c-119">В поле "Проверка кредитного лимита" указывается метод, используемый для расчета кредитного остатка клиента.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-119">The Check credit limit field specifies the method that’s used to calculate a customer's remaining credit.</span></span> <span data-ttu-id="c1e2c-120">По умолчанию он копируется со страницы "Параметры расчетов с клиентами".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-120">By default, it’s copied from the Accounts receivable parameters page.</span></span> <span data-ttu-id="c1e2c-121">Если вы хотите пропустить проверку кредитного лимита при подтверждении конкретного заказа на продажу, выберите в поле "Проверка кредитного лимита" значение "Нет".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-121">If you want to skip the credit limit check when confirming a specific sales order, set the Check credit limit to None.</span></span> <span data-ttu-id="c1e2c-122">Однако следует иметь в виду, что даже когда в этом поле выбрано значение "Нет", проверка кредитного лимита все равно будет выполняться, если в справочнике клиента установлен флажок "Обязательный кредитный лимит".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-122">However, you should be aware that even with if this field is set to None, the credit limit check will still be performed if the Mandatory credit limit option is selected on the customer master data.</span></span>  
8. <span data-ttu-id="c1e2c-123">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-123">Click OK.</span></span>
9. <span data-ttu-id="c1e2c-124">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-124">Click Yes.</span></span>
10. <span data-ttu-id="c1e2c-125">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-125">Close the page.</span></span>
11. <span data-ttu-id="c1e2c-126">В области действий щелкните "Параметры".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="c1e2c-127">Щелкните "Изменить режим просмотра".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-127">Click Change view.</span></span>
13. <span data-ttu-id="c1e2c-128">Щелкните Вид заголовка.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-128">Click Header view.</span></span>
    * <span data-ttu-id="c1e2c-129">При подтверждении заказа параметр "Статус документа" устанавливается в значение "Подтверждение".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-129">When an order is confirmed, the Document status is set to Confirmation.</span></span>  
14. <span data-ttu-id="c1e2c-130">В области действий щелкните "Продажа".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-130">On the Action Pane, click Sell.</span></span>
15. <span data-ttu-id="c1e2c-131">Щелкните "Подтверждение заказа на продажу".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-131">Click Sales order confirmation.</span></span>
16. <span data-ttu-id="c1e2c-132">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-132">Close the page.</span></span>

## <a name="confirm-multiple-sales-orders-at-once"></a><span data-ttu-id="c1e2c-133">Подтверждение сразу нескольких заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="c1e2c-133">Confirm multiple sales orders at once</span></span>
1. <span data-ttu-id="c1e2c-134">Перейдите в раздел "Продажи и маркетинг" > "Заказы на продажу" > "Подтверждение заказа" > "Подтверждение заказа на продажу".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-134">Go to Sales and marketing > Sales orders > Order confirmation > Confirm sales order.</span></span>
2. <span data-ttu-id="c1e2c-135">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-135">Click Select.</span></span>
3. <span data-ttu-id="c1e2c-136">В списке на вкладке "Диапазон", найдите и выберите запись, которая ссылается на поле "Счет клиента".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-136">In the list on the Range tab, find and select the record that references the Customer account field.</span></span>
4. <span data-ttu-id="c1e2c-137">В поле "Критерии" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-137">In the Criteria field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c1e2c-138">В списке найдите и выберите счет клиента с несколькими заказами, которые вы хотите подтвердить.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-138">In the list, find and select the customer account that has multiple orders which you want to mass confirm.</span></span>
    * <span data-ttu-id="c1e2c-139">При использовании USMF можно выбрать счет US-027.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-139">If you’re using USMF, you can select account US-027.</span></span>  
6. <span data-ttu-id="c1e2c-140">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-140">Click OK.</span></span>
    * <span data-ttu-id="c1e2c-141">На вкладке "Обзор" отображается список заказов, отвечающих критериям запроса.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-141">The Overview tab displays a list of the orders that match the query criteria.</span></span> <span data-ttu-id="c1e2c-142">Эти заказы будут включены в подтверждение.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-142">These will be included in the confirmation.</span></span>  
    * <span data-ttu-id="c1e2c-143">Поле "Суммарная обработка для" задает параметр, по которому несколько заказов должны объединяться в один документ подтверждения.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-143">The Summary update for field specifies the parameter by which multiple orders are to be summarized into one confirmation document.</span></span> <span data-ttu-id="c1e2c-144">По умолчанию этот параметр копируется из значений, заданных по умолчанию для суммарной обработки на странице "Параметры модуля расчетов с клиентами".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-144">By default, the option is copied from the Default values for summary update setting on the Accounts receivable parameters page.</span></span>  
7. <span data-ttu-id="c1e2c-145">В поле "Суммарная обработка для" выберите "Заказ".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-145">In the Summary update for field, select 'Order'.</span></span>
    * <span data-ttu-id="c1e2c-146">Минимальные параметры, необходимые для создания суммарных обработок, — это "Счет накладной" и "Валюта".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-146">The minimum parameters that are required to create summary updates are Invoice account and Currency.</span></span> <span data-ttu-id="c1e2c-147">Это означает, что суммарные обработки с разными счетами накладных и разными валютами не допускаются.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-147">This means that summary updates that have different invoice accounts and different currencies are not allowed.</span></span> <span data-ttu-id="c1e2c-148">Дополнительные параметры можно настроить на странице "Параметры суммарной обработки", которая доступна со страницы "Параметры модуля расчетов с клиентами".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-148">Additional parameters can be set up in the Summary update parameters page which is accessible from the Accounts receivable parameters page.</span></span>  
8. <span data-ttu-id="c1e2c-149">В поле "Заказ на продажу" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-149">In the Sales order field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="c1e2c-150">В списке выберите номер заказа на продажу, который должен стать суммарным заказом.</span><span class="sxs-lookup"><span data-stu-id="c1e2c-150">In the list, select the order number that you want to be the summary order.</span></span>
10. <span data-ttu-id="c1e2c-151">Щелкните "Упорядочить".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-151">Click Arrange.</span></span>
11. <span data-ttu-id="c1e2c-152">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-152">Click OK.</span></span>
12. <span data-ttu-id="c1e2c-153">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c1e2c-153">Click OK.</span></span>

