---
title: Получение номенклатур в заказе на покупку из потребности в номенклатуре
description: В этой теме показано, как получить номенклатуры по заказу на покупку из потребности в номенклатуре.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7afdae65c5ae7e3196c6b9f142dd87aec39b5ea3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174428"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="5fe51-103">Получение номенклатур в заказе на покупку из потребности в номенклатуре</span><span class="sxs-lookup"><span data-stu-id="5fe51-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5fe51-104">В этой теме показано, как получить номенклатуры по заказу на покупку из потребности в номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="5fe51-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="5fe51-105">Используя потребность в номенклатуре вместо проводки с номенклатурой, можно запланировать поставку перед самым моментом использования данной номенклатуры, создать заказ на покупку, включить номенклатуру в схему коммерческих соглашений, и использовать потребность в номенклатуре при планировании производства.</span><span class="sxs-lookup"><span data-stu-id="5fe51-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="5fe51-106">В этой задаче используется набор данных компании USSI.</span><span class="sxs-lookup"><span data-stu-id="5fe51-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="5fe51-107">В области переходов выберите **Модули > Управление и учет по проектам > Проекты > Все проекты**.</span><span class="sxs-lookup"><span data-stu-id="5fe51-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="5fe51-108">В списке выберите ссылку в требуемой строке.</span><span class="sxs-lookup"><span data-stu-id="5fe51-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="5fe51-109">В области действий выберите **План**.</span><span class="sxs-lookup"><span data-stu-id="5fe51-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="5fe51-110">Выберите **Требования по номенклатурам**.</span><span class="sxs-lookup"><span data-stu-id="5fe51-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="5fe51-111">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="5fe51-111">Select **New**.</span></span>
6. <span data-ttu-id="5fe51-112">В новой строке введите или выберите значение в поле **Код номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="5fe51-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="5fe51-113">В поле **Количество** введите число.</span><span class="sxs-lookup"><span data-stu-id="5fe51-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="5fe51-114">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="5fe51-114">Select **Save**.</span></span>
9. <span data-ttu-id="5fe51-115">На панели операций выберите **Управление**.</span><span class="sxs-lookup"><span data-stu-id="5fe51-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="5fe51-116">Выберите **Функции**.</span><span class="sxs-lookup"><span data-stu-id="5fe51-116">Select **Functions**.</span></span>
11. <span data-ttu-id="5fe51-117">Выберите **Создать заказ на покупку**.</span><span class="sxs-lookup"><span data-stu-id="5fe51-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="5fe51-118">Установите флажок **Включить все**.</span><span class="sxs-lookup"><span data-stu-id="5fe51-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="5fe51-119">В поле **Счет поставщика** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="5fe51-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="5fe51-120">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5fe51-120">Select **OK**.</span></span>
15. <span data-ttu-id="5fe51-121">В области перехода перейдите к **Модули > Расчеты с поставщиками > Заказы на покупку > Все заказы на покупку**.</span><span class="sxs-lookup"><span data-stu-id="5fe51-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="5fe51-122">В списке выберите ссылку в требуемой строке.</span><span class="sxs-lookup"><span data-stu-id="5fe51-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="5fe51-123">На панели операций выберите **Покупка**.</span><span class="sxs-lookup"><span data-stu-id="5fe51-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="5fe51-124">Выберите **Подтвердить**.</span><span class="sxs-lookup"><span data-stu-id="5fe51-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="5fe51-125">На панели операций выберите **Получить**.</span><span class="sxs-lookup"><span data-stu-id="5fe51-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="5fe51-126">Выберите **Поступление продуктов**.</span><span class="sxs-lookup"><span data-stu-id="5fe51-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="5fe51-127">В поле **Поступление продуктов** введите значение.</span><span class="sxs-lookup"><span data-stu-id="5fe51-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="5fe51-128">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5fe51-128">Select **OK**.</span></span>

