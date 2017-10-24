---
title: "Настройка профиля обзора поступления номенклатуры"
description: "Эта задача заключается в настройке профиля обзора прибытия."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: b971e72febbd78ff7c27ad2029e5061b978dc44e
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="122ce-103">Настройка профиля обзора поступления номенклатуры</span><span class="sxs-lookup"><span data-stu-id="122ce-103">Set up an item arrival overview profile</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="122ce-104">Эта задача заключается в настройке профиля обзора прибытия.</span><span class="sxs-lookup"><span data-stu-id="122ce-104">This task focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="122ce-105">Профиль обзора прибытия — это коллекция правил, которые будут применяться при открытии пользователем страницы "Обзор прибытия".</span><span class="sxs-lookup"><span data-stu-id="122ce-105">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="122ce-106">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="122ce-106">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="122ce-107">Обычно эту процедуру выполняет сотрудник, ответственный за приемку.</span><span class="sxs-lookup"><span data-stu-id="122ce-107">This procedure would typically be carried out by a receiving clerk.</span></span>





1. <span data-ttu-id="122ce-108">Перейдите в раздел "Управление запасами" > "Настройка" > "Распределение" > "Профили обзора прибытия".</span><span class="sxs-lookup"><span data-stu-id="122ce-108">Go to Inventory management > Setup > Distribution > Arrival overview profiles.</span></span>
2. <span data-ttu-id="122ce-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="122ce-109">Click New.</span></span>
    * <span data-ttu-id="122ce-110">Поскольку вы практически всегда будете работать на одном и том же складе и разгружать полностью загруженные грузовики, вам следует создать профиль обзора прибытия для упрощения процесса регистрации полученных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="122ce-110">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="122ce-111">В поле "Имя профиля обзора прибытия" введите значение.</span><span class="sxs-lookup"><span data-stu-id="122ce-111">In the Arrival overview profile name field, type a value.</span></span>
4. <span data-ttu-id="122ce-112">В поле "Показать строки" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="122ce-112">In the Show lines field, select an option.</span></span>
    * <span data-ttu-id="122ce-113">Выберите, какие строки должны отображаться для приходов:   "Все" — отображение всех строк вне зависимости от статуса.</span><span class="sxs-lookup"><span data-stu-id="122ce-113">Select which lines to show for the receipts:   All – Show all lines, regardless of status.</span></span>   <span data-ttu-id="122ce-114">"В обработке" — отображение строк для приходов со степенью выполнения "Завершено" и "Частично".</span><span class="sxs-lookup"><span data-stu-id="122ce-114">In progress – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="122ce-115">Это значит, что для каждой строки всё количество или его часть зарегистрированы в журнале прихода.</span><span class="sxs-lookup"><span data-stu-id="122ce-115">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   <span data-ttu-id="122ce-116">"Не завершено "— отображение строк для приходов со степенью выполнения "Нет" и "Частично".</span><span class="sxs-lookup"><span data-stu-id="122ce-116">Not complete – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="122ce-117">Это значит, что для каждой строки в журнале прихода зарегистрирована лишь часть количества, или количество не зарегистрировано вовсе.</span><span class="sxs-lookup"><span data-stu-id="122ce-117">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  
5. <span data-ttu-id="122ce-118">Разверните или сверните раздел "Параметры прибытия".</span><span class="sxs-lookup"><span data-stu-id="122ce-118">Expand or collapse the Arrival options section.</span></span>
6. <span data-ttu-id="122ce-119">В поле "Дней вперед" введите значение.</span><span class="sxs-lookup"><span data-stu-id="122ce-119">In the Days forward field, type a value.</span></span>
    * <span data-ttu-id="122ce-120">В результате будет установлен фильтр для отображения строк прихода, получение которых ожидается в течение следующих нескольких дней (в зависимости от заданного вами числа).</span><span class="sxs-lookup"><span data-stu-id="122ce-120">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="122ce-121">В поле "Дней назад" введите значение.</span><span class="sxs-lookup"><span data-stu-id="122ce-121">In the Days back field, type a value.</span></span>
    * <span data-ttu-id="122ce-122">В результате будет установлен фильтр для отображения строк прихода, получение которых ожидается за определенное количество дней до сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="122ce-122">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="122ce-123">В поле "Склады" введите значение.</span><span class="sxs-lookup"><span data-stu-id="122ce-123">In the Warehouses field, type a value.</span></span>
    * <span data-ttu-id="122ce-124">Отфильтруйте список по одному или нескольким складам.</span><span class="sxs-lookup"><span data-stu-id="122ce-124">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="122ce-125">В поле "Способ поставки" выберите значение.</span><span class="sxs-lookup"><span data-stu-id="122ce-125">In the Mode of delivery field, select a value.</span></span>
    * <span data-ttu-id="122ce-126">В результате будет установлен фильтр для отображения только строк приходов с этим способом поставки.</span><span class="sxs-lookup"><span data-stu-id="122ce-126">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="122ce-127">В поле "Имя" выберите "WHS".</span><span class="sxs-lookup"><span data-stu-id="122ce-127">In the Name field, select WHS.</span></span>
11. <span data-ttu-id="122ce-128">В поле "Склад" выберите склад 24.</span><span class="sxs-lookup"><span data-stu-id="122ce-128">In the Warehouse field, select warehouse 24.</span></span>
    * <span data-ttu-id="122ce-129">Это склад по умолчанию, который будет использоваться для зарегистрированных строк прихода, в которых используется данный профиль.</span><span class="sxs-lookup"><span data-stu-id="122ce-129">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="122ce-130">В поле "Местонахождение" выберите "Поднимающаяся дверь".</span><span class="sxs-lookup"><span data-stu-id="122ce-130">In the Location field, select Baydoor.</span></span>
    * <span data-ttu-id="122ce-131">Это местонахождение по умолчанию, который будет использоваться для зарегистрированных строк прихода, в которых используется данный профиль.</span><span class="sxs-lookup"><span data-stu-id="122ce-131">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="122ce-132">Разверните или сверните раздел "Сведения о запросе прибытия".</span><span class="sxs-lookup"><span data-stu-id="122ce-132">Expand or collapse the Arrival query details section.</span></span>
14. <span data-ttu-id="122ce-133">В поле "Ограничить по сайту" выберите сайт 2.</span><span class="sxs-lookup"><span data-stu-id="122ce-133">In the Restrict to site field, select site 2.</span></span>
    * <span data-ttu-id="122ce-134">В результате будет установлен фильтр для отображения только строк приходов с этим сайтом.</span><span class="sxs-lookup"><span data-stu-id="122ce-134">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="122ce-135">Установите для параметра "Заказы на покупку" значение "Да".</span><span class="sxs-lookup"><span data-stu-id="122ce-135">Set the Purchase orders option to Yes.</span></span>
    * <span data-ttu-id="122ce-136">Выберите строки прихода из заказов на покупку.</span><span class="sxs-lookup"><span data-stu-id="122ce-136">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="122ce-137">Установите для параметра "Заказы на перемещение" значение "Да".</span><span class="sxs-lookup"><span data-stu-id="122ce-137">Set the Transfer orders option to Yes.</span></span>
    * <span data-ttu-id="122ce-138">Выберите строки прихода из заказов на перемещение.</span><span class="sxs-lookup"><span data-stu-id="122ce-138">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="122ce-139">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="122ce-139">Click Save.</span></span>
18. <span data-ttu-id="122ce-140">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="122ce-140">Close the page.</span></span>
