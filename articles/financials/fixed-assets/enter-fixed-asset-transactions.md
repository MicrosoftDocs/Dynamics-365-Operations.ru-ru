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
ms.search.scope: Core, Operations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 18352ad921c2e2d110a7535f979272685105662f
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="fixed-asset-transaction-options"></a><span data-ttu-id="6f876-103">Параметры проводки с основными средствами</span><span class="sxs-lookup"><span data-stu-id="6f876-103">Fixed asset transaction options</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6f876-104">Эта статья описывает различные методы, доступные для создания проводок с основными средствами.</span><span class="sxs-lookup"><span data-stu-id="6f876-104">This article describes the different methods available to create fixed asset transactions.</span></span>

<span data-ttu-id="6f876-105">Модуль "Основные средства" можно настроить для интеграции с модулями "Расчеты с поставщиками", "Расчеты с клиентами", "Материально-техническое снабжение" и "Главная книга".</span><span class="sxs-lookup"><span data-stu-id="6f876-105">You can set up Fixed assets for integration with Accounts payable, Accounts receivable, Procurement and sourcing, and General ledger.</span></span> <span data-ttu-id="6f876-106">Есть также возможность переноса номенклатур из модуля "Управление запасами" в модуль "Основные средства", если эти номенклатуры требуется использовать внутри системы.</span><span class="sxs-lookup"><span data-stu-id="6f876-106">You can also transfer items in Inventory management to Fixed assets if you want to use those items internally.</span></span>

## <a name="accounts-payable"></a><span data-ttu-id="6f876-107">Расчеты с поставщиками</span><span class="sxs-lookup"><span data-stu-id="6f876-107">Accounts payable</span></span>
<span data-ttu-id="6f876-108">Проводки по основным средствам вводятся на странице "Ваучер журнала".</span><span class="sxs-lookup"><span data-stu-id="6f876-108">You can enter Fixed assets transactions in the Journal voucher page.</span></span> <span data-ttu-id="6f876-109">Эту страницу можно открыть на странице "Журнал накладных".</span><span class="sxs-lookup"><span data-stu-id="6f876-109">This page can be opened from the Invoice journal page.</span></span> <span data-ttu-id="6f876-110">Страницу "Ваучер журнала" также можно открыть на странице "Журнал утверждения накладных".</span><span class="sxs-lookup"><span data-stu-id="6f876-110">You can also open the Journal voucher page from the Invoice approval journal page.</span></span> <span data-ttu-id="6f876-111">В поле "Тип корр. счета" выберите "Основные средства".</span><span class="sxs-lookup"><span data-stu-id="6f876-111">In the Offset account type field, select Fixed assets.</span></span> <span data-ttu-id="6f876-112">В поле "Корр. счет" выберите номер основного средства.</span><span class="sxs-lookup"><span data-stu-id="6f876-112">Then, in the Offset account field, select a fixed asset number.</span></span> <span data-ttu-id="6f876-113">На вкладке "Основные средства" введите значения в поля "Тип проводки" и "Книга".</span><span class="sxs-lookup"><span data-stu-id="6f876-113">On the Fixed assets tab, enter values in the Transaction type and Book fields.</span></span>

## <a name="accounts-receivable"></a><span data-ttu-id="6f876-114">Расчеты с клиентами</span><span class="sxs-lookup"><span data-stu-id="6f876-114">Accounts receivable</span></span>
<span data-ttu-id="6f876-115">Проводки по основным средствам вводятся на странице "Накладная с произвольным текстом".</span><span class="sxs-lookup"><span data-stu-id="6f876-115">You can enter Fixed assets transactions in the Free text invoice page.</span></span>  <span data-ttu-id="6f876-116">На странице "Накладная с произвольным текстом" в сетке строк накладной выберите номенклатуру строки.</span><span class="sxs-lookup"><span data-stu-id="6f876-116">In the Free text invoice page, in the Invoice lines grid, select a line item.</span></span> <span data-ttu-id="6f876-117">Перейдите на экспресс-вкладку "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="6f876-117">Click the Line details FastTab.</span></span> <span data-ttu-id="6f876-118">Введите номер основных средств и книгу для проводки реализации.</span><span class="sxs-lookup"><span data-stu-id="6f876-118">Enter the fixed asset number and book for the disposal transaction.</span></span> <span data-ttu-id="6f876-119">Для накладных с произвольным текстом проводка основных средств всегда имеет тип "Выбытие (продажа)".</span><span class="sxs-lookup"><span data-stu-id="6f876-119">For free text invoices, the fixed asset transaction type is always Disposal - sale.</span></span>

## <a name="procurement-and-sourcing"></a><span data-ttu-id="6f876-120">Закупки и источники</span><span class="sxs-lookup"><span data-stu-id="6f876-120">Procurement and sourcing</span></span>
<span data-ttu-id="6f876-121">Проводки основных средств можно ввести на странице "Заказ на покупку".</span><span class="sxs-lookup"><span data-stu-id="6f876-121">You can enter Fixed assets transactions in the Purchase order page.</span></span> <span data-ttu-id="6f876-122">Введите необходимые сведения для создания заказа на покупку и нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="6f876-122">Enter the required information to create a purchase order, and then click OK.</span></span> <span data-ttu-id="6f876-123">На странице "Заказ на покупку" перейдите на экспресс-вкладку "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="6f876-123">In the Purchase order page, click the Line details FastTab.</span></span> <span data-ttu-id="6f876-124">Затем на вкладке "Основные средства" введите сведения об основном средстве.</span><span class="sxs-lookup"><span data-stu-id="6f876-124">Then, on the Fixed assets tab, enter information about the fixed asset.</span></span> 

<span data-ttu-id="6f876-125">Чтобы разнести проводку приобретения существующего основного средства, укажите номер основного средства, книгу и тип проводки.</span><span class="sxs-lookup"><span data-stu-id="6f876-125">To post an acquisition transaction for an existing fixed asset, specify the fixed asset number, book, and transaction type.</span></span> <span data-ttu-id="6f876-126">Если какая-либо часть этих сведений отсутствует, проводку основного средства не удастся выполнить.</span><span class="sxs-lookup"><span data-stu-id="6f876-126">The fixed asset cannot be posted if any of this information is missing.</span></span> <span data-ttu-id="6f876-127">Чтобы разнести проводку приобретения для нового основного средства, установите флажок "Новые основные средства?" и выберите группу основных средств, которая будут назначена новому основному средству.</span><span class="sxs-lookup"><span data-stu-id="6f876-127">To post an acquisition transaction for a new fixed asset, select the New fixed asset? option, and then select the fixed asset group to assign the new asset to.</span></span> <span data-ttu-id="6f876-128">Однако для строки не будут доступны никакие поля основных средств, если номенклатура входит в группу складских моделей, использующую складскую модель нормативных затрат.</span><span class="sxs-lookup"><span data-stu-id="6f876-128">However, no fixed asset fields are available for a line if the item is in an inventory model group that uses a standard cost inventory model.</span></span> <span data-ttu-id="6f876-129">Кроме того, параметрами, задаваемыми на странице "Параметры основных средств", определяется возможность разноски проводок приобретения из модулей покупок.</span><span class="sxs-lookup"><span data-stu-id="6f876-129">Additionally, the options that are defined in the Fixed assets parameters page determine whether you can post acquisition transactions from the purchasing modules.</span></span> 

<span data-ttu-id="6f876-130">Когда для приобретения основных средств используется заказ на покупку или журнал "Запасы в основное средство", изменению подвергается стоимость запасов.</span><span class="sxs-lookup"><span data-stu-id="6f876-130">When a purchase order or the Inventory to fixed assets journal is used to acquire fixed assets, the inventory value is affected.</span></span>

## <a name="general-ledger"></a><span data-ttu-id="6f876-131">Главная книга</span><span class="sxs-lookup"><span data-stu-id="6f876-131">General ledger</span></span>
<span data-ttu-id="6f876-132">Проводки любого типа по основным средствам могут быть разнесены на странице "Общий журнал".</span><span class="sxs-lookup"><span data-stu-id="6f876-132">Any fixed asset transaction type can be posted in the General journal page.</span></span> <span data-ttu-id="6f876-133">Для разноски проводок по основным средствам можно также использовать журналы в модуле "Основные средства".</span><span class="sxs-lookup"><span data-stu-id="6f876-133">You can also use journals in Fixed assets to post fixed asset transactions.</span></span>

## <a name="options-for-entering-fixed-asset-transaction-types"></a><span data-ttu-id="6f876-134">Параметры ввода типов проводок по основным средствам</span><span class="sxs-lookup"><span data-stu-id="6f876-134">Options for entering fixed asset transaction types</span></span>


| <span data-ttu-id="6f876-135">Тип транзакции</span><span class="sxs-lookup"><span data-stu-id="6f876-135">Transaction type</span></span>                    | <span data-ttu-id="6f876-136">Модуль</span><span class="sxs-lookup"><span data-stu-id="6f876-136">Module</span></span>                   | <span data-ttu-id="6f876-137">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f876-137">Options</span></span>                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| <span data-ttu-id="6f876-138">Приобретение, корректировка приобретения</span><span class="sxs-lookup"><span data-stu-id="6f876-138">Acquisition, Acquisition adjustment</span></span> | <span data-ttu-id="6f876-139">Основные средства</span><span class="sxs-lookup"><span data-stu-id="6f876-139">Fixed assets</span></span>             | <span data-ttu-id="6f876-140">Основные средства, запасы в основное средство</span><span class="sxs-lookup"><span data-stu-id="6f876-140">Fixed assets, Inventory to fixed assets</span></span>   |
|                                     | <span data-ttu-id="6f876-141">Главная книга</span><span class="sxs-lookup"><span data-stu-id="6f876-141">General ledger</span></span>           | <span data-ttu-id="6f876-142">Общий журнал</span><span class="sxs-lookup"><span data-stu-id="6f876-142">General journal</span></span>                           |
|                                     | <span data-ttu-id="6f876-143">Расчеты с поставщиками</span><span class="sxs-lookup"><span data-stu-id="6f876-143">Accounts payable</span></span>         | <span data-ttu-id="6f876-144">Журнал накладных, журнал утверждения накладных</span><span class="sxs-lookup"><span data-stu-id="6f876-144">Invoice journal, Invoice approval journal</span></span> |
|                                     | <span data-ttu-id="6f876-145">Закупки и источники</span><span class="sxs-lookup"><span data-stu-id="6f876-145">Procurement and sourcing</span></span> | <span data-ttu-id="6f876-146">Заказ на покупку</span><span class="sxs-lookup"><span data-stu-id="6f876-146">Purchase order</span></span>                            |
| <span data-ttu-id="6f876-147">Амортизация</span><span class="sxs-lookup"><span data-stu-id="6f876-147">Depreciation</span></span>                        | <span data-ttu-id="6f876-148">Основные средства</span><span class="sxs-lookup"><span data-stu-id="6f876-148">Fixed assets</span></span>             | <span data-ttu-id="6f876-149">Основные средства</span><span class="sxs-lookup"><span data-stu-id="6f876-149">Fixed assets</span></span>                              |
|                                     | <span data-ttu-id="6f876-150">Главная книга</span><span class="sxs-lookup"><span data-stu-id="6f876-150">General ledger</span></span>           | <span data-ttu-id="6f876-151">Общий журнал</span><span class="sxs-lookup"><span data-stu-id="6f876-151">General journal</span></span>                           |
| <span data-ttu-id="6f876-152">Выбытие</span><span class="sxs-lookup"><span data-stu-id="6f876-152">Disposal</span></span>                            | <span data-ttu-id="6f876-153">Основные средства</span><span class="sxs-lookup"><span data-stu-id="6f876-153">Fixed assets</span></span>             | <span data-ttu-id="6f876-154">Основные средства</span><span class="sxs-lookup"><span data-stu-id="6f876-154">Fixed assets</span></span>                              |
| <span data-ttu-id="6f876-155">** **</span><span class="sxs-lookup"><span data-stu-id="6f876-155">** **</span></span>                               | <span data-ttu-id="6f876-156">Главная книга</span><span class="sxs-lookup"><span data-stu-id="6f876-156">General ledger</span></span>           | <span data-ttu-id="6f876-157">Общий журнал</span><span class="sxs-lookup"><span data-stu-id="6f876-157">General journal</span></span>                           |
| <span data-ttu-id="6f876-158">** **</span><span class="sxs-lookup"><span data-stu-id="6f876-158">** **</span></span>                               | <span data-ttu-id="6f876-159">Расчеты с клиентами</span><span class="sxs-lookup"><span data-stu-id="6f876-159">Accounts receivable</span></span>      | <span data-ttu-id="6f876-160">Накладная с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="6f876-160">Free text invoice</span></span>                         |



<span data-ttu-id="6f876-161">Дополнительные сведения см. в разделе [Интеграция основных средств](fixed-asset-integration.md).</span><span class="sxs-lookup"><span data-stu-id="6f876-161">For more information, see [Fixed assets integration](fixed-asset-integration.md).</span></span>




