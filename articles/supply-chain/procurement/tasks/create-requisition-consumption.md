---
title: Создание заявки на потребление
description: Эта процедура демонстрирует процесс создания заявки.
author: mkirknel
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e81ca3966cf7dae88468ccf107b52b8c3d7b323d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "366566"
---
# <a name="create-a-requisition-for-consumption"></a><span data-ttu-id="e3c6e-103">Создание заявки на потребление</span><span class="sxs-lookup"><span data-stu-id="e3c6e-103">Create a requisition for consumption</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e3c6e-104">Эта процедура демонстрирует процесс создания заявки.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-104">This procedure walks you through the process of creating a requisition.</span></span> <span data-ttu-id="e3c6e-105">В ней показаны различные способы поиска продуктов в каталоге закупаемой продукции, а также порядок добавления продукта, который отсутствует в каталоге.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-105">It shows you different ways to search for products in your procurement catalog and how to add a product that isn’t in your catalog.</span></span> <span data-ttu-id="e3c6e-106">Перед началом процедуры необходимо иметь настроенную политику закупок, в которой в качестве типа заявки по умолчанию указан тип "Потребление".</span><span class="sxs-lookup"><span data-stu-id="e3c6e-106">Before you start this procedure, you must have a purchasing policy set up with Consumption as the default type of requisition.</span></span> <span data-ttu-id="e3c6e-107">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="e3c6e-108">Эта процедура может быть выполнена только профилем пользователя, настроенного как работник.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-108">The procedure can only be carried out by a user profile that is set up as worker.</span></span>  <span data-ttu-id="e3c6e-109">Эта задача обычно выполняется сотрудником.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-109">This task would normally be carried out by an employee.</span></span> <span data-ttu-id="e3c6e-110">Роль безопасности "Сотрудник" позволит вам выполнить все задачи; или, если вы пользуетесь компанией USMF, вы можете войти как пользователь Alicia.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-110">The Employee employ security role will allow you to carry out the tasks, or if you’re using USMF, you can log in as Alicia.</span></span>


## <a name="create-a-new-requisition"></a><span data-ttu-id="e3c6e-111">Создание новой заявки</span><span class="sxs-lookup"><span data-stu-id="e3c6e-111">Create a new requisition</span></span>
1. <span data-ttu-id="e3c6e-112">Перейдите в раздел "Закупки и источники" > "Заявки на закупку" > "Заявки на покупку, подготовленные мной".</span><span class="sxs-lookup"><span data-stu-id="e3c6e-112">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="e3c6e-113">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="e3c6e-113">Click New.</span></span>
3. <span data-ttu-id="e3c6e-114">В поле "Имя" введите имя для заявки.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-114">In the Name field, give the requisition a name.</span></span>
4. <span data-ttu-id="e3c6e-115">В поле "Запрошенная дата" введите дату.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-115">In the Requested date field, enter a date.</span></span>
    * <span data-ttu-id="e3c6e-116">По умолчанию запрошенная дата и дата учета копируются в строки заявки на покупку.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-116">By default, the requested date and accounting date are copied to the purchase requisition lines.</span></span> <span data-ttu-id="e3c6e-117">Их можно изменить на уровне строки.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-117">They can be changed at the line level.</span></span> <span data-ttu-id="e3c6e-118">Запрошенная дата — запрошенная дата поставки.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-118">The requested date is the requested delivery date.</span></span>  
5. <span data-ttu-id="e3c6e-119">В поле "Дата учета" введите дату.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-119">In the Accounting date field, enter a date.</span></span>
    * <span data-ttu-id="e3c6e-120">Дата учета используется для регистрации учетной записи в ГК и для проверки доступности бюджетных средств.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-120">The accounting date is used to record the accounting entry in the general ledger, and to validate whether budget funds are available.</span></span>  
6. <span data-ttu-id="e3c6e-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e3c6e-121">Click OK.</span></span>
7. <span data-ttu-id="e3c6e-122">В поле "Основание" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-122">In the Reason field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e3c6e-123">Выбранная причина делового обоснования отображается по умолчанию для строк заявки на покупку, но ее можно изменить на уровне строки.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-123">By default, the business justification reason that you select appears for the purchase requisition lines, but you can change it at the line level.</span></span>    
8. <span data-ttu-id="e3c6e-124">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-124">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="e3c6e-125">Выбор основания</span><span class="sxs-lookup"><span data-stu-id="e3c6e-125">Select the reason</span></span>
10. <span data-ttu-id="e3c6e-126">В поле сведений введите более описательное основание для заявки.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-126">In the details field enter a more descriptive justification for the requisition</span></span>

## <a name="add-a-line-to-the-requisition"></a><span data-ttu-id="e3c6e-127">Добавление строки в заявку</span><span class="sxs-lookup"><span data-stu-id="e3c6e-127">Add a line to the requisition</span></span>
1. <span data-ttu-id="e3c6e-128">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="e3c6e-128">Click Add line.</span></span>
    * <span data-ttu-id="e3c6e-129">Существует два способа добавления строк в заявку на покупку.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-129">There are two ways of adding lines to the purchase requisition.</span></span> <span data-ttu-id="e3c6e-130">Если вы уже знаете номер продукта или уже знаете, что запрашиваете продукт, которого нет в каталоге продуктов, вы можете добавить строку непосредственно с помощью команды "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="e3c6e-130">If you already know the product number or you already  know that you are requesting a product that is not in the product catalog, then you can add the line directly with "Add line".</span></span> <span data-ttu-id="e3c6e-131">Другой способ — воспользоваться командой "Добавить продукты", которая позволяет использовать поиск и фильтрацию для нахождения номенклатур в каталоге товаров.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-131">The other way is to use "Add products" where you can use searching and filtering to find items in the product catalog.</span></span>    
2. <span data-ttu-id="e3c6e-132">Щелкните только что созданную строку.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-132">Click on the row you just created.</span></span>
    * <span data-ttu-id="e3c6e-133">Инициатор запроса — это работник, который подал заявку.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-133">The requester is the worker that has requested the requisition.</span></span>   
    * <span data-ttu-id="e3c6e-134">По умолчанию заявку подготавливает работник, который ее подает.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-134">By default the person preparing the requisition is the worker who has requested it.</span></span> <span data-ttu-id="e3c6e-135">Для подготовки строки заявки от имени другого работника вы должны получить соответствующее разрешение.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-135">You have to be given permission to prepare a requisition line on behalf of another worker.</span></span> <span data-ttu-id="e3c6e-136">Если у вас есть такие разрешения, в этом поле поиска буду отображаться другие работники.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-136">If you have such permissions then the other workers will show up in this lookup.</span></span>  
3. <span data-ttu-id="e3c6e-137">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-137">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="e3c6e-138">Номенклатуры, доступные для выбора, ограничены политикой доступа к категориям и каталогом закупаемой продукции для покупающего юридического лица.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-138">The items that are available for you to choose are limited by the category access policy and the procurement catalog for the buying legal entity.</span></span>   
4. <span data-ttu-id="e3c6e-139">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-139">In the Quantity field, enter a number.</span></span>

## <a name="add-more-products-to-the-requisition"></a><span data-ttu-id="e3c6e-140">Добавление в заявку дополнительных продуктов</span><span class="sxs-lookup"><span data-stu-id="e3c6e-140">Add more products to the requisition</span></span>
1. <span data-ttu-id="e3c6e-141">Щелкните Добавить продукты.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-141">Click Add products.</span></span>
    * <span data-ttu-id="e3c6e-142">При использовании этого варианта можно выполнять поиск продуктов в каталоге продуктов.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-142">This is the option where you can search for products in the product catalog.</span></span>    
2. <span data-ttu-id="e3c6e-143">В поле "Поиск узла категории закупаемой продукции" введите первую часть имени категорию, которую вы ищете, и нажмите клавишу "Ввод".</span><span class="sxs-lookup"><span data-stu-id="e3c6e-143">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="e3c6e-144">Например, введите "компьют".</span><span class="sxs-lookup"><span data-stu-id="e3c6e-144">For example, type comput.</span></span>  
3. <span data-ttu-id="e3c6e-145">Используйте ярлык InvokeDefaultButton.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-145">Use the InvokeDefaultButton shortcut.</span></span>
4. <span data-ttu-id="e3c6e-146">С помощью фильтра отфильтруйте список продуктов в выбранной категории.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-146">Use the Filter to filter the list of products in the selected category.</span></span>
5. <span data-ttu-id="e3c6e-147">Выберите карточку продукта, которую вы хотите добавить в заявку.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-147">Select the product card that you want to add to the requisition.</span></span>
6. <span data-ttu-id="e3c6e-148">Щелкните "Добавить в строки".</span><span class="sxs-lookup"><span data-stu-id="e3c6e-148">Click Add to lines.</span></span>
7. <span data-ttu-id="e3c6e-149">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-149">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="e3c6e-150">В поле "Поиск узла категории закупаемой продукции" введите первую часть имени категорию, которую вы ищете, и нажмите клавишу "Ввод".</span><span class="sxs-lookup"><span data-stu-id="e3c6e-150">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="e3c6e-151">Например, введите "мар" (маркеры).</span><span class="sxs-lookup"><span data-stu-id="e3c6e-151">For example, type High (highlighters).</span></span>  
9. <span data-ttu-id="e3c6e-152">Используйте ярлык InvokeDefaultButton.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-152">Use the InvokeDefaultButton shortcut.</span></span>
10. <span data-ttu-id="e3c6e-153">Щелкните "Добавить неперечисленный продукт в строки", чтобы добавить продукт, которого нет в каталоге закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-153">Click Add unlisted product to lines to add a product that’s not listed in the procurement catalog.</span></span>
11. <span data-ttu-id="e3c6e-154">В поле "Имя продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-154">In the Product name field, type a value.</span></span>
12. <span data-ttu-id="e3c6e-155">В поле "Единица измерения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-155">In the Unit field, type a value.</span></span>
13. <span data-ttu-id="e3c6e-156">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-156">Click OK.</span></span>
14. <span data-ttu-id="e3c6e-157">В поле "Описание номенклатуры" введите описание продукта.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-157">In the Item description field, add a description of the product.</span></span>
15. <span data-ttu-id="e3c6e-158">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-158">In the Quantity field, enter a number.</span></span>
16. <span data-ttu-id="e3c6e-159">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-159">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="e3c6e-160">Если вы знаете цену для определенного поставщика (которого вы выбираете в поле поставщика), можно ввести эту цену</span><span class="sxs-lookup"><span data-stu-id="e3c6e-160">If you know the price for a particular vendor (that you select in the vendor account field) then that price can be entered</span></span>   
17. <span data-ttu-id="e3c6e-161">В поле "Счет поставщика" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-161">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e3c6e-162">Поставщики, доступные в этом поле, зависят от политик закупок и статуса, который поставщик имеет для текущей категории закупаемой продукции.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-162">The vendors that are available in this field depend on the purchasing policies and the status that the vendor has for the current procurement category.</span></span> <span data-ttu-id="e3c6e-163">В качестве альтернативы выбору здесь поставщика можно нажать кнопку "Предложить поставщиков".</span><span class="sxs-lookup"><span data-stu-id="e3c6e-163">As an alternative to selecting a vendor here, you can click the Suggest vendor button.</span></span>    
18. <span data-ttu-id="e3c6e-164">Выберите в списке поставщика, которого вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-164">In the list, select the vendor you want to use.</span></span>
19. <span data-ttu-id="e3c6e-165">В поле "Внешний код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-165">In the External item number field, type a value.</span></span>
    * <span data-ttu-id="e3c6e-166">Это номер ссылки на продукт, который известен поставщику.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-166">This is a reference number for the product that is known by the vendor.</span></span> <span data-ttu-id="e3c6e-167">Например, это может быть номер номенклатуры продукта в собственном каталоге поставщика.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-167">For example, this could be the item number of the product in the vendor's own catalog.</span></span>  
20. <span data-ttu-id="e3c6e-168">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e3c6e-168">Click OK.</span></span>

## <a name="distribute-amounts"></a><span data-ttu-id="e3c6e-169">Распределить суммы</span><span class="sxs-lookup"><span data-stu-id="e3c6e-169">Distribute amounts</span></span>
1. <span data-ttu-id="e3c6e-170">Щелкните "Статистика".</span><span class="sxs-lookup"><span data-stu-id="e3c6e-170">Click Financials.</span></span>
2. <span data-ttu-id="e3c6e-171">Щелкните "Распределить суммы".</span><span class="sxs-lookup"><span data-stu-id="e3c6e-171">Click Distribute amounts.</span></span>
    * <span data-ttu-id="e3c6e-172">Этот процесс показывает, как распределить затраты для первой строки между двумя счетами.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-172">This process shows you how to distribute the cost for the first line between 2 accounts.</span></span> <span data-ttu-id="e3c6e-173">Это можно также сделать позже, когда заявка будет находиться на этапе рассмотрения.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-173">This can also be done later when the requisition is in review.</span></span>  
3. <span data-ttu-id="e3c6e-174">Щелкните "Разбиение", чтобы создать новую строку распределения.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-174">Click Split to create a new distribution line.</span></span>
4. <span data-ttu-id="e3c6e-175">В поле "Счет ГК" выберите первый центр затрат, на который будет отнесена часть затрат.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-175">In the Ledger account field select the first cost center that should take part of the cost.</span></span>
5. <span data-ttu-id="e3c6e-176">Выберите вторую строку распределения.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-176">Select the other distribution line.</span></span>
6. <span data-ttu-id="e3c6e-177">В поле "Счет ГК" укажите второй центр затрат.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-177">In the Ledger account field specify the other cost center.</span></span>
7. <span data-ttu-id="e3c6e-178">Щелкните "Распределить поровну".</span><span class="sxs-lookup"><span data-stu-id="e3c6e-178">Click Distribute equally.</span></span>
8. <span data-ttu-id="e3c6e-179">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-179">Close the page.</span></span>

## <a name="view-line-details"></a><span data-ttu-id="e3c6e-180">Посмотреть сведения о строке</span><span class="sxs-lookup"><span data-stu-id="e3c6e-180">View line details</span></span>
1. <span data-ttu-id="e3c6e-181">Переключите развертывание раздела "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="e3c6e-181">Toggle the expansion of the Line details section.</span></span>

## <a name="submit-the-requisition"></a><span data-ttu-id="e3c6e-182">Отправка заявки</span><span class="sxs-lookup"><span data-stu-id="e3c6e-182">Submit the requisition</span></span>
1. <span data-ttu-id="e3c6e-183">Щелкните "Документооборот", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-183">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="e3c6e-184">Щелкните Отправить.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-184">Click Submit.</span></span>
3. <span data-ttu-id="e3c6e-185">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-185">Close the page.</span></span>
4. <span data-ttu-id="e3c6e-186">В поле "Комментарий" введите примечание для пользователя, который будет утверждать заявку.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-186">In the Comment field, type a note for the approver of the requisition.</span></span>
5. <span data-ttu-id="e3c6e-187">Щелкните Отправить.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-187">Click Submit.</span></span>
6. <span data-ttu-id="e3c6e-188">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-188">Close the page.</span></span>
7. <span data-ttu-id="e3c6e-189">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-189">Refresh the page.</span></span>

