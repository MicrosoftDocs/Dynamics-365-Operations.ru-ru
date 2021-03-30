---
title: Проверка доступности запасов
description: В этой процедуре показано, как проверить запасы в наличии и физические запасы в наличии для определенного кода номенклатуры.
author: ShylaThompson
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand, InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2153117d9c921b43658edeade49a8403553e371
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238070"
---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="b2bc2-103">Проверка доступности запасов</span><span class="sxs-lookup"><span data-stu-id="b2bc2-103">Check the availability of stock</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b2bc2-104">В этой процедуре показано, как проверить запасы в наличии и физические запасы в наличии для определенного кода номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="b2bc2-105">В ней также показано, как получить информацию о поставках, связанную с номенклатурой.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="b2bc2-106">Физические запасы в наличии — это доступные запасы в наличии, то есть они куплены, получены и зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-106">Physical on-hand inventory is the on-hand inventory that's available – that is, it's purchased, received and registered.</span></span> <span data-ttu-id="b2bc2-107">Запасы в наличии включают доступные запасы в наличии, но также запасы, которые были заказаны и ожидаются, но еще не получены и не зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-107">On-hand inventory includes the available on-hand inventory, but also the inventory that's been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="b2bc2-108">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="b2bc2-109">При использовании USMF можно использовать представленные примеры значений.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="b2bc2-110">Эти задачи обычно выполняются работником склада.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="b2bc2-111">Проверка запасов в наличии для номенклатуры</span><span class="sxs-lookup"><span data-stu-id="b2bc2-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="b2bc2-112">Перейдите в раздел **Область переходов > Модули > Управление запасами > Запросы и отчеты > Запасы в наличии**.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-112">Go to **Navigation pane > Modules > Inventory management > Inquiries and reports > On-hand inventory**.</span></span>
2. <span data-ttu-id="b2bc2-113">Выберите строку **Код номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-113">Select the **Item number** row.</span></span> <span data-ttu-id="b2bc2-114">Для запроса запасов в наличии по коду номенклатуры выберите строку, в которой для параметра "Таблица" задано значение **Запасы в наличии**, а для параметра "Поле" — **Код номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-114">To query the on-hand inventory by item number, select the row where the Table is set to **On-hand inventory** and Field is set to **Item** number.</span></span>
3. <span data-ttu-id="b2bc2-115">В поле **Критерии** выберите номенклатуру для запроса.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-115">In the **Criteria** field, select the item you want to query.</span></span> <span data-ttu-id="b2bc2-116">При использовании компании с демонстрационными данными USMF можно выбрать значение "M9201".</span><span class="sxs-lookup"><span data-stu-id="b2bc2-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="b2bc2-117">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-117">Click **OK**.</span></span>
5. <span data-ttu-id="b2bc2-118">В области **Панель операций** щелкните **Аналитики**.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-118">On the **Action Pane**, click **Dimensions**.</span></span> <span data-ttu-id="b2bc2-119">На вкладке **Аналитики** можно указать, какие сведения о запасах в наличии будут отображаться.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-119">The **Dimensions** tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="b2bc2-120">Если требуются данные, связанные с резервированием, необходимо отобразить все складские аналитики для номенклатур, использующих расширенные процессы управления складом.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WMS) processes.</span></span>
6. <span data-ttu-id="b2bc2-121">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-121">Click **OK**.</span></span>
7. <span data-ttu-id="b2bc2-122">В области **Панель операций** щелкните **Связанные сведения**.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-122">On the **Action Pane**, click **Related information**.</span></span> <span data-ttu-id="b2bc2-123">Если этот параметр не отображается, может потребоваться нажать кнопку многоточия (…), чтобы просмотреть дополнительные параметры области действий.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-123">If you don't see this option, you may need to click on the Ellipsis button (…) to see additional Action Pane options.</span></span>
8. <span data-ttu-id="b2bc2-124">Щелкните **Обзор поставки**.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-124">Click **Supply overview**.</span></span> <span data-ttu-id="b2bc2-125">На вкладке **Обзор поставки** отображаются сведения о поставках для конкретной номенклатуры, например количество в наличии, время упреждения и сведения о поставщике.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-125">The **Supply overview** tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="b2bc2-126">Разверните раздел **В наличии**.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-126">Expand the **On-hand** section.</span></span>
10. <span data-ttu-id="b2bc2-127">Разверните раздел **Поставщики**.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-127">Expand the **Vendors** section.</span></span>
11. <span data-ttu-id="b2bc2-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-128">Close the page.</span></span>
12. <span data-ttu-id="b2bc2-129">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="b2bc2-130">Проверка физических запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="b2bc2-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="b2bc2-131">Перейдите в раздел **Область переходов > Модули > Управление складом > Запросы и отчеты > Физические запасы в наличии**.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-131">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > Physical on-hand inventory**.</span></span>
2. <span data-ttu-id="b2bc2-132">В поле **Код номенклатуры** введите значение.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-132">In the **Item number** field, type a value.</span></span> <span data-ttu-id="b2bc2-133">Поля "Сайт" и "Склад" можно использовать для фильтрации списка номенклатур.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-133">You can use the Site and Warehouse fields to filter the list of items.</span></span> 
3. <span data-ttu-id="b2bc2-134">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-134">Refresh the page.</span></span>
4. <span data-ttu-id="b2bc2-135">В области **Панель операций** щелкните **Отобразить аналитики**.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-135">On the **Action Pane**, click **Display Dimensions**.</span></span> <span data-ttu-id="b2bc2-136">На вкладке "Отображение аналитик" можно указать, какие сведения о запасах в наличии будут отображаться.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>
5. <span data-ttu-id="b2bc2-137">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-137">Click **OK**.</span></span>
6. <span data-ttu-id="b2bc2-138">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="b2bc2-139">Проверка запасов в наличии по местоположению</span><span class="sxs-lookup"><span data-stu-id="b2bc2-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="b2bc2-140">Перейдите в раздел **Область переходов > Модули > Управление складом > Запросы и отчеты > В наличии по местонахождению**.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-140">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > On hand by location**.</span></span>
2. <span data-ttu-id="b2bc2-141">В поле **Склад** введите значение.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-141">In the **Warehouse** field, type a value.</span></span> <span data-ttu-id="b2bc2-142">При использовании компании с демонстрационными данными USMF можно использовать значение "51".</span><span class="sxs-lookup"><span data-stu-id="b2bc2-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="b2bc2-143">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-143">Refresh the page.</span></span>
4. <span data-ttu-id="b2bc2-144">Щелкните **Отобразить аналитики**.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-144">Click **Display Dimensions**.</span></span>
5. <span data-ttu-id="b2bc2-145">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-145">Click **OK**.</span></span>
6. <span data-ttu-id="b2bc2-146">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b2bc2-146">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]