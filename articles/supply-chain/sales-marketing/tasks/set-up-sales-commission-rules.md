--- 
title: "Настройка правил комиссий продаж"
description: "Эта процедура описывает, как настроить и включить расчет комиссии по продажам и отслеживание."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8d81765884f741443d1c0f5b0cb8bc545945e1a1
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-sales-commission-rules"></a><span data-ttu-id="8f2bf-103">Настройка правил комиссий продаж</span><span class="sxs-lookup"><span data-stu-id="8f2bf-103">Set up sales commission rules</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8f2bf-104">Эта процедура описывает, как настроить и включить расчет комиссии по продажам и отслеживание.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-104">This procedure shows you how to set up and enable sales commission calculation and tracking.</span></span> <span data-ttu-id="8f2bf-105">Процедура показывает, как создать группы комиссий клиента и номенклатуры, а затем как связать выбранных клиента и продукта с соответствующими группами.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-105">The procedure shows how to create both customer and item commission groups, and then how to link a selected customer and product to the respective groups.</span></span> <span data-ttu-id="8f2bf-106">Затем эти группы используются при настройке расчета комиссии для создания комбинации клиента, номенклатуры и торговых представителей, которая должна быть сопоставлена заказом на продажу для назначения продавцов для комиссии.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-106">Those groups are then used in the commission calculation setup to create a customer, item, and sales representatives combination that must be matched by the sales order to entitle the sales people to a commission.</span></span> <span data-ttu-id="8f2bf-107">Создание групп комиссий клиента и номенклатуры является необязательным, так как расчет комиссии можно также сделать для отдельного клиента и/или номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-107">Creating customer and item commission groups are optional, as the calculation of commission can also be done for an individual customer and/or item.</span></span> <span data-ttu-id="8f2bf-108">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-commission-groups-and-commission-rates"></a><span data-ttu-id="8f2bf-109">Настройка групп комиссий и ставок комиссии</span><span class="sxs-lookup"><span data-stu-id="8f2bf-109">Set up commission groups and commission rates</span></span>
1. <span data-ttu-id="8f2bf-110">Перейдите в раздел "Продажи и маркетинг" > "Комиссии" > "Группы клиентов для комиссии".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-110">Go to Sales and marketing > Commissions > Customer groups for commission.</span></span>
2. <span data-ttu-id="8f2bf-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-111">Click New.</span></span>
3. <span data-ttu-id="8f2bf-112">В поле "Группа" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-112">In the Group field, type a value.</span></span>
4. <span data-ttu-id="8f2bf-113">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="8f2bf-114">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-114">Click Save.</span></span>
6. <span data-ttu-id="8f2bf-115">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-115">Close the page.</span></span>
7. <span data-ttu-id="8f2bf-116">Перейдите в раздел "Продажи и маркетинг" > "Комиссии" > "Группы номенклатур".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-116">Go to Sales and marketing > Commissions > Item groups.</span></span>
8. <span data-ttu-id="8f2bf-117">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-117">Click New.</span></span>
9. <span data-ttu-id="8f2bf-118">В поле "Группа" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-118">In the Group field, type a value.</span></span>
10. <span data-ttu-id="8f2bf-119">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-119">In the Name field, type a value.</span></span>
11. <span data-ttu-id="8f2bf-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-120">Close the page.</span></span>
12. <span data-ttu-id="8f2bf-121">Перейдите в раздел "Продажи и маркетинг" > "Комиссии" > "Группы продаж".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-121">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="8f2bf-122">Группа комиссий по продажам задает сотрудников в ролях торгового представителя, которые имеют право получать комиссию, когда клиент, связанный с соответствующей группой продажи, покупает некоторые номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-122">A Commission sales group specifies the employees in sales representative roles who are eligible to receive a commission when a customer associated with the relevant sales group buys certain items.</span></span>  
    * <span data-ttu-id="8f2bf-123">В компании демонстрационных данных USMF имеется группа продаж с названием "Торговые представители США".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-123">In the USMF demo data company, there is a sales group called "Sales reps US."</span></span>  
13. <span data-ttu-id="8f2bf-124">В области действий щелкните "Общие".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-124">On the Action Pane, click General.</span></span>
14. <span data-ttu-id="8f2bf-125">Щелкните "Торговый представитель".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-125">Click Sales rep..</span></span>
    * <span data-ttu-id="8f2bf-126">На странице торговых представителей отображается список продавец компании, связанных с конкретной группой комиссий.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-126">The Sales rep. page displays a list of the company's sales people who are associated with a specific commission group.</span></span> <span data-ttu-id="8f2bf-127">Можно назначить несколько торговых представителей для одной группы и определить их соответствующую долю в общем сборе комиссии как значение процента.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-127">You can assign multiple sales representatives to the same group and define their respective share of the total commission fee as a percentage value.</span></span> <span data-ttu-id="8f2bf-128">Полная доля комиссии по всем сотрудникам не должна превышать 100.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-128">The total commission share across all employees must not exceed 100.</span></span>  
15. <span data-ttu-id="8f2bf-129">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-129">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="8f2bf-130">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-130">Click Edit.</span></span>
17. <span data-ttu-id="8f2bf-131">Задайте долю комиссии как "50".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-131">Set Commission share to '50'.</span></span>
18. <span data-ttu-id="8f2bf-132">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-132">Click New.</span></span>
19. <span data-ttu-id="8f2bf-133">В поле "Имя" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-133">In the Name field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="8f2bf-134">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="8f2bf-135">Например, отфильтруйте поле "Имя" по значению "Susan Burk".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-135">For example, filter on the Name field with a value of 'Susan Burk'.</span></span>
21. <span data-ttu-id="8f2bf-136">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-136">Click Select.</span></span>
22. <span data-ttu-id="8f2bf-137">Задайте долю комиссии как "50".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-137">Set Commission share to '50'.</span></span>
23. <span data-ttu-id="8f2bf-138">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-138">Click Save.</span></span>
24. <span data-ttu-id="8f2bf-139">Перейдите в раздел "Продажи и маркетинг" > "Комиссии" > "Расчет комиссии".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-139">Go to Sales and marketing > Commissions > Commission calculation.</span></span>
    * <span data-ttu-id="8f2bf-140">На странице расчета комиссии вы определяете ставку комиссии, которую сотрудник должен получить для проводки по продажам, когда она содержит предварительно заданную комбинацию клиент-продукт.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-140">In the Commission calculation page you define the commission rate that the employee is to receive for a sales transaction when it contains the pre-set combination of customer and product.</span></span> <span data-ttu-id="8f2bf-141">В процессе настройки ставки комиссии необходимо указать основу расчета комиссии и должна ли она включать или исключать скидки.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-141">As part of the commission rate setup, you must specify the commission calculation basis and whether it should include or exclude discounts.</span></span> <span data-ttu-id="8f2bf-142">Можно также ввести период действия, когда ставка комиссии активна.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-142">You can also enter a validity period for when the commission rate is active.</span></span>  
25. <span data-ttu-id="8f2bf-143">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-143">Click New.</span></span>
26. <span data-ttu-id="8f2bf-144">В поле "Код номенклатуры" выберите "Группа".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-144">In the Item code field, select 'Group'.</span></span>
27. <span data-ttu-id="8f2bf-145">В поле "Связь номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-145">In the Item relation field, click the drop-down button to open the lookup.</span></span>
28. <span data-ttu-id="8f2bf-146">Найдите в списке и выберите группу, созданную ранее.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-146">In the list, find and select the group that you created earlier.</span></span>
29. <span data-ttu-id="8f2bf-147">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="8f2bf-148">В поле "Код клиента" выберите "Группа".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-148">In the Customer code field, select 'Group'.</span></span>
31. <span data-ttu-id="8f2bf-149">В поле "Связь клиента" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-149">In the Customer relation field, click the drop-down button to open the lookup.</span></span>
32. <span data-ttu-id="8f2bf-150">Найдите в списке и выберите группу, настроенную ранее.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-150">In the list, select the group that you set up earlier.</span></span>
33. <span data-ttu-id="8f2bf-151">На странице связей торговых представителей нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-151">In the Sales rep. relation field, click the drop-down button to open the lookup.</span></span>
34. <span data-ttu-id="8f2bf-152">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-152">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8f2bf-153">Сохраните параметр "До расчета скидки по строке".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-153">Keep the "Before line discount" option.</span></span>  
    * <span data-ttu-id="8f2bf-154">Сохраните параметр "Выручка" в качестве основы для расчета значения комиссии.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-154">Keep the "Revenue" option as the basis for commission value calculation.</span></span>    
35. <span data-ttu-id="8f2bf-155">В поле "Процент комиссии" введите число.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-155">In the Commission percentage field, enter a number.</span></span>
36. <span data-ttu-id="8f2bf-156">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-156">Click Save.</span></span>

## <a name="setting-up-commission-posting"></a><span data-ttu-id="8f2bf-157">Настройка разноски комиссии</span><span class="sxs-lookup"><span data-stu-id="8f2bf-157">Setting up commission posting</span></span>
1. <span data-ttu-id="8f2bf-158">Перейдите в раздел "Продажи и маркетинг" > "Комиссии" > "Разноска комиссии".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-158">Go to Sales and marketing > Commissions > Commission posting.</span></span>
    * <span data-ttu-id="8f2bf-159">Сборы комиссии подлежат оплате для сотрудников и поэтому должны быть настроены для обеспечения правильной финансовой разноски на соответствующие счета в главной книге.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-159">Commission fees are payable to the employees and must therefore be set up to ensure correct financial posting to the appropriate accounts in the General ledger.</span></span> <span data-ttu-id="8f2bf-160">Это выполняется на странице разноски комиссий.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-160">This is done in the Commission posting page.</span></span> <span data-ttu-id="8f2bf-161">Проверьте настройку, доступную для текущей компании.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-161">Review the setup that is available for the current company.</span></span> <span data-ttu-id="8f2bf-162">Обычно разносятся суммы комиссии на выделенный счет расходов и сопоставляются с выделенным счетом к оплате.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-162">Typically, the commission amounts are posted to a dedicated expense account and are offset to a dedicated payable account.</span></span> <span data-ttu-id="8f2bf-163">Если правила разноски комиссий не настроены, система не сможет выполнить выставление накладных по заказу на продажу с подходящими комиссиями.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-163">If you don't have the commission posting rules set up, the system will fail to complete invoicing of a sales order which has eligible commissions.</span></span>  
2. <span data-ttu-id="8f2bf-164">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-164">Close the page.</span></span>

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a><span data-ttu-id="8f2bf-165">Назначение группы комиссий клиенту и продукту</span><span class="sxs-lookup"><span data-stu-id="8f2bf-165">Assign a commission group to a customer and a product</span></span>
1. <span data-ttu-id="8f2bf-166">Перейдите в раздел "Продажи и маркетинг" > "Клиенты" > "Все клиенты".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-166">Go to Sales and marketing > Customers > All customers.</span></span>
2. <span data-ttu-id="8f2bf-167">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-167">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="8f2bf-168">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-168">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8f2bf-169">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-169">Click Edit.</span></span>
5. <span data-ttu-id="8f2bf-170">Разверните раздел "Значения заказов на продажу по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-170">Expand the Sales order defaults section.</span></span>
6. <span data-ttu-id="8f2bf-171">В поле "Группа комиссий" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-171">In the Commission group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8f2bf-172">Найдите в списке и выберите группу, созданную ранее.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-172">In the list, select the group that you created earlier.</span></span>
8. <span data-ttu-id="8f2bf-173">В поле "Группа продаж" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-173">In the Sales group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="8f2bf-174">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-174">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="8f2bf-175">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-175">Click Save.</span></span>
11. <span data-ttu-id="8f2bf-176">Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-176">Go to Product information management > Products > Released products.</span></span>
12. <span data-ttu-id="8f2bf-177">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-177">Use the Quick Filter to find records.</span></span> <span data-ttu-id="8f2bf-178">Например, отфильтруйте поле "Номер номенклатуры" по значению "T0020".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-178">For example, filter on the Item number field with a value of 'T0020 '.</span></span>
13. <span data-ttu-id="8f2bf-179">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-179">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="8f2bf-180">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-180">Click Edit.</span></span>
15. <span data-ttu-id="8f2bf-181">Разверните раздел "Продажи".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-181">Expand the Sell section.</span></span>
16. <span data-ttu-id="8f2bf-182">В поле "Группа комиссий" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-182">In the Commission group field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="8f2bf-183">В списке выберите группу комиссий, созданную ранее.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-183">In the list, select the commission group that you created earlier.</span></span>

