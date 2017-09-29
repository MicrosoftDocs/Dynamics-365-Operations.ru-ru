--- 
title: "Настройка перевозчиков"
description: "В этой процедура показано, как настроить перевозчика и задать сведений, такие как услуга, режим отгрузки, платежное средство за транспортировку, ограничения по транспортировке и ставка транспортировки."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
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
ms.openlocfilehash: e27be049bebd63c9266029b8981874417a9f0a8c
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="19216-103">Настройка перевозчиков</span><span class="sxs-lookup"><span data-stu-id="19216-103">Set up shipping carriers</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="19216-104">В этой процедура показано, как настроить перевозчика и задать сведений, такие как услуга, режим отгрузки, платежное средство за транспортировку, ограничения по транспортировке и ставка транспортировки.</span><span class="sxs-lookup"><span data-stu-id="19216-104">This procedure shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="19216-105">Координатор транспортировки может затем назначить перевозчика входящей или исходящей загрузке.</span><span class="sxs-lookup"><span data-stu-id="19216-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="19216-106">Создание нового перевозчика</span><span class="sxs-lookup"><span data-stu-id="19216-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="19216-107">Перейдите в раздел "Управление транспортировкой" > "Настройка" > "Перевозчики" > "Перевозчики".</span><span class="sxs-lookup"><span data-stu-id="19216-107">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="19216-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="19216-108">Click New.</span></span>
3. <span data-ttu-id="19216-109">В поле "Перевозчик, осуществляющий доставку" введите значение.</span><span class="sxs-lookup"><span data-stu-id="19216-109">In the Shipping carrier field, type a value.</span></span>
4. <span data-ttu-id="19216-110">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="19216-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="19216-111">В поле "Режим" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="19216-111">In the Mode field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="19216-112">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="19216-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="19216-113">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="19216-113">In the list, click the link in the selected row.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="19216-114">Ввод общей информации о перевозчике</span><span class="sxs-lookup"><span data-stu-id="19216-114">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="19216-115">Переключите развертывание раздела "Обзор".</span><span class="sxs-lookup"><span data-stu-id="19216-115">Toggle the expansion of the Overview section.</span></span>
2. <span data-ttu-id="19216-116">Установите или снимите флажок "Активировать перевозчика".</span><span class="sxs-lookup"><span data-stu-id="19216-116">Check or uncheck the Activate shipping carrier checkbox.</span></span>
3. <span data-ttu-id="19216-117">В поле "Поставщик" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="19216-117">In the Vendor field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="19216-118">Выберите счет поставщика, которому требуется назначить перевозчика.</span><span class="sxs-lookup"><span data-stu-id="19216-118">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="19216-119">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="19216-119">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="19216-120">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="19216-120">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="19216-121">В поле "Тип платежного средства за транспортировку" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="19216-121">In the Transportation tender type field, select an option.</span></span>
    * <span data-ttu-id="19216-122">Выберите вариант "Вручную", чтобы использовать страницу "Платежное средство за транспортировку", или выберите "EDI", чтобы обновить платежное средство с помощью Electronic Data Interchange (EDI).</span><span class="sxs-lookup"><span data-stu-id="19216-122">Select Manual to use the Transportation Tender page, or select EDI to update the tender by using Electronic Data Interchange (EDI).</span></span>  
7. <span data-ttu-id="19216-123">Установите или снимите флажок "Активировать ставку перевозчика".</span><span class="sxs-lookup"><span data-stu-id="19216-123">Check or uncheck the Activate carrier rating checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="19216-124">Создание необходимых услуг для перевозчика</span><span class="sxs-lookup"><span data-stu-id="19216-124">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="19216-125">Переключите развертывание раздела "Услуги".</span><span class="sxs-lookup"><span data-stu-id="19216-125">Toggle the expansion of the Services section.</span></span>
2. <span data-ttu-id="19216-126">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="19216-126">Click New.</span></span>
3. <span data-ttu-id="19216-127">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="19216-127">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="19216-128">В поле "Услуга перевозчика" введите значение.</span><span class="sxs-lookup"><span data-stu-id="19216-128">In the Carrier service field, type a value.</span></span>
5. <span data-ttu-id="19216-129">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="19216-129">In the Name field, type a value.</span></span>
6. <span data-ttu-id="19216-130">В поле "Способ транспортировки" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="19216-130">In the Transportation method field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="19216-131">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="19216-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="19216-132">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="19216-132">In the list, click the link in the selected row.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="19216-133">Настройка адреса для перевозчика (необязательно)</span><span class="sxs-lookup"><span data-stu-id="19216-133">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="19216-134">Переключите развертывание раздела "Адреса".</span><span class="sxs-lookup"><span data-stu-id="19216-134">Toggle the expansion of the Addresses section.</span></span>
2. <span data-ttu-id="19216-135">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="19216-135">Click New.</span></span>
3. <span data-ttu-id="19216-136">В поле "Имя или описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="19216-136">In the Name or description field, type a value.</span></span>
4. <span data-ttu-id="19216-137">В поле "Страна/регион" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="19216-137">In the Country/region field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="19216-138">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="19216-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="19216-139">В поле "Почтовый индекс" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="19216-139">In the ZIP/postal code field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="19216-140">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="19216-140">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="19216-141">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="19216-141">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="19216-142">В поле "Улица" введите значение.</span><span class="sxs-lookup"><span data-stu-id="19216-142">In the Street field, type a value.</span></span>
10. <span data-ttu-id="19216-143">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="19216-143">Click OK.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="19216-144">Настройка профиля ставок для перевозчика</span><span class="sxs-lookup"><span data-stu-id="19216-144">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="19216-145">Переключите развертывание раздела "Профили оценки".</span><span class="sxs-lookup"><span data-stu-id="19216-145">Toggle the expansion of the Rating profiles section.</span></span>
2. <span data-ttu-id="19216-146">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="19216-146">Click New.</span></span>
3. <span data-ttu-id="19216-147">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="19216-147">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="19216-148">В поле "Профиль оценки" введите значение.</span><span class="sxs-lookup"><span data-stu-id="19216-148">In the Rating profile field, type a value.</span></span>
5. <span data-ttu-id="19216-149">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="19216-149">In the Name field, type a value.</span></span>
6. <span data-ttu-id="19216-150">В поле "Сайт" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="19216-150">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="19216-151">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="19216-151">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="19216-152">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="19216-152">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="19216-153">В поле "Склад" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="19216-153">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="19216-154">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="19216-154">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="19216-155">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="19216-155">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="19216-156">В поле "Механизм ставок" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="19216-156">In the Rate engine field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="19216-157">Выберите механизм ставок, соответствующий контракту, заключенному между вами и перевозчиком.</span><span class="sxs-lookup"><span data-stu-id="19216-157">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
13. <span data-ttu-id="19216-158">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="19216-158">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="19216-159">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="19216-159">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="19216-160">В поле "Шаблон ставки" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="19216-160">In the Rate master field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="19216-161">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="19216-161">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="19216-162">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="19216-162">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="19216-163">В поле "Механизм расчета транзитного времени" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="19216-163">In the Transit time engine field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="19216-164">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="19216-164">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="19216-165">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="19216-165">Click Save.</span></span>


