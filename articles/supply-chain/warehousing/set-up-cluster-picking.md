---
title: Настройка комплектации кластера
description: В этом разделе описывается порядок настройки комплектации кластера и способ применения подтверждения номенклатуры с комплектацией кластера.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86aed1b2071875117b74309030ac5e9008babdaf
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2020
ms.locfileid: "3367415"
---
# <a name="set-up-cluster-picking"></a><span data-ttu-id="71153-103">Настройка комплектации кластера</span><span class="sxs-lookup"><span data-stu-id="71153-103">Set up cluster picking</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="71153-104">В этом разделе описывается, как разрешить работникам использовать мобильные устройства для группировки работ комплектации в кластеры, чтобы они могли скомплектовать номенклатуры из одного местонахождения для нескольких заказов на выполнение работ одновременно.</span><span class="sxs-lookup"><span data-stu-id="71153-104">This topic describes how to enable workers to use their mobile devices to group picking work into clusters, so that they can pick items from a single location for multiple work orders at the same time.</span></span> <span data-ttu-id="71153-105">Это называется *комплектацией кластера*.</span><span class="sxs-lookup"><span data-stu-id="71153-105">This is called *cluster picking*.</span></span>

## <a name="about-cluster-picking"></a><span data-ttu-id="71153-106">О комплектации кластера</span><span class="sxs-lookup"><span data-stu-id="71153-106">About cluster picking</span></span>

<span data-ttu-id="71153-107">После того как заказы на выполнение работ выпускаются на склад, работник может использовать мобильное устройство, чтобы назначить заказы кластеру.</span><span class="sxs-lookup"><span data-stu-id="71153-107">After work orders are released to the warehouse, the worker can use a mobile device to assign the orders to a cluster.</span></span> <span data-ttu-id="71153-108">Кластер организует работу комплектации для работника.</span><span class="sxs-lookup"><span data-stu-id="71153-108">The cluster will organize the picking work for the worker.</span></span> <span data-ttu-id="71153-109">При назначении заказа на выполнение работ кластеру работник должен использовать комплектацию кластера для выполнения работы комплектации по заказу.</span><span class="sxs-lookup"><span data-stu-id="71153-109">When a work order is assigned to a cluster, the worker must use cluster picking to perform the picking work for the order.</span></span> <span data-ttu-id="71153-110">Работник не сможет использовать другие методы комплектации.</span><span class="sxs-lookup"><span data-stu-id="71153-110">The worker cannot use other picking methods.</span></span> <span data-ttu-id="71153-111">Если заказ на выполнение работ назначен кластеру по ошибке, то работнику необходимо удалить кластер, а затем повторно создать его.</span><span class="sxs-lookup"><span data-stu-id="71153-111">If a work order is assigned to a cluster by mistake, the worker must break the cluster and then re-create it.</span></span>

<span data-ttu-id="71153-112">При необходимости работник может передавать кластер другому работнику.</span><span class="sxs-lookup"><span data-stu-id="71153-112">If needed, a worker can pass a cluster to another worker.</span></span> <span data-ttu-id="71153-113">В результате статус кластера изменится на Передано.</span><span class="sxs-lookup"><span data-stu-id="71153-113">This changes the cluster status to Passed.</span></span> <span data-ttu-id="71153-114">Если работник использует мобильное устройство, чтобы указать, что работа комплектации и размещения завершена, отгрузку или загрузку необходимо подтвердить в клиенте.</span><span class="sxs-lookup"><span data-stu-id="71153-114">When the worker uses a mobile device to indicate that the picking and put away work is completed, the shipment or load must be confirmed in the client.</span></span>

## <a name="enable-cluster-picking"></a><span data-ttu-id="71153-115">Включение комплектации кластера</span><span class="sxs-lookup"><span data-stu-id="71153-115">Enable cluster picking</span></span>

<span data-ttu-id="71153-116">Чтобы включить комплектацию кластера, необходимо настроить следующие значения.</span><span class="sxs-lookup"><span data-stu-id="71153-116">To enable cluster picking, you must set up the following:</span></span>

- <span data-ttu-id="71153-117">**Профили кластера** — укажите, следует ли автоматически создавать коды кластеров, число позиций для использования, время удаления кластеров, а также как устанавливать последовательность и выполнять проверку работы комплектации.</span><span class="sxs-lookup"><span data-stu-id="71153-117">**Cluster profiles** – Specify whether to automatically generate cluster   IDs, the number of positions to use, when to break clusters, and how to   sequence and verify the picking work.</span></span>

- <span data-ttu-id="71153-118">**Шаблоны работ** — укажите, как создать работу комплектации для комплектации кластера.</span><span class="sxs-lookup"><span data-stu-id="71153-118">**Work templates** – Define how to create the picking work for cluster   picking.</span></span>

- <span data-ttu-id="71153-119">**Директивы для мест хранения** — укажите местонахождение для комплектации и размещения номенклатур.</span><span class="sxs-lookup"><span data-stu-id="71153-119">**Location directives** – Specify where to pick items from, and where to put   them.</span></span>

- <span data-ttu-id="71153-120">**Пункты меню мобильного устройства** — настройте пункт меню мобильного устройства для использования существующей работы по управлением комплектации кластера.</span><span class="sxs-lookup"><span data-stu-id="71153-120">**Mobile device menu items** – Configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="71153-121">Затем необходимо добавить пункт меню в меню мобильного устройства, чтобы он отображался на мобильных устройствах.</span><span class="sxs-lookup"><span data-stu-id="71153-121">You must then add the menu item to a mobile device menu so that it is displayed on mobile devices.</span></span>

- <span data-ttu-id="71153-122">**Параметры управления складом** — укажите номерную серию, которая будет использоваться, если необходимо создать коды для кластеров.</span><span class="sxs-lookup"><span data-stu-id="71153-122">**Warehouse management parameters** – Specify the number sequence to use if   you want to generate identifiers for clusters.</span></span>

## <a name="set-up-a-cluster-profile"></a><span data-ttu-id="71153-123">Настройка профиля кластера</span><span class="sxs-lookup"><span data-stu-id="71153-123">Set up a cluster profile</span></span>

<span data-ttu-id="71153-124">Чтобы настроить профиль кластера, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="71153-124">To set up a cluster profile, follow these steps:</span></span>

1. <span data-ttu-id="71153-125">Щелкните **Управление складом** \> **Настройка** \> **Мобильное устройство** \> **Профили кластера**.</span><span class="sxs-lookup"><span data-stu-id="71153-125">Click **Warehouse management** \> **Setup** \> **Mobile device** \>  **Cluster profiles**.</span></span>

1. <span data-ttu-id="71153-126">Щелкните **Создать**, чтобы создать новый профиль.</span><span class="sxs-lookup"><span data-stu-id="71153-126">Click **New** to create a new profile.</span></span>

1. <span data-ttu-id="71153-127">Щелкните **Создать кластер** и в разделе **Сортировка кластера**, щелкните **Создать** для настройки критериев сортировки для кластера.</span><span class="sxs-lookup"><span data-stu-id="71153-127">Click **Create cluster** and, under **Cluster sorting**, click **New** to set up the sorting criteria for the cluster.</span></span> <span data-ttu-id="71153-128">Критерии сортировки определяют порядок, в котором работник выполняет работу комплектации.</span><span class="sxs-lookup"><span data-stu-id="71153-128">The sorting criteria control the order in which the worker will perform the picking work.</span></span> <span data-ttu-id="71153-129">Можно добавить любое количество критериев.</span><span class="sxs-lookup"><span data-stu-id="71153-129">You can add as many criteria as needed.</span></span>

1. <span data-ttu-id="71153-130">В поле **Порядковый номер** введите номер для определения порядка, в котором будут обрабатываться критерии сортировки.</span><span class="sxs-lookup"><span data-stu-id="71153-130">In the **Sequence number** field, enter a number to define the order in  which the sorting criteria are processed.</span></span>

1. <span data-ttu-id="71153-131">В поле **Имя поля** выберите поле, определяющее сортировку.</span><span class="sxs-lookup"><span data-stu-id="71153-131">In the **Field name** field, select the field that will determine the sorting.</span></span> <span data-ttu-id="71153-132">Например, если выбрать поле **WMSLocationId**, работа будет отсортирована по местонахождению.</span><span class="sxs-lookup"><span data-stu-id="71153-132">For example, if you select the **WMSLocationId** field, the work will be sorted by location.</span></span>

1. <span data-ttu-id="71153-133">В поле **Сортировка** выберите один из следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="71153-133">In the **Sorting** field, select one of the following options.</span></span>

| <span data-ttu-id="71153-134">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="71153-134">**Option**</span></span>     | <span data-ttu-id="71153-135">**Описание**</span><span class="sxs-lookup"><span data-stu-id="71153-135">**Description**</span></span>                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71153-136">**В возрастающем порядке**</span><span class="sxs-lookup"><span data-stu-id="71153-136">**Ascending**</span></span>  | <span data-ttu-id="71153-137">Работы комплектации упорядочены в порядке возрастания на основе критериев сортировки.</span><span class="sxs-lookup"><span data-stu-id="71153-137">Picking work is sequenced in ascending order based on the sorting criteria.</span></span> <span data-ttu-id="71153-138">Например, если в качестве критериев сортировки используется поле **WMSLocationId** и в качестве кодов местонахождений используются числа 1, 2, 3 и 4, сначала для комплектации будет использоваться местонахождение 4.</span><span class="sxs-lookup"><span data-stu-id="71153-138">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 4 first.</span></span> |
| <span data-ttu-id="71153-139">**Убывание**</span><span class="sxs-lookup"><span data-stu-id="71153-139">**Descending**</span></span> | <span data-ttu-id="71153-140">Работы комплектации упорядочены в порядке убывания на основе критериев сортировки.</span><span class="sxs-lookup"><span data-stu-id="71153-140">Picking work is sequenced in descending order based on the sorting criteria.</span></span> <span data-ttu-id="71153-141">Например, если в качестве критериев сортировки используется поле **WMSLocationId** и в качестве кодов местонахождений используются числа 1, 2, 3 и 4, сначала для комплектации будет использоваться местонахождение 1.</span><span class="sxs-lookup"><span data-stu-id="71153-141">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 1 first.</span></span> |

## <a name="item-confirmation"></a><span data-ttu-id="71153-142">Подтверждение номенклатуры</span><span class="sxs-lookup"><span data-stu-id="71153-142">Item confirmation</span></span>

<span data-ttu-id="71153-143">При применении комплектации кластера критически важно подтверждение номенклатуры для проверки номенклатур, которые добавляются в кластеры.</span><span class="sxs-lookup"><span data-stu-id="71153-143">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="71153-144">Вы можете проверить номенклатуры в комплектации кластера во время процесса комплектации кластера.</span><span class="sxs-lookup"><span data-stu-id="71153-144">You can verify items in cluster picking during the cluster picking process.</span></span> <span data-ttu-id="71153-145">Настройка основана на настройке штрих-кода продукта.</span><span class="sxs-lookup"><span data-stu-id="71153-145">The setup is based on the product bar code setup.</span></span>

### <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="71153-146">Настройка проверки номенклатуры с комплектацией кластера</span><span class="sxs-lookup"><span data-stu-id="71153-146">Set up item verification with cluster picking</span></span>

1. <span data-ttu-id="71153-147">В меню мобильного устройства откройте форму настройки для подтверждения работы: **Управление складом** \> **Управление складом** \> **Настройка** \> **Мобильное устройство** \> **Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="71153-147">On a mobile device menu item, open the setup form for work confirmation:  **Warehouse management** \> **Warehouse management** \> **Setup** \>  **Mobile device** \> **Mobile device menu items**.</span></span>

1. <span data-ttu-id="71153-148">В пунктах меню мобильного устройства откройте **Настройка подтверждения работы**.</span><span class="sxs-lookup"><span data-stu-id="71153-148">From the mobile device menu item, open **Work confirmation setup**.</span></span> <span data-ttu-id="71153-149">Параметр **Подтверждение продукта** позволяет подтвердить каждую позицию запасов с мобильного устройства при сканировании.</span><span class="sxs-lookup"><span data-stu-id="71153-149">The **Product confirmation** option allows you to verify each piece of inventory from the mobile device when scanned.</span></span>
