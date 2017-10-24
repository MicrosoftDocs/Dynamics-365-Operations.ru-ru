---
title: "Поштучное подтверждение комплектации"
description: "В этом разделе описывается, как настроить и применить поштучное подтверждение комплектации на мобильном устройстве."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 62b637b81a522c353067248deea79cfbf98518e9
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="piece-picking-confirmation"></a><span data-ttu-id="5b7f5-103">Поштучное подтверждение комплектации</span><span class="sxs-lookup"><span data-stu-id="5b7f5-103">Piece picking confirmation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5b7f5-104">Поштучная комплектация позволяет подтверждать каждую штуку запасов посредством работ по комплектации или инвентаризации на мобильном устройстве</span><span class="sxs-lookup"><span data-stu-id="5b7f5-104">Piece picking allows you to confirm each piece of inventory through picking or counting work on a mobile device.</span></span> <span data-ttu-id="5b7f5-105">При комплектации можно подтвердить количество работы, подлежащей обработке, вплоть до количества, указанного в работе для комплектации.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-105">For picks, you can confirm the quantity of work to be processed up to the quantity that is specified on work to be picked.</span></span> <span data-ttu-id="5b7f5-106">Для работы по инвентаризации вы можете сканировать запасы, которые подсчитываете, и отслеживать общую сумму.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-106">For counting work, you can scan the inventory that you are counting and track the total amount.</span></span>

<span data-ttu-id="5b7f5-107">При включении поштучной комплектации подтверждение продукта устанавливается автоматически.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-107">When you enable piece picking, product confirmation is automatically selected.</span></span> <span data-ttu-id="5b7f5-108">Для работ типа "комплектация" включается максимальное число штук.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-108">For work-type picks, a maximum number of pieces is enabled.</span></span> <span data-ttu-id="5b7f5-109">Это позволяет задать максимальное число штук, которые должны быть подтверждены во время рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-109">This allows you to set a maximum to the number of pieces that must be confirmed during the work process.</span></span> <span data-ttu-id="5b7f5-110">Максимальное количество основывается на текущей единице измерения работы, которая обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-110">The maximum quantity is based on the current work unit that is being processed.</span></span> <span data-ttu-id="5b7f5-111">Для работ типа "инвентаризация" ввод максимума не предусмотрен.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-111">The counting work type does not allow a maximum.</span></span>

<span data-ttu-id="5b7f5-112">Можно также использовать количество и единицу измерения, связанные со сканируемым штрих-кодом.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-112">You can also use the quantity and unit of measure (UOM) that is associated with a scanned bar code.</span></span> <span data-ttu-id="5b7f5-113">Это будет работать для оформления прихода входящих потоков, включая получение грузомест со смешанными номенклатурами, номенклатуры заказа на покупку, номенклатуры заказа на перемещение и номенклатуры загрузки.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-113">This will work for receiving on inbound flows including mixed license plate receiving, purchase order item, transfer order item, and load item.</span></span> <span data-ttu-id="5b7f5-114">Это также работает для поштучной комплектации, где сканирование штрих-кода будет добавлять количество к общему количеству подтвержденных штук, с преобразованием между единицей измерения в штрих-коде и единицей измерения работы.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-114">It also works for piece picking where scanning the bar code will add the quantity to the total number of confirmed pieces converting between the UOM on the bar code and the work unit.</span></span> <span data-ttu-id="5b7f5-115">Если при подсчете единицы измерения в штрих-коде подтверждается, что количество разрешено для подсчета в группе упорядочения, количество будет добавлено к общему количеству.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-115">If, when counting the UOM on the bar code, it is confirmed that the quantity is allowed for counting on the sequence group, the quantity will be added to the total count.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="5b7f5-116">Где это применяется</span><span class="sxs-lookup"><span data-stu-id="5b7f5-116">Where it applies</span></span>

<span data-ttu-id="5b7f5-117">Поштучная комплектация подходит для всех работ по инвентаризации и для первоначальной комплектации для любого типа работы.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-117">Piece picking works for all counting work and for the initial pick for any type of work.</span></span> <span data-ttu-id="5b7f5-118">Поштучная комплектация не применяется, если номенклатура контролируется по серийным номерам или если это комплектация для производства или комплектация по канбану с грузоместа, и номенклатура перемещается в промежуточное местонахождение.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-118">Piece picking does not apply if the item is controlled by serial numbers or if it is a production or kanban pick from a license plate (LP) location and the item is set to staging.</span></span>

## <a name="set-up-piece-picking"></a><span data-ttu-id="5b7f5-119">Настройка поштучной комплектации</span><span class="sxs-lookup"><span data-stu-id="5b7f5-119">Set up piece picking</span></span>

1.  <span data-ttu-id="5b7f5-120">В меню мобильного устройства откройте форму настройки для подтверждения работы: Управление складом> **Управление складом** > **Настройка** > **Мобильное устройство** > **Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-120">On a mobile device menu item, open the setup form for work confirmation: Warehouse management > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span> 
2. <span data-ttu-id="5b7f5-121">В пунктах меню мобильного устройства откройте "Настройка подтверждения работы".</span><span class="sxs-lookup"><span data-stu-id="5b7f5-121">From the mobile device menu item, open Work confirmation setup.</span></span>

<span data-ttu-id="5b7f5-122">Следующие параметры становятся доступны для выбора, когда тип работы — "комплектация" или "инвентаризация".</span><span class="sxs-lookup"><span data-stu-id="5b7f5-122">The following options become available for selection when the work type is pick or counting.</span></span>

| <span data-ttu-id="5b7f5-123">Параметр</span><span class="sxs-lookup"><span data-stu-id="5b7f5-123">Option</span></span>        | <span data-ttu-id="5b7f5-124">описание</span><span class="sxs-lookup"><span data-stu-id="5b7f5-124">Description</span></span>   | 
| ------------- | ------------- |
| <span data-ttu-id="5b7f5-125">Поштучное подтверждение комплектации</span><span class="sxs-lookup"><span data-stu-id="5b7f5-125">Piece picking confirmation</span></span>   | <span data-ttu-id="5b7f5-126">Доступно для типов работы "комплектация" и "инвентаризация".</span><span class="sxs-lookup"><span data-stu-id="5b7f5-126">Available for pick and counting work types.</span></span> <span data-ttu-id="5b7f5-127">Подтверждение продукта устанавливается автоматически.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-127">Product confirmation is automatically selected.</span></span> <span data-ttu-id="5b7f5-128">Позволяет подтверждать каждую штуку запасов с мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-128">Allows you to confirm each piece of inventory from the mobile device.</span></span> | 
| <span data-ttu-id="5b7f5-129">Максимальное число штук</span><span class="sxs-lookup"><span data-stu-id="5b7f5-129">Maximum number of pieces</span></span>     | <span data-ttu-id="5b7f5-130">Доступно для типа работы "комплектация", если включено подтверждение комплектации.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-130">Available for pick work if piece picking confirmation is enabled.</span></span> <span data-ttu-id="5b7f5-131">Устанавливает ограничение на количество штук, которые необходимо подтвердить.</span><span class="sxs-lookup"><span data-stu-id="5b7f5-131">Sets a limit to the number of pieces that you must confirm.</span></span> |  

