---
title: Создание заказа пополнения консигнационных запасов
description: В этой теме описан порядок создания заказа на пополнение коносамента, где можно отслеживать предполагаемую доставку от поставщика в своих консигнационные запасы.
author: mkirknel
manager: AnnBe
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 766f29f7511c16eccd37e93f2de366ac23c35545
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145809"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="9e28a-103">Создание заказа пополнения консигнационных запасов</span><span class="sxs-lookup"><span data-stu-id="9e28a-103">Create a consignment replenishment order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9e28a-104">В этой теме описан порядок создания заказа на пополнение коносамента, где можно отслеживать предполагаемую доставку от поставщика в своих консигнационные запасы.</span><span class="sxs-lookup"><span data-stu-id="9e28a-104">This topic explains how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="9e28a-105">Она также показывает, как зарегистрировать поступление продуктов, чтобы запасы коносамента были зарегистрированы как запасы в наличии, принадлежащие поставщику.</span><span class="sxs-lookup"><span data-stu-id="9e28a-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="9e28a-106">Обычно эту процедуру выполняет специалист по закупкам.</span><span class="sxs-lookup"><span data-stu-id="9e28a-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="9e28a-107">Это руководство можно использовать в компании с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="9e28a-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="9e28a-108">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="9e28a-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="9e28a-109">Создание заказа пополнения консигнационных запасов</span><span class="sxs-lookup"><span data-stu-id="9e28a-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="9e28a-110">В области перехода перейдите к **Модули > Закупки и источники > Коносамент > Заказы пополнения коносамента**.</span><span class="sxs-lookup"><span data-stu-id="9e28a-110">In the navigation pane, go to **Modules > Procurement and sourcing > Consignment > Consignment replenishment orders**.</span></span>
2. <span data-ttu-id="9e28a-111">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="9e28a-111">Select **New**.</span></span>
3. <span data-ttu-id="9e28a-112">В поле **Счет поставщика** выберите поставщика **US-104** (необходимо выбрать поставщика, который зарегистрирован в качестве владельца на странице **владельцы запасов**).</span><span class="sxs-lookup"><span data-stu-id="9e28a-112">In the **Vendor account** field, select vendor **US-104** (you must select a vendor that's registered as an owner in the **inventory owners** page).</span></span> 
4. <span data-ttu-id="9e28a-113">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9e28a-113">Select **OK**.</span></span>
5. <span data-ttu-id="9e28a-114">Выберите **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="9e28a-114">Select **Add line**.</span></span>
6. <span data-ttu-id="9e28a-115">В поле **Код номенклатуры** введите `M9211CI` (необходимо выбрать номенклатуру, настроенную для запасов коносамента).</span><span class="sxs-lookup"><span data-stu-id="9e28a-115">In the **Item number** field, type `M9211CI` (you must select an item that is set up for consignment inventory).</span></span>
7. <span data-ttu-id="9e28a-116">В поле **Количество** введите число.</span><span class="sxs-lookup"><span data-stu-id="9e28a-116">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="9e28a-117">В поле **Запрошенная дата доставки** введите дату.</span><span class="sxs-lookup"><span data-stu-id="9e28a-117">In the **Requested delivery date** field, enter a date.</span></span> <span data-ttu-id="9e28a-118">Запрошенные и подтвержденные даты используются модулем MRP для ожидаемого прихода товаров.</span><span class="sxs-lookup"><span data-stu-id="9e28a-118">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="9e28a-119">В поле **Подтвержденная дата доставки** введите дату.</span><span class="sxs-lookup"><span data-stu-id="9e28a-119">In the **Confirmed delivery date** field, enter a date.</span></span>
10. <span data-ttu-id="9e28a-120">Разверните раздел **Сведения о строке**.</span><span class="sxs-lookup"><span data-stu-id="9e28a-120">Expand the **Line details** section.</span></span>
11. <span data-ttu-id="9e28a-121">Выберите вкладку **Складские аналитики**.</span><span class="sxs-lookup"><span data-stu-id="9e28a-121">Select the **Inventory dimensions** tab.</span></span>
12. <span data-ttu-id="9e28a-122">Чтобы отобразить владельца в поле **Владелец складских аналитик**, обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="9e28a-122">To show the owner in the **Inventory dimensions owner** field, refresh the page.</span></span> <span data-ttu-id="9e28a-123">Поставщик US-104 теперь указан в качестве владельца.</span><span class="sxs-lookup"><span data-stu-id="9e28a-123">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="9e28a-124">Проверка статуса складской проводки</span><span class="sxs-lookup"><span data-stu-id="9e28a-124">Check the inventory transaction status</span></span>
1. <span data-ttu-id="9e28a-125">Выберите **Запасы**.</span><span class="sxs-lookup"><span data-stu-id="9e28a-125">Select **Inventory**.</span></span>
2. <span data-ttu-id="9e28a-126">Выберите **Проводки**.</span><span class="sxs-lookup"><span data-stu-id="9e28a-126">Select **Transactions**.</span></span>
3. <span data-ttu-id="9e28a-127">В требуемой строке обратите внимание, что в поле **Приход** установлено значение **Заказано**.</span><span class="sxs-lookup"><span data-stu-id="9e28a-127">In the desired row, notice that the **Receipt** field is set to **Ordered**.</span></span>  
4. <span data-ttu-id="9e28a-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9e28a-128">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="9e28a-129">Получить номенклатуры</span><span class="sxs-lookup"><span data-stu-id="9e28a-129">Receive items</span></span>
1. <span data-ttu-id="9e28a-130">Выберите **Поступление продуктов**.</span><span class="sxs-lookup"><span data-stu-id="9e28a-130">Select **Product receipt**.</span></span>
2. <span data-ttu-id="9e28a-131">В поле **Внешнее поступление продуктов** введите значение.</span><span class="sxs-lookup"><span data-stu-id="9e28a-131">In the **External product receipt** field, type a value.</span></span>
3. <span data-ttu-id="9e28a-132">В поле **Количество** введите номер, который меньше номера, который отображается здесь.</span><span class="sxs-lookup"><span data-stu-id="9e28a-132">In the **Quantity** field, enter a number that's lower than the number that's shown there.</span></span> 
4. <span data-ttu-id="9e28a-133">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9e28a-133">Select **OK**.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="9e28a-134">Проверка запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="9e28a-134">Check the on-hand inventory</span></span>
1. <span data-ttu-id="9e28a-135">Выберите **Запасы**.</span><span class="sxs-lookup"><span data-stu-id="9e28a-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="9e28a-136">Выберите **Запасы в наличии**.</span><span class="sxs-lookup"><span data-stu-id="9e28a-136">Select **On-hand**.</span></span>
3. <span data-ttu-id="9e28a-137">Выберите **Обзор**.</span><span class="sxs-lookup"><span data-stu-id="9e28a-137">Select **Overview**.</span></span> <span data-ttu-id="9e28a-138">Номенклатуры, которые были получены как консигнационные запасы, принадлежащие поставщику, доступны в наличии.</span><span class="sxs-lookup"><span data-stu-id="9e28a-138">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="9e28a-139">Оставшееся количество заказанного пополнения коносамента отображается в поле **Всего заказано**.</span><span class="sxs-lookup"><span data-stu-id="9e28a-139">The remaining quantity on the consignment replenishment order is shown in the **Ordered in total** field.</span></span>  
4. <span data-ttu-id="9e28a-140">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9e28a-140">Close the page.</span></span>

