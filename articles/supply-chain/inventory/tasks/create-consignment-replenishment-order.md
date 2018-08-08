---
title: "Создание заказа пополнения консигнационных запасов"
description: "В этой процедуре описан порядок создания заказа на пополнение коносамента, где можно отслеживать предполагаемую доставку от поставщика в своих консигнационные запасы."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 6366d6188d97ca54ba65c11699140be9ae2d4002
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="ec949-103">Создание заказа пополнения консигнационных запасов</span><span class="sxs-lookup"><span data-stu-id="ec949-103">Create a consignment replenishment order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ec949-104">В этой процедуре описан порядок создания заказа на пополнение коносамента, где можно отслеживать предполагаемую доставку от поставщика в своих консигнационные запасы.</span><span class="sxs-lookup"><span data-stu-id="ec949-104">This procedure shows how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="ec949-105">Она также показывает, как зарегистрировать поступление продуктов, чтобы запасы коносамента были зарегистрированы как запасы в наличии, принадлежащие поставщику.</span><span class="sxs-lookup"><span data-stu-id="ec949-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="ec949-106">Обычно эту процедуру выполняет специалист по закупкам.</span><span class="sxs-lookup"><span data-stu-id="ec949-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="ec949-107">Это руководство можно использовать в компании с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="ec949-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="ec949-108">Эта процедура предназначена для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="ec949-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>




## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="ec949-109">Создание заказа пополнения консигнационных запасов</span><span class="sxs-lookup"><span data-stu-id="ec949-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="ec949-110">Перейдите в раздел "Закупки и источники" > "Коносамент" > "Заказы пополнения коносамента".</span><span class="sxs-lookup"><span data-stu-id="ec949-110">Go to Procurement and sourcing > Consignment > Consignment replenishment orders.</span></span>
2. <span data-ttu-id="ec949-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="ec949-111">Click New.</span></span>
3. <span data-ttu-id="ec949-112">В поле "Счет поставщика" выберите поставщика "US-104".</span><span class="sxs-lookup"><span data-stu-id="ec949-112">In the Vendor account field, select vendor US-104.</span></span>
    * <span data-ttu-id="ec949-113">Необходимо выбрать поставщика, зарегистрированного в качестве владельца на странице "Владельцы запасов".</span><span class="sxs-lookup"><span data-stu-id="ec949-113">You must select a vendor that’s registered as an owner in the Inventory owners page.</span></span>  
4. <span data-ttu-id="ec949-114">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ec949-114">Click OK.</span></span>
5. <span data-ttu-id="ec949-115">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="ec949-115">Click Add line.</span></span>
6. <span data-ttu-id="ec949-116">В поле "Код номенклатуры" введите "M9211CI".</span><span class="sxs-lookup"><span data-stu-id="ec949-116">In the Item number field, type M9211CI.</span></span>
    * <span data-ttu-id="ec949-117">Необходимо выбрать номенклатуру, которая настроена для консигнационных запасов.</span><span class="sxs-lookup"><span data-stu-id="ec949-117">You must select an item that is set up for consignment inventory.</span></span>  
7. <span data-ttu-id="ec949-118">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="ec949-118">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="ec949-119">В поле "Запрошенная дата доставки" введите дату.</span><span class="sxs-lookup"><span data-stu-id="ec949-119">In the Requested delivery date field, enter a date.</span></span>
    * <span data-ttu-id="ec949-120">Запрошенные и подтвержденные даты используются модулем MRP для ожидаемого прихода товаров.</span><span class="sxs-lookup"><span data-stu-id="ec949-120">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="ec949-121">В поле "Подтвержденная дата доставки" введите дату.</span><span class="sxs-lookup"><span data-stu-id="ec949-121">In the Confirmed delivery date field, enter a date.</span></span>
10. <span data-ttu-id="ec949-122">Разверните раздел "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="ec949-122">Expand the Line details section.</span></span>
11. <span data-ttu-id="ec949-123">Перейдите на вкладку "Складские аналитики".</span><span class="sxs-lookup"><span data-stu-id="ec949-123">Click the Inventory dimensions tab.</span></span>
12. <span data-ttu-id="ec949-124">Чтобы отобразить владельца в поле владельца складских аналитик, обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="ec949-124">To show the owner in the Inventory dimensions owner field, refresh the page.</span></span>
    * <span data-ttu-id="ec949-125">Поставщик US-104 теперь указан в качестве владельца.</span><span class="sxs-lookup"><span data-stu-id="ec949-125">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="ec949-126">Проверка статуса складской проводки</span><span class="sxs-lookup"><span data-stu-id="ec949-126">Check the inventory transaction status</span></span>
1. <span data-ttu-id="ec949-127">Щелкните запасы.</span><span class="sxs-lookup"><span data-stu-id="ec949-127">Click Inventory.</span></span>
2. <span data-ttu-id="ec949-128">Щелкните "Проводки".</span><span class="sxs-lookup"><span data-stu-id="ec949-128">Click Transactions.</span></span>
3. <span data-ttu-id="ec949-129">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="ec949-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ec949-130">Обратите внимание, что в поле "Приход" установлено значение "Заказано".</span><span class="sxs-lookup"><span data-stu-id="ec949-130">Notice that the Receipt field is set to Ordered.</span></span>  
4. <span data-ttu-id="ec949-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ec949-131">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="ec949-132">Получить номенклатуры</span><span class="sxs-lookup"><span data-stu-id="ec949-132">Receive items</span></span>
1. <span data-ttu-id="ec949-133">Щелкните "Поступление продуктов".</span><span class="sxs-lookup"><span data-stu-id="ec949-133">Click Product receipt.</span></span>
2. <span data-ttu-id="ec949-134">В поле "Внешнее поступление продуктов" введите значение.</span><span class="sxs-lookup"><span data-stu-id="ec949-134">In the External product receipt field, type a value.</span></span>
3. <span data-ttu-id="ec949-135">В поле "Количество" введите номер, который меньше номера, который отображается здесь.</span><span class="sxs-lookup"><span data-stu-id="ec949-135">In the Quantity field, enter a number that’s lower than the number that’s shown there.</span></span>
4. <span data-ttu-id="ec949-136">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ec949-136">Click OK.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="ec949-137">Проверка запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="ec949-137">Check the on-hand inventory</span></span>
1. <span data-ttu-id="ec949-138">Щелкните запасы.</span><span class="sxs-lookup"><span data-stu-id="ec949-138">Click Inventory.</span></span>
2. <span data-ttu-id="ec949-139">Щелкните "В наличии".</span><span class="sxs-lookup"><span data-stu-id="ec949-139">Click On-hand.</span></span>
3. <span data-ttu-id="ec949-140">Щелкните "Обзор".</span><span class="sxs-lookup"><span data-stu-id="ec949-140">Click Overview.</span></span>
    * <span data-ttu-id="ec949-141">Номенклатуры, которые были получены как консигнационные запасы, принадлежащие поставщику, доступны в наличии.</span><span class="sxs-lookup"><span data-stu-id="ec949-141">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="ec949-142">Оставшееся количество заказанного пополнения коносамента отображается в поле "Всего заказано".</span><span class="sxs-lookup"><span data-stu-id="ec949-142">The remaining quantity on the consignment replenishment order is shown in the Ordered in total field.</span></span>  
4. <span data-ttu-id="ec949-143">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ec949-143">Close the page.</span></span>
5. <span data-ttu-id="ec949-144">Щелкните "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="ec949-144">Click Close.</span></span>

