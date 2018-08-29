--- 
title: "Программы непрерывности продаж и обработка соответствующих заказов на продажу"
description: "Эта процедура демонстрирует продажу в программе непрерывности и обработку соответствующих заказов на продажу."
author: scott-tucker
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 5fe1823c9b684bbc5ac5bd0871cc5c0a0e6ce678
ms.contentlocale: ru-ru
ms.lasthandoff: 08/09/2018

---
# <a name="selling-continuity-programs-and-processing-related-sales-orders"></a><span data-ttu-id="5affc-103">Программы непрерывности продаж и обработка соответствующих заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="5affc-103">Selling continuity programs and processing related sales orders</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="5affc-104">Эта процедура демонстрирует продажу в программе непрерывности и обработку соответствующих заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="5affc-104">This procedure walks through selling a continuity program and processing related sales orders.</span></span> <span data-ttu-id="5affc-105">Чтобы выполнить эту процедуру, пользователь должен быть настроен в качестве пользователя центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="5affc-105">To complete this procedure, the user has to be set up as a call center user.</span></span> <span data-ttu-id="5affc-106">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="5affc-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="5affc-107">Перейдите в раздел "Розничная торговля и коммерция" > "Клиенты" > "Обслуживание клиентов".</span><span class="sxs-lookup"><span data-stu-id="5affc-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="5affc-108">В поле SearchText введите "Karen" и нажмите клавишу TAB.</span><span class="sxs-lookup"><span data-stu-id="5affc-108">In the SearchText field, type 'Karen' and then press the Tab key.</span></span>
    * <span data-ttu-id="5affc-109">Открывается диалоговое окно расширенного поиска.</span><span class="sxs-lookup"><span data-stu-id="5affc-109">The advanced search dialog should pop up.</span></span> <span data-ttu-id="5affc-110">Если оно не открылось, нажмите кнопку "Поиск" справа от этого поля.</span><span class="sxs-lookup"><span data-stu-id="5affc-110">If it doesn't, click Search to the right of this field.</span></span>  
3. <span data-ttu-id="5affc-111">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5affc-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5affc-112">Должна быть только одна строка, в которой отображается имя Karen Berg.</span><span class="sxs-lookup"><span data-stu-id="5affc-112">There should be only one row with Karen Berg showing.</span></span> <span data-ttu-id="5affc-113">Выберите эту строку, нажав в столбце с флажками с левого края сетки.</span><span class="sxs-lookup"><span data-stu-id="5affc-113">Select the row by clicking on the checkmark column on the far left of the grid.</span></span>  
4. <span data-ttu-id="5affc-114">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="5affc-114">Click Select.</span></span>
5. <span data-ttu-id="5affc-115">Щелкните "Новый заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="5affc-115">Click New sales order.</span></span>
    * <span data-ttu-id="5affc-116">Рекомендуется записать номер заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="5affc-116">It's a good idea to note the sales order number.</span></span> <span data-ttu-id="5affc-117">Он придется позже в этой процедуре.</span><span class="sxs-lookup"><span data-stu-id="5affc-117">You'll need it later in this procedure.</span></span>  
6. <span data-ttu-id="5affc-118">В поле "Код номенклатуры" введите "88000", затем нажмите клавишу TAB.</span><span class="sxs-lookup"><span data-stu-id="5affc-118">In the Item number field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="5affc-119">Это номенклатура непрерывности в демонстрационных данных USRT.</span><span class="sxs-lookup"><span data-stu-id="5affc-119">This is a continuity item in the USRT demo data.</span></span>  
7. <span data-ttu-id="5affc-120">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="5affc-120">Click Complete.</span></span>
8. <span data-ttu-id="5affc-121">В поле "Способ платежа" введите "Visa".</span><span class="sxs-lookup"><span data-stu-id="5affc-121">In the Payment method field, enter 'Visa'.</span></span>
9. <span data-ttu-id="5affc-122">Нажмите "Добавить кредитную карту".</span><span class="sxs-lookup"><span data-stu-id="5affc-122">Click Add credit card.</span></span>
    * <span data-ttu-id="5affc-123">Введите требуемые сведения о кредитной карте на этой странице.</span><span class="sxs-lookup"><span data-stu-id="5affc-123">Enter the required credit card information on this page.</span></span>  
10. <span data-ttu-id="5affc-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="5affc-124">Click OK.</span></span>
11. <span data-ttu-id="5affc-125">Разверните раздел "Платеж".</span><span class="sxs-lookup"><span data-stu-id="5affc-125">Expand the Payment section.</span></span>
    * <span data-ttu-id="5affc-126">Чтобы отправить заказ центра обработки вызовов, необходимо ввести платежи для заказа.</span><span class="sxs-lookup"><span data-stu-id="5affc-126">To submit a call center order, payments have to be entered for the order.</span></span>  
12. <span data-ttu-id="5affc-127">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="5affc-127">Click OK.</span></span>
13. <span data-ttu-id="5affc-128">Щелкните Отправить.</span><span class="sxs-lookup"><span data-stu-id="5affc-128">Click Submit.</span></span>
    * <span data-ttu-id="5affc-129">Создание нового заказа непрерывности завершено.</span><span class="sxs-lookup"><span data-stu-id="5affc-129">You're done creating a new continuity order.</span></span> <span data-ttu-id="5affc-130">Далее вы запустите два процесса пакетной обработки, используемые для обработки заказов непрерывности.</span><span class="sxs-lookup"><span data-stu-id="5affc-130">Next, you'll run two batch processes that are used to process the continuity orders.</span></span>  
14. <span data-ttu-id="5affc-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5affc-131">Close the page.</span></span>
15. <span data-ttu-id="5affc-132">Перейдите в раздел "Розничная торговля и коммерция" > "Непрерывность" > "Обработать платежи непрерывности".</span><span class="sxs-lookup"><span data-stu-id="5affc-132">Go to Retail and commerce > Continuity > Process continuity payments.</span></span>
16. <span data-ttu-id="5affc-133">В поле "Номенклатура непрерывности" введите "88000", затем нажмите клавишу TAB.</span><span class="sxs-lookup"><span data-stu-id="5affc-133">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
17. <span data-ttu-id="5affc-134">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="5affc-134">Click OK.</span></span>
18. <span data-ttu-id="5affc-135">Перейдите в раздел "Розничная торговля и коммерция" > "Непрерывность" > "Создать дочерние непрерывные заказы".</span><span class="sxs-lookup"><span data-stu-id="5affc-135">Go to Retail and commerce > Continuity > Create continuity child orders.</span></span>
    * <span data-ttu-id="5affc-136">Этот процесс создаст новые заказы на продажу на основании настроек ваших программ непрерывности.</span><span class="sxs-lookup"><span data-stu-id="5affc-136">This process will create new sales orders based on the settings of your continuity programs.</span></span>  
19. <span data-ttu-id="5affc-137">В поле "Номенклатура непрерывности" введите "88000", затем нажмите клавишу TAB.</span><span class="sxs-lookup"><span data-stu-id="5affc-137">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="5affc-138">Номенклатура "88000" является номенклатурой непрерывности в демонстрационных данных USRT.</span><span class="sxs-lookup"><span data-stu-id="5affc-138">Item '88000' is a continuity item in the USRT demo data.</span></span>  
20. <span data-ttu-id="5affc-139">В поле "Заказ на продажу" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="5affc-139">In the Sales order field, enter or select a value.</span></span>
    * <span data-ttu-id="5affc-140">Введите номер заказа на продажу, который записали ранее в этой процедуре.</span><span class="sxs-lookup"><span data-stu-id="5affc-140">Enter the sales order number that you noted earlier in the procedure.</span></span> <span data-ttu-id="5affc-141">Это сведет к минимуму время обработки для этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="5affc-141">This will keep the processing time to a minimal for this procedure.</span></span> <span data-ttu-id="5affc-142">Поле "Заказ на продажу" не является обязательным — можно обработать все заказы для любой одной программы.</span><span class="sxs-lookup"><span data-stu-id="5affc-142">The Sales order field is optional--you could process all orders for any one program.</span></span>  
21. <span data-ttu-id="5affc-143">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="5affc-143">Click OK.</span></span>


