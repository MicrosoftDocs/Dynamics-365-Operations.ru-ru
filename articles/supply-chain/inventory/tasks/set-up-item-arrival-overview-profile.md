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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 885dc6c4fff53b9c1ddbac64e97b2b415bac1c7a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204064"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="ab32b-103">Настройка профиля обзора поступления номенклатуры</span><span class="sxs-lookup"><span data-stu-id="ab32b-103">Set up an item arrival overview profile</span></span>

<span data-ttu-id="ab32b-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="ab32b-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="ab32b-105">В этой теме основное внимание уделяется настройке профиля обзора прибытия.</span><span class="sxs-lookup"><span data-stu-id="ab32b-105">This topic focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="ab32b-106">Профиль обзора прибытия — это коллекция правил, которые будут применяться при открытии пользователем страницы "Обзор прибытия".</span><span class="sxs-lookup"><span data-stu-id="ab32b-106">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="ab32b-107">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="ab32b-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="ab32b-108">Обычно эту процедуру выполняет сотрудник, ответственный за приемку.</span><span class="sxs-lookup"><span data-stu-id="ab32b-108">This procedure would typically be carried out by a receiving clerk.</span></span>

1. <span data-ttu-id="ab32b-109">В области перехода перейдите к **Модули > Управление запасами > Настройка > Распределение > Профили обзора прибытия**.</span><span class="sxs-lookup"><span data-stu-id="ab32b-109">In the navigation pane, go to **Modules > Inventory management > Setup > Distribution > Arrival overview profiles**.</span></span>
2. <span data-ttu-id="ab32b-110">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ab32b-110">Select **New**.</span></span> <span data-ttu-id="ab32b-111">Поскольку вы практически всегда будете работать на одном и том же складе и разгружать полностью загруженные грузовики, вам следует создать профиль обзора прибытия для упрощения процесса регистрации полученных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="ab32b-111">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="ab32b-112">В поле **Имя профиля обзора прибытия** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ab32b-112">In the **Arrival overview profile name** field, type a value.</span></span>
4. <span data-ttu-id="ab32b-113">В поле **Показать строки** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="ab32b-113">In the **Show lines** field, select an option.</span></span> <span data-ttu-id="ab32b-114">Выбор строк, которые необходимо отображать в приходах:</span><span class="sxs-lookup"><span data-stu-id="ab32b-114">Select which lines to show for the receipts:</span></span>  

    - <span data-ttu-id="ab32b-115">**Все** — отображение всех строк вне зависимости от статуса.</span><span class="sxs-lookup"><span data-stu-id="ab32b-115">**All** – Show all lines, regardless of status.</span></span>   
    - <span data-ttu-id="ab32b-116">**В обработке** — отображение строк для приходов со степенью выполнения "Завершено" и "Частично".</span><span class="sxs-lookup"><span data-stu-id="ab32b-116">**In progress** – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="ab32b-117">Это значит, что для каждой строки всё количество или его часть зарегистрированы в журнале прихода.</span><span class="sxs-lookup"><span data-stu-id="ab32b-117">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   
    - <span data-ttu-id="ab32b-118">**Не завершено** — отображение строк для приходов со степенью выполнения "Нет" и "Частично".</span><span class="sxs-lookup"><span data-stu-id="ab32b-118">**Not complete** – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="ab32b-119">Это значит, что для каждой строки в журнале прихода зарегистрирована лишь часть количества, или количество не зарегистрировано вовсе.</span><span class="sxs-lookup"><span data-stu-id="ab32b-119">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  

5. <span data-ttu-id="ab32b-120">Разверните или сверните раздел **Параметры прибытия**.</span><span class="sxs-lookup"><span data-stu-id="ab32b-120">Expand or collapse the **Arrival options** section.</span></span>
6. <span data-ttu-id="ab32b-121">В поле **Дней вперед** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ab32b-121">In the **Days forward** field, type a value.</span></span> <span data-ttu-id="ab32b-122">В результате будет установлен фильтр для отображения строк прихода, получение которых ожидается в течение следующих нескольких дней (в зависимости от заданного вами числа).</span><span class="sxs-lookup"><span data-stu-id="ab32b-122">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="ab32b-123">В поле **Дней назад** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ab32b-123">In the **Days back** field, type a value.</span></span> <span data-ttu-id="ab32b-124">В результате будет установлен фильтр для отображения строк прихода, получение которых ожидается за определенное количество дней до сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="ab32b-124">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="ab32b-125">В поле **Склады** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ab32b-125">In the **Warehouses** field, type a value.</span></span> <span data-ttu-id="ab32b-126">Отфильтруйте список по одному или нескольким складам.</span><span class="sxs-lookup"><span data-stu-id="ab32b-126">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="ab32b-127">В поле **Способ поставки** выберите значение.</span><span class="sxs-lookup"><span data-stu-id="ab32b-127">In the **Mode of delivery** field, select a value.</span></span> <span data-ttu-id="ab32b-128">В результате будет установлен фильтр для отображения только строк приходов с этим способом поставки.</span><span class="sxs-lookup"><span data-stu-id="ab32b-128">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="ab32b-129">В поле **Имя** выберите WHS.</span><span class="sxs-lookup"><span data-stu-id="ab32b-129">In the **Name** field, select WHS.</span></span>
11. <span data-ttu-id="ab32b-130">В поле **Склад** выберите склад 24.</span><span class="sxs-lookup"><span data-stu-id="ab32b-130">In the **Warehouse** field, select warehouse 24.</span></span> <span data-ttu-id="ab32b-131">Это склад по умолчанию, который будет использоваться для зарегистрированных строк прихода, в которых используется данный профиль.</span><span class="sxs-lookup"><span data-stu-id="ab32b-131">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="ab32b-132">В поле **Местонахождение** выберите **Поднимающаяся дверь**.</span><span class="sxs-lookup"><span data-stu-id="ab32b-132">In the **Location** field, select **Baydoor**.</span></span> <span data-ttu-id="ab32b-133">Это местонахождение по умолчанию, который будет использоваться для зарегистрированных строк прихода, в которых используется данный профиль.</span><span class="sxs-lookup"><span data-stu-id="ab32b-133">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="ab32b-134">Разверните или сверните раздел **Сведения о запросе прибытия**.</span><span class="sxs-lookup"><span data-stu-id="ab32b-134">Expand or collapse the **Arrival query details** section.</span></span>
14. <span data-ttu-id="ab32b-135">В поле **Ограничить по сайту** выберите сайт 2.</span><span class="sxs-lookup"><span data-stu-id="ab32b-135">In the **Restrict to site** field, select site 2.</span></span> <span data-ttu-id="ab32b-136">В результате будет установлен фильтр для отображения только строк приходов с этим сайтом.</span><span class="sxs-lookup"><span data-stu-id="ab32b-136">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="ab32b-137">Установите для параметра **Заказы на покупку** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="ab32b-137">Set the **Purchase orders** option to **Yes**.</span></span> <span data-ttu-id="ab32b-138">Выберите строки прихода из заказов на покупку.</span><span class="sxs-lookup"><span data-stu-id="ab32b-138">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="ab32b-139">Установите для параметра **Заказы на перемещение** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="ab32b-139">Set the **Transfer** orders option to **Yes**.</span></span> <span data-ttu-id="ab32b-140">Выберите строки прихода из заказов на перемещение.</span><span class="sxs-lookup"><span data-stu-id="ab32b-140">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="ab32b-141">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ab32b-141">Select **Save**.</span></span>
18. <span data-ttu-id="ab32b-142">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ab32b-142">Close the page.</span></span>

