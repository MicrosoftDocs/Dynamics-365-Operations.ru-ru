---
title: "Частичная отгрузка загрузки транспорта"
description: "В этом разделе объясняется, как можно частично отгрузить груз и отложить планирование вместимости для груза."
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 8c172f1b66e56f60e89f56ea98910f8d0e4f3e36
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---

# <a name="partial-shipment-of-a-transport-load"></a><span data-ttu-id="f6392-103">Частичная отгрузка загрузки транспорта</span><span class="sxs-lookup"><span data-stu-id="f6392-103">Partial shipment of a transport load</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f6392-104">Настраивая частичную отгрузку грузов, можно обработать грузы, в которых вместимость не может быть определена, пока в груз не будут добавлены все строки продаж.</span><span class="sxs-lookup"><span data-stu-id="f6392-104">By setting up partial shipment of loads, you can handle loads where the capacity can't be determined until all the sales lines have been added to a load.</span></span> <span data-ttu-id="f6392-105">Процесс затем может быть завершен, когда станет известно точное число палет.</span><span class="sxs-lookup"><span data-stu-id="f6392-105">The process can then be finalized when the exact pallet count is known.</span></span> <span data-ttu-id="f6392-106">Таким образом, не нужно решать, какие палеты будут назначены какому транспорту, до момента, когда транспорт физически загружается с промежуточного склада.</span><span class="sxs-lookup"><span data-stu-id="f6392-106">Therefore, you don't have to decide which pallets will be assigned to which transport until the moment when a transport is being physically loaded out of the staged inventory.</span></span>

<span data-ttu-id="f6392-107">Эта функция является альтернативой принудительного применения более жесткой структуры, в которой необходимо определить, какие палеты будут назначены какому транспорту, прежде чем можно будет создать работу комплектации или работу загрузки.</span><span class="sxs-lookup"><span data-stu-id="f6392-107">This feature offers an alternative to the enforcement of a more rigid structure, where you must determine which pallets will be assigned to which transport before picking work or loading work can be created.</span></span> <span data-ttu-id="f6392-108">Вместо этого пользователи могут настраивать отдельные грузы для подтверждения частичной отгрузки.</span><span class="sxs-lookup"><span data-stu-id="f6392-108">Instead, users can configure individual loads for a partial shipment confirmation.</span></span> <span data-ttu-id="f6392-109">Затем могут выполняться процессы загрузки транспорта для этих грузов.</span><span class="sxs-lookup"><span data-stu-id="f6392-109">The transport loading processes for those loads can then occur.</span></span> <span data-ttu-id="f6392-110">Таким образом отдел планирования перевозок может планировать грузы без необходимости учитываться вместимость отдельных транспортных средств.</span><span class="sxs-lookup"><span data-stu-id="f6392-110">Therefore, the transportation planning department can plan loads without having to consider the capacity of individual transports.</span></span>

<span data-ttu-id="f6392-111">Во время погрузки работники могут определить новую загрузку транспорта, в который может быть загружена палета.</span><span class="sxs-lookup"><span data-stu-id="f6392-111">At the time of loading, workers can define a new transport load that a pallet can be loaded to.</span></span> <span data-ttu-id="f6392-112">Кроме того, они могут определить существующую загрузку транспорта.</span><span class="sxs-lookup"><span data-stu-id="f6392-112">Alternatively, they can identify an existing transport load.</span></span> <span data-ttu-id="f6392-113">Эти данные могут быть записаны с помощью мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="f6392-113">This data can be recorded via a mobile device.</span></span> <span data-ttu-id="f6392-114">Таким образом, несколько сотрудников склада могут загрузить запасы из одних грузов или из различных грузов в одни грузовик.</span><span class="sxs-lookup"><span data-stu-id="f6392-114">Therefore, several warehouse workers can load inventory from the same loads or different loads onto the same truck.</span></span> <span data-ttu-id="f6392-115">Загрузки затем могут быть полностью или частично отгружены.</span><span class="sxs-lookup"><span data-stu-id="f6392-115">The loads can then be fully or partially shipped.</span></span>

> [!NOTE] 
> <span data-ttu-id="f6392-116">Чтобы загрузить запасы из загрузки в специальную транспортную загрузку и частично отгрузить груз, работа должна быть создана с помощью класса загрузки в шаблоне работы.</span><span class="sxs-lookup"><span data-stu-id="f6392-116">In order to load inventory from a load to a specific transport load and partially ship the load, work must be generated by using a loading class in a work template.</span></span> <span data-ttu-id="f6392-117">Обычная работа комплектации типа **Комплектация** не может быть загружена в транспортную загрузку, такую как грузовик.</span><span class="sxs-lookup"><span data-stu-id="f6392-117">Ordinary picking work of the **Picking** type can't be loaded to a transport load such as a truck.</span></span>

## <a name="set-up-transport-loads-for-partial-shipment"></a><span data-ttu-id="f6392-118">Настройка транспортных загрузок для частичной отгрузки</span><span class="sxs-lookup"><span data-stu-id="f6392-118">Set up transport loads for partial shipment</span></span>

<span data-ttu-id="f6392-119">Настройка для частичной отгрузки загрузок состоит из следующих двух процедур.</span><span class="sxs-lookup"><span data-stu-id="f6392-119">The setup for partial shipment of loads consists of the following two procedures.</span></span>

### <a name="set-the-loading-strategy"></a><span data-ttu-id="f6392-120">Задание стратегии загрузки</span><span class="sxs-lookup"><span data-stu-id="f6392-120">Set the loading strategy</span></span>

<span data-ttu-id="f6392-121">Необходимо включить частичную загрузку, задав стратегию загрузки.</span><span class="sxs-lookup"><span data-stu-id="f6392-121">You must enable partial loading by setting the loading strategy.</span></span> <span data-ttu-id="f6392-122">Стратегию загрузки можно задать после создания загрузки.</span><span class="sxs-lookup"><span data-stu-id="f6392-122">You can set the loading strategy after you've created a load.</span></span>

1. <span data-ttu-id="f6392-123">Выберите **Управление складом** \> **Загрузки** \> **Все загрузки**.</span><span class="sxs-lookup"><span data-stu-id="f6392-123">Select **Warehouse management** \> **Loads** \> **All loads**.</span></span>
2. <span data-ttu-id="f6392-124">Выберите загрузку и щелкните **Заголовок**.</span><span class="sxs-lookup"><span data-stu-id="f6392-124">Select a load, and then click **Header**.</span></span>
3. <span data-ttu-id="f6392-125">В поле **Стратегия загрузки** выберите **Допускается частичная отгрузка загрузки**.</span><span class="sxs-lookup"><span data-stu-id="f6392-125">In the **Loading strategy** field, select **Partial load shipping allowed**.</span></span>

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a><span data-ttu-id="f6392-126">Создание пункта меню для загрузки грузов транспорта</span><span class="sxs-lookup"><span data-stu-id="f6392-126">Create a menu item for loading of transport loads</span></span>

<span data-ttu-id="f6392-127">Необходимо создать новый пункт меню, который позволяет загружать транспортные загрузки.</span><span class="sxs-lookup"><span data-stu-id="f6392-127">You must create a new menu item that enables transport loads to be loaded.</span></span> <span data-ttu-id="f6392-128">Транспортная загрузка позволяет группировать строки работы из одной или нескольких загрузок.</span><span class="sxs-lookup"><span data-stu-id="f6392-128">A transport load lets you group work lines from one load or multiple loads.</span></span> <span data-ttu-id="f6392-129">Все, что добавлено в транспортную загрузку, может быть затем отгружено с помощью мобильного сканера.</span><span class="sxs-lookup"><span data-stu-id="f6392-129">Everything that is added to the transport load can then be shipped by using a mobile scanner.</span></span>

1. <span data-ttu-id="f6392-130">Выберите **Управление складом** \> **Настройка** \> **Мобильное устройство** \> **Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="f6392-130">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="f6392-131">Выберите **Создать**, а затем в поле **Режим** выберите **Работа**.</span><span class="sxs-lookup"><span data-stu-id="f6392-131">Select **New**, and then, in the **Mode** field, select **Work**.</span></span>
3. <span data-ttu-id="f6392-132">Укажите для **Использовать существующую работу** вариант **Да**.</span><span class="sxs-lookup"><span data-stu-id="f6392-132">Set the **Use existing work** option to **Yes**.</span></span>
4. <span data-ttu-id="f6392-133">На вкладке **Общие** в поле **Кем управляется** выберите значение **Загрузка транспорта**.</span><span class="sxs-lookup"><span data-stu-id="f6392-133">On the **General** tab, in the **Directed by** field, select **Transport loading**.</span></span>
5. <span data-ttu-id="f6392-134">Чтобы включить подтверждение отгрузки для мобильного сканера, в поле **Разрешенный тип подтверждения отгрузки** выберите **Загрузка транспорта**.</span><span class="sxs-lookup"><span data-stu-id="f6392-134">To enable shipment confirmation on a mobile scanner, in the **Allowed ship confirmation type** field, select **Transport load**.</span></span>

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a><span data-ttu-id="f6392-135">Подтверждение отгрузки загрузки транспорта из клиента</span><span class="sxs-lookup"><span data-stu-id="f6392-135">Confirm shipment of a transport load from the client</span></span>

<span data-ttu-id="f6392-136">Эта настройка позволяет подтвердить загрузку транспорта, которая включает полную или частичную загрузку для отгрузки.</span><span class="sxs-lookup"><span data-stu-id="f6392-136">This setup lets you confirm a transport load that includes a full load or a partially loaded load to be shipped.</span></span>

1. <span data-ttu-id="f6392-137">Выберите **Управление складом** \> **Загрузки** \> **Загрузки транспорта**.</span><span class="sxs-lookup"><span data-stu-id="f6392-137">Select **Warehouse management** \> **Loads** \> **Transport loads**.</span></span>
2. <span data-ttu-id="f6392-138">В области действий на вкладке **Отгрузка и получение** в группе **Подтверждение** выберите **Транспортировка**.</span><span class="sxs-lookup"><span data-stu-id="f6392-138">On the Action Pane, on the **Ship and receive** tab, in the **Confirm** group, select **Transport**.</span></span>

