--- 
title: "Создание документа перемещения для внутреннего перемещения запасов"
description: "Эта процедура демонстрирует порядок создания документов перемещения для перемещения товаров внутри компании."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 1dc48b3d8761f72bbdf2c611c9280960f7ee119b
ms.contentlocale: ru-ru
ms.lasthandoff: 09/11/2018

---
# <a name="generate-a-transfer-document-for-an-internal-inventory-transfer"></a><span data-ttu-id="2592e-103">Создание документа перемещения для внутреннего перемещения запасов</span><span class="sxs-lookup"><span data-stu-id="2592e-103">Generate a transfer document for an internal inventory transfer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2592e-104">Эта процедура демонстрирует порядок создания документов перемещения для перемещения товаров внутри компании.</span><span class="sxs-lookup"><span data-stu-id="2592e-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="2592e-105">Эта процедура доступна только для юридических лиц с основным адресом в Литве.</span><span class="sxs-lookup"><span data-stu-id="2592e-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="2592e-106">Процедура была создана с использованием компании с демонстрационными данными DEMF с основным адресом в Литве.</span><span class="sxs-lookup"><span data-stu-id="2592e-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="2592e-107">Перед выполнением данной процедуры необходимо завершить процедуру "Настройка документов переноса для перемещения товаров в компании".</span><span class="sxs-lookup"><span data-stu-id="2592e-107">Before you can complete this procedure, you must complete the “Set up transfer documents for goods movement inside a company” procedure.</span></span> <span data-ttu-id="2592e-108">Эта процедура предназначена для бухгалтеров по складскому учету.</span><span class="sxs-lookup"><span data-stu-id="2592e-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="2592e-109">Эта процедура предназначена для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="2592e-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="2592e-110">Создание заказа на перемещение</span><span class="sxs-lookup"><span data-stu-id="2592e-110">Create a transfer order</span></span>
1. <span data-ttu-id="2592e-111">Перейдите в раздел "Управление запасами" > "Входящие заказы" > "Заказ на перемещение".</span><span class="sxs-lookup"><span data-stu-id="2592e-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="2592e-112">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="2592e-112">Click New.</span></span>
3. <span data-ttu-id="2592e-113">В поле "Со склада" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="2592e-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="2592e-114">В поле "На склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="2592e-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="2592e-115">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="2592e-115">Click Add.</span></span>
6. <span data-ttu-id="2592e-116">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="2592e-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="2592e-117">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="2592e-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="2592e-118">Ввод сведений о транспортировке для заказа на перемещение</span><span class="sxs-lookup"><span data-stu-id="2592e-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="2592e-119">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="2592e-119">Click Save.</span></span>
2. <span data-ttu-id="2592e-120">В области действий щелкните "Отгрузить".</span><span class="sxs-lookup"><span data-stu-id="2592e-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="2592e-121">Щелкните "Сведения о транспортировке".</span><span class="sxs-lookup"><span data-stu-id="2592e-121">Click Transportation details.</span></span>
4. <span data-ttu-id="2592e-122">Выберите "Да" в поле "Печать сведений о транспортировке".</span><span class="sxs-lookup"><span data-stu-id="2592e-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="2592e-123">В поле "Товары выдал" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="2592e-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="2592e-124">В поле "Упаковка" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2592e-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="2592e-125">В поле "Уровень риска для груза" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2592e-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="2592e-126">В поле "Перевозчик" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="2592e-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="2592e-127">В поле "Модель" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="2592e-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="2592e-128">В поле "Регистрационный номер" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2592e-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="2592e-129">В поле "Регистрационный номер прицепа" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2592e-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="2592e-130">В поле "Водитель" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="2592e-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="2592e-131">В поле "Имя водителя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2592e-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="2592e-132">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="2592e-132">Click Save.</span></span>
15. <span data-ttu-id="2592e-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2592e-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="2592e-134">Просмотр отборочной накладной для неразнесенного заказа на перемещение</span><span class="sxs-lookup"><span data-stu-id="2592e-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="2592e-135">Щелкните "Отборочная накладная".</span><span class="sxs-lookup"><span data-stu-id="2592e-135">Click Packing slip.</span></span>
2. <span data-ttu-id="2592e-136">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2592e-136">Click OK.</span></span>
3. <span data-ttu-id="2592e-137">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2592e-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="2592e-138">Просмотр отборочной накладной для разнесенного заказа на перемещение</span><span class="sxs-lookup"><span data-stu-id="2592e-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="2592e-139">В области действий щелкните "Заказ на перемещение".</span><span class="sxs-lookup"><span data-stu-id="2592e-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="2592e-140">В области действий щелкните "Отгрузить".</span><span class="sxs-lookup"><span data-stu-id="2592e-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="2592e-141">Щелкните "Отгрузить заказ на перемещение".</span><span class="sxs-lookup"><span data-stu-id="2592e-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="2592e-142">Перейдите на вкладку "Общие".</span><span class="sxs-lookup"><span data-stu-id="2592e-142">Click the General tab.</span></span>
5. <span data-ttu-id="2592e-143">В поле "Обновить" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="2592e-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="2592e-144">Перейдите на вкладку "Обзор".</span><span class="sxs-lookup"><span data-stu-id="2592e-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="2592e-145">В поле "Отборочная накладная" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2592e-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="2592e-146">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2592e-146">Click OK.</span></span>
9. <span data-ttu-id="2592e-147">В области действий щелкните "Отгрузить".</span><span class="sxs-lookup"><span data-stu-id="2592e-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="2592e-148">Щелкните "Отборочная накладная".</span><span class="sxs-lookup"><span data-stu-id="2592e-148">Click Packing slip.</span></span>
11. <span data-ttu-id="2592e-149">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2592e-149">Click OK.</span></span>


