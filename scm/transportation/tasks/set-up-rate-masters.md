--- 
title: "Настройка шаблонов ставок"
description: "В этой процедуре показано, как настроить справочник ставок."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b7c02e5a6f5eeee270ca4b6f91e90f7799c2ca11
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-rate-masters"></a><span data-ttu-id="cda5b-103">Настройка шаблонов ставок</span><span class="sxs-lookup"><span data-stu-id="cda5b-103">Set up rate masters</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cda5b-104">В этой процедуре показано, как настроить справочник ставок.</span><span class="sxs-lookup"><span data-stu-id="cda5b-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="cda5b-105">Справочники ставок обычно настраивает менеджер по логистике, в зависимости от контрактов, подписанных с перевозчиками.</span><span class="sxs-lookup"><span data-stu-id="cda5b-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="cda5b-106">В этом сценарии вам предстоит настроить справочник ставок для авиаперевозчика.</span><span class="sxs-lookup"><span data-stu-id="cda5b-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="cda5b-107">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="cda5b-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-rate-master"></a><span data-ttu-id="cda5b-108">Настройка справочника ставок</span><span class="sxs-lookup"><span data-stu-id="cda5b-108">Set up rate master</span></span>
1. <span data-ttu-id="cda5b-109">Перейдите в раздел "Управление транспортировкой" > "Настройка" > "Расчет ставок" > "Шаблон ставки".</span><span class="sxs-lookup"><span data-stu-id="cda5b-109">Go to Transportation management > Setup > Rating > Rate master.</span></span>
2. <span data-ttu-id="cda5b-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="cda5b-110">Click New.</span></span>
3. <span data-ttu-id="cda5b-111">В поле "Шаблон ставки" введите значение.</span><span class="sxs-lookup"><span data-stu-id="cda5b-111">In the Rate master field, type a value.</span></span>
4. <span data-ttu-id="cda5b-112">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="cda5b-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="cda5b-113">В поле "Код метаданных оценки" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="cda5b-113">In the Rating metadata ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="cda5b-114">Код метаданных ставок определяет, какие данные необходимы для справочника ставок, поскольку он определяет метаданные, которых ожидает механизм TMS при использовании этого справочника ставок.</span><span class="sxs-lookup"><span data-stu-id="cda5b-114">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the TMS engine using this rate master.</span></span>  
6. <span data-ttu-id="cda5b-115">В данном примере выберите вариант P2P</span><span class="sxs-lookup"><span data-stu-id="cda5b-115">For this example, select the P2P option</span></span>
7. <span data-ttu-id="cda5b-116">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="cda5b-116">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="cda5b-117">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="cda5b-117">Click Save.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="cda5b-118">Настройка базы ставки</span><span class="sxs-lookup"><span data-stu-id="cda5b-118">Set up rate base</span></span>
1. <span data-ttu-id="cda5b-119">Щелкните "База ставки".</span><span class="sxs-lookup"><span data-stu-id="cda5b-119">Click Rate base.</span></span>
    * <span data-ttu-id="cda5b-120">База ставки определяет ставку перевозчика и может использоваться для настройки структуры тарифов, поскольку она определяет изменения ставки в точках останова, определенных в справочнике градаций.</span><span class="sxs-lookup"><span data-stu-id="cda5b-120">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="cda5b-121">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="cda5b-121">Click New.</span></span>
3. <span data-ttu-id="cda5b-122">В поле "База ставки" введите значение.</span><span class="sxs-lookup"><span data-stu-id="cda5b-122">In the Rate base field, type a value.</span></span>
4. <span data-ttu-id="cda5b-123">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="cda5b-123">In the Name field, type a value.</span></span>
5. <span data-ttu-id="cda5b-124">В поле "Шаблон градации ставки" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="cda5b-124">In the Break master field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="cda5b-125">Справочники градаций используются для определения ценовой структуры и точек останова в ней.</span><span class="sxs-lookup"><span data-stu-id="cda5b-125">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="cda5b-126">Ценовая структура предполагает использование многоуровневого ценообразования, которое основывается на физических аналитиках.</span><span class="sxs-lookup"><span data-stu-id="cda5b-126">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="cda5b-127">В этом примере будет использоваться вес</span><span class="sxs-lookup"><span data-stu-id="cda5b-127">For this example, use weight</span></span>
7. <span data-ttu-id="cda5b-128">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="cda5b-128">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="cda5b-129">Переключите развертывание раздела "Подробности".</span><span class="sxs-lookup"><span data-stu-id="cda5b-129">Toggle the expansion of the Details section.</span></span>
9. <span data-ttu-id="cda5b-130">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="cda5b-130">Click New.</span></span>
10. <span data-ttu-id="cda5b-131">В поле "Почтовый индекс выгрузки из" введите "30301".</span><span class="sxs-lookup"><span data-stu-id="cda5b-131">In the Drop-off Postal Code From field, type '30301'.</span></span>
11. <span data-ttu-id="cda5b-132">В поле "Почтовый индекс выгрузки в" введите "30318".</span><span class="sxs-lookup"><span data-stu-id="cda5b-132">In the Drop-off Postal Code To field, type '30318'.</span></span>
12. <span data-ttu-id="cda5b-133">В поле "Страна/регион выгрузки" введите "США".</span><span class="sxs-lookup"><span data-stu-id="cda5b-133">In the Drop-off Country Region field, type 'USA'.</span></span>
13. <span data-ttu-id="cda5b-134">В поле "<1,00 фунта" введите "100".</span><span class="sxs-lookup"><span data-stu-id="cda5b-134">In the <1.00 Lbs field, type '100'.</span></span>
    * <span data-ttu-id="cda5b-135">Вставьте ставку за фунт, если общий вес груза меньше 1 фунта.</span><span class="sxs-lookup"><span data-stu-id="cda5b-135">Insert the rate per lbs if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="cda5b-136">В поле "<5,00 фунта" введите "300".</span><span class="sxs-lookup"><span data-stu-id="cda5b-136">In the <5.00 Lbs field, type '300'.</span></span>
    * <span data-ttu-id="cda5b-137">Вставьте ставку за фунт, если общий вес груза меньше 5 фунтов.</span><span class="sxs-lookup"><span data-stu-id="cda5b-137">Insert the rate per lbs if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="cda5b-138">В поле "<20,00 фунта" введите "500".</span><span class="sxs-lookup"><span data-stu-id="cda5b-138">In the <20.00 Lbs field, type '500'.</span></span>
    * <span data-ttu-id="cda5b-139">Вставьте ставку за фунт, если общий вес груза меньше 20 фунтов.</span><span class="sxs-lookup"><span data-stu-id="cda5b-139">Insert the rate per lbs if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="cda5b-140">В поле "<100,00 фунта" введите "1000".</span><span class="sxs-lookup"><span data-stu-id="cda5b-140">In the <100.00 Lbs field, type '1000'.</span></span>
    * <span data-ttu-id="cda5b-141">Вставьте ставку за фунт, если общий вес груза меньше 100 фунтов.</span><span class="sxs-lookup"><span data-stu-id="cda5b-141">Insert the rate per lbs if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="cda5b-142">В поле "<1.000,00 фунта" введите "3000".</span><span class="sxs-lookup"><span data-stu-id="cda5b-142">In the <1,000.00 Lbs field, type '3000'.</span></span>
    * <span data-ttu-id="cda5b-143">Вставьте ставку за фунт, если общий вес груза меньше 1000 фунтов.</span><span class="sxs-lookup"><span data-stu-id="cda5b-143">Insert the rate per lbs if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="cda5b-144">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="cda5b-144">Click Save.</span></span>
19. <span data-ttu-id="cda5b-145">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="cda5b-145">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="cda5b-146">Назначение базы ставки</span><span class="sxs-lookup"><span data-stu-id="cda5b-146">Assign rate base</span></span>
1. <span data-ttu-id="cda5b-147">Переключите развертывание раздела "Назначения базы ставки".</span><span class="sxs-lookup"><span data-stu-id="cda5b-147">Toggle the expansion of the Rate base assignments section.</span></span>
2. <span data-ttu-id="cda5b-148">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="cda5b-148">Click New.</span></span>
    * <span data-ttu-id="cda5b-149">Для каждого справочника ставок может быть несколько назначений базы ставки.</span><span class="sxs-lookup"><span data-stu-id="cda5b-149">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="cda5b-150">Это дает возможность создать для каждого перевозчика несколько различных ценовых точек в зависимости от мест назначения, услуг или разных баз ставок.</span><span class="sxs-lookup"><span data-stu-id="cda5b-150">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="cda5b-151">В этой процедуре вам предстоит создать только одно назначение базы ставки.</span><span class="sxs-lookup"><span data-stu-id="cda5b-151">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="cda5b-152">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="cda5b-152">In the Name field, type a value.</span></span>
4. <span data-ttu-id="cda5b-153">В поле "База ставки" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="cda5b-153">In the Rate base field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="cda5b-154">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="cda5b-154">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="cda5b-155">В поле "Услуга" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="cda5b-155">In the Service field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="cda5b-156">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="cda5b-156">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="cda5b-157">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="cda5b-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="cda5b-158">В поле "Почтовый индекс вывоза" введите "98052".</span><span class="sxs-lookup"><span data-stu-id="cda5b-158">In the Pick-up Postal Code field, type '98052'.</span></span>
    * <span data-ttu-id="cda5b-159">Укажите, с какого почтового индекса должно быть действительно это назначение базы ставки.</span><span class="sxs-lookup"><span data-stu-id="cda5b-159">Specify which postal code this rate base assignment should be valid from.</span></span>    
10. <span data-ttu-id="cda5b-160">В поле "Страна/регион вывоза" введите "США".</span><span class="sxs-lookup"><span data-stu-id="cda5b-160">In the Pick-up Country Region field, type 'USA'.</span></span>
11. <span data-ttu-id="cda5b-161">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="cda5b-161">Click Save.</span></span>


