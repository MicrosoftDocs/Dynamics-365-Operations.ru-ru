---
title: Создание и изменение предложений по продаже
description: Эта процедура демонстрирует способ создания и обновления предложения по продажам.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b5618a815aaff12dd366523920ed275801b3b16
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "343635"
---
# <a name="create-and-edit-sales-quotations"></a><span data-ttu-id="40e30-103">Создание и изменение предложений по продаже</span><span class="sxs-lookup"><span data-stu-id="40e30-103">Create and edit sales quotations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="40e30-104">Эта процедура демонстрирует способ создания и обновления предложения по продажам.</span><span class="sxs-lookup"><span data-stu-id="40e30-104">This procedure demonstrates how to create and update a sales quotation.</span></span> <span data-ttu-id="40e30-105">Эту процедуру можно выполнить со своими данными или с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="40e30-105">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-sales-quotation"></a><span data-ttu-id="40e30-106">Создание предложения по продаже</span><span class="sxs-lookup"><span data-stu-id="40e30-106">Create a sales quotation</span></span>
1. <span data-ttu-id="40e30-107">Перейдите в раздел "Продажи и маркетинг" > "Предложение по продажам" > "Все предложения".</span><span class="sxs-lookup"><span data-stu-id="40e30-107">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
2. <span data-ttu-id="40e30-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="40e30-108">Click New.</span></span>
3. <span data-ttu-id="40e30-109">В поле "Тип счета" выберите "Перспективный клиент".</span><span class="sxs-lookup"><span data-stu-id="40e30-109">In the Account type field, select 'Prospect'.</span></span>
4. <span data-ttu-id="40e30-110">В поле "Перспективный клиент введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="40e30-110">In the Prospect field, enter or select a value.</span></span>
5. <span data-ttu-id="40e30-111">Разверните раздел "Общие".</span><span class="sxs-lookup"><span data-stu-id="40e30-111">Expand the General section.</span></span>
    * <span data-ttu-id="40e30-112">Поскольку было выбрано создание предложения из зоны "Продажи и маркетинг", тип автоматически изменяется на "Предложение по продажам".</span><span class="sxs-lookup"><span data-stu-id="40e30-112">Because you chose to create a quotation from the Sales and Marketing area, the type is automatically set to Sales quotation.</span></span> <span data-ttu-id="40e30-113">Для создания предложения для проекта необходимо получить к нему доступ из модуля " Управление и учет по проектам ".</span><span class="sxs-lookup"><span data-stu-id="40e30-113">To create a quotation for a project you must access it from the Project management and accounting module.</span></span>   
6. <span data-ttu-id="40e30-114">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="40e30-114">Click OK.</span></span>
    * <span data-ttu-id="40e30-115">Поля и действия в строках предложения похожи на таковые в строках заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="40e30-115">The fields and actions on the quotation lines are very similar to the ones on the sales order lines.</span></span>   <span data-ttu-id="40e30-116">Как и заказы на продажу, предложения могут быть созданы для определенной номенклатуры или, если код номенклатуры неизвестен или не существует во время создания предложения, предложения могут быть созданы для категории продаж.</span><span class="sxs-lookup"><span data-stu-id="40e30-116">Like sales orders, quotations can be created for a specific item or, when item number is not known or does not exist at the time of quotation creation, quotations can be created for a sales category.</span></span>  
7. <span data-ttu-id="40e30-117">В поле "Номенклатура" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="40e30-117">In the Item field, enter or select a value.</span></span>
8. <span data-ttu-id="40e30-118">В поле "Номенклатура" введите значение.</span><span class="sxs-lookup"><span data-stu-id="40e30-118">In the Item field, type a value.</span></span>
9. <span data-ttu-id="40e30-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="40e30-119">Close the page.</span></span>
10. <span data-ttu-id="40e30-120">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="40e30-120">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="40e30-121">Если имеются допустимые коммерческие соглашения для выбранной номенклатуры в строке, применимые цена и скидки автоматически копируются в строку предложения.</span><span class="sxs-lookup"><span data-stu-id="40e30-121">If there are valid trade agreements for the item selected on the line, the applicable price and discounts will be automatically copied to the quotation line.</span></span> <span data-ttu-id="40e30-122">Убедитесь, что поле "Цена за единицу" содержит значение, а также можно ввести значения скидки, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="40e30-122">Make sure that the Unit price field contains a value and you can also enter discount values if you want to.</span></span>  
11. <span data-ttu-id="40e30-123">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="40e30-123">Click Save.</span></span>
12. <span data-ttu-id="40e30-124">В области действий щелкните "Предложение по продаже".</span><span class="sxs-lookup"><span data-stu-id="40e30-124">On the Action Pane, click Sales quotation.</span></span>
13. <span data-ttu-id="40e30-125">Щелкните "Итоги".</span><span class="sxs-lookup"><span data-stu-id="40e30-125">Click Totals.</span></span>
14. <span data-ttu-id="40e30-126">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="40e30-126">Click OK.</span></span>
15. <span data-ttu-id="40e30-127">Щелкните "Строка предложения по продаже".</span><span class="sxs-lookup"><span data-stu-id="40e30-127">Click Sales quotation line.</span></span>
16. <span data-ttu-id="40e30-128">Щелкните "Цены".</span><span class="sxs-lookup"><span data-stu-id="40e30-128">Click Prices.</span></span>
    * <span data-ttu-id="40e30-129">На странице "Запустить моделирование цены" можно поэкспериментировать с корректировкой предполагаемой выручки или рентабельности по предложению на основе требуемых цены за единицу, суммы скидки, процента скидки, общей суммы, маржи или процентной маржи.</span><span class="sxs-lookup"><span data-stu-id="40e30-129">In the Run price simulation page you can experiment with adjusting the expected revenue or profitability of your quotation based on the desired unit price, discount amount, discount percentage, total amount, margin, or contribution ratio.</span></span>   <span data-ttu-id="40e30-130">Когда будет достигнуто целевое значение, предложение применяется к строке предложения, и его поля, связанные с ценами, будут соответствующим образом обновлены.</span><span class="sxs-lookup"><span data-stu-id="40e30-130">When you are satisfied with the target figures, you apply the suggestion to the quotation line, and its price-related fields will be updated accordingly.</span></span>  
    * <span data-ttu-id="40e30-131">Вы можете создавать сколько угодно вариантов моделирования цены.</span><span class="sxs-lookup"><span data-stu-id="40e30-131">Y ou can create as many price simulations as you wish.</span></span> <span data-ttu-id="40e30-132">Когда вы нажимаете "Создать", условия цены из строки текущего предложения копируются на страницу.</span><span class="sxs-lookup"><span data-stu-id="40e30-132">When you click New, the price conditions from the current quotation line are copied to the page.</span></span> <span data-ttu-id="40e30-133">Затем можно изменить значения в любом поле, связанном с ценой, на нужные.</span><span class="sxs-lookup"><span data-stu-id="40e30-133">You can then modify values in any of the price-related fields to the target ones.</span></span> <span data-ttu-id="40e30-134">Изменение в одном из полей вызовет пересчет во всех остальных полях.</span><span class="sxs-lookup"><span data-stu-id="40e30-134">A change in one of the fields will trigger recalculation in all the other fields.</span></span> <span data-ttu-id="40e30-135">Чтобы система рассчитывала маржу продажи и процентную маржу, необходимо знать стоимость единицы продукта.</span><span class="sxs-lookup"><span data-stu-id="40e30-135">In order for the system to calculate the sales margin and contribution ratio, the product's unit cost has to be known.</span></span> <span data-ttu-id="40e30-136">Используйте вкладку "Смоделированные цены" для подробного просмотра исходных цен, предлагаемых изменений и их влияния на итоговые значения предложения.</span><span class="sxs-lookup"><span data-stu-id="40e30-136">Use the Simulated prices tab for a detailed view of the original prices, proposed changes and their effect on the quotation totals.</span></span>   <span data-ttu-id="40e30-137">Как правило, когда моделирование задает новую сумму, применяемую в строке предложения, система пересчитывает и вводит новое значение в поле "Цена за единицу".</span><span class="sxs-lookup"><span data-stu-id="40e30-137">As a general rule, when a simulation that sets a new amount is applied to the quotation line, the system recalculates and enters a new value in the Unit price field.</span></span> <span data-ttu-id="40e30-138">Если моделирование основано на новой марже или новой процентной марже, обновляется только поле "Чистая сумма", а поле "Цена за единицу" остается пустым.</span><span class="sxs-lookup"><span data-stu-id="40e30-138">If the simulation is based on a new margin or a new contribution ratio, only the Net amount field is updated, and the Unit price is blank.</span></span> <span data-ttu-id="40e30-139">В обоих случаях все скидки, которые содержались в строке предложения перед выполнением моделирования, будут удалены.</span><span class="sxs-lookup"><span data-stu-id="40e30-139">In both cases, any discounts that were on the quotation line before simulation will be deleted.</span></span>  
17. <span data-ttu-id="40e30-140">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="40e30-140">Close the page.</span></span>
18. <span data-ttu-id="40e30-141">В области действий щелкните "Предложение".</span><span class="sxs-lookup"><span data-stu-id="40e30-141">On the Action Pane, click Quotation.</span></span>
19. <span data-ttu-id="40e30-142">Щелкните "Отправить предложение".</span><span class="sxs-lookup"><span data-stu-id="40e30-142">Click Send quotation.</span></span>
20. <span data-ttu-id="40e30-143">В поле "Печать предложения" выберите значение "Да".</span><span class="sxs-lookup"><span data-stu-id="40e30-143">Select Yes in the Print quotation field.</span></span>
21. <span data-ttu-id="40e30-144">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="40e30-144">Click OK.</span></span>
    * <span data-ttu-id="40e30-145">Создание отчета может занять минуту.</span><span class="sxs-lookup"><span data-stu-id="40e30-145">The report may take a minute to generate.</span></span> <span data-ttu-id="40e30-146">Не закрывайте страницу до окончания операции.</span><span class="sxs-lookup"><span data-stu-id="40e30-146">Don’t close the page until it does so.</span></span>  
22. <span data-ttu-id="40e30-147">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="40e30-147">Close the page.</span></span>

## <a name="update-a-sales-quotation"></a><span data-ttu-id="40e30-148">Обновление предложения по продаже</span><span class="sxs-lookup"><span data-stu-id="40e30-148">Update a sales quotation</span></span>
1. <span data-ttu-id="40e30-149">В области действий щелкните "Обработка результатов".</span><span class="sxs-lookup"><span data-stu-id="40e30-149">On the Action Pane, click Follow up.</span></span>
2. <span data-ttu-id="40e30-150">Щелкните "Перевод в клиента".</span><span class="sxs-lookup"><span data-stu-id="40e30-150">Click Convert to customer.</span></span>
3. <span data-ttu-id="40e30-151">В поле "Счет клиента" введите значение.</span><span class="sxs-lookup"><span data-stu-id="40e30-151">In the Customer account field, type a value.</span></span>
4. <span data-ttu-id="40e30-152">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="40e30-152">Click Check.</span></span>
    * <span data-ttu-id="40e30-153">Убедитесь, что видите сообщение, для которого можно указывать номер счета.</span><span class="sxs-lookup"><span data-stu-id="40e30-153">Make sure you see a message that the account number you typed in is free to use.</span></span>  
5. <span data-ttu-id="40e30-154">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="40e30-154">Click OK.</span></span>
    * <span data-ttu-id="40e30-155">Теперь система создала новый счет клиента для перспективного клиента в предложении.</span><span class="sxs-lookup"><span data-stu-id="40e30-155">The system has now created a new customer account for the prospect on the quotation.</span></span>  
6. <span data-ttu-id="40e30-156">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="40e30-156">Close the page.</span></span>
7. <span data-ttu-id="40e30-157">В области действий щелкните "Обработка результатов".</span><span class="sxs-lookup"><span data-stu-id="40e30-157">On the Action Pane, click Follow up.</span></span>
8. <span data-ttu-id="40e30-158">Нажмите кнопку "Подтвердить".</span><span class="sxs-lookup"><span data-stu-id="40e30-158">Click Confirm.</span></span>
9. <span data-ttu-id="40e30-159">В поле "Причина" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="40e30-159">In the Reason field, enter or select a value.</span></span>
10. <span data-ttu-id="40e30-160">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="40e30-160">Click OK.</span></span>
11. <span data-ttu-id="40e30-161">В области действий щелкните "Общие".</span><span class="sxs-lookup"><span data-stu-id="40e30-161">On the Action Pane, click General.</span></span>
12. <span data-ttu-id="40e30-162">Щелкните "Заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="40e30-162">Click Sales orders.</span></span>
13. <span data-ttu-id="40e30-163">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="40e30-163">Close the page.</span></span>

