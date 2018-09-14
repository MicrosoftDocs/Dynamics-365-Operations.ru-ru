--- 
title: "Выполнение договоров продажи"
description: "Эта процедура описывает, как выполнить договор продажи, связав с ним заказы на продажу."
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: f03f05b85b8d242db1c85d0e84667949e241f1f7
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="fulfill-sales-agreements"></a><span data-ttu-id="9fcec-103">Выполнение договоров продажи</span><span class="sxs-lookup"><span data-stu-id="9fcec-103">Fulfill sales agreements</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9fcec-104">Эта процедура описывает, как выполнить договор продажи, связав с ним заказы на продажу.</span><span class="sxs-lookup"><span data-stu-id="9fcec-104">This procedure shows you how to fulfill a sales agreement by associating sales orders with it.</span></span> <span data-ttu-id="9fcec-105">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="9fcec-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="9fcec-106">Перед началом этого руководства убедитесь, что у вас есть действующий договор продажи типа "Обязательство по стоимости продукта".</span><span class="sxs-lookup"><span data-stu-id="9fcec-106">Before starting this guide, make sure you have an effective sales agreement of type "Product value commitment".</span></span> <span data-ttu-id="9fcec-107">Или же можно выполнить руководство по задаче "Создание договоров продажи".</span><span class="sxs-lookup"><span data-stu-id="9fcec-107">Alternatively, you can run the task guide called "Create sales agreements".</span></span>  




## <a name="release-a-sales-order-from-the-agreement"></a><span data-ttu-id="9fcec-108">Запуск заказа на продажу в производство из договора</span><span class="sxs-lookup"><span data-stu-id="9fcec-108">Release a sales order from the agreement</span></span>
1. <span data-ttu-id="9fcec-109">Перейдите в раздел "Продажи и маркетинг" > "Договоры продажи" > "Договоры продажи".</span><span class="sxs-lookup"><span data-stu-id="9fcec-109">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="9fcec-110">В списке откройте договор, по которому требуется запустить в производство заказ.</span><span class="sxs-lookup"><span data-stu-id="9fcec-110">In the list, open the agreement against which you want to release the order.</span></span>
3. <span data-ttu-id="9fcec-111">В области действий щелкните "Договор продажи".</span><span class="sxs-lookup"><span data-stu-id="9fcec-111">On the Action Pane, click Sales agreement.</span></span>
4. <span data-ttu-id="9fcec-112">Щелкните "Заказ на запуск в производство".</span><span class="sxs-lookup"><span data-stu-id="9fcec-112">Click Release order.</span></span>
    * <span data-ttu-id="9fcec-113">Согласно тексту в верхней части страницы "Создать заказ на запуск в производство", сведения, необходимые для строк заказа на продажу, будут отличаться в зависимости того, на чем основано соглашение: количество или стоимость.</span><span class="sxs-lookup"><span data-stu-id="9fcec-113">As the text on top of the  Create release order page points out, the details required for the sales order lines will differ depending on whether the agreement is quantity- or value-based.</span></span>  
    * <span data-ttu-id="9fcec-114">Соглашение в этом руководстве имеет тип "Обязательство по стоимости продукта".</span><span class="sxs-lookup"><span data-stu-id="9fcec-114">The agreement in this guide is of type "Product value commitment".</span></span> <span data-ttu-id="9fcec-115">Именно поэтому раздел "Строки" на этой странице не заполнен.</span><span class="sxs-lookup"><span data-stu-id="9fcec-115">This is why the Lines section of this page is blank.</span></span> <span data-ttu-id="9fcec-116">Если обязательство было бы основано на количестве, сведения по строкам были бы скопированы из договора.</span><span class="sxs-lookup"><span data-stu-id="9fcec-116">If the commitment was based on quantity, the line information would be copied from the agreement.</span></span>  
5. <span data-ttu-id="9fcec-117">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9fcec-117">Click Create.</span></span>
    * <span data-ttu-id="9fcec-118">Сообщение указывает, что заказ на покупку продажу создан.</span><span class="sxs-lookup"><span data-stu-id="9fcec-118">The message informs you that a sales order has been created.</span></span> <span data-ttu-id="9fcec-119">Поскольку заказ не содержит никаких строк, необходимо добавить данные строк, чтобы завершить процесс выпуска.</span><span class="sxs-lookup"><span data-stu-id="9fcec-119">Since the order does not contain any lines, you must add order line details to complete the release process.</span></span>   
6. <span data-ttu-id="9fcec-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9fcec-120">Close the page.</span></span>
7. <span data-ttu-id="9fcec-121">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9fcec-121">Close the page.</span></span>
8. <span data-ttu-id="9fcec-122">Перейдите в раздел "Продажи и маркетинг" > "Заказы на продажу" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="9fcec-122">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
9. <span data-ttu-id="9fcec-123">В списке найдите и откройте заказ, созданный в результате запуска заказа в производство в предыдущей задаче.</span><span class="sxs-lookup"><span data-stu-id="9fcec-123">In the list, find and open the order that was created as the result of the order release in the previous task.</span></span>
10. <span data-ttu-id="9fcec-124">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="9fcec-124">Click Add line.</span></span>
11. <span data-ttu-id="9fcec-125">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="9fcec-125">In the Item number field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="9fcec-126">В поле "Код номенклатуры" введите или выберите номенклатуру, заданную в связанном договоре продажи.</span><span class="sxs-lookup"><span data-stu-id="9fcec-126">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
13. <span data-ttu-id="9fcec-127">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="9fcec-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="9fcec-128">Убедитесь, что вы вводите количество, снижающее чистую сумму ниже значения соответствующего договора продажи.</span><span class="sxs-lookup"><span data-stu-id="9fcec-128">Make sure that you enter a quantity that brings the Net amount under the value of the associated sales agreement.</span></span>  
    * <span data-ttu-id="9fcec-129">Обратите внимание, что поскольку заказ на продажу связан с соглашением, опубликованный процент скидки применяется к строке заказа.</span><span class="sxs-lookup"><span data-stu-id="9fcec-129">Notice that because the sales order is linked to the agreement, the negotiated discount percent is applied to the order line.</span></span>  
14. <span data-ttu-id="9fcec-130">Щелкните "Обновить строку".</span><span class="sxs-lookup"><span data-stu-id="9fcec-130">Click Update line.</span></span>
15. <span data-ttu-id="9fcec-131">Щелкните "Присоединено".</span><span class="sxs-lookup"><span data-stu-id="9fcec-131">Click Attached.</span></span>
    * <span data-ttu-id="9fcec-132">На странице "Присоединенный договор" показан код и условия договора, из которого запускается строка.</span><span class="sxs-lookup"><span data-stu-id="9fcec-132">The Attached agreement page shows the ID and terms of the agreement from which the line is released.</span></span>  
16. <span data-ttu-id="9fcec-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9fcec-133">Close the page.</span></span>
17. <span data-ttu-id="9fcec-134">В области действий щелкните "Общие".</span><span class="sxs-lookup"><span data-stu-id="9fcec-134">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="9fcec-135">Щелкните "Присоединенный договор продажи".</span><span class="sxs-lookup"><span data-stu-id="9fcec-135">Click Attached sales agreement.</span></span>
19. <span data-ttu-id="9fcec-136">Разверните раздел "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="9fcec-136">Expand the Line details section.</span></span>
20. <span data-ttu-id="9fcec-137">Перейдите на вкладку "Выполнение".</span><span class="sxs-lookup"><span data-stu-id="9fcec-137">Click the Fulfillment tab.</span></span>
    * <span data-ttu-id="9fcec-138">На вкладке "Выполнение" показана сводка по всем строкам заказа на продажу, связанным с этим обязательством, и их состоянии выполнения, а также сумме или количеству, которое не запущено в производство.</span><span class="sxs-lookup"><span data-stu-id="9fcec-138">The Fulfillment tab shows a summary of all the sales order lines that are associated with this commitment, and their fulfillment state, as well as the amount or quantity that has not yet been released.</span></span>   
21. <span data-ttu-id="9fcec-139">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9fcec-139">Close the page.</span></span>
22. <span data-ttu-id="9fcec-140">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9fcec-140">Close the page.</span></span>
23. <span data-ttu-id="9fcec-141">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9fcec-141">Close the page.</span></span>

## <a name="apply-sales-agreement-in-the-order-process"></a><span data-ttu-id="9fcec-142">Применение договора продажи в процессе заказов</span><span class="sxs-lookup"><span data-stu-id="9fcec-142">Apply sales agreement in the order process</span></span>
1. <span data-ttu-id="9fcec-143">Перейдите в раздел "Продажи и маркетинг" > "Заказы на продажу" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="9fcec-143">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="9fcec-144">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9fcec-144">Click New.</span></span>
3. <span data-ttu-id="9fcec-145">В поле "Счет клиента" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="9fcec-145">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9fcec-146">В списке найдите и выберите клиента, указанного в договоре продажи.</span><span class="sxs-lookup"><span data-stu-id="9fcec-146">In the list, find and select the customer specified on the sales agreement.</span></span>
5. <span data-ttu-id="9fcec-147">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="9fcec-147">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="9fcec-148">Разверните раздел "Общие".</span><span class="sxs-lookup"><span data-stu-id="9fcec-148">Expand the General section.</span></span>
7. <span data-ttu-id="9fcec-149">В поле "Код договора продажи" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="9fcec-149">In the Sales agreement ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="9fcec-150">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="9fcec-150">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="9fcec-151">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="9fcec-151">Click Yes.</span></span>
10. <span data-ttu-id="9fcec-152">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="9fcec-152">Click OK.</span></span>
11. <span data-ttu-id="9fcec-153">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="9fcec-153">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="9fcec-154">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="9fcec-154">In the Item number field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="9fcec-155">В поле "Код номенклатуры" введите или выберите номенклатуру, заданную в связанном договоре продажи.</span><span class="sxs-lookup"><span data-stu-id="9fcec-155">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
14. <span data-ttu-id="9fcec-156">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="9fcec-156">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="9fcec-157">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="9fcec-157">Click Save.</span></span>
16. <span data-ttu-id="9fcec-158">В области действий щелкните "Комплектация и упаковка".</span><span class="sxs-lookup"><span data-stu-id="9fcec-158">On the Action Pane, click Pick and pack.</span></span>
17. <span data-ttu-id="9fcec-159">Щелкните "Разноска отборочной накладной".</span><span class="sxs-lookup"><span data-stu-id="9fcec-159">Click Post packing slip.</span></span>
18. <span data-ttu-id="9fcec-160">Разверните раздел "Параметры".</span><span class="sxs-lookup"><span data-stu-id="9fcec-160">Expand the Parameters section.</span></span>
19. <span data-ttu-id="9fcec-161">Выберите значение "Да" в поле "Разноска".</span><span class="sxs-lookup"><span data-stu-id="9fcec-161">Select Yes in the Posting field.</span></span>
20. <span data-ttu-id="9fcec-162">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="9fcec-162">Click OK.</span></span>
21. <span data-ttu-id="9fcec-163">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="9fcec-163">Click OK.</span></span>
22. <span data-ttu-id="9fcec-164">В области действий щелкните "Общие".</span><span class="sxs-lookup"><span data-stu-id="9fcec-164">On the Action Pane, click General.</span></span>
23. <span data-ttu-id="9fcec-165">Щелкните "Присоединенный договор продажи".</span><span class="sxs-lookup"><span data-stu-id="9fcec-165">Click Attached sales agreement.</span></span>
24. <span data-ttu-id="9fcec-166">Перейдите на вкладку "Выполнение".</span><span class="sxs-lookup"><span data-stu-id="9fcec-166">Click the Fulfillment tab.</span></span>


