---
title: Создание заявки, которая использует запрос предложения
description: В этой теме объясняется, как добавить сведения о цене и поставщике в заявку на покупку из процесса запроса предложения.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 205cba2325e76dae9572301e44e0e89cbcfd106e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204708"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="addb9-103">Создание заявки, которая использует запрос предложения</span><span class="sxs-lookup"><span data-stu-id="addb9-103">Create a requisition that uses an RFQ</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="addb9-104">В этой теме объясняется, как добавить сведения о цене и поставщике в заявку на покупку из процесса запроса предложения.</span><span class="sxs-lookup"><span data-stu-id="addb9-104">This topic explains how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="addb9-105">Пример, представленный в этом руководстве, можно использовать в компании с демонстрационными данными USMF, при этом вы должны выполнить вход в систему как администратор, чтобы завершить выполнение всех шагов.</span><span class="sxs-lookup"><span data-stu-id="addb9-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="addb9-106">Задачи в этом руководстве обычно выполняются специалистами по закупкам.</span><span class="sxs-lookup"><span data-stu-id="addb9-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="addb9-107">Создание заявки</span><span class="sxs-lookup"><span data-stu-id="addb9-107">Create a requisition</span></span>
1. <span data-ttu-id="addb9-108">В области переходов выберите **Модули > Закупки и источники > Заявки на закупку > Заявки на покупку, подготовленные мной**.</span><span class="sxs-lookup"><span data-stu-id="addb9-108">In the navigation pane, go to **Modules > Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me**.</span></span>
2. <span data-ttu-id="addb9-109">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="addb9-109">Select **New**.</span></span>
3. <span data-ttu-id="addb9-110">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="addb9-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="addb9-111">В поле **Запрошенная дата** введите дату.</span><span class="sxs-lookup"><span data-stu-id="addb9-111">In the **Requested date** field, enter a date.</span></span>
5. <span data-ttu-id="addb9-112">В поле **Дата учета** введите дату.</span><span class="sxs-lookup"><span data-stu-id="addb9-112">In the **Accounting date** field, enter a date.</span></span>
6. <span data-ttu-id="addb9-113">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="addb9-113">Select **OK**.</span></span>
7. <span data-ttu-id="addb9-114">В поле **Причина** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="addb9-114">In the **Reason** field, enter or select a value.</span></span>
8. <span data-ttu-id="addb9-115">Выберите **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="addb9-115">Select **Add line**.</span></span>
9. <span data-ttu-id="addb9-116">В поле **Категория закупаемой продукции** выберите категорию в дереве и выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="addb9-116">In the **Procurement category** field, select a category in the tree, and then select **OK**.</span></span>
10. <span data-ttu-id="addb9-117">В поле **Имя продукта** введите значение.</span><span class="sxs-lookup"><span data-stu-id="addb9-117">In the **Product name** field, type a value.</span></span>
11. <span data-ttu-id="addb9-118">В поле **Количество** введите число.</span><span class="sxs-lookup"><span data-stu-id="addb9-118">In the **Quantity** field, enter a number.</span></span>
12. <span data-ttu-id="addb9-119">В поле **Единица измерения** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="addb9-119">In the **Unit** field, enter or select a value.</span></span>
13. <span data-ttu-id="addb9-120">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="addb9-120">Select **Save**.</span></span>
14. <span data-ttu-id="addb9-121">Выберите **Документооборот**, чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="addb9-121">Select **Workflow** to open the drop dialog.</span></span>
15. <span data-ttu-id="addb9-122">Выберите **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="addb9-122">Select **Submit**.</span></span>
16. <span data-ttu-id="addb9-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="addb9-123">Close the page.</span></span>
17. <span data-ttu-id="addb9-124">Выберите **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="addb9-124">Select **Submit**.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="addb9-125">Повторное назначение задачи workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="addb9-125">Reassign a workflow task</span></span>
<span data-ttu-id="addb9-126">Следующая задача — создание запроса предложения для получения предложений от поставщиков относительно продукта.</span><span class="sxs-lookup"><span data-stu-id="addb9-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="addb9-127">В компании с демонстрационными данными USMF workflow-процесс заявки настроен с правилом, согласно которому, если поставщик не выбран или цена за единицу равна 0 для строки, задача назначается определенному работнику для создания запроса предложения.</span><span class="sxs-lookup"><span data-stu-id="addb9-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="addb9-128">Для продолжения выполнения этого руководства необходимо повторно назначить эту задачу другому пользователю (самостоятельно).</span><span class="sxs-lookup"><span data-stu-id="addb9-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="addb9-129">Это можно сделать, только если вы выполнили вход в систему как администратор.</span><span class="sxs-lookup"><span data-stu-id="addb9-129">You can only do this if you are logged in as an Admin.</span></span>  

1. <span data-ttu-id="addb9-130">Выберите **Документооборот**, чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="addb9-130">Select **Workflow** to open the drop dialog.</span></span>
2. <span data-ttu-id="addb9-131">Выберите **Просмотр журнала**.</span><span class="sxs-lookup"><span data-stu-id="addb9-131">Select **View history**.</span></span>
3. <span data-ttu-id="addb9-132">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="addb9-132">Refresh the page.</span></span>
4. <span data-ttu-id="addb9-133">Разверните раздел **Отслеживание сведений**.</span><span class="sxs-lookup"><span data-stu-id="addb9-133">Expand the **Tracking details** section.</span></span>
5. <span data-ttu-id="addb9-134">В дереве выберите строку, которая начинается со слов "Рабочий процесс строки активирован для".</span><span class="sxs-lookup"><span data-stu-id="addb9-134">In the tree, select the line that starts with "Line workflow activated on".</span></span>
6. <span data-ttu-id="addb9-135">Выберите **Просмотреть сведения о workflow-процессе**.</span><span class="sxs-lookup"><span data-stu-id="addb9-135">Select **View workflow details**.</span></span>
7. <span data-ttu-id="addb9-136">Разверните раздел **Рабочие элементы**.</span><span class="sxs-lookup"><span data-stu-id="addb9-136">Expand the **Work items** section.</span></span>
8. <span data-ttu-id="addb9-137">Выберите **Назначить повторно**.</span><span class="sxs-lookup"><span data-stu-id="addb9-137">Select **Reassign**.</span></span>
9. <span data-ttu-id="addb9-138">В поле **Пользователь** выберите **Администратор**.</span><span class="sxs-lookup"><span data-stu-id="addb9-138">In the **User** field, select **Admin**.</span></span>
10. <span data-ttu-id="addb9-139">Выберите **Назначить повторно**.</span><span class="sxs-lookup"><span data-stu-id="addb9-139">Select **Reassign**.</span></span>
11. <span data-ttu-id="addb9-140">Закройте две страницы.</span><span class="sxs-lookup"><span data-stu-id="addb9-140">Close the two pages.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="addb9-141">Создание запроса предложения</span><span class="sxs-lookup"><span data-stu-id="addb9-141">Create an RFQ</span></span>

1. <span data-ttu-id="addb9-142">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="addb9-142">Refresh the page.</span></span>
2. <span data-ttu-id="addb9-143">Выберите **Запрос предложения**.</span><span class="sxs-lookup"><span data-stu-id="addb9-143">Select **Request for quotation**.</span></span>
3. <span data-ttu-id="addb9-144">В поле **Юридическое лицо-покупатель** выберите **USMF**.</span><span class="sxs-lookup"><span data-stu-id="addb9-144">In the **Buying legal entity** field, select **USMF**.</span></span> <span data-ttu-id="addb9-145">Следует выбрать то же юридическое лицо, которое выбрано в строке заявки.</span><span class="sxs-lookup"><span data-stu-id="addb9-145">You must select the same legal entity that's on the requisition line.</span></span>  
4. <span data-ttu-id="addb9-146">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="addb9-146">In the list, mark the selected row.</span></span> <span data-ttu-id="addb9-147">При наличии нескольких строк в заявке на покупку выберите все строки, которые следует добавить в запрос предложения.</span><span class="sxs-lookup"><span data-stu-id="addb9-147">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="addb9-148">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="addb9-148">Select **OK**.</span></span>
6. <span data-ttu-id="addb9-149">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="addb9-149">Refresh the page.</span></span>
7. <span data-ttu-id="addb9-150">Убедитесь, что открыто информационное поле, затем разверните раздел **Связанные документы**.</span><span class="sxs-lookup"><span data-stu-id="addb9-150">Ensure that the FactBox is open, then expand the **Related documents** section.</span></span>
8. <span data-ttu-id="addb9-151">Выберите ссылку в поле **Запрос предложения**, чтобы открыть созданный запрос предложения.</span><span class="sxs-lookup"><span data-stu-id="addb9-151">Select the link in the **Request for quotation** field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="addb9-152">Выберите **Заголовок**.</span><span class="sxs-lookup"><span data-stu-id="addb9-152">Select **Header**.</span></span>
10. <span data-ttu-id="addb9-153">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="addb9-153">Select **Add**.</span></span>
11. <span data-ttu-id="addb9-154">В поле **Счет поставщика** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="addb9-154">In the **Vendor account** field, enter or select a value.</span></span>
12. <span data-ttu-id="addb9-155">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="addb9-155">Select **Add**.</span></span>
13. <span data-ttu-id="addb9-156">В поле **Счет поставщика** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="addb9-156">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="addb9-157">Выберите **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="addb9-157">Select **Send**.</span></span>
15. <span data-ttu-id="addb9-158">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="addb9-158">Select **OK**.</span></span>
16. <span data-ttu-id="addb9-159">Выберите **Введите ответ**.</span><span class="sxs-lookup"><span data-stu-id="addb9-159">Select **Enter reply**.</span></span>
17. <span data-ttu-id="addb9-160">В области действий выберите **Ответ**.</span><span class="sxs-lookup"><span data-stu-id="addb9-160">On the Action Pane, select **Reply**.</span></span>
18. <span data-ttu-id="addb9-161">Выберите **Копировать данные в ответ**.</span><span class="sxs-lookup"><span data-stu-id="addb9-161">Select **Copy data to reply**.</span></span> <span data-ttu-id="addb9-162">В результате будут скопированы данные, такие как количество и даты, из запроса предложения в ответ.</span><span class="sxs-lookup"><span data-stu-id="addb9-162">This copies data, such as the quantity and dates, from the RFQ to the reply.</span></span>  
19. <span data-ttu-id="addb9-163">В поле **Цена за единицу** введите число.</span><span class="sxs-lookup"><span data-stu-id="addb9-163">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="addb9-164">Это цена, что полученная от поставщика.</span><span class="sxs-lookup"><span data-stu-id="addb9-164">This is the price that you've received from the vendor.</span></span> <span data-ttu-id="addb9-165">Может также потребоваться ввести дополнительную информацию от поставщика.</span><span class="sxs-lookup"><span data-stu-id="addb9-165">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="addb9-166">Выберите **Принять**.</span><span class="sxs-lookup"><span data-stu-id="addb9-166">Select **Accept**.</span></span>
21. <span data-ttu-id="addb9-167">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="addb9-167">Select **OK**.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="addb9-168">Проверьте, что цена и поставщик были перенесены в заявку.</span><span class="sxs-lookup"><span data-stu-id="addb9-168">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="addb9-169">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="addb9-169">Close the page.</span></span>
2. <span data-ttu-id="addb9-170">Выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="addb9-170">Select **Lines**.</span></span>
3. <span data-ttu-id="addb9-171">Выберите **Связанные сведения**.</span><span class="sxs-lookup"><span data-stu-id="addb9-171">Select **Related information**.</span></span>
4. <span data-ttu-id="addb9-172">Выберите **Заявка на покупку**.</span><span class="sxs-lookup"><span data-stu-id="addb9-172">Select **Purchase requisition**.</span></span>
5. <span data-ttu-id="addb9-173">Выберите строку, которая была перенесена в запрос предложения.</span><span class="sxs-lookup"><span data-stu-id="addb9-173">Select the line that was transferred to the RFQ.</span></span> <span data-ttu-id="addb9-174">Проверьте, что цена и поставщик были скопированы в заявку.</span><span class="sxs-lookup"><span data-stu-id="addb9-174">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="addb9-175">Выберите **Документооборот**, чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="addb9-175">Select **Workflow** to open the drop dialog.</span></span>
7. <span data-ttu-id="addb9-176">Выберите "Завершить".</span><span class="sxs-lookup"><span data-stu-id="addb9-176">Select Complete.</span></span>
8. <span data-ttu-id="addb9-177">Выберите страницу.</span><span class="sxs-lookup"><span data-stu-id="addb9-177">Select the page.</span></span>
9. <span data-ttu-id="addb9-178">Выберите "Завершить".</span><span class="sxs-lookup"><span data-stu-id="addb9-178">Select Complete.</span></span>

