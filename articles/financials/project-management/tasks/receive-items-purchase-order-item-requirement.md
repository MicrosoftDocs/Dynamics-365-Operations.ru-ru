--- 
title: "Получение номенклатур в заказе на покупку из потребности в номенклатуре"
description: "В этой процедуре показано, как получить номенклатуры по заказу на покупку из потребности в номенклатуре."
author: KimANelson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: faaea6c46e83dc85e9b7efe7a9ca5c261811a3de
ms.contentlocale: ru-ru
ms.lasthandoff: 09/11/2018

---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="d16a0-103">Получение номенклатур в заказе на покупку из потребности в номенклатуре</span><span class="sxs-lookup"><span data-stu-id="d16a0-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d16a0-104">В этой процедуре показано, как получить номенклатуры по заказу на покупку из потребности в номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="d16a0-104">This procedure shows how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="d16a0-105">Используя потребность в номенклатуре вместо проводки с номенклатурой, можно запланировать поставку перед самым моментом использования данной номенклатуры, создать заказ на покупку, включить номенклатуру в схему коммерческих соглашений, и использовать потребность в номенклатуре при планировании производства.</span><span class="sxs-lookup"><span data-stu-id="d16a0-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="d16a0-106">В этой задаче используется набор данных компании USSI.</span><span class="sxs-lookup"><span data-stu-id="d16a0-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="d16a0-107">Перейдите в раздел "Управление и учет по проектам" > "Проекты" > "Все проекты".</span><span class="sxs-lookup"><span data-stu-id="d16a0-107">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="d16a0-108">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="d16a0-108">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="d16a0-109">В области действий щелкните "План".</span><span class="sxs-lookup"><span data-stu-id="d16a0-109">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="d16a0-110">Щелкните "Потребности в номенклатуре".</span><span class="sxs-lookup"><span data-stu-id="d16a0-110">Click Item requirements.</span></span>
5. <span data-ttu-id="d16a0-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d16a0-111">Click New.</span></span>
6. <span data-ttu-id="d16a0-112">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="d16a0-112">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="d16a0-113">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d16a0-113">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="d16a0-114">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="d16a0-114">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="d16a0-115">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d16a0-115">Click Save.</span></span>
10. <span data-ttu-id="d16a0-116">В области действий щелкните "Управлять".</span><span class="sxs-lookup"><span data-stu-id="d16a0-116">On the Action Pane, click Manage.</span></span>
11. <span data-ttu-id="d16a0-117">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="d16a0-117">Click Functions.</span></span>
12. <span data-ttu-id="d16a0-118">Щелкните "Создать заказ на покупку".</span><span class="sxs-lookup"><span data-stu-id="d16a0-118">Click Create purchase order.</span></span>
13. <span data-ttu-id="d16a0-119">Установите флажок "Включить".</span><span class="sxs-lookup"><span data-stu-id="d16a0-119">Select the Include check box.</span></span>
14. <span data-ttu-id="d16a0-120">В поле "Счет поставщика" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d16a0-120">In the Vendor account field, enter or select a value.</span></span>
15. <span data-ttu-id="d16a0-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d16a0-121">Click OK.</span></span>
16. <span data-ttu-id="d16a0-122">Перейдите в раздел "Расчеты с поставщиками" > "Заказы на покупку" > "Все заказы на покупку".</span><span class="sxs-lookup"><span data-stu-id="d16a0-122">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
17. <span data-ttu-id="d16a0-123">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="d16a0-123">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="d16a0-124">В области действий щелкните "Покупка".</span><span class="sxs-lookup"><span data-stu-id="d16a0-124">On the Action Pane, click Purchase.</span></span>
19. <span data-ttu-id="d16a0-125">Нажмите кнопку "Подтвердить".</span><span class="sxs-lookup"><span data-stu-id="d16a0-125">Click Confirm.</span></span>
20. <span data-ttu-id="d16a0-126">В области действий щелкните "Получение".</span><span class="sxs-lookup"><span data-stu-id="d16a0-126">On the Action Pane, click Receive.</span></span>
21. <span data-ttu-id="d16a0-127">Щелкните "Поступление продуктов".</span><span class="sxs-lookup"><span data-stu-id="d16a0-127">Click Product receipt.</span></span>
22. <span data-ttu-id="d16a0-128">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="d16a0-128">In the list, mark the selected row.</span></span>
23. <span data-ttu-id="d16a0-129">В поле "Поступление продуктов" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d16a0-129">In the Product receipt field, type a value.</span></span>
24. <span data-ttu-id="d16a0-130">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d16a0-130">Click OK.</span></span>


