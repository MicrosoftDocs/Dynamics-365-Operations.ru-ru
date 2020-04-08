---
title: Настройка перевозчиков
description: В этой теме показано, как настроить перевозчика и задать сведений, такие как услуга, режим отгрузки, платежное средство за транспортировку, ограничения по транспортировке и ставка транспортировки.
author: ShylaThompson
manager: AnnBe
ms.date: 07/19/2019
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
ms.openlocfilehash: bb39d58336e7f867e19d7ba6d9f801200de5a0aa
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148563"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="ec16a-103">Настройка перевозчиков</span><span class="sxs-lookup"><span data-stu-id="ec16a-103">Set up shipping carriers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ec16a-104">В этой теме показано, как настроить перевозчика и задать сведений, такие как услуга, режим отгрузки, платежное средство за транспортировку, ограничения по транспортировке и ставка транспортировки.</span><span class="sxs-lookup"><span data-stu-id="ec16a-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="ec16a-105">Координатор транспортировки может затем назначить перевозчика входящей или исходящей загрузке.</span><span class="sxs-lookup"><span data-stu-id="ec16a-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="ec16a-106">Создание нового перевозчика</span><span class="sxs-lookup"><span data-stu-id="ec16a-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="ec16a-107">Выберите **Область перехода > Модули > Управление транспортировкой > Настройка > Перевозчики > Перевозчики**.</span><span class="sxs-lookup"><span data-stu-id="ec16a-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="ec16a-108">Выберите **Создать** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="ec16a-108">Select **New** in the Action pane.</span></span>
3. <span data-ttu-id="ec16a-109">В поле **Перевозчик, осуществляющий доставку** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ec16a-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="ec16a-110">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ec16a-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="ec16a-111">В поле **Режим** выберите вариант в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="ec16a-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="ec16a-112">Ввод общей информации о перевозчике</span><span class="sxs-lookup"><span data-stu-id="ec16a-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="ec16a-113">Переключите развертывание раздела **Обзор**.</span><span class="sxs-lookup"><span data-stu-id="ec16a-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="ec16a-114">Установите или снимите флажок **Активировать перевозчика**.</span><span class="sxs-lookup"><span data-stu-id="ec16a-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="ec16a-115">В поле **Счет поставщика** выберите вариант в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="ec16a-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="ec16a-116">Выберите счет поставщика, которому требуется назначить перевозчика.</span><span class="sxs-lookup"><span data-stu-id="ec16a-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="ec16a-117">В поле **Тип платежного средства за транспортировку** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="ec16a-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="ec16a-118">Выберите вариант **Вручную**, чтобы использовать страницу "Платежное средство за транспортировку", или выберите **EDI**, чтобы обновить платежное средство с помощью Electronic Data Interchange (EDI).</span><span class="sxs-lookup"><span data-stu-id="ec16a-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="ec16a-119">Установите или снимите флажок **Активировать ставку перевозчика**.</span><span class="sxs-lookup"><span data-stu-id="ec16a-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="ec16a-120">Создание необходимых услуг для перевозчика</span><span class="sxs-lookup"><span data-stu-id="ec16a-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="ec16a-121">Переключите развертывание раздела **Услуги**.</span><span class="sxs-lookup"><span data-stu-id="ec16a-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="ec16a-122">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ec16a-122">Select **New**.</span></span>
3. <span data-ttu-id="ec16a-123">В поле **Услуга перевозчика** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ec16a-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="ec16a-124">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ec16a-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="ec16a-125">В поле **Способ транспортировки** выберите вариант в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="ec16a-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="ec16a-126">Настройка адреса для перевозчика (необязательно)</span><span class="sxs-lookup"><span data-stu-id="ec16a-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="ec16a-127">Переключите развертывание раздела **Адреса**.</span><span class="sxs-lookup"><span data-stu-id="ec16a-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="ec16a-128">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ec16a-128">Select **New**.</span></span>
3. <span data-ttu-id="ec16a-129">В поле **Имя или описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ec16a-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="ec16a-130">В поле **Страна/регион** выберите вариант в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="ec16a-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="ec16a-131">В поле **Почтовый индекс** выберите вариант в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="ec16a-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="ec16a-132">В поле **Улица** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ec16a-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="ec16a-133">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ec16a-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="ec16a-134">Настройка профиля ставок для перевозчика</span><span class="sxs-lookup"><span data-stu-id="ec16a-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="ec16a-135">Переключите развертывание раздела **Профили оценки**.</span><span class="sxs-lookup"><span data-stu-id="ec16a-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="ec16a-136">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ec16a-136">Select **New**.</span></span>
3. <span data-ttu-id="ec16a-137">В поле **Профиль оценки** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ec16a-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="ec16a-138">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ec16a-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="ec16a-139">В поле **Сайт** выберите вариант в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="ec16a-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="ec16a-140">В поле **Склад** выберите вариант в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="ec16a-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="ec16a-141">В поле **Механизм ставок** выберите вариант в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="ec16a-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="ec16a-142">Выберите механизм ставок, соответствующий контракту, заключенному между вами и перевозчиком.</span><span class="sxs-lookup"><span data-stu-id="ec16a-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="ec16a-143">В поле **Шаблон ставки** выберите вариант в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="ec16a-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="ec16a-144">В поле **Механизм расчета транзитного времени** выберите вариант в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="ec16a-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="ec16a-145">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ec16a-145">Select **Save**.</span></span>

