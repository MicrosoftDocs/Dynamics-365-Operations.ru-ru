--- 
title: "Настройка внутрихолдингового выставления накладных по проектам"
description: "В этой процедуре показано, как настроить выставление накладных по проекту между двумя компаниями в организации."
author: KimANelson
manager: AnnBe
ms.date: 02/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4de7257ed5e9c9c08ec6cc423c29739a541926d5
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="eb81b-103">Настройка внутрихолдингового выставления накладных по проектам</span><span class="sxs-lookup"><span data-stu-id="eb81b-103">Configure intercompany project invoicing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eb81b-104">В этой процедуре показано, как настроить выставление накладных по проекту между двумя компаниями в организации.</span><span class="sxs-lookup"><span data-stu-id="eb81b-104">This procedure shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="eb81b-105">В этой задаче используется набор данных компании USSI.</span><span class="sxs-lookup"><span data-stu-id="eb81b-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="eb81b-106">Перейдите в раздел "Расчеты с поставщиками" > "Поставщики" > "Все поставщики".</span><span class="sxs-lookup"><span data-stu-id="eb81b-106">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="eb81b-107">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="eb81b-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="eb81b-108">В области действий щелкните "Общее".</span><span class="sxs-lookup"><span data-stu-id="eb81b-108">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="eb81b-109">Щелкните "Внутрихолдинговый".</span><span class="sxs-lookup"><span data-stu-id="eb81b-109">Click Intercompany.</span></span>
5. <span data-ttu-id="eb81b-110">Установите для параметра "Активно" значение "Да", чтобы включить внутрихолдинговые торговые отношения.</span><span class="sxs-lookup"><span data-stu-id="eb81b-110">Set Active to Yes to enable intercompany trading.</span></span>
6. <span data-ttu-id="eb81b-111">В поле "Компания-клиент" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="eb81b-111">In the Customer company field, enter or select a value.</span></span>
7. <span data-ttu-id="eb81b-112">В поле "Мой счет" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="eb81b-112">In the My account field, enter or select a value.</span></span>
8. <span data-ttu-id="eb81b-113">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="eb81b-113">Click Save.</span></span>
9. <span data-ttu-id="eb81b-114">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="eb81b-114">Close the page.</span></span>
10. <span data-ttu-id="eb81b-115">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="eb81b-115">Close the page.</span></span>
11. <span data-ttu-id="eb81b-116">Перейдите в раздел "Управление и учет по проектам" > "Настройка" > «Параметры модуля "Управление и учет по проектам"».</span><span class="sxs-lookup"><span data-stu-id="eb81b-116">Go to Project management and accounting > Setup > Project management and accounting parameters.</span></span>
12. <span data-ttu-id="eb81b-117">Перейдите на вкладку "Внутрихолдинговый".</span><span class="sxs-lookup"><span data-stu-id="eb81b-117">Click the Intercompany tab.</span></span>
13. <span data-ttu-id="eb81b-118">Переместите ползунок в положение "Да", чтобы включить планирование и графики внутрихолдинговых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eb81b-118">Move the slider to Yes to enable intercompany resource scheduling and timesheets.</span></span>
14. <span data-ttu-id="eb81b-119">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="eb81b-119">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="eb81b-120">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="eb81b-120">Click New.</span></span>
16. <span data-ttu-id="eb81b-121">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="eb81b-121">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="eb81b-122">В поле "Получающее юридическое лицо" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="eb81b-122">In the Borrowing legal entity field, enter or select a value.</span></span>
18. <span data-ttu-id="eb81b-123">Установите флажок "Начислить выручку".</span><span class="sxs-lookup"><span data-stu-id="eb81b-123">Select the Accrue revenue check box.</span></span>
19. <span data-ttu-id="eb81b-124">В поле "Категория табеля учета рабочего времени по умолчанию" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="eb81b-124">In the Default timesheet category field, enter or select a value.</span></span>
20. <span data-ttu-id="eb81b-125">В поле "Категория расходов по умолчанию" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="eb81b-125">In the Default expense category field, enter or select a value.</span></span>
21. <span data-ttu-id="eb81b-126">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="eb81b-126">Click Save.</span></span>
22. <span data-ttu-id="eb81b-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="eb81b-127">Close the page.</span></span>
23. <span data-ttu-id="eb81b-128">Перейдите в раздел "Управление и учет по проектам" > "Настройка" > "Разноска" > "Настройка разноски ГК".</span><span class="sxs-lookup"><span data-stu-id="eb81b-128">Go to Project management and accounting > Setup > Posting > Ledger posting setup.</span></span>
24. <span data-ttu-id="eb81b-129">В поле "Типы счетов ГК" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="eb81b-129">In the Ledger account types field, select an option.</span></span>
25. <span data-ttu-id="eb81b-130">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="eb81b-130">Click New.</span></span>
26. <span data-ttu-id="eb81b-131">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="eb81b-131">In the list, mark the selected row.</span></span>
27. <span data-ttu-id="eb81b-132">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="eb81b-132">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="eb81b-133">В поле "Счет ГК" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="eb81b-133">In the Main account field, specify the desired values.</span></span>
29. <span data-ttu-id="eb81b-134">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="eb81b-134">Click Save.</span></span>
30. <span data-ttu-id="eb81b-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="eb81b-135">Close the page.</span></span>
31. <span data-ttu-id="eb81b-136">Перейдите в раздел "Управление и учет по проектам" > "Настройка" > "Цены" > "Трансферная цена".</span><span class="sxs-lookup"><span data-stu-id="eb81b-136">Go to Project management and accounting > Setup > Prices > Transfer price.</span></span>
32. <span data-ttu-id="eb81b-137">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="eb81b-137">Click New.</span></span>
33. <span data-ttu-id="eb81b-138">В поле "Действует с" введите дату.</span><span class="sxs-lookup"><span data-stu-id="eb81b-138">In the Effective date field, enter a date.</span></span>
34. <span data-ttu-id="eb81b-139">В поле "Получающее юридическое лицо" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="eb81b-139">In the Borrowing legal entity field, enter or select a value.</span></span>
35. <span data-ttu-id="eb81b-140">В поле "Модель трансферных цен" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="eb81b-140">In the Transfer price model field, select an option.</span></span>
36. <span data-ttu-id="eb81b-141">В поле "Ценообразование" введите число.</span><span class="sxs-lookup"><span data-stu-id="eb81b-141">In the Pricing field, enter a number.</span></span>
37. <span data-ttu-id="eb81b-142">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="eb81b-142">Click Save.</span></span>


