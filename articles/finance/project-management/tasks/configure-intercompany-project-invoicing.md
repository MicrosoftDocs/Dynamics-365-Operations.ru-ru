---
title: Настройка внутрихолдингового выставления накладных по проектам
description: В этой теме показано, как настроить выставление накладных по проекту между двумя компаниями в организации.
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c89b17c09a4f145b5a4ca9cdd127b4e635447d4b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174451"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="336d7-103">Настройка внутрихолдингового выставления накладных по проектам</span><span class="sxs-lookup"><span data-stu-id="336d7-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="336d7-104">В этой теме показано, как настроить выставление накладных по проекту между двумя компаниями в организации.</span><span class="sxs-lookup"><span data-stu-id="336d7-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="336d7-105">В этой задаче используется набор данных компании USSI.</span><span class="sxs-lookup"><span data-stu-id="336d7-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="336d7-106">В области переходов выберите **Модули > Расчеты с поставщиками > Поставщики > Все поставщики**.</span><span class="sxs-lookup"><span data-stu-id="336d7-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="336d7-107">В списке **Все поставщики** найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="336d7-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="336d7-108">На панели операций выберите **Общее**.</span><span class="sxs-lookup"><span data-stu-id="336d7-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="336d7-109">Выберите **Внутрихолдинговый**.</span><span class="sxs-lookup"><span data-stu-id="336d7-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="336d7-110">Установите для параметра **Активно** значение **Да**, чтобы включить внутрихолдинговые торговые отношения.</span><span class="sxs-lookup"><span data-stu-id="336d7-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="336d7-111">В поле **Компания-клиент** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="336d7-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="336d7-112">В поле **Мой счет** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="336d7-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="336d7-113">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="336d7-113">Select **Save**.</span></span>
9. <span data-ttu-id="336d7-114">Закройте страницы и вернитесь на домашнюю страницу.</span><span class="sxs-lookup"><span data-stu-id="336d7-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="336d7-115">В области переходов выберите **Модули > Управление и учет по проектам > Настройка > Параметры модуля "Управление и учет по проектам**.</span><span class="sxs-lookup"><span data-stu-id="336d7-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="336d7-116">Выберите вкладку **Внутрихолдинговый**.</span><span class="sxs-lookup"><span data-stu-id="336d7-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="336d7-117">Переместите ползунок в положение **Да**, чтобы включить планирование и графики внутрихолдинговых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="336d7-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="336d7-118">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="336d7-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="336d7-119">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="336d7-119">Select **New**.</span></span>
15. <span data-ttu-id="336d7-120">В поле **Получающее юридическое лицо** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="336d7-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="336d7-121">Установите флажок **Начислить выручку**.</span><span class="sxs-lookup"><span data-stu-id="336d7-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="336d7-122">В поле **Категория табеля учета рабочего времени по умолчанию** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="336d7-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="336d7-123">В поле **Категория расходов по умолчанию** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="336d7-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="336d7-124">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="336d7-124">Select **Save**.</span></span>
20. <span data-ttu-id="336d7-125">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="336d7-125">Close the page.</span></span>
21. <span data-ttu-id="336d7-126">В области переходов выберите **Модули > Управление и учет по проектам > Настройка > Разноска > Настройка разноски ГК**.</span><span class="sxs-lookup"><span data-stu-id="336d7-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="336d7-127">В поле **Типы счетов ГК** выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="336d7-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="336d7-128">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="336d7-128">Select **New**.</span></span>
24. <span data-ttu-id="336d7-129">В поле **Счет ГК** в новой строке укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="336d7-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="336d7-130">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="336d7-130">Select **Save**.</span></span>
26. <span data-ttu-id="336d7-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="336d7-131">Close the page.</span></span>
27. <span data-ttu-id="336d7-132">В области переходов выберите **Модули > Управление и учет по проектам > Настройка > Цены > Трансферная цена**.</span><span class="sxs-lookup"><span data-stu-id="336d7-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="336d7-133">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="336d7-133">Select **New**.</span></span>
29. <span data-ttu-id="336d7-134">В поле **Действует с** введите дату.</span><span class="sxs-lookup"><span data-stu-id="336d7-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="336d7-135">В поле **Получающее юридическое лицо** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="336d7-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="336d7-136">В поле **Модель трансферных цен** выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="336d7-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="336d7-137">В поле **Ценообразование** введите число.</span><span class="sxs-lookup"><span data-stu-id="336d7-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="336d7-138">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="336d7-138">Select **Save**.</span></span>

