---
title: Настройка перевозчиков
description: В этой процедура показано, как настроить перевозчика и задать сведений, такие как услуга, режим отгрузки, платежное средство за транспортировку, ограничения по транспортировке и ставка транспортировки.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c5ac13d17c97f20ee79e7faf57c570f02158424
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "314494"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="19e77-103">Настройка перевозчиков</span><span class="sxs-lookup"><span data-stu-id="19e77-103">Set up shipping carriers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="19e77-104">В этой процедура показано, как настроить перевозчика и задать сведений, такие как услуга, режим отгрузки, платежное средство за транспортировку, ограничения по транспортировке и ставка транспортировки.</span><span class="sxs-lookup"><span data-stu-id="19e77-104">This procedure shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="19e77-105">Координатор транспортировки может затем назначить перевозчика входящей или исходящей загрузке.</span><span class="sxs-lookup"><span data-stu-id="19e77-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="19e77-106">Создание нового перевозчика</span><span class="sxs-lookup"><span data-stu-id="19e77-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="19e77-107">Перейдите в раздел "Управление транспортировкой" > "Настройка" > "Перевозчики" > "Перевозчики".</span><span class="sxs-lookup"><span data-stu-id="19e77-107">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="19e77-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="19e77-108">Click New.</span></span>
3. <span data-ttu-id="19e77-109">В поле "Перевозчик, осуществляющий доставку" введите значение.</span><span class="sxs-lookup"><span data-stu-id="19e77-109">In the Shipping carrier field, type a value.</span></span>
4. <span data-ttu-id="19e77-110">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="19e77-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="19e77-111">В поле "Режим" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="19e77-111">In the Mode field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="19e77-112">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="19e77-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="19e77-113">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="19e77-113">In the list, click the link in the selected row.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="19e77-114">Ввод общей информации о перевозчике</span><span class="sxs-lookup"><span data-stu-id="19e77-114">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="19e77-115">Переключите развертывание раздела "Обзор".</span><span class="sxs-lookup"><span data-stu-id="19e77-115">Toggle the expansion of the Overview section.</span></span>
2. <span data-ttu-id="19e77-116">Установите или снимите флажок "Активировать перевозчика".</span><span class="sxs-lookup"><span data-stu-id="19e77-116">Check or uncheck the Activate shipping carrier checkbox.</span></span>
3. <span data-ttu-id="19e77-117">В поле "Поставщик" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="19e77-117">In the Vendor field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="19e77-118">Выберите счет поставщика, которому требуется назначить перевозчика.</span><span class="sxs-lookup"><span data-stu-id="19e77-118">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="19e77-119">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="19e77-119">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="19e77-120">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="19e77-120">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="19e77-121">В поле "Тип платежного средства за транспортировку" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="19e77-121">In the Transportation tender type field, select an option.</span></span>
    * <span data-ttu-id="19e77-122">Выберите вариант "Вручную", чтобы использовать страницу "Платежное средство за транспортировку", или выберите "EDI", чтобы обновить платежное средство с помощью Electronic Data Interchange (EDI).</span><span class="sxs-lookup"><span data-stu-id="19e77-122">Select Manual to use the Transportation Tender page, or select EDI to update the tender by using Electronic Data Interchange (EDI).</span></span>  
7. <span data-ttu-id="19e77-123">Установите или снимите флажок "Активировать ставку перевозчика".</span><span class="sxs-lookup"><span data-stu-id="19e77-123">Check or uncheck the Activate carrier rating checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="19e77-124">Создание необходимых услуг для перевозчика</span><span class="sxs-lookup"><span data-stu-id="19e77-124">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="19e77-125">Переключите развертывание раздела "Услуги".</span><span class="sxs-lookup"><span data-stu-id="19e77-125">Toggle the expansion of the Services section.</span></span>
2. <span data-ttu-id="19e77-126">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="19e77-126">Click New.</span></span>
3. <span data-ttu-id="19e77-127">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="19e77-127">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="19e77-128">В поле "Услуга перевозчика" введите значение.</span><span class="sxs-lookup"><span data-stu-id="19e77-128">In the Carrier service field, type a value.</span></span>
5. <span data-ttu-id="19e77-129">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="19e77-129">In the Name field, type a value.</span></span>
6. <span data-ttu-id="19e77-130">В поле "Способ транспортировки" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="19e77-130">In the Transportation method field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="19e77-131">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="19e77-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="19e77-132">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="19e77-132">In the list, click the link in the selected row.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="19e77-133">Настройка адреса для перевозчика (необязательно)</span><span class="sxs-lookup"><span data-stu-id="19e77-133">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="19e77-134">Переключите развертывание раздела "Адреса".</span><span class="sxs-lookup"><span data-stu-id="19e77-134">Toggle the expansion of the Addresses section.</span></span>
2. <span data-ttu-id="19e77-135">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="19e77-135">Click New.</span></span>
3. <span data-ttu-id="19e77-136">В поле "Имя или описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="19e77-136">In the Name or description field, type a value.</span></span>
4. <span data-ttu-id="19e77-137">В поле "Страна/регион" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="19e77-137">In the Country/region field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="19e77-138">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="19e77-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="19e77-139">В поле "Почтовый индекс" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="19e77-139">In the ZIP/postal code field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="19e77-140">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="19e77-140">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="19e77-141">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="19e77-141">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="19e77-142">В поле "Улица" введите значение.</span><span class="sxs-lookup"><span data-stu-id="19e77-142">In the Street field, type a value.</span></span>
10. <span data-ttu-id="19e77-143">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="19e77-143">Click OK.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="19e77-144">Настройка профиля ставок для перевозчика</span><span class="sxs-lookup"><span data-stu-id="19e77-144">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="19e77-145">Переключите развертывание раздела "Профили оценки".</span><span class="sxs-lookup"><span data-stu-id="19e77-145">Toggle the expansion of the Rating profiles section.</span></span>
2. <span data-ttu-id="19e77-146">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="19e77-146">Click New.</span></span>
3. <span data-ttu-id="19e77-147">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="19e77-147">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="19e77-148">В поле "Профиль оценки" введите значение.</span><span class="sxs-lookup"><span data-stu-id="19e77-148">In the Rating profile field, type a value.</span></span>
5. <span data-ttu-id="19e77-149">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="19e77-149">In the Name field, type a value.</span></span>
6. <span data-ttu-id="19e77-150">В поле "Сайт" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="19e77-150">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="19e77-151">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="19e77-151">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="19e77-152">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="19e77-152">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="19e77-153">В поле "Склад" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="19e77-153">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="19e77-154">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="19e77-154">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="19e77-155">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="19e77-155">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="19e77-156">В поле "Механизм ставок" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="19e77-156">In the Rate engine field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="19e77-157">Выберите механизм ставок, соответствующий контракту, заключенному между вами и перевозчиком.</span><span class="sxs-lookup"><span data-stu-id="19e77-157">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
13. <span data-ttu-id="19e77-158">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="19e77-158">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="19e77-159">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="19e77-159">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="19e77-160">В поле "Шаблон ставки" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="19e77-160">In the Rate master field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="19e77-161">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="19e77-161">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="19e77-162">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="19e77-162">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="19e77-163">В поле "Механизм расчета транзитного времени" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="19e77-163">In the Transit time engine field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="19e77-164">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="19e77-164">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="19e77-165">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="19e77-165">Click Save.</span></span>

