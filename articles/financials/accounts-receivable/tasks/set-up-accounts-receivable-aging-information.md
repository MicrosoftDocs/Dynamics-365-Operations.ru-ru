--- 
title: "Настройка и создание сведений о распределении по срокам для расчетов с клиентами"
description: "Это руководство поможет настроить определение периода распределения по срокам, распределить сальдо клиента по срокам и просмотреть сальдо в списке \"Сальдо с распределением по срокам\" и на странице \"Сборы\"."
author: mikefalkner
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 47402c31ac24f4276288e8957911d30ae98b5643
ms.contentlocale: ru-ru
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a><span data-ttu-id="36d0c-103">Настройка и создание сведений о распределении по срокам для расчетов с клиентами</span><span class="sxs-lookup"><span data-stu-id="36d0c-103">Set up and generate accounts receivable aging information</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="36d0c-104">Это руководство поможет настроить определение периода распределения по срокам, распределить сальдо клиента по срокам и просмотреть сальдо в списке "Сальдо с распределением по срокам" и на странице "Сборы".</span><span class="sxs-lookup"><span data-stu-id="36d0c-104">This guide will help you set up an aging period definition, age customer balances, and view balances in the Aged balance list and the Collections page.</span></span> <span data-ttu-id="36d0c-105">В данной записи используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="36d0c-105">This recording uses the USMF demo company.</span></span>


## <a name="create-an-aging-period-definition"></a><span data-ttu-id="36d0c-106">Создание определения периода распределения по срокам</span><span class="sxs-lookup"><span data-stu-id="36d0c-106">Create an aging period definition</span></span>
1. <span data-ttu-id="36d0c-107">Перейдите в раздел "Кредит и сборы" > "Настройка" > "Определения периодов распределения по срокам".</span><span class="sxs-lookup"><span data-stu-id="36d0c-107">Go to Credit and collections > Setup > Aging period definitions.</span></span>
2. <span data-ttu-id="36d0c-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="36d0c-108">Click New.</span></span>
3. <span data-ttu-id="36d0c-109">В поле "Определение периода распределения по срокам" введите значение.</span><span class="sxs-lookup"><span data-stu-id="36d0c-109">In the Aging period definition field, type a value.</span></span>
4. <span data-ttu-id="36d0c-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="36d0c-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="36d0c-111">Щелкните "Добавить ниже", чтобы вставить новый период распределения по срокам.</span><span class="sxs-lookup"><span data-stu-id="36d0c-111">Click Add below to insert a new aging period.</span></span>
6. <span data-ttu-id="36d0c-112">В поле "Период" введите описание для отображения в отчетах по распределению по срокам.</span><span class="sxs-lookup"><span data-stu-id="36d0c-112">In the Period field, enter the description to show on aging reports.</span></span>
7. <span data-ttu-id="36d0c-113">В поле "Единица измерения" введите число.</span><span class="sxs-lookup"><span data-stu-id="36d0c-113">In the Unit field, enter a number.</span></span>
8. <span data-ttu-id="36d0c-114">В поле "Интервал" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="36d0c-114">In the Interval field, select an option.</span></span>
    * <span data-ttu-id="36d0c-115">Период ГК соответствует периоду календаря главной книги.</span><span class="sxs-lookup"><span data-stu-id="36d0c-115">Ledger period matches the period to your ledger calendar.</span></span> <span data-ttu-id="36d0c-116">День, неделя, месяц, квартал и годы определяют продолжительность интервала по типу даты.</span><span class="sxs-lookup"><span data-stu-id="36d0c-116">Day, week, month, quarter and years define the size of the interval by date type.</span></span> <span data-ttu-id="36d0c-117">При выборе параметра "Неограниченно" будут выбраны все проводки до или после предыдущего периода в зависимости от того, первый это период или последний.</span><span class="sxs-lookup"><span data-stu-id="36d0c-117">Unlimited selects all transactions before or after the previous period, depending on whether it is the first or last period.</span></span>  
9. <span data-ttu-id="36d0c-118">В поле "Индикатор распределения по срокам" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="36d0c-118">In the Aging indicator field, select an option.</span></span>
10. <span data-ttu-id="36d0c-119">Выберите период в верхней части сетки.</span><span class="sxs-lookup"><span data-stu-id="36d0c-119">Select the period at the top of the grid.</span></span> <span data-ttu-id="36d0c-120">Обновление описания для описания самого раннего периода в определении периода распределения по срокам</span><span class="sxs-lookup"><span data-stu-id="36d0c-120">Update the description to describe the oldest period in the aging period definition</span></span>
11. <span data-ttu-id="36d0c-121">В поле "Период" введите новое описание периода распределения по срокам.</span><span class="sxs-lookup"><span data-stu-id="36d0c-121">In the Period field, enter the new description of the aging period.</span></span>
12. <span data-ttu-id="36d0c-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="36d0c-122">Close the page.</span></span>

## <a name="age-the-balances"></a><span data-ttu-id="36d0c-123">Распределение сальдо по срокам</span><span class="sxs-lookup"><span data-stu-id="36d0c-123">Age the balances</span></span>
1. <span data-ttu-id="36d0c-124">Перейдите в раздел "Кредит и сборы" > "Периодические задачи" > "Распределить сальдо клиента по срокам".</span><span class="sxs-lookup"><span data-stu-id="36d0c-124">Go to Credit and collections > Periodic tasks > Age customer balances.</span></span>
2. <span data-ttu-id="36d0c-125">В поле "Определение периода распределения по срокам" выберите созданное определение периода распределения по срокам.</span><span class="sxs-lookup"><span data-stu-id="36d0c-125">In the Aging period definition field, select the aging period definition that you created.</span></span>
    * <span data-ttu-id="36d0c-126">Можно иметь один активный снимок для каждого определения периода распределения по срокам.</span><span class="sxs-lookup"><span data-stu-id="36d0c-126">You can have one active snapshot for each aging period definition.</span></span>  
    * <span data-ttu-id="36d0c-127">Все клиенты обрабатываются по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="36d0c-127">All customers are processed by default.</span></span> <span data-ttu-id="36d0c-128">Этот параметр можно использовать для расчета одного кластера сборов клиентов.</span><span class="sxs-lookup"><span data-stu-id="36d0c-128">You can use this selection to calculate a single collections pool of customers.</span></span>  
    * <span data-ttu-id="36d0c-129">Выберите дату из проводки, которая используется для распределения по срокам.</span><span class="sxs-lookup"><span data-stu-id="36d0c-129">Select the date from the transaction that you will use for the aging.</span></span>  
    * <span data-ttu-id="36d0c-130">Выберите дату "по состоянию на" для распределения по срокам.</span><span class="sxs-lookup"><span data-stu-id="36d0c-130">Select an "as of" date for aging.</span></span> <span data-ttu-id="36d0c-131">По умолчанию используется текущая дата, но если изменить значение этого поля на "Выбрано", можно будет выбрать любую дату.</span><span class="sxs-lookup"><span data-stu-id="36d0c-131">The default is today but, if you change this field to Selected date, you will be able to pick the date that you want.</span></span> <span data-ttu-id="36d0c-132">Для пакетной обработки используется значение "Текущая дата".</span><span class="sxs-lookup"><span data-stu-id="36d0c-132">For batch processing, use Today's date.</span></span>  
3. <span data-ttu-id="36d0c-133">Разверните диапазон "Компания".</span><span class="sxs-lookup"><span data-stu-id="36d0c-133">Expand the Company range.</span></span> <span data-ttu-id="36d0c-134">Можно выбрать компании для включения в снимок.</span><span class="sxs-lookup"><span data-stu-id="36d0c-134">You can select the companies that will be included in the snapshot.</span></span> <span data-ttu-id="36d0c-135">Текущая компания выбирается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="36d0c-135">The current company is selected by default.</span></span>
4. <span data-ttu-id="36d0c-136">Нажмите кнопку ОК, чтобы обработать снимок.</span><span class="sxs-lookup"><span data-stu-id="36d0c-136">Click Ok to process the snapshot.</span></span> <span data-ttu-id="36d0c-137">Это займет некоторое время, поэтому подождите, пока не исчезнет ползунок, и проверьте наличие сообщения в центре сообщений.</span><span class="sxs-lookup"><span data-stu-id="36d0c-137">It will take some time so wait for the slider to disappear and check the message center for a message.</span></span>

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a><span data-ttu-id="36d0c-138">Просмотр сальдо в списке "Сальдо по срокам" и на странице "Сбор"</span><span class="sxs-lookup"><span data-stu-id="36d0c-138">View the balances on the Aged balances list and on the Collection page</span></span>
1. <span data-ttu-id="36d0c-139">Перейдите в раздел "Кредит и сборы" > "Сборы" > "Сальдо по срокам".</span><span class="sxs-lookup"><span data-stu-id="36d0c-139">Go to Credit and collections > Collections > Aged balances.</span></span>
    * <span data-ttu-id="36d0c-140">На странице списка отображаются сальдо для клиента.</span><span class="sxs-lookup"><span data-stu-id="36d0c-140">The list page shows the balances for the customer.</span></span> <span data-ttu-id="36d0c-141">Значок распределения по срокам показывает период распределения по срокам для самой ранней проводки.</span><span class="sxs-lookup"><span data-stu-id="36d0c-141">The aging icon shows the aging period for the oldest transaction.</span></span>  
2. <span data-ttu-id="36d0c-142">Выберите клиента с сальдо.</span><span class="sxs-lookup"><span data-stu-id="36d0c-142">Select a customer with a balance.</span></span>
3. <span data-ttu-id="36d0c-143">Разверните информационное поле "Распределение по срокам", чтобы просмотреть сальдо с распределением по срокам.</span><span class="sxs-lookup"><span data-stu-id="36d0c-143">Expand the Aging fact box area to view the aged balances.</span></span>
    * <span data-ttu-id="36d0c-144">Определение периода распределения по срокам для информационного поля берется из определения периода распределения по срокам по умолчанию, указанного в параметрах.</span><span class="sxs-lookup"><span data-stu-id="36d0c-144">The aging period definition for the fact box is taken from the default aging period definition specified in the parameters.</span></span> <span data-ttu-id="36d0c-145">Его можно изменить с помощью меню "Сбор".</span><span class="sxs-lookup"><span data-stu-id="36d0c-145">You can change it using the Collect menu.</span></span>  


