---
title: Настройка шаблонов ставок
description: В этой процедуре показано, как настроить справочник ставок.
author: ShylaThompson
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cb25726e05f11420c7355c39f7e262abca5da62
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808998"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="7f38b-103">Настройка шаблонов ставок</span><span class="sxs-lookup"><span data-stu-id="7f38b-103">Set up rate masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7f38b-104">В этой процедуре показано, как настроить справочник ставок.</span><span class="sxs-lookup"><span data-stu-id="7f38b-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="7f38b-105">Справочники ставок обычно настраивает менеджер по логистике, в зависимости от контрактов, подписанных с перевозчиками.</span><span class="sxs-lookup"><span data-stu-id="7f38b-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="7f38b-106">В этом сценарии вам предстоит настроить справочник ставок для авиаперевозчика.</span><span class="sxs-lookup"><span data-stu-id="7f38b-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="7f38b-107">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="7f38b-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-break-master"></a><span data-ttu-id="7f38b-108">Настройка шаблона градации ставки</span><span class="sxs-lookup"><span data-stu-id="7f38b-108">Set up break master</span></span>

1. <span data-ttu-id="7f38b-109">Перейдите в раздел **Управление транспортировкой > Настройка > Расчет ставок > Шаблон градации ставки**.</span><span class="sxs-lookup"><span data-stu-id="7f38b-109">Go to **Transportation management > Setup > Rating > Break master**.</span></span> <span data-ttu-id="7f38b-110">Справочники градаций используются для определения ценовой структуры и точек останова в ней.</span><span class="sxs-lookup"><span data-stu-id="7f38b-110">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="7f38b-111">Ценовая структура предполагает использование многоуровневого ценообразования, которое основывается на физических аналитиках.</span><span class="sxs-lookup"><span data-stu-id="7f38b-111">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
1. <span data-ttu-id="7f38b-112">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="7f38b-112">Select **New**.</span></span>
1. <span data-ttu-id="7f38b-113">В поле **Шаблон градации ставки** введите значение.</span><span class="sxs-lookup"><span data-stu-id="7f38b-113">In the **Break master** field, enter a value.</span></span>
1. <span data-ttu-id="7f38b-114">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="7f38b-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="7f38b-115">В поле **Тип данных** выберите тип данных.</span><span class="sxs-lookup"><span data-stu-id="7f38b-115">In the **Data type** field, select the data type.</span></span>
1. <span data-ttu-id="7f38b-116">В поле **Сравнение** введите требуемый тип сравнения (с помощью операторов).</span><span class="sxs-lookup"><span data-stu-id="7f38b-116">In the **Comparison** field, enter the kind of comparison requested (using operators).</span></span>
1. <span data-ttu-id="7f38b-117">В поле **Единица градации ставки** введите значения единицы градации ставки.</span><span class="sxs-lookup"><span data-stu-id="7f38b-117">In the **Break unit** field, enter the break unit.</span></span>
1. <span data-ttu-id="7f38b-118">В разделе **Сведения** создайте столько градаций ставки, сколько необходимо для структуры ценообразования.</span><span class="sxs-lookup"><span data-stu-id="7f38b-118">In the **Details** section, create as many breaks as needed for the pricing structure.</span></span>
1. <span data-ttu-id="7f38b-119">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="7f38b-119">Select **Save**.</span></span>

## <a name="set-up-rate-master"></a><span data-ttu-id="7f38b-120">Настройка справочника ставок</span><span class="sxs-lookup"><span data-stu-id="7f38b-120">Set up rate master</span></span>

1. <span data-ttu-id="7f38b-121">Перейдите в раздел **Управление транспортировкой > Настройка > Расчет ставок > Шаблон ставки**.</span><span class="sxs-lookup"><span data-stu-id="7f38b-121">Go to **Transportation management > Setup > Rating > Rate master**.</span></span>
1. <span data-ttu-id="7f38b-122">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="7f38b-122">Select **New**.</span></span>
1. <span data-ttu-id="7f38b-123">В поле **Шаблон ставки** введите значение.</span><span class="sxs-lookup"><span data-stu-id="7f38b-123">In the **Rate master** field, type a value.</span></span>
1. <span data-ttu-id="7f38b-124">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="7f38b-124">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="7f38b-125">В поле **Код метаданных оценки** выберите кнопку раскрывающегося списка, чтобы открыть подстановку.</span><span class="sxs-lookup"><span data-stu-id="7f38b-125">In the **Rating metadata ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="7f38b-126">Код метаданных ставок определяет, какие данные необходимы для справочника ставок, поскольку он определяет метаданные, которых ожидает механизм управления транспортировкой при использовании этого справочника ставок.</span><span class="sxs-lookup"><span data-stu-id="7f38b-126">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the transportation management engine using this rate master.</span></span>  
1. <span data-ttu-id="7f38b-127">В данном примере выберите вариант P2P.</span><span class="sxs-lookup"><span data-stu-id="7f38b-127">For this example, select the P2P option.</span></span> <span data-ttu-id="7f38b-128">Это значение уже определено в демонстрационных данных.</span><span class="sxs-lookup"><span data-stu-id="7f38b-128">This is already defined in the demo data.</span></span>
1. <span data-ttu-id="7f38b-129">В списке выберите ссылку в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="7f38b-129">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="7f38b-130">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="7f38b-130">Select **Save**.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="7f38b-131">Настройка базы ставки</span><span class="sxs-lookup"><span data-stu-id="7f38b-131">Set up rate base</span></span>

1. <span data-ttu-id="7f38b-132">Выберите **База ставки**.</span><span class="sxs-lookup"><span data-stu-id="7f38b-132">Select **Rate base**.</span></span>
    * <span data-ttu-id="7f38b-133">База ставки определяет ставку перевозчика и может использоваться для настройки структуры тарифов, поскольку она определяет изменения ставки в точках останова, определенных в справочнике градаций.</span><span class="sxs-lookup"><span data-stu-id="7f38b-133">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="7f38b-134">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="7f38b-134">Select **New**.</span></span>
3. <span data-ttu-id="7f38b-135">В поле **База ставки** введите значение.</span><span class="sxs-lookup"><span data-stu-id="7f38b-135">In the **Rate base** field, type a value.</span></span>
4. <span data-ttu-id="7f38b-136">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="7f38b-136">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="7f38b-137">В поле **Шаблон градации ставки** выберите раскрывающийся список, чтобы открыть подстановку.</span><span class="sxs-lookup"><span data-stu-id="7f38b-137">In the **Break master** field, select the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7f38b-138">Справочники градаций используются для определения ценовой структуры и точек останова в ней.</span><span class="sxs-lookup"><span data-stu-id="7f38b-138">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="7f38b-139">Ценовая структура предполагает использование многоуровневого ценообразования, которое основывается на физических аналитиках.</span><span class="sxs-lookup"><span data-stu-id="7f38b-139">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="7f38b-140">В этом примере будет использоваться вес.</span><span class="sxs-lookup"><span data-stu-id="7f38b-140">For this example, use weight.</span></span> <span data-ttu-id="7f38b-141">Это значение уже определено в демонстрационных данных.</span><span class="sxs-lookup"><span data-stu-id="7f38b-141">This is already defined in the demo data.</span></span>
7. <span data-ttu-id="7f38b-142">В списке выберите ссылку в выделенной строке.</span><span class="sxs-lookup"><span data-stu-id="7f38b-142">In the list, select the link in the highlighted row.</span></span>
8. <span data-ttu-id="7f38b-143">Разверните раздел **Сведения**.</span><span class="sxs-lookup"><span data-stu-id="7f38b-143">Expand the **Details** section.</span></span>
9. <span data-ttu-id="7f38b-144">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="7f38b-144">Select **New**.</span></span>
10. <span data-ttu-id="7f38b-145">В поле **Почтовый индекс выгрузки из** введите "30301".</span><span class="sxs-lookup"><span data-stu-id="7f38b-145">In the **Drop-off Postal Code From** field, type "30301".</span></span>
11. <span data-ttu-id="7f38b-146">В поле **Почтовый индекс выгрузки в** введите "30318".</span><span class="sxs-lookup"><span data-stu-id="7f38b-146">In the **Drop-off Postal Code To** field, type "30318".</span></span>
12. <span data-ttu-id="7f38b-147">В поле **Страна/регион выгрузки** введите "США".</span><span class="sxs-lookup"><span data-stu-id="7f38b-147">In the **Drop-off Country Region** field, type "USA".</span></span>
13. <span data-ttu-id="7f38b-148">В поле **<1,00 фунта** введите "100".</span><span class="sxs-lookup"><span data-stu-id="7f38b-148">In the **<1.00 Lbs** field, type "100".</span></span>
    * <span data-ttu-id="7f38b-149">Вставьте ставку за фунт, если общий вес груза меньше 1 фунта.</span><span class="sxs-lookup"><span data-stu-id="7f38b-149">Insert the rate per pounds if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="7f38b-150">В поле **<5,00 фунтов** введите "300".</span><span class="sxs-lookup"><span data-stu-id="7f38b-150">In the **<5.00 Lbs** field, type "300".</span></span>
    * <span data-ttu-id="7f38b-151">Вставьте ставку за фунт, если общий вес груза меньше 5 фунтов.</span><span class="sxs-lookup"><span data-stu-id="7f38b-151">Insert the rate per pounds if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="7f38b-152">В поле **<20,00 фунтов** введите "500".</span><span class="sxs-lookup"><span data-stu-id="7f38b-152">In the **<20.00 Lbs** field, type "500".</span></span>
    * <span data-ttu-id="7f38b-153">Вставьте ставку за фунт, если общий вес груза меньше 20 фунтов.</span><span class="sxs-lookup"><span data-stu-id="7f38b-153">Insert the rate per pounds if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="7f38b-154">В поле **<100,00 фунтов** введите "1000".</span><span class="sxs-lookup"><span data-stu-id="7f38b-154">In the **<100.00 Lbs** field, type "1000".</span></span>
    * <span data-ttu-id="7f38b-155">Вставьте ставку за фунт, если общий вес груза меньше 100 фунтов.</span><span class="sxs-lookup"><span data-stu-id="7f38b-155">Insert the rate per pounds if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="7f38b-156">В поле **<1 000,00 фунтов** введите "3000".</span><span class="sxs-lookup"><span data-stu-id="7f38b-156">In the **<1,000.00 Lbs** field, type "3000".</span></span>
    * <span data-ttu-id="7f38b-157">Вставьте ставку за фунт, если общий вес груза меньше 1000 фунтов.</span><span class="sxs-lookup"><span data-stu-id="7f38b-157">Insert the rate per pounds if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="7f38b-158">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="7f38b-158">Select **Save**.</span></span>
19. <span data-ttu-id="7f38b-159">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="7f38b-159">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="7f38b-160">Назначение базы ставки</span><span class="sxs-lookup"><span data-stu-id="7f38b-160">Assign rate base</span></span>

1. <span data-ttu-id="7f38b-161">Разверните раздел **Назначения базы ставки**.</span><span class="sxs-lookup"><span data-stu-id="7f38b-161">Expand the **Rate base assignments** section.</span></span>
2. <span data-ttu-id="7f38b-162">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="7f38b-162">Select **New**.</span></span>
    * <span data-ttu-id="7f38b-163">Для каждого справочника ставок может быть несколько назначений базы ставки.</span><span class="sxs-lookup"><span data-stu-id="7f38b-163">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="7f38b-164">Это дает возможность создать для каждого перевозчика несколько различных ценовых точек в зависимости от мест назначения, услуг или разных баз ставок.</span><span class="sxs-lookup"><span data-stu-id="7f38b-164">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="7f38b-165">В этой процедуре вам предстоит создать только одно назначение базы ставки.</span><span class="sxs-lookup"><span data-stu-id="7f38b-165">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="7f38b-166">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="7f38b-166">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="7f38b-167">В поле **База ставки** выберите кнопку раскрывающегося списка, чтобы открыть подстановку.</span><span class="sxs-lookup"><span data-stu-id="7f38b-167">In the **Rate base** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="7f38b-168">В списке выберите ссылку в выделенной строке.</span><span class="sxs-lookup"><span data-stu-id="7f38b-168">In the list, select the link in the highlighted row.</span></span>
6. <span data-ttu-id="7f38b-169">В поле **Служба** выберите кнопку раскрывающегося списка, чтобы открыть подстановку.</span><span class="sxs-lookup"><span data-stu-id="7f38b-169">In the **Service** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="7f38b-170">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="7f38b-170">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="7f38b-171">В списке выберите ссылку в выделенной строке.</span><span class="sxs-lookup"><span data-stu-id="7f38b-171">In the list, select the link in the highlighted row.</span></span>
9. <span data-ttu-id="7f38b-172">В поле **Почтовый индекс вывоза** введите "98052".</span><span class="sxs-lookup"><span data-stu-id="7f38b-172">In the **Pick-up Postal Code** field, type "98052".</span></span>
    * <span data-ttu-id="7f38b-173">Укажите, с какого почтового индекса должно быть действительно это назначение базы ставки.</span><span class="sxs-lookup"><span data-stu-id="7f38b-173">Specify which postal code this rate base assignment should be valid from.</span></span>
10. <span data-ttu-id="7f38b-174">В поле **Страна/регион вывоза** введите "США".</span><span class="sxs-lookup"><span data-stu-id="7f38b-174">In the **Pick-up Country Region** field, type "USA".</span></span>
11. <span data-ttu-id="7f38b-175">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="7f38b-175">Select **Save**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]