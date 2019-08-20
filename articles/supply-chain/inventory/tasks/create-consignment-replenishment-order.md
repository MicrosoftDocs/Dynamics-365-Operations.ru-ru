---
title: Создание заказа пополнения консигнационных запасов
description: В этой процедуре описан порядок создания заказа на пополнение коносамента, где можно отслеживать предполагаемую доставку от поставщика в своих консигнационные запасы.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 2cf2e8f742fee2dedaac72902d207af0081700ca
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845554"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="d3544-103">Создание заказа пополнения консигнационных запасов</span><span class="sxs-lookup"><span data-stu-id="d3544-103">Create a consignment replenishment order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d3544-104">В этой процедуре описан порядок создания заказа на пополнение коносамента, где можно отслеживать предполагаемую доставку от поставщика в своих консигнационные запасы.</span><span class="sxs-lookup"><span data-stu-id="d3544-104">This procedure shows how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="d3544-105">Она также показывает, как зарегистрировать поступление продуктов, чтобы запасы коносамента были зарегистрированы как запасы в наличии, принадлежащие поставщику.</span><span class="sxs-lookup"><span data-stu-id="d3544-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="d3544-106">Обычно эту процедуру выполняет специалист по закупкам.</span><span class="sxs-lookup"><span data-stu-id="d3544-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="d3544-107">Это руководство можно использовать в компании с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="d3544-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="d3544-108">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="d3544-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>




## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="d3544-109">Создание заказа пополнения консигнационных запасов</span><span class="sxs-lookup"><span data-stu-id="d3544-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="d3544-110">Перейдите в раздел "Закупки и источники" > "Коносамент" > "Заказы пополнения коносамента".</span><span class="sxs-lookup"><span data-stu-id="d3544-110">Go to Procurement and sourcing > Consignment > Consignment replenishment orders.</span></span>
2. <span data-ttu-id="d3544-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d3544-111">Click New.</span></span>
3. <span data-ttu-id="d3544-112">В поле "Счет поставщика" выберите поставщика "US-104".</span><span class="sxs-lookup"><span data-stu-id="d3544-112">In the Vendor account field, select vendor US-104.</span></span>
    * <span data-ttu-id="d3544-113">Необходимо выбрать поставщика, зарегистрированного в качестве владельца на странице "Владельцы запасов".</span><span class="sxs-lookup"><span data-stu-id="d3544-113">You must select a vendor that’s registered as an owner in the Inventory owners page.</span></span>  
4. <span data-ttu-id="d3544-114">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d3544-114">Click OK.</span></span>
5. <span data-ttu-id="d3544-115">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="d3544-115">Click Add line.</span></span>
6. <span data-ttu-id="d3544-116">В поле "Код номенклатуры" введите "M9211CI".</span><span class="sxs-lookup"><span data-stu-id="d3544-116">In the Item number field, type M9211CI.</span></span>
    * <span data-ttu-id="d3544-117">Необходимо выбрать номенклатуру, которая настроена для консигнационных запасов.</span><span class="sxs-lookup"><span data-stu-id="d3544-117">You must select an item that is set up for consignment inventory.</span></span>  
7. <span data-ttu-id="d3544-118">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="d3544-118">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="d3544-119">В поле "Запрошенная дата доставки" введите дату.</span><span class="sxs-lookup"><span data-stu-id="d3544-119">In the Requested delivery date field, enter a date.</span></span>
    * <span data-ttu-id="d3544-120">Запрошенные и подтвержденные даты используются модулем MRP для ожидаемого прихода товаров.</span><span class="sxs-lookup"><span data-stu-id="d3544-120">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="d3544-121">В поле "Подтвержденная дата доставки" введите дату.</span><span class="sxs-lookup"><span data-stu-id="d3544-121">In the Confirmed delivery date field, enter a date.</span></span>
10. <span data-ttu-id="d3544-122">Разверните раздел "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="d3544-122">Expand the Line details section.</span></span>
11. <span data-ttu-id="d3544-123">Перейдите на вкладку "Складские аналитики".</span><span class="sxs-lookup"><span data-stu-id="d3544-123">Click the Inventory dimensions tab.</span></span>
12. <span data-ttu-id="d3544-124">Чтобы отобразить владельца в поле владельца складских аналитик, обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="d3544-124">To show the owner in the Inventory dimensions owner field, refresh the page.</span></span>
    * <span data-ttu-id="d3544-125">Поставщик US-104 теперь указан в качестве владельца.</span><span class="sxs-lookup"><span data-stu-id="d3544-125">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="d3544-126">Проверка статуса складской проводки</span><span class="sxs-lookup"><span data-stu-id="d3544-126">Check the inventory transaction status</span></span>
1. <span data-ttu-id="d3544-127">Щелкните запасы.</span><span class="sxs-lookup"><span data-stu-id="d3544-127">Click Inventory.</span></span>
2. <span data-ttu-id="d3544-128">Щелкните "Проводки".</span><span class="sxs-lookup"><span data-stu-id="d3544-128">Click Transactions.</span></span>
3. <span data-ttu-id="d3544-129">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="d3544-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d3544-130">Обратите внимание, что в поле "Приход" установлено значение "Заказано".</span><span class="sxs-lookup"><span data-stu-id="d3544-130">Notice that the Receipt field is set to Ordered.</span></span>  
4. <span data-ttu-id="d3544-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d3544-131">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="d3544-132">Получить номенклатуры</span><span class="sxs-lookup"><span data-stu-id="d3544-132">Receive items</span></span>
1. <span data-ttu-id="d3544-133">Щелкните "Поступление продуктов".</span><span class="sxs-lookup"><span data-stu-id="d3544-133">Click Product receipt.</span></span>
2. <span data-ttu-id="d3544-134">В поле "Внешнее поступление продуктов" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d3544-134">In the External product receipt field, type a value.</span></span>
3. <span data-ttu-id="d3544-135">В поле "Количество" введите номер, который меньше номера, который отображается здесь.</span><span class="sxs-lookup"><span data-stu-id="d3544-135">In the Quantity field, enter a number that’s lower than the number that’s shown there.</span></span> 
4. <span data-ttu-id="d3544-136">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d3544-136">Click OK.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="d3544-137">Проверка запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="d3544-137">Check the on-hand inventory</span></span>
1. <span data-ttu-id="d3544-138">Щелкните запасы.</span><span class="sxs-lookup"><span data-stu-id="d3544-138">Click Inventory.</span></span>
2. <span data-ttu-id="d3544-139">Щелкните "В наличии".</span><span class="sxs-lookup"><span data-stu-id="d3544-139">Click On-hand.</span></span>
3. <span data-ttu-id="d3544-140">Щелкните "Обзор".</span><span class="sxs-lookup"><span data-stu-id="d3544-140">Click Overview.</span></span>
    * <span data-ttu-id="d3544-141">Номенклатуры, которые были получены как консигнационные запасы, принадлежащие поставщику, доступны в наличии.</span><span class="sxs-lookup"><span data-stu-id="d3544-141">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="d3544-142">Оставшееся количество заказанного пополнения коносамента отображается в поле "Всего заказано".</span><span class="sxs-lookup"><span data-stu-id="d3544-142">The remaining quantity on the consignment replenishment order is shown in the Ordered in total field.</span></span>  
4. <span data-ttu-id="d3544-143">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d3544-143">Close the page.</span></span>
5. <span data-ttu-id="d3544-144">Щелкните "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="d3544-144">Click Close.</span></span>

