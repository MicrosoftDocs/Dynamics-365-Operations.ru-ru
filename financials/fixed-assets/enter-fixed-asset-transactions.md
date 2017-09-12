---
title: "Параметры проводки с основными средствами"
description: "Эта статья описывает различные методы, доступные для создания проводок с основными средствами."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 3d16b43eda0157e63a0d30fe806dac9a359d5fa4
ms.contentlocale: ru-ru
ms.lasthandoff: 06/29/2017


---

# <a name="fixed-asset-transaction-options"></a><span data-ttu-id="103d8-103">Параметры проводки с основными средствами</span><span class="sxs-lookup"><span data-stu-id="103d8-103">Fixed asset transaction options</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="103d8-104">Эта статья описывает различные методы, доступные для создания проводок с основными средствами.</span><span class="sxs-lookup"><span data-stu-id="103d8-104">This article describes the different methods available to create fixed asset transactions.</span></span>

<span data-ttu-id="103d8-105">Модуль "Основные средства" можно настроить для интеграции с модулями "Расчеты с поставщиками", "Расчеты с клиентами", "Материально-техническое снабжение" и "Главная книга".</span><span class="sxs-lookup"><span data-stu-id="103d8-105">You can set up Fixed assets for integration with Accounts payable, Accounts receivable, Procurement and sourcing, and General ledger.</span></span> <span data-ttu-id="103d8-106">Есть также возможность переноса номенклатур из модуля "Управление запасами" в модуль "Основные средства", если эти номенклатуры требуется использовать внутри системы.</span><span class="sxs-lookup"><span data-stu-id="103d8-106">You can also transfer items in Inventory management to Fixed assets if you want to use those items internally.</span></span>

## <a name="accounts-payable"></a><span data-ttu-id="103d8-107">Расчеты с поставщиками</span><span class="sxs-lookup"><span data-stu-id="103d8-107">Accounts payable</span></span>
<span data-ttu-id="103d8-108">Проводки по основным средствам вводятся на странице "Ваучер журнала".</span><span class="sxs-lookup"><span data-stu-id="103d8-108">You can enter Fixed assets transactions in the Journal voucher page.</span></span> <span data-ttu-id="103d8-109">Эту страницу можно открыть на странице "Журнал накладных".</span><span class="sxs-lookup"><span data-stu-id="103d8-109">This page can be opened from the Invoice journal page.</span></span> <span data-ttu-id="103d8-110">Страницу "Ваучер журнала" также можно открыть на странице "Журнал утверждения накладных".</span><span class="sxs-lookup"><span data-stu-id="103d8-110">You can also open the Journal voucher page from the Invoice approval journal page.</span></span> <span data-ttu-id="103d8-111">В поле "Тип корр. счета" выберите "Основные средства".</span><span class="sxs-lookup"><span data-stu-id="103d8-111">In the Offset account type field, select Fixed assets.</span></span> <span data-ttu-id="103d8-112">В поле "Корр. счет" выберите номер основного средства.</span><span class="sxs-lookup"><span data-stu-id="103d8-112">Then, in the Offset account field, select a fixed asset number.</span></span> <span data-ttu-id="103d8-113">На вкладке "Основные средства" введите значения в поля "Тип проводки" и "Книга".</span><span class="sxs-lookup"><span data-stu-id="103d8-113">On the Fixed assets tab, enter values in the Transaction type and Book fields.</span></span>

## <a name="accounts-receivable"></a><span data-ttu-id="103d8-114">Расчеты с клиентами</span><span class="sxs-lookup"><span data-stu-id="103d8-114">Accounts receivable</span></span>
<span data-ttu-id="103d8-115">Проводки по основным средствам вводятся на странице "Накладная с произвольным текстом".</span><span class="sxs-lookup"><span data-stu-id="103d8-115">You can enter Fixed assets transactions in the Free text invoice page.</span></span>  <span data-ttu-id="103d8-116">На странице "Накладная с произвольным текстом" в сетке строк накладной выберите номенклатуру строки.</span><span class="sxs-lookup"><span data-stu-id="103d8-116">In the Free text invoice page, in the Invoice lines grid, select a line item.</span></span> <span data-ttu-id="103d8-117">Перейдите на экспресс-вкладку "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="103d8-117">Click the Line details FastTab.</span></span> <span data-ttu-id="103d8-118">Введите номер основных средств и книгу для проводки реализации.</span><span class="sxs-lookup"><span data-stu-id="103d8-118">Enter the fixed asset number and book for the disposal transaction.</span></span> <span data-ttu-id="103d8-119">Для накладных с произвольным текстом проводка основных средств всегда имеет тип "Выбытие (продажа)".</span><span class="sxs-lookup"><span data-stu-id="103d8-119">For free text invoices, the fixed asset transaction type is always Disposal - sale.</span></span>

## <a name="procurement-and-sourcing"></a><span data-ttu-id="103d8-120">Закупки и источники</span><span class="sxs-lookup"><span data-stu-id="103d8-120">Procurement and sourcing</span></span>
<span data-ttu-id="103d8-121">Проводки основных средств можно ввести на странице "Заказ на покупку".</span><span class="sxs-lookup"><span data-stu-id="103d8-121">You can enter Fixed assets transactions in the Purchase order page.</span></span> <span data-ttu-id="103d8-122">Введите необходимые сведения для создания заказа на покупку и нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="103d8-122">Enter the required information to create a purchase order, and then click OK.</span></span> <span data-ttu-id="103d8-123">На странице "Заказ на покупку" перейдите на экспресс-вкладку "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="103d8-123">In the Purchase order page, click the Line details FastTab.</span></span> <span data-ttu-id="103d8-124">Затем на вкладке "Основные средства" введите сведения об основном средстве.</span><span class="sxs-lookup"><span data-stu-id="103d8-124">Then, on the Fixed assets tab, enter information about the fixed asset.</span></span> 

<span data-ttu-id="103d8-125">Чтобы разнести проводку приобретения существующего основного средства, укажите номер основного средства, книгу и тип проводки.</span><span class="sxs-lookup"><span data-stu-id="103d8-125">To post an acquisition transaction for an existing fixed asset, specify the fixed asset number, book, and transaction type.</span></span> <span data-ttu-id="103d8-126">Если какая-либо часть этих сведений отсутствует, проводку основного средства не удастся выполнить.</span><span class="sxs-lookup"><span data-stu-id="103d8-126">The fixed asset cannot be posted if any of this information is missing.</span></span> <span data-ttu-id="103d8-127">Чтобы разнести проводку приобретения для нового основного средства, установите флажок "Новые основные средства?" и выберите группу основных средств, которая будут назначена новому основному средству.</span><span class="sxs-lookup"><span data-stu-id="103d8-127">To post an acquisition transaction for a new fixed asset, select the New fixed asset? option, and then select the fixed asset group to assign the new asset to.</span></span> <span data-ttu-id="103d8-128">Однако для строки не будут доступны никакие поля основных средств, если номенклатура входит в группу складских моделей, использующую складскую модель нормативных затрат.</span><span class="sxs-lookup"><span data-stu-id="103d8-128">However, no fixed asset fields are available for a line if the item is in an inventory model group that uses a standard cost inventory model.</span></span> <span data-ttu-id="103d8-129">Кроме того, параметрами, задаваемыми на странице "Параметры основных средств", определяется возможность разноски проводок приобретения из модулей покупок.</span><span class="sxs-lookup"><span data-stu-id="103d8-129">Additionally, the options that are defined in the Fixed assets parameters page determine whether you can post acquisition transactions from the purchasing modules.</span></span> 

<span data-ttu-id="103d8-130">Когда для приобретения основных средств используется заказ на покупку или журнал "Запасы в основное средство", изменению подвергается стоимость запасов.</span><span class="sxs-lookup"><span data-stu-id="103d8-130">When a purchase order or the Inventory to fixed assets journal is used to acquire fixed assets, the inventory value is affected.</span></span>

## <a name="general-ledger"></a><span data-ttu-id="103d8-131">Главная книга</span><span class="sxs-lookup"><span data-stu-id="103d8-131">General ledger</span></span>
<span data-ttu-id="103d8-132">Проводки любого типа по основным средствам могут быть разнесены на странице "Общий журнал".</span><span class="sxs-lookup"><span data-stu-id="103d8-132">Any fixed asset transaction type can be posted in the General journal page.</span></span> <span data-ttu-id="103d8-133">Для разноски проводок по основным средствам можно также использовать журналы в модуле "Основные средства".</span><span class="sxs-lookup"><span data-stu-id="103d8-133">You can also use journals in Fixed assets to post fixed asset transactions.</span></span>

## <a name="options-for-entering-fixed-asset-transaction-types"></a><span data-ttu-id="103d8-134">Параметры ввода типов проводок по основным средствам</span><span class="sxs-lookup"><span data-stu-id="103d8-134">Options for entering fixed asset transaction types</span></span>


| <span data-ttu-id="103d8-135">Тип транзакции</span><span class="sxs-lookup"><span data-stu-id="103d8-135">Transaction type</span></span>                    | <span data-ttu-id="103d8-136">Модуль</span><span class="sxs-lookup"><span data-stu-id="103d8-136">Module</span></span>                   | <span data-ttu-id="103d8-137">Параметры</span><span class="sxs-lookup"><span data-stu-id="103d8-137">Options</span></span>                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| <span data-ttu-id="103d8-138">Приобретение, корректировка приобретения</span><span class="sxs-lookup"><span data-stu-id="103d8-138">Acquisition, Acquisition adjustment</span></span> | <span data-ttu-id="103d8-139">Основные средства</span><span class="sxs-lookup"><span data-stu-id="103d8-139">Fixed assets</span></span>             | <span data-ttu-id="103d8-140">Основные средства, запасы в основное средство</span><span class="sxs-lookup"><span data-stu-id="103d8-140">Fixed assets, Inventory to fixed assets</span></span>   |
|                                     | <span data-ttu-id="103d8-141">Главная книга</span><span class="sxs-lookup"><span data-stu-id="103d8-141">General ledger</span></span>           | <span data-ttu-id="103d8-142">Общий журнал</span><span class="sxs-lookup"><span data-stu-id="103d8-142">General journal</span></span>                           |
|                                     | <span data-ttu-id="103d8-143">Расчеты с поставщиками</span><span class="sxs-lookup"><span data-stu-id="103d8-143">Accounts payable</span></span>         | <span data-ttu-id="103d8-144">Журнал накладных, журнал утверждения накладных</span><span class="sxs-lookup"><span data-stu-id="103d8-144">Invoice journal, Invoice approval journal</span></span> |
|                                     | <span data-ttu-id="103d8-145">Закупки и источники</span><span class="sxs-lookup"><span data-stu-id="103d8-145">Procurement and sourcing</span></span> | <span data-ttu-id="103d8-146">Заказ на покупку</span><span class="sxs-lookup"><span data-stu-id="103d8-146">Purchase order</span></span>                            |
| <span data-ttu-id="103d8-147">Амортизация</span><span class="sxs-lookup"><span data-stu-id="103d8-147">Depreciation</span></span>                        | <span data-ttu-id="103d8-148">Основные средства</span><span class="sxs-lookup"><span data-stu-id="103d8-148">Fixed assets</span></span>             | <span data-ttu-id="103d8-149">Основные средства</span><span class="sxs-lookup"><span data-stu-id="103d8-149">Fixed assets</span></span>                              |
|                                     | <span data-ttu-id="103d8-150">Главная книга</span><span class="sxs-lookup"><span data-stu-id="103d8-150">General ledger</span></span>           | <span data-ttu-id="103d8-151">Общий журнал</span><span class="sxs-lookup"><span data-stu-id="103d8-151">General journal</span></span>                           |
| <span data-ttu-id="103d8-152">Выбытие</span><span class="sxs-lookup"><span data-stu-id="103d8-152">Disposal</span></span>                            | <span data-ttu-id="103d8-153">Основные средства</span><span class="sxs-lookup"><span data-stu-id="103d8-153">Fixed assets</span></span>             | <span data-ttu-id="103d8-154">Основные средства</span><span class="sxs-lookup"><span data-stu-id="103d8-154">Fixed assets</span></span>                              |
| <span data-ttu-id="103d8-155">** **</span><span class="sxs-lookup"><span data-stu-id="103d8-155">** **</span></span>                               | <span data-ttu-id="103d8-156">Главная книга</span><span class="sxs-lookup"><span data-stu-id="103d8-156">General ledger</span></span>           | <span data-ttu-id="103d8-157">Общий журнал</span><span class="sxs-lookup"><span data-stu-id="103d8-157">General journal</span></span>                           |
| <span data-ttu-id="103d8-158">** **</span><span class="sxs-lookup"><span data-stu-id="103d8-158">** **</span></span>                               | <span data-ttu-id="103d8-159">Расчеты с клиентами</span><span class="sxs-lookup"><span data-stu-id="103d8-159">Accounts receivable</span></span>      | <span data-ttu-id="103d8-160">Накладная с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="103d8-160">Free text invoice</span></span>                         |



<span data-ttu-id="103d8-161">Дополнительные сведения см. в разделе [Интеграция основных средств](fixed-asset-integration.md).</span><span class="sxs-lookup"><span data-stu-id="103d8-161">For more information, see [Fixed assets integration](fixed-asset-integration.md).</span></span>




