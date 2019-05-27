---
title: Создание заявки, которая использует запрос предложения
description: В этом руководстве показано, как добавить сведения о цене и поставщике в заявку на покупку из процесса запроса предложения.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a9418b526f992008086f10ce78e95cb682bc164
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547410"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="d6e2f-103">Создание заявки, которая использует запрос предложения</span><span class="sxs-lookup"><span data-stu-id="d6e2f-103">Create a requisition that uses an RFQ</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d6e2f-104">В этом руководстве показано, как добавить сведения о цене и поставщике в заявку на покупку из процесса запроса предложения.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-104">This guide shows how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="d6e2f-105">Пример, представленный в этом руководстве, можно использовать в компании с демонстрационными данными USMF, при этом вы должны выполнить вход в систему как администратор, чтобы завершить выполнение всех шагов.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="d6e2f-106">Задачи в этом руководстве обычно выполняются специалистами по закупкам.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="d6e2f-107">Создание заявки</span><span class="sxs-lookup"><span data-stu-id="d6e2f-107">Create a requisition</span></span>
1. <span data-ttu-id="d6e2f-108">Перейдите в раздел "Закупки и источники" > "Заявки на закупку" > "Заявки на покупку, подготовленные мной".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-108">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="d6e2f-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-109">Click New.</span></span>
3. <span data-ttu-id="d6e2f-110">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="d6e2f-111">В поле "Запрошенная дата" введите дату.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-111">In the Requested date field, enter a date.</span></span>
5. <span data-ttu-id="d6e2f-112">В поле "Дата учета" введите дату.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-112">In the Accounting date field, enter a date.</span></span>
6. <span data-ttu-id="d6e2f-113">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-113">Click OK.</span></span>
7. <span data-ttu-id="d6e2f-114">В поле "Причина" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-114">In the Reason field, enter or select a value.</span></span>
8. <span data-ttu-id="d6e2f-115">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-115">Click Add line.</span></span>
9. <span data-ttu-id="d6e2f-116">В поле "Категория закупаемой продукции " выберите категорию в дереве и нажмите кнопку ОК.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-116">In the Procurement category field, select a category in the tree, and then click OK.</span></span>
10. <span data-ttu-id="d6e2f-117">В поле "Имя продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-117">In the Product name field, type a value.</span></span>
11. <span data-ttu-id="d6e2f-118">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="d6e2f-119">В поле "Единица измерения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-119">In the Unit field, enter or select a value.</span></span>
13. <span data-ttu-id="d6e2f-120">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-120">Click Save.</span></span>
14. <span data-ttu-id="d6e2f-121">Щелкните "Документооборот", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-121">Click Workflow to open the drop dialog.</span></span>
15. <span data-ttu-id="d6e2f-122">Щелкните Отправить.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-122">Click Submit.</span></span>
16. <span data-ttu-id="d6e2f-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-123">Close the page.</span></span>
17. <span data-ttu-id="d6e2f-124">Щелкните Отправить.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-124">Click Submit.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="d6e2f-125">Повторное назначение задачи workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="d6e2f-125">Reassign a workflow task</span></span>
    * <span data-ttu-id="d6e2f-126">Следующая задача — создание запроса предложения для получения предложений от поставщиков относительно продукта.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="d6e2f-127">В компании с демонстрационными данными USMF workflow-процесс заявки настроен с правилом, согласно которому, если поставщик не выбран или цена за единицу равна 0 для строки, задача назначается определенному работнику для создания запроса предложения.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="d6e2f-128">Для продолжения выполнения этого руководства необходимо повторно назначить эту задачу другому пользователю (самостоятельно).</span><span class="sxs-lookup"><span data-stu-id="d6e2f-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="d6e2f-129">Это можно сделать, только если вы выполнили вход в систему как администратор.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-129">You can only do this if you are logged in as an Admin.</span></span>  
1. <span data-ttu-id="d6e2f-130">Щелкните "Документооборот", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-130">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="d6e2f-131">Щелкните "Просмотр истории".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-131">Click View history.</span></span>
3. <span data-ttu-id="d6e2f-132">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-132">Refresh the page.</span></span>
4. <span data-ttu-id="d6e2f-133">Разверните раздел "Отслеживание сведений".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-133">Expand the Tracking details section.</span></span>
5. <span data-ttu-id="d6e2f-134">В дереве выберите строку, которая начинается со слов "Workflow-процесс строки активирован для".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-134">In the tree, select 'the line that starts with “Line workflow activated on”'.</span></span>
6. <span data-ttu-id="d6e2f-135">Щелкните "Просмотреть сведения о workflow-процессе".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-135">Click View workflow details.</span></span>
7. <span data-ttu-id="d6e2f-136">Разверните раздел "Рабочие элементы".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-136">Expand the Work items section.</span></span>
8. <span data-ttu-id="d6e2f-137">Щелкните "Назначить повторно".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-137">Click Reassign.</span></span>
9. <span data-ttu-id="d6e2f-138">В поле "Пользователь" выберите "Администратор".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-138">In the User field, select Admin.</span></span>
10. <span data-ttu-id="d6e2f-139">Щелкните "Назначить повторно".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-139">Click Reassign.</span></span>
11. <span data-ttu-id="d6e2f-140">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-140">Close the page.</span></span>
12. <span data-ttu-id="d6e2f-141">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-141">Close the page.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="d6e2f-142">Создание запроса предложения</span><span class="sxs-lookup"><span data-stu-id="d6e2f-142">Create an RFQ</span></span>
1. <span data-ttu-id="d6e2f-143">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-143">Refresh the page.</span></span>
2. <span data-ttu-id="d6e2f-144">Щелкните "Запрос предложения".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-144">Click Request for quotation.</span></span>
3. <span data-ttu-id="d6e2f-145">В поле "Юридическое лицо-покупатель" выберите USMF.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-145">In the Buying legal entity field, select USMF.</span></span>
    * <span data-ttu-id="d6e2f-146">Следует выбрать то же юридическое лицо, которое выбрано в строке заявки.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-146">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="d6e2f-147">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-147">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d6e2f-148">При наличии нескольких строк в заявке на покупку выберите все строки, которые следует добавить в запрос предложения.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-148">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="d6e2f-149">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-149">Click OK.</span></span>
6. <span data-ttu-id="d6e2f-150">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-150">Refresh the page.</span></span>
7. <span data-ttu-id="d6e2f-151">Откройте информационное поле и разверните раздел "Связанные документы".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-151">Open the FactBox and then expand the Related documents section.</span></span>
    * <span data-ttu-id="d6e2f-152">Возможно, информационное поле уже открыто.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-152">You may already have the FactBox open.</span></span> <span data-ttu-id="d6e2f-153">Найдите значок со стрелкой справа от переключателей "Строки/заголовок".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-153">Look for the icon with an arrow on it, to the right of the Lines/Header toggle buttons.</span></span> <span data-ttu-id="d6e2f-154">Если стрелка указывает направо, информационное поле уже открыто.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-154">If the arrow is pointing to the right, the FactBox is already open.</span></span> <span data-ttu-id="d6e2f-155">Если стрелка указывает налево, щелкните ее, чтобы открыть информационное поле.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-155">If the arrow points to the left, click it to open the FactBox.</span></span>  
8. <span data-ttu-id="d6e2f-156">Перейдите по ссылке в поле "Запрос предложения", чтобы открыть созданный запрос предложения.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-156">Click the link in the Request for quotation field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="d6e2f-157">Щелкните "Заголовок".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-157">Click Header.</span></span>
10. <span data-ttu-id="d6e2f-158">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-158">Click Add.</span></span>
11. <span data-ttu-id="d6e2f-159">В поле "Счет поставщика" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-159">In the Vendor account field, enter or select a value.</span></span>
12. <span data-ttu-id="d6e2f-160">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-160">Click Add.</span></span>
13. <span data-ttu-id="d6e2f-161">В поле "Счет поставщика" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-161">In the Vendor account field, enter or select a value.</span></span>
14. <span data-ttu-id="d6e2f-162">Нажмите кнопку Отправить.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-162">Click Send.</span></span>
15. <span data-ttu-id="d6e2f-163">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-163">Click OK.</span></span>
16. <span data-ttu-id="d6e2f-164">Щелкните "Введите ответ".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-164">Click Enter reply.</span></span>
17. <span data-ttu-id="d6e2f-165">В области действий щелкните "Ответ".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-165">On the Action Pane, click Reply.</span></span>
18. <span data-ttu-id="d6e2f-166">Щелкните "Копировать данные в ответ".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-166">Click Copy data to reply.</span></span>
    * <span data-ttu-id="d6e2f-167">В результате будут скопированы данные, такие как количество и даты, из запроса предложения в ответ.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-167">This copies data, such as the quantity and dates, from the RFQ to the reply .</span></span>  
19. <span data-ttu-id="d6e2f-168">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-168">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="d6e2f-169">Это цена, что полученная от поставщика.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-169">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="d6e2f-170">Может также потребоваться ввести дополнительную информацию от поставщика.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-170">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="d6e2f-171">Щелкните "Принять".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-171">Click Accept.</span></span>
21. <span data-ttu-id="d6e2f-172">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-172">Click OK.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="d6e2f-173">Проверьте, что цена и поставщик были перенесены в заявку.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-173">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="d6e2f-174">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-174">Close the page.</span></span>
2. <span data-ttu-id="d6e2f-175">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-175">Click Lines.</span></span>
3. <span data-ttu-id="d6e2f-176">Щелкните "Связанные сведения".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-176">Click Related information.</span></span>
4. <span data-ttu-id="d6e2f-177">Щелкните "Заявка на покупку".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-177">Click Purchase requisition.</span></span>
5. <span data-ttu-id="d6e2f-178">Выберите строку, которая была перенесена в запрос предложения.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-178">Select the line that was transferred to the RFQ.</span></span>
    * <span data-ttu-id="d6e2f-179">Проверьте, что цена и поставщик были скопированы в заявку.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-179">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="d6e2f-180">Щелкните "Документооборот", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-180">Click Workflow to open the drop dialog.</span></span>
7. <span data-ttu-id="d6e2f-181">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-181">Click Complete.</span></span>
8. <span data-ttu-id="d6e2f-182">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d6e2f-182">Close the page.</span></span>
9. <span data-ttu-id="d6e2f-183">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="d6e2f-183">Click Complete.</span></span>

