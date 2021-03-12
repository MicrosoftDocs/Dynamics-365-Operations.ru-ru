---
title: Настройка профиля обзора поступления номенклатуры
description: В этой теме основное внимание уделяется настройке профиля обзора прибытия.
author: ShylaThompson
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ecfe132d9b0e096c5fdf015f80a6efb34c9b178
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961444"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="1d54c-103">Настройка профиля обзора поступления номенклатуры</span><span class="sxs-lookup"><span data-stu-id="1d54c-103">Set up an item arrival overview profile</span></span>

<span data-ttu-id="1d54c-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="1d54c-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="1d54c-105">В этой теме основное внимание уделяется настройке профиля обзора прибытия.</span><span class="sxs-lookup"><span data-stu-id="1d54c-105">This topic focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="1d54c-106">Профиль обзора прибытия — это коллекция правил, которые будут применяться при открытии пользователем страницы "Обзор прибытия".</span><span class="sxs-lookup"><span data-stu-id="1d54c-106">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="1d54c-107">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="1d54c-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="1d54c-108">Обычно эту процедуру выполняет сотрудник, ответственный за приемку.</span><span class="sxs-lookup"><span data-stu-id="1d54c-108">This procedure would typically be carried out by a receiving clerk.</span></span>

1. <span data-ttu-id="1d54c-109">В области перехода перейдите к **Модули > Управление запасами > Настройка > Распределение > Профили обзора прибытия**.</span><span class="sxs-lookup"><span data-stu-id="1d54c-109">In the navigation pane, go to **Modules > Inventory management > Setup > Distribution > Arrival overview profiles**.</span></span>
2. <span data-ttu-id="1d54c-110">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1d54c-110">Select **New**.</span></span> <span data-ttu-id="1d54c-111">Поскольку вы практически всегда будете работать на одном и том же складе и разгружать полностью загруженные грузовики, вам следует создать профиль обзора прибытия для упрощения процесса регистрации полученных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="1d54c-111">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="1d54c-112">В поле **Имя профиля обзора прибытия** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1d54c-112">In the **Arrival overview profile name** field, type a value.</span></span>
4. <span data-ttu-id="1d54c-113">В поле **Показать строки** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="1d54c-113">In the **Show lines** field, select an option.</span></span> <span data-ttu-id="1d54c-114">Выбор строк, которые необходимо отображать в приходах:</span><span class="sxs-lookup"><span data-stu-id="1d54c-114">Select which lines to show for the receipts:</span></span>  

    - <span data-ttu-id="1d54c-115">**Все** — отображение всех строк вне зависимости от статуса.</span><span class="sxs-lookup"><span data-stu-id="1d54c-115">**All** – Show all lines, regardless of status.</span></span>   
    - <span data-ttu-id="1d54c-116">**В обработке** — отображение строк для приходов со степенью выполнения "Завершено" и "Частично".</span><span class="sxs-lookup"><span data-stu-id="1d54c-116">**In progress** – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="1d54c-117">Это значит, что для каждой строки всё количество или его часть зарегистрированы в журнале прихода.</span><span class="sxs-lookup"><span data-stu-id="1d54c-117">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   
    - <span data-ttu-id="1d54c-118">**Не завершено** — отображение строк для приходов со степенью выполнения "Нет" и "Частично".</span><span class="sxs-lookup"><span data-stu-id="1d54c-118">**Not complete** – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="1d54c-119">Это значит, что для каждой строки в журнале прихода зарегистрирована лишь часть количества, или количество не зарегистрировано вовсе.</span><span class="sxs-lookup"><span data-stu-id="1d54c-119">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  

5. <span data-ttu-id="1d54c-120">Разверните или сверните раздел **Параметры прибытия**.</span><span class="sxs-lookup"><span data-stu-id="1d54c-120">Expand or collapse the **Arrival options** section.</span></span>
6. <span data-ttu-id="1d54c-121">В поле **Дней вперед** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1d54c-121">In the **Days forward** field, type a value.</span></span> <span data-ttu-id="1d54c-122">В результате будет установлен фильтр для отображения строк прихода, получение которых ожидается в течение следующих нескольких дней (в зависимости от заданного вами числа).</span><span class="sxs-lookup"><span data-stu-id="1d54c-122">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="1d54c-123">В поле **Дней назад** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1d54c-123">In the **Days back** field, type a value.</span></span> <span data-ttu-id="1d54c-124">В результате будет установлен фильтр для отображения строк прихода, получение которых ожидается за определенное количество дней до сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="1d54c-124">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="1d54c-125">В поле **Склады** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1d54c-125">In the **Warehouses** field, type a value.</span></span> <span data-ttu-id="1d54c-126">Отфильтруйте список по одному или нескольким складам.</span><span class="sxs-lookup"><span data-stu-id="1d54c-126">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="1d54c-127">В поле **Способ поставки** выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1d54c-127">In the **Mode of delivery** field, select a value.</span></span> <span data-ttu-id="1d54c-128">В результате будет установлен фильтр для отображения только строк приходов с этим способом поставки.</span><span class="sxs-lookup"><span data-stu-id="1d54c-128">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="1d54c-129">В поле **Имя** выберите WHS.</span><span class="sxs-lookup"><span data-stu-id="1d54c-129">In the **Name** field, select WHS.</span></span>
11. <span data-ttu-id="1d54c-130">В поле **Склад** выберите склад 24.</span><span class="sxs-lookup"><span data-stu-id="1d54c-130">In the **Warehouse** field, select warehouse 24.</span></span> <span data-ttu-id="1d54c-131">Это склад по умолчанию, который будет использоваться для зарегистрированных строк прихода, в которых используется данный профиль.</span><span class="sxs-lookup"><span data-stu-id="1d54c-131">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="1d54c-132">В поле **Местонахождение** выберите **Поднимающаяся дверь**.</span><span class="sxs-lookup"><span data-stu-id="1d54c-132">In the **Location** field, select **Baydoor**.</span></span> <span data-ttu-id="1d54c-133">Это местонахождение по умолчанию, который будет использоваться для зарегистрированных строк прихода, в которых используется данный профиль.</span><span class="sxs-lookup"><span data-stu-id="1d54c-133">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="1d54c-134">Разверните или сверните раздел **Сведения о запросе прибытия**.</span><span class="sxs-lookup"><span data-stu-id="1d54c-134">Expand or collapse the **Arrival query details** section.</span></span>
14. <span data-ttu-id="1d54c-135">В поле **Ограничить по сайту** выберите сайт 2.</span><span class="sxs-lookup"><span data-stu-id="1d54c-135">In the **Restrict to site** field, select site 2.</span></span> <span data-ttu-id="1d54c-136">В результате будет установлен фильтр для отображения только строк приходов с этим сайтом.</span><span class="sxs-lookup"><span data-stu-id="1d54c-136">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="1d54c-137">Установите для параметра **Заказы на покупку** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="1d54c-137">Set the **Purchase orders** option to **Yes**.</span></span> <span data-ttu-id="1d54c-138">Выберите строки прихода из заказов на покупку.</span><span class="sxs-lookup"><span data-stu-id="1d54c-138">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="1d54c-139">Установите для параметра **Заказы на перемещение** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="1d54c-139">Set the **Transfer** orders option to **Yes**.</span></span> <span data-ttu-id="1d54c-140">Выберите строки прихода из заказов на перемещение.</span><span class="sxs-lookup"><span data-stu-id="1d54c-140">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="1d54c-141">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1d54c-141">Select **Save**.</span></span>
18. <span data-ttu-id="1d54c-142">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1d54c-142">Close the page.</span></span>

