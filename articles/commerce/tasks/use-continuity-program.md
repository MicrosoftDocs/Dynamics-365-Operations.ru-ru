---
title: Использование программы непрерывности
description: Эта процедура демонстрирует продажу в программе непрерывности и обработку соответствующих заказов на продажу.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1de6d2cd88ba31f526621497d6fab36db631933e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232649"
---
# <a name="using-continuity-program"></a><span data-ttu-id="485f7-103">Использование программы непрерывности</span><span class="sxs-lookup"><span data-stu-id="485f7-103">Using continuity program</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="485f7-104">Эта процедура демонстрирует продажу в программе непрерывности и обработку соответствующих заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="485f7-104">This procedure walks through selling a continuity program and processing related sales orders.</span></span> <span data-ttu-id="485f7-105">Чтобы выполнить эту процедуру, пользователь должен быть настроен в качестве пользователя центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="485f7-105">To complete this procedure, the user has to be set up as a call center user.</span></span> <span data-ttu-id="485f7-106">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="485f7-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="485f7-107">Перейдите в раздел "Retail и Commerce" > "Клиенты" > "Обслуживание клиентов".</span><span class="sxs-lookup"><span data-stu-id="485f7-107">Go to Retail and Commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="485f7-108">В поле SearchText введите "Karen" и нажмите клавишу TAB.</span><span class="sxs-lookup"><span data-stu-id="485f7-108">In the SearchText field, type 'Karen' and then press the Tab key.</span></span>
    * <span data-ttu-id="485f7-109">Открывается диалоговое окно расширенного поиска.</span><span class="sxs-lookup"><span data-stu-id="485f7-109">The advanced search dialog should pop up.</span></span> <span data-ttu-id="485f7-110">Если оно не открылось, нажмите кнопку "Поиск" справа от этого поля.</span><span class="sxs-lookup"><span data-stu-id="485f7-110">If it doesn't, click Search to the right of this field.</span></span>  
3. <span data-ttu-id="485f7-111">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="485f7-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="485f7-112">Должна быть только одна строка, в которой отображается имя Karen Berg.</span><span class="sxs-lookup"><span data-stu-id="485f7-112">There should be only one row with Karen Berg showing.</span></span> <span data-ttu-id="485f7-113">Выберите эту строку, нажав в столбце с флажками с левого края сетки.</span><span class="sxs-lookup"><span data-stu-id="485f7-113">Select the row by clicking on the checkmark column on the far left of the grid.</span></span>  
4. <span data-ttu-id="485f7-114">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="485f7-114">Click Select.</span></span>
5. <span data-ttu-id="485f7-115">Щелкните "Новый заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="485f7-115">Click New sales order.</span></span>
    * <span data-ttu-id="485f7-116">Рекомендуется записать номер заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="485f7-116">It's a good idea to note the sales order number.</span></span> <span data-ttu-id="485f7-117">Он придется позже в этой процедуре.</span><span class="sxs-lookup"><span data-stu-id="485f7-117">You'll need it later in this procedure.</span></span>  
6. <span data-ttu-id="485f7-118">В поле "Код номенклатуры" введите "88000", затем нажмите клавишу TAB.</span><span class="sxs-lookup"><span data-stu-id="485f7-118">In the Item number field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="485f7-119">Это номенклатура непрерывности в демонстрационных данных USRT.</span><span class="sxs-lookup"><span data-stu-id="485f7-119">This is a continuity item in the USRT demo data.</span></span>  
7. <span data-ttu-id="485f7-120">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="485f7-120">Click Complete.</span></span>
8. <span data-ttu-id="485f7-121">В поле "Способ платежа" введите "Visa".</span><span class="sxs-lookup"><span data-stu-id="485f7-121">In the Payment method field, enter 'Visa'.</span></span>
9. <span data-ttu-id="485f7-122">Нажмите "Добавить кредитную карту".</span><span class="sxs-lookup"><span data-stu-id="485f7-122">Click Add credit card.</span></span>
    * <span data-ttu-id="485f7-123">Введите требуемые сведения о кредитной карте на этой странице.</span><span class="sxs-lookup"><span data-stu-id="485f7-123">Enter the required credit card information on this page.</span></span>  
10. <span data-ttu-id="485f7-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="485f7-124">Click OK.</span></span>
11. <span data-ttu-id="485f7-125">Разверните раздел "Платеж".</span><span class="sxs-lookup"><span data-stu-id="485f7-125">Expand the Payment section.</span></span>
    * <span data-ttu-id="485f7-126">Чтобы отправить заказ центра обработки вызовов, необходимо ввести платежи для заказа.</span><span class="sxs-lookup"><span data-stu-id="485f7-126">To submit a call center order, payments have to be entered for the order.</span></span>  
12. <span data-ttu-id="485f7-127">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="485f7-127">Click OK.</span></span>
13. <span data-ttu-id="485f7-128">Щелкните Отправить.</span><span class="sxs-lookup"><span data-stu-id="485f7-128">Click Submit.</span></span>
    * <span data-ttu-id="485f7-129">Создание нового заказа непрерывности завершено.</span><span class="sxs-lookup"><span data-stu-id="485f7-129">You're done creating a new continuity order.</span></span> <span data-ttu-id="485f7-130">Далее вы запустите два процесса пакетной обработки, используемые для обработки заказов непрерывности.</span><span class="sxs-lookup"><span data-stu-id="485f7-130">Next, you'll run two batch processes that are used to process the continuity orders.</span></span>  
14. <span data-ttu-id="485f7-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="485f7-131">Close the page.</span></span>
15. <span data-ttu-id="485f7-132">Перейдите в раздел "Retail и Commerce" > "Непрерывность" > "Обработать платежи непрерывности".</span><span class="sxs-lookup"><span data-stu-id="485f7-132">Go to Retail and Commerce > Continuity > Process continuity payments.</span></span>
16. <span data-ttu-id="485f7-133">В поле "Номенклатура непрерывности" введите "88000", затем нажмите клавишу TAB.</span><span class="sxs-lookup"><span data-stu-id="485f7-133">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
17. <span data-ttu-id="485f7-134">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="485f7-134">Click OK.</span></span>
18. <span data-ttu-id="485f7-135">Перейдите в раздел "Retail и Commerce" > "Непрерывность" > "Создать дочерние непрерывные заказы".</span><span class="sxs-lookup"><span data-stu-id="485f7-135">Go to Retail and Commerce > Continuity > Create continuity child orders.</span></span>
    * <span data-ttu-id="485f7-136">Этот процесс создаст новые заказы на продажу на основании настроек ваших программ непрерывности.</span><span class="sxs-lookup"><span data-stu-id="485f7-136">This process will create new sales orders based on the settings of your continuity programs.</span></span>  
19. <span data-ttu-id="485f7-137">В поле "Номенклатура непрерывности" введите "88000", затем нажмите клавишу TAB.</span><span class="sxs-lookup"><span data-stu-id="485f7-137">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="485f7-138">Номенклатура "88000" является номенклатурой непрерывности в демонстрационных данных USRT.</span><span class="sxs-lookup"><span data-stu-id="485f7-138">Item '88000' is a continuity item in the USRT demo data.</span></span>  
20. <span data-ttu-id="485f7-139">В поле "Заказ на продажу" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="485f7-139">In the Sales order field, enter or select a value.</span></span>
    * <span data-ttu-id="485f7-140">Введите номер заказа на продажу, который записали ранее в этой процедуре.</span><span class="sxs-lookup"><span data-stu-id="485f7-140">Enter the sales order number that you noted earlier in the procedure.</span></span> <span data-ttu-id="485f7-141">Это сведет к минимуму время обработки для этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="485f7-141">This will keep the processing time to a minimal for this procedure.</span></span> <span data-ttu-id="485f7-142">Поле "Заказ на продажу" не является обязательным — можно обработать все заказы для любой одной программы.</span><span class="sxs-lookup"><span data-stu-id="485f7-142">The Sales order field field is optional--you could process all orders for any one program.</span></span>  
21. <span data-ttu-id="485f7-143">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="485f7-143">Click OK.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]