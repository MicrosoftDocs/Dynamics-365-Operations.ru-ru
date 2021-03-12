---
title: Настройка документов перемещения для перемещения товаров в компании
description: Эта процедура демонстрирует порядок создания документов перемещения для перемещения товаров внутри компании.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4c71d1b0e756cc20fa68bf79102479447cf8f86
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988053"
---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a><span data-ttu-id="aff94-103">Настройка документов перемещения для перемещения товаров в компании</span><span class="sxs-lookup"><span data-stu-id="aff94-103">Set up the transfer documents for goods movement inside a company</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aff94-104">Эта процедура демонстрирует порядок создания документов перемещения для перемещения товаров внутри компании.</span><span class="sxs-lookup"><span data-stu-id="aff94-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="aff94-105">Эта процедура доступна только для юридических лиц с основным адресом в Литве.</span><span class="sxs-lookup"><span data-stu-id="aff94-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="aff94-106">Процедура была создана с использованием компании с демонстрационными данными DEMF с основным адресом в Литве.</span><span class="sxs-lookup"><span data-stu-id="aff94-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="aff94-107">Перед выполнением данной процедуры необходимо завершить процедуру "Настройка документов переноса для перемещения товаров в компании".</span><span class="sxs-lookup"><span data-stu-id="aff94-107">Before you can complete this procedure, you must complete the "Set up transfer documents for goods movement inside a company" procedure.</span></span> <span data-ttu-id="aff94-108">Эта процедура предназначена для бухгалтеров по складскому учету.</span><span class="sxs-lookup"><span data-stu-id="aff94-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="aff94-109">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="aff94-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="aff94-110">Создание заказа на перемещение</span><span class="sxs-lookup"><span data-stu-id="aff94-110">Create a transfer order</span></span>
1. <span data-ttu-id="aff94-111">Перейдите в раздел "Управление запасами" > "Входящие заказы" > "Заказ на перемещение".</span><span class="sxs-lookup"><span data-stu-id="aff94-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="aff94-112">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="aff94-112">Click New.</span></span>
3. <span data-ttu-id="aff94-113">В поле "Со склада" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="aff94-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="aff94-114">В поле "На склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="aff94-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="aff94-115">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="aff94-115">Click Add.</span></span>
6. <span data-ttu-id="aff94-116">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="aff94-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="aff94-117">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="aff94-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="aff94-118">Ввод сведений о транспортировке для заказа на перемещение</span><span class="sxs-lookup"><span data-stu-id="aff94-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="aff94-119">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="aff94-119">Click Save.</span></span>
2. <span data-ttu-id="aff94-120">В области действий щелкните "Отгрузить".</span><span class="sxs-lookup"><span data-stu-id="aff94-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="aff94-121">Щелкните "Сведения о транспортировке".</span><span class="sxs-lookup"><span data-stu-id="aff94-121">Click Transportation details.</span></span>
4. <span data-ttu-id="aff94-122">Выберите "Да" в поле "Печать сведений о транспортировке".</span><span class="sxs-lookup"><span data-stu-id="aff94-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="aff94-123">В поле "Товары выдал" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="aff94-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="aff94-124">В поле "Упаковка" введите значение.</span><span class="sxs-lookup"><span data-stu-id="aff94-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="aff94-125">В поле "Уровень риска для груза" введите значение.</span><span class="sxs-lookup"><span data-stu-id="aff94-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="aff94-126">В поле "Перевозчик" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="aff94-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="aff94-127">В поле "Модель" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="aff94-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="aff94-128">В поле "Регистрационный номер" введите значение.</span><span class="sxs-lookup"><span data-stu-id="aff94-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="aff94-129">В поле "Регистрационный номер прицепа" введите значение.</span><span class="sxs-lookup"><span data-stu-id="aff94-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="aff94-130">В поле "Водитель" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="aff94-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="aff94-131">В поле "Имя водителя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="aff94-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="aff94-132">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="aff94-132">Click Save.</span></span>
15. <span data-ttu-id="aff94-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="aff94-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="aff94-134">Просмотр отборочной накладной для неразнесенного заказа на перемещение</span><span class="sxs-lookup"><span data-stu-id="aff94-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="aff94-135">Щелкните "Отборочная накладная".</span><span class="sxs-lookup"><span data-stu-id="aff94-135">Click Packing slip.</span></span>
2. <span data-ttu-id="aff94-136">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="aff94-136">Click OK.</span></span>
3. <span data-ttu-id="aff94-137">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="aff94-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="aff94-138">Просмотр отборочной накладной для разнесенного заказа на перемещение</span><span class="sxs-lookup"><span data-stu-id="aff94-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="aff94-139">В области действий щелкните "Заказ на перемещение".</span><span class="sxs-lookup"><span data-stu-id="aff94-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="aff94-140">В области действий щелкните "Отгрузить".</span><span class="sxs-lookup"><span data-stu-id="aff94-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="aff94-141">Щелкните "Отгрузить заказ на перемещение".</span><span class="sxs-lookup"><span data-stu-id="aff94-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="aff94-142">Перейдите на вкладку "Общие".</span><span class="sxs-lookup"><span data-stu-id="aff94-142">Click the General tab.</span></span>
5. <span data-ttu-id="aff94-143">В поле "Обновить" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="aff94-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="aff94-144">Перейдите на вкладку "Обзор".</span><span class="sxs-lookup"><span data-stu-id="aff94-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="aff94-145">В поле "Отборочная накладная" введите значение.</span><span class="sxs-lookup"><span data-stu-id="aff94-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="aff94-146">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="aff94-146">Click OK.</span></span>
9. <span data-ttu-id="aff94-147">В области действий щелкните "Отгрузить".</span><span class="sxs-lookup"><span data-stu-id="aff94-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="aff94-148">Щелкните "Отборочная накладная".</span><span class="sxs-lookup"><span data-stu-id="aff94-148">Click Packing slip.</span></span>
11. <span data-ttu-id="aff94-149">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="aff94-149">Click OK.</span></span>

