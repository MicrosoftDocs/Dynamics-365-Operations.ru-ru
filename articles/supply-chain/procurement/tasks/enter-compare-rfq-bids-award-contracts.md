--- 
title: "Ввод и сравнение предложений по запросу предложения и заключение контрактов"
description: "В этой процедуре показано, как ввести ответы на запрос предложения, поставить оценку и сравнить предложения, а затем присудить предложение одному из поставщиков."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTableListPage, PurchRFQCaseTable, PurchRFQReplyTable, PurchRFQCompare, PurchRFQEditLines, PurchRFQEditLinesParameters, PurchTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 7cd4876acfebcc9595abb358cfc9b355e93041d6
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a><span data-ttu-id="09f59-103">Ввод и сравнение предложений по запросу предложения и заключение контрактов</span><span class="sxs-lookup"><span data-stu-id="09f59-103">Enter and compare RFQ bids, and award contracts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="09f59-104">В этой процедуре показано, как ввести ответы на запрос предложения, поставить оценку и сравнить предложения, а затем присудить предложение одному из поставщиков.</span><span class="sxs-lookup"><span data-stu-id="09f59-104">This procedure shows you how to enter replies to an RFQ, score and compare bids, and then award the bid to one of the vendors.</span></span> <span data-ttu-id="09f59-105">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="09f59-105">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="09f59-106">Перед началом работы необходимо иметь запрос предложения с двумя строками, которое было отправлено хотя бы двум поставщикам.</span><span class="sxs-lookup"><span data-stu-id="09f59-106">Before you start, you must have an RFQ with two lines that has been sent to at least two vendors.</span></span> <span data-ttu-id="09f59-107">Можно выполнить процедуру "Создание запроса предложения" как необходимое условие для их создания.</span><span class="sxs-lookup"><span data-stu-id="09f59-107">You can run the "Create a request for quotation" procedure as a prerequisite to create this.</span></span> <span data-ttu-id="09f59-108">Перед выполнением этой процедуры необходимо настроить критерии оценки.</span><span class="sxs-lookup"><span data-stu-id="09f59-108">You need to have set up scoring criteria before you can run this procedure.</span></span>


## <a name="enter-a-reply-from-a-vendor"></a><span data-ttu-id="09f59-109">Ввод ответа поставщика</span><span class="sxs-lookup"><span data-stu-id="09f59-109">Enter a reply from a vendor</span></span>
1. <span data-ttu-id="09f59-110">Перейдите в раздел "Закупки и источники" > "Запросы предложений" > "Все запросы предложений".</span><span class="sxs-lookup"><span data-stu-id="09f59-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="09f59-111">Выберите запрос предложения со статусом "Отправлено" и перейдите по ссылке в номере обращения "Запрос предложения".</span><span class="sxs-lookup"><span data-stu-id="09f59-111">Select an RFQ that has a status of Sent and click the link on the Request for quotation case number.</span></span>
    * <span data-ttu-id="09f59-112">Запрос предложения необходимо было отправить хотя бы 2 поставщикам.</span><span class="sxs-lookup"><span data-stu-id="09f59-112">The RFQ should have been sent to at least 2 vendors.</span></span>  
3. <span data-ttu-id="09f59-113">Щелкните заголовок, чтобы перейти к списку поставщиков.</span><span class="sxs-lookup"><span data-stu-id="09f59-113">Click Header to go to the list of vendors.</span></span>
4. <span data-ttu-id="09f59-114">Выберите поставщика, для которого требуется ввести ответ на запрос предложения.</span><span class="sxs-lookup"><span data-stu-id="09f59-114">Select the vendor for whom you want to enter a response on the RFQ.</span></span>
5. <span data-ttu-id="09f59-115">Щелкните "Введите ответ".</span><span class="sxs-lookup"><span data-stu-id="09f59-115">Click Enter reply.</span></span>
6. <span data-ttu-id="09f59-116">В области действий щелкните "Ответ".</span><span class="sxs-lookup"><span data-stu-id="09f59-116">On the Action Pane, click Reply.</span></span>
7. <span data-ttu-id="09f59-117">Щелкните "Копировать данные в ответ".</span><span class="sxs-lookup"><span data-stu-id="09f59-117">Click Copy data to reply.</span></span>
    * <span data-ttu-id="09f59-118">В результате этого действия будут скопированы выбранные данные, например количество из обращения по запросу предложения в ответ на запрос предложения.</span><span class="sxs-lookup"><span data-stu-id="09f59-118">This action will copy selected data, for example, the quantity from the RFQ case to the RFQ reply.</span></span> <span data-ttu-id="09f59-119">Либо можно пропустить это действие и заполнить все поля ответа вручную при изменении ответа.</span><span class="sxs-lookup"><span data-stu-id="09f59-119">Alternatively you can skip this action and fill in all the response fields manually when you edit the reply.</span></span>  
8. <span data-ttu-id="09f59-120">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="09f59-120">Click Edit.</span></span>
9. <span data-ttu-id="09f59-121">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="09f59-121">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="09f59-122">Выберите другую строку предложения.</span><span class="sxs-lookup"><span data-stu-id="09f59-122">Choose the other quotation line.</span></span>
11. <span data-ttu-id="09f59-123">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="09f59-123">In the Unit price field, enter a number.</span></span>

## <a name="score-the-bid"></a><span data-ttu-id="09f59-124">Оценка предложения</span><span class="sxs-lookup"><span data-stu-id="09f59-124">Score the bid</span></span>
1. <span data-ttu-id="09f59-125">Щелкните заголовок, чтобы перейти к оценке предложения.</span><span class="sxs-lookup"><span data-stu-id="09f59-125">Click Header to go to the scoring of the bid.</span></span>
2. <span data-ttu-id="09f59-126">Разверните раздел "Оценка предложения".</span><span class="sxs-lookup"><span data-stu-id="09f59-126">Expand the Bid scoring section.</span></span>
3. <span data-ttu-id="09f59-127">В поле "Оценка" введите число для одного из критериев оценки.</span><span class="sxs-lookup"><span data-stu-id="09f59-127">In the Score field, enter a number for one of the scoring criteria.</span></span>
    * <span data-ttu-id="09f59-128">При наведении указателя мыши на один из критериев оценки отобразится подсказка с диапазоном оценки.</span><span class="sxs-lookup"><span data-stu-id="09f59-128">If you hover over one of the scoring criteria a tooltip shows the range that you have to score within.</span></span> <span data-ttu-id="09f59-129">В этой демонстрации можно добавить число от 1 до 5 к любым критериям.</span><span class="sxs-lookup"><span data-stu-id="09f59-129">In this demo you can add a number between 1 and 5 to any of the criteria.</span></span>  
4. <span data-ttu-id="09f59-130">Выберите другой критерий оценки.</span><span class="sxs-lookup"><span data-stu-id="09f59-130">Select another scoring criterion.</span></span>
5. <span data-ttu-id="09f59-131">В поле "Оценка" введите число.</span><span class="sxs-lookup"><span data-stu-id="09f59-131">In the Score field, enter a number.</span></span>
6. <span data-ttu-id="09f59-132">Разверните раздел "Анкеты".</span><span class="sxs-lookup"><span data-stu-id="09f59-132">Expand the Questionnaires section.</span></span>
    * <span data-ttu-id="09f59-133">Если обращение по запросу предложения содержит анкету, которая была отправлена поставщикам, можно ввести их ответы в разделе анкеты.</span><span class="sxs-lookup"><span data-stu-id="09f59-133">If the RFQ case has a questionnaire that was sent to the vendors, you can enter their responses in the questionnaire section.</span></span>  
7. <span data-ttu-id="09f59-134">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="09f59-134">Close the page.</span></span>

## <a name="enter-a-reply-for-another-vendor"></a><span data-ttu-id="09f59-135">Ввод ответа для другого поставщика</span><span class="sxs-lookup"><span data-stu-id="09f59-135">Enter a reply for another vendor</span></span>
1. <span data-ttu-id="09f59-136">Выберите следующего поставщика, очистив поставщика, для которого только что был введен ответ, а затем выберите строку для следующего поставщика.</span><span class="sxs-lookup"><span data-stu-id="09f59-136">Select the next vendor by clearing the vendor you have just entered the reply for and then selecting the row for the next vendor.</span></span>
2. <span data-ttu-id="09f59-137">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="09f59-137">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="09f59-138">Щелкните "Введите ответ".</span><span class="sxs-lookup"><span data-stu-id="09f59-138">Click Enter reply.</span></span>
4. <span data-ttu-id="09f59-139">Щелкните "Копировать данные в ответ".</span><span class="sxs-lookup"><span data-stu-id="09f59-139">Click Copy data to reply.</span></span>
5. <span data-ttu-id="09f59-140">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="09f59-140">Click Edit.</span></span>
6. <span data-ttu-id="09f59-141">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="09f59-141">In the Unit price field, enter a number.</span></span>
7. <span data-ttu-id="09f59-142">Выберите другую строку предложения.</span><span class="sxs-lookup"><span data-stu-id="09f59-142">Choose the other quotation line.</span></span>
8. <span data-ttu-id="09f59-143">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="09f59-143">In the Unit price field, enter a number.</span></span>

## <a name="score-the-second-bid"></a><span data-ttu-id="09f59-144">Оценка второго предложения</span><span class="sxs-lookup"><span data-stu-id="09f59-144">Score the second bid</span></span>
1. <span data-ttu-id="09f59-145">Щелкните заголовок, чтобы перейти к оценке предложения.</span><span class="sxs-lookup"><span data-stu-id="09f59-145">Click Header to go to scoring of the bid.</span></span>
2. <span data-ttu-id="09f59-146">В поле "Оценка" введите число.</span><span class="sxs-lookup"><span data-stu-id="09f59-146">In the Score field, enter a number.</span></span>
3. <span data-ttu-id="09f59-147">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="09f59-147">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="09f59-148">В поле "Оценка" введите число.</span><span class="sxs-lookup"><span data-stu-id="09f59-148">In the Score field, enter a number.</span></span>

## <a name="compare-the-replies"></a><span data-ttu-id="09f59-149">Сравнить ответы</span><span class="sxs-lookup"><span data-stu-id="09f59-149">Compare the replies</span></span>
1. <span data-ttu-id="09f59-150">В области действий щелкните "Общие".</span><span class="sxs-lookup"><span data-stu-id="09f59-150">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="09f59-151">Щелкните "Сравнить ответы".</span><span class="sxs-lookup"><span data-stu-id="09f59-151">Click Compare replies.</span></span>
3. <span data-ttu-id="09f59-152">В поле "Ранг" введите число.</span><span class="sxs-lookup"><span data-stu-id="09f59-152">In the Rank field, enter a number.</span></span>
    * <span data-ttu-id="09f59-153">На этой странице отображаются предложения с заголовком и строками, а также общая оценка на уровне заголовка.</span><span class="sxs-lookup"><span data-stu-id="09f59-153">This page shows the bids with the header and lines, and the total score on the header level.</span></span> <span data-ttu-id="09f59-154">Вы можете сравнить строки, отсортировав их в сетке так, чтобы соответствующие строки располагались рядом друг с другом.</span><span class="sxs-lookup"><span data-stu-id="09f59-154">You can compare the lines by sorting in the grid so that comparable lines are next to each other.</span></span> <span data-ttu-id="09f59-155">Информация также включает:    Количество — количество, указанное поставщиком.</span><span class="sxs-lookup"><span data-stu-id="09f59-155">The information also includes:   Quantity: The quantity quoted by the vendor.</span></span> <span data-ttu-id="09f59-156">Это количество может не совпадать с количеством, указанным в запросе предложения.</span><span class="sxs-lookup"><span data-stu-id="09f59-156">This might not equal the quantity specified in the RFQ.</span></span>   <span data-ttu-id="09f59-157">Чистая сумма — цена, указанная поставщиком после вычета всех скидок, для элементов строки.</span><span class="sxs-lookup"><span data-stu-id="09f59-157">Net amount: The price quoted by a vendor, after subtracting any discounts, for the items on the line.</span></span>   <span data-ttu-id="09f59-158">Отклонение — количество дней, на которое дата поставки в строке или заголовке предложения отличается от запрошенной даты поставки, указанной в строке или заголовке запроса предложения.</span><span class="sxs-lookup"><span data-stu-id="09f59-158">Deviation: The number of days that the delivery date in the bid header or line deviates from the requested delivery date in the RFQ header or RFQ line.</span></span>   <span data-ttu-id="09f59-159">Можно ввести ранг для каждого предложения.</span><span class="sxs-lookup"><span data-stu-id="09f59-159">You can enter a rank for each bid.</span></span>  
4. <span data-ttu-id="09f59-160">Выберите строку заголовка для другого предложения, которое требуется ранжировать.</span><span class="sxs-lookup"><span data-stu-id="09f59-160">Select the header line for the other bid that you want to rank.</span></span>
5. <span data-ttu-id="09f59-161">В поле "Ранг" введите число.</span><span class="sxs-lookup"><span data-stu-id="09f59-161">In the Rank field, enter a number.</span></span>
6. <span data-ttu-id="09f59-162">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="09f59-162">Click Save.</span></span>

## <a name="reject-a-bid"></a><span data-ttu-id="09f59-163">Отклонить предложение</span><span class="sxs-lookup"><span data-stu-id="09f59-163">Reject a bid</span></span>
1. <span data-ttu-id="09f59-164">Выберите строку заголовка для предложения, которое требуется отклонить.</span><span class="sxs-lookup"><span data-stu-id="09f59-164">Select the header line for the bid that you want to reject.</span></span>
    * <span data-ttu-id="09f59-165">Одновременно можно принять, отклонить или вернуть только одно предложение или строки в пределах одного предложения.</span><span class="sxs-lookup"><span data-stu-id="09f59-165">You can only accept, reject, or return one bid or lines within one bid at a time.</span></span>  
2. <span data-ttu-id="09f59-166">Установите флажок "Пометка".</span><span class="sxs-lookup"><span data-stu-id="09f59-166">Select the Mark check box.</span></span>
    * <span data-ttu-id="09f59-167">Если установить флажок "Пометить" в заголовке предложения, также будут помечены все строки.</span><span class="sxs-lookup"><span data-stu-id="09f59-167">If you select the Mark check box on the Header of the bid then all the lines will be marked as well.</span></span> <span data-ttu-id="09f59-168">Также можно пометить подмножество строк в пределах предложения, чтобы отклонить или принять их.</span><span class="sxs-lookup"><span data-stu-id="09f59-168">You could also choose to mark a subset of the lines within the bid to reject or accept those.</span></span> <span data-ttu-id="09f59-169">Можно принять одно предложение поставщика для определенных строк запроса предложения, а затем передать другие строки запроса предложения другому поставщику. Однако это необходимо выполнить за 2 шага, одно предложение за раз.</span><span class="sxs-lookup"><span data-stu-id="09f59-169">It’s possible to accept one vendor’s bid for some lines of an RFQ, and then award other RFQ lines to a different vendor, however you need to do this in 2 steps, one bid at a time.</span></span> <span data-ttu-id="09f59-170">Если присутствуют альтернативные строки, можно принять только исходную строку предложения или только альтернативные строки, но не оба типа строк одновременно.</span><span class="sxs-lookup"><span data-stu-id="09f59-170">If alternate lines are present, you can only accept either the original bid line or its alternate, but not both.</span></span>  
3. <span data-ttu-id="09f59-171">Щелкните "Отклонить".</span><span class="sxs-lookup"><span data-stu-id="09f59-171">Click Reject.</span></span>
4. <span data-ttu-id="09f59-172">Щелкните "Параметры", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="09f59-172">Click Parameters to open the drop dialog.</span></span>
5. <span data-ttu-id="09f59-173">В поле "Причина отклонения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="09f59-173">In the Reason reject field, enter or select a value.</span></span>
    * <span data-ttu-id="09f59-174">Причина отклонения будет сохранена в ответе.</span><span class="sxs-lookup"><span data-stu-id="09f59-174">The reason for rejection will be stored on the reply.</span></span>  
6. <span data-ttu-id="09f59-175">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="09f59-175">Click OK.</span></span>
7. <span data-ttu-id="09f59-176">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="09f59-176">Click OK.</span></span>
8. <span data-ttu-id="09f59-177">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="09f59-177">Close the page.</span></span>
9. <span data-ttu-id="09f59-178">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="09f59-178">Close the page.</span></span>
10. <span data-ttu-id="09f59-179">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="09f59-179">Refresh the page.</span></span>

## <a name="accept-a-bid"></a><span data-ttu-id="09f59-180">Принять предложение</span><span class="sxs-lookup"><span data-stu-id="09f59-180">Accept a bid</span></span>
1. <span data-ttu-id="09f59-181">Выберите предложение, которое требуется принять, и перейдите по ссылке в поле "Запрос предложения".</span><span class="sxs-lookup"><span data-stu-id="09f59-181">Select the bid that you want to accept and then click the link in the Request for quotation field.</span></span>
2. <span data-ttu-id="09f59-182">В области действий щелкните "Ответ".</span><span class="sxs-lookup"><span data-stu-id="09f59-182">On the Action Pane, click Reply.</span></span>
3. <span data-ttu-id="09f59-183">Щелкните "Принять".</span><span class="sxs-lookup"><span data-stu-id="09f59-183">Click Accept.</span></span>
    * <span data-ttu-id="09f59-184">Если имеются помеченные строки, но не другие строки, действие принятия будет содержать только помеченные строки.</span><span class="sxs-lookup"><span data-stu-id="09f59-184">If you have marked specific lines and not others then the accept action will only include the marked lines.</span></span> <span data-ttu-id="09f59-185">Если требуется принять все строки в предложении, не следует помечать строки.</span><span class="sxs-lookup"><span data-stu-id="09f59-185">If you want to accept all lines on the bid then you do not have to mark the lines.</span></span>  
4. <span data-ttu-id="09f59-186">Щелкните "Параметры", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="09f59-186">Click Parameters to open the drop dialog.</span></span>
    * <span data-ttu-id="09f59-187">Это позволяет записать причину принятия заявки.</span><span class="sxs-lookup"><span data-stu-id="09f59-187">This allows you to record a reason for accepting the bid.</span></span> <span data-ttu-id="09f59-188">Причина будет сохранена в предложении.</span><span class="sxs-lookup"><span data-stu-id="09f59-188">The reason will be stored on the bid.</span></span>  
5. <span data-ttu-id="09f59-189">В поле "Причина принятия" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="09f59-189">In the Reason accept field, enter or select a value.</span></span>
6. <span data-ttu-id="09f59-190">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="09f59-190">Click OK.</span></span>
7. <span data-ttu-id="09f59-191">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="09f59-191">Click OK.</span></span>
    * <span data-ttu-id="09f59-192">При нажатии кнопки ОК создается заказ на покупку на основе строк, включенных в принятый запрос предложения.</span><span class="sxs-lookup"><span data-stu-id="09f59-192">When you click OK this generates a purchase order based on the lines that are included in the RFQ acceptance.</span></span> <span data-ttu-id="09f59-193">Если имеются другие предложения, которые не были обработаны (принято, отклонено или возвращено), система выдаст запрос на отклонение оставшихся предложений.</span><span class="sxs-lookup"><span data-stu-id="09f59-193">If there are other bids that have not been processed (accepted, rejected, or returned) then the system will prompt you to reject the remaining bids.</span></span>  

## <a name="view-the-purchase-order-thats-been-generated"></a><span data-ttu-id="09f59-194">Просмотр созданного заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="09f59-194">View the purchase order that's been generated</span></span>
1. <span data-ttu-id="09f59-195">В области действий щелкните "Общие".</span><span class="sxs-lookup"><span data-stu-id="09f59-195">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="09f59-196">Щелкните "Заказ на покупку".</span><span class="sxs-lookup"><span data-stu-id="09f59-196">Click Purchase order.</span></span>
    * <span data-ttu-id="09f59-197">Здесь можно просмотреть заказ на покупку, созданный при принятии предложения.</span><span class="sxs-lookup"><span data-stu-id="09f59-197">Here you can see the purchase order that was generated when you accepted the bid.</span></span>  
3. <span data-ttu-id="09f59-198">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="09f59-198">Close the page.</span></span>
4. <span data-ttu-id="09f59-199">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="09f59-199">Close the page.</span></span>
5. <span data-ttu-id="09f59-200">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="09f59-200">Close the page.</span></span>
6. <span data-ttu-id="09f59-201">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="09f59-201">Close the page.</span></span>


