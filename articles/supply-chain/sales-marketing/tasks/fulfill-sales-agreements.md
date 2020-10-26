---
title: Выполнение договоров продажи
description: Эта процедура описывает, как выполнить договор продажи, связав с ним заказы на продажу.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines, SalesAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d3a35c7140b886f931df48e583b1582201b6547
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982025"
---
# <a name="fulfill-sales-agreements"></a><span data-ttu-id="72499-103">Выполнение договоров продажи</span><span class="sxs-lookup"><span data-stu-id="72499-103">Fulfill sales agreements</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="72499-104">Эта процедура описывает, как выполнить договор продажи, связав с ним заказы на продажу.</span><span class="sxs-lookup"><span data-stu-id="72499-104">This procedure shows you how to fulfill a sales agreement by associating sales orders with it.</span></span> <span data-ttu-id="72499-105">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="72499-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="72499-106">Перед началом этого руководства убедитесь, что у вас есть действующий договор продажи типа "Обязательство по стоимости продукта".</span><span class="sxs-lookup"><span data-stu-id="72499-106">Before starting this guide, make sure you have an effective sales agreement of type "Product value commitment".</span></span> <span data-ttu-id="72499-107">Или же можно выполнить руководство по задаче "Создание договоров продажи".</span><span class="sxs-lookup"><span data-stu-id="72499-107">Alternatively, you can run the task guide called "Create sales agreements".</span></span>  




## <a name="release-a-sales-order-from-the-agreement"></a><span data-ttu-id="72499-108">Запуск заказа на продажу в производство из договора</span><span class="sxs-lookup"><span data-stu-id="72499-108">Release a sales order from the agreement</span></span>
1. <span data-ttu-id="72499-109">Перейдите в раздел "Продажи и маркетинг" > "Договоры продажи" > "Договоры продажи".</span><span class="sxs-lookup"><span data-stu-id="72499-109">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="72499-110">В списке откройте договор, по которому требуется запустить в производство заказ.</span><span class="sxs-lookup"><span data-stu-id="72499-110">In the list, open the agreement against which you want to release the order.</span></span>
3. <span data-ttu-id="72499-111">В области действий щелкните "Договор продажи".</span><span class="sxs-lookup"><span data-stu-id="72499-111">On the Action Pane, click Sales agreement.</span></span>
4. <span data-ttu-id="72499-112">Щелкните "Заказ на запуск в производство".</span><span class="sxs-lookup"><span data-stu-id="72499-112">Click Release order.</span></span>
    * <span data-ttu-id="72499-113">Согласно тексту в верхней части страницы "Создать заказ на запуск в производство", сведения, необходимые для строк заказа на продажу, будут отличаться в зависимости того, на чем основано соглашение: количество или стоимость.</span><span class="sxs-lookup"><span data-stu-id="72499-113">As the text on top of the  Create release order page points out, the details required for the sales order lines will differ depending on whether the agreement is quantity- or value-based.</span></span>  
    * <span data-ttu-id="72499-114">Соглашение в этом руководстве имеет тип "Обязательство по стоимости продукта".</span><span class="sxs-lookup"><span data-stu-id="72499-114">The agreement in this guide is of type "Product value commitment".</span></span> <span data-ttu-id="72499-115">Именно поэтому раздел "Строки" на этой странице не заполнен.</span><span class="sxs-lookup"><span data-stu-id="72499-115">This is why the Lines section of this page is blank.</span></span> <span data-ttu-id="72499-116">Если обязательство было бы основано на количестве, сведения по строкам были бы скопированы из договора.</span><span class="sxs-lookup"><span data-stu-id="72499-116">If the commitment was based on quantity, the line information would be copied from the agreement.</span></span>  
5. <span data-ttu-id="72499-117">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="72499-117">Click Create.</span></span>
    * <span data-ttu-id="72499-118">Сообщение указывает, что заказ на покупку продажу создан.</span><span class="sxs-lookup"><span data-stu-id="72499-118">The message informs you that a sales order has been created.</span></span> <span data-ttu-id="72499-119">Поскольку заказ не содержит никаких строк, необходимо добавить данные строк, чтобы завершить процесс выпуска.</span><span class="sxs-lookup"><span data-stu-id="72499-119">Since the order does not contain any lines, you must add order line details to complete the release process.</span></span>   
6. <span data-ttu-id="72499-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="72499-120">Close the page.</span></span>
7. <span data-ttu-id="72499-121">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="72499-121">Close the page.</span></span>
8. <span data-ttu-id="72499-122">Перейдите в раздел "Продажи и маркетинг" > "Заказы на продажу" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="72499-122">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
9. <span data-ttu-id="72499-123">В списке найдите и откройте заказ, созданный в результате запуска заказа в производство в предыдущей задаче.</span><span class="sxs-lookup"><span data-stu-id="72499-123">In the list, find and open the order that was created as the result of the order release in the previous task.</span></span>
10. <span data-ttu-id="72499-124">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="72499-124">Click Add line.</span></span>
11. <span data-ttu-id="72499-125">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="72499-125">In the Item number field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="72499-126">В поле "Код номенклатуры" введите или выберите номенклатуру, заданную в связанном договоре продажи.</span><span class="sxs-lookup"><span data-stu-id="72499-126">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
13. <span data-ttu-id="72499-127">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="72499-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="72499-128">Убедитесь, что вы вводите количество, снижающее чистую сумму ниже значения соответствующего договора продажи.</span><span class="sxs-lookup"><span data-stu-id="72499-128">Make sure that you enter a quantity that brings the Net amount under the value of the associated sales agreement.</span></span>  
    * <span data-ttu-id="72499-129">Обратите внимание, что поскольку заказ на продажу связан с соглашением, опубликованный процент скидки применяется к строке заказа.</span><span class="sxs-lookup"><span data-stu-id="72499-129">Notice that because the sales order is linked to the agreement, the negotiated discount percent is applied to the order line.</span></span>  
14. <span data-ttu-id="72499-130">Щелкните "Обновить строку".</span><span class="sxs-lookup"><span data-stu-id="72499-130">Click Update line.</span></span>
15. <span data-ttu-id="72499-131">Щелкните "Присоединено".</span><span class="sxs-lookup"><span data-stu-id="72499-131">Click Attached.</span></span>
    * <span data-ttu-id="72499-132">На странице "Присоединенный договор" показан код и условия договора, из которого запускается строка.</span><span class="sxs-lookup"><span data-stu-id="72499-132">The Attached agreement page shows the ID and terms of the agreement from which the line is released.</span></span>  
16. <span data-ttu-id="72499-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="72499-133">Close the page.</span></span>
17. <span data-ttu-id="72499-134">В области действий щелкните "Общие".</span><span class="sxs-lookup"><span data-stu-id="72499-134">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="72499-135">Щелкните "Присоединенный договор продажи".</span><span class="sxs-lookup"><span data-stu-id="72499-135">Click Attached sales agreement.</span></span>
19. <span data-ttu-id="72499-136">Разверните раздел "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="72499-136">Expand the Line details section.</span></span>
20. <span data-ttu-id="72499-137">Перейдите на вкладку "Выполнение".</span><span class="sxs-lookup"><span data-stu-id="72499-137">Click the Fulfillment tab.</span></span>
    * <span data-ttu-id="72499-138">На вкладке "Выполнение" показана сводка по всем строкам заказа на продажу, связанным с этим обязательством, и их состоянии выполнения, а также сумме или количеству, которое не запущено в производство.</span><span class="sxs-lookup"><span data-stu-id="72499-138">The Fulfillment tab shows a summary of all the sales order lines that are associated with this commitment, and their fulfillment state, as well as the amount or quantity that has not yet been released.</span></span>   
21. <span data-ttu-id="72499-139">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="72499-139">Close the page.</span></span>
22. <span data-ttu-id="72499-140">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="72499-140">Close the page.</span></span>
23. <span data-ttu-id="72499-141">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="72499-141">Close the page.</span></span>

## <a name="apply-sales-agreement-in-the-order-process"></a><span data-ttu-id="72499-142">Применение договора продажи в процессе заказов</span><span class="sxs-lookup"><span data-stu-id="72499-142">Apply sales agreement in the order process</span></span>
1. <span data-ttu-id="72499-143">Перейдите в раздел "Продажи и маркетинг" > "Заказы на продажу" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="72499-143">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="72499-144">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="72499-144">Click New.</span></span>
3. <span data-ttu-id="72499-145">В поле "Счет клиента" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="72499-145">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="72499-146">В списке найдите и выберите клиента, указанного в договоре продажи.</span><span class="sxs-lookup"><span data-stu-id="72499-146">In the list, find and select the customer specified on the sales agreement.</span></span>
5. <span data-ttu-id="72499-147">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="72499-147">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="72499-148">Разверните раздел "Общие".</span><span class="sxs-lookup"><span data-stu-id="72499-148">Expand the General section.</span></span>
7. <span data-ttu-id="72499-149">В поле "Код договора продажи" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="72499-149">In the Sales agreement ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="72499-150">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="72499-150">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="72499-151">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="72499-151">Click Yes.</span></span>
10. <span data-ttu-id="72499-152">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="72499-152">Click OK.</span></span>
11. <span data-ttu-id="72499-153">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="72499-153">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="72499-154">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="72499-154">In the Item number field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="72499-155">В поле "Код номенклатуры" введите или выберите номенклатуру, заданную в связанном договоре продажи.</span><span class="sxs-lookup"><span data-stu-id="72499-155">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
14. <span data-ttu-id="72499-156">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="72499-156">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="72499-157">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="72499-157">Click Save.</span></span>
16. <span data-ttu-id="72499-158">В области действий щелкните "Комплектация и упаковка".</span><span class="sxs-lookup"><span data-stu-id="72499-158">On the Action Pane, click Pick and pack.</span></span>
17. <span data-ttu-id="72499-159">Щелкните "Разноска отборочной накладной".</span><span class="sxs-lookup"><span data-stu-id="72499-159">Click Post packing slip.</span></span>
18. <span data-ttu-id="72499-160">Разверните раздел "Параметры".</span><span class="sxs-lookup"><span data-stu-id="72499-160">Expand the Parameters section.</span></span>
19. <span data-ttu-id="72499-161">Выберите значение "Да" в поле "Разноска".</span><span class="sxs-lookup"><span data-stu-id="72499-161">Select Yes in the Posting field.</span></span>
20. <span data-ttu-id="72499-162">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="72499-162">Click OK.</span></span>
21. <span data-ttu-id="72499-163">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="72499-163">Click OK.</span></span>
22. <span data-ttu-id="72499-164">В области действий щелкните "Общие".</span><span class="sxs-lookup"><span data-stu-id="72499-164">On the Action Pane, click General.</span></span>
23. <span data-ttu-id="72499-165">Щелкните "Присоединенный договор продажи".</span><span class="sxs-lookup"><span data-stu-id="72499-165">Click Attached sales agreement.</span></span>
24. <span data-ttu-id="72499-166">Перейдите на вкладку "Выполнение".</span><span class="sxs-lookup"><span data-stu-id="72499-166">Click the Fulfillment tab.</span></span>

