---
title: Получение грузоместа через складское мобильное приложение
description: В этой теме объясняется, как настроить складское мобильное приложение для поддержки использования процесса получения грузоместа для получения физических запасов.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 98cd608edea1d5365d0d3532244f1fcdb6293d3c
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261370"
---
# <a name="license-plate-receiving-via-the-warehousing-mobile-app"></a><span data-ttu-id="d7132-103">Получение грузоместа через складское мобильное приложение</span><span class="sxs-lookup"><span data-stu-id="d7132-103">License plate receiving via the Warehousing mobile app</span></span>

<span data-ttu-id="d7132-104">В этой теме объясняется, как настроить складское мобильное приложение, чтобы оно поддерживало использование процесса получения грузоместа для получения физических запасов.</span><span class="sxs-lookup"><span data-stu-id="d7132-104">This topic explains how to set up the Warehousing mobile app so that it supports using a license plate receiving process to receive physical inventory.</span></span>

<span data-ttu-id="d7132-105">Можно использовать эту функцию для быстрой регистрации прихода входящих запасов, которые относятся к предварительному уведомлению об отгрузке (ASN).</span><span class="sxs-lookup"><span data-stu-id="d7132-105">You can use this functionality to quickly record the receipt of inbound inventory that is related to an advance ship notice (ASN).</span></span> <span data-ttu-id="d7132-106">Система автоматически создает ASN, когда процессы управления складом используются для отгрузки заказа на перемещение.</span><span class="sxs-lookup"><span data-stu-id="d7132-106">The system automatically creates an ASN when warehouse management processes are used to ship a transfer order.</span></span> <span data-ttu-id="d7132-107">Для процесса заказа на покупку ASN может быть записано вручную, либо оно может быть автоматически импортировано с помощью входящего процесса информационного объекта ASN.</span><span class="sxs-lookup"><span data-stu-id="d7132-107">For the purchase order process, an ASN can be manually recorded, or it can be automatically imported by using an inbound ASN data entity process.</span></span>

<span data-ttu-id="d7132-108">Данные ASN связаны с загрузками и отгрузками через *упаковочные структуры*, где палеты (родительские грузоместа) могут содержать ящики (вложенные грузоместа).</span><span class="sxs-lookup"><span data-stu-id="d7132-108">The ASN data is linked to loads and shipments via the *packing structures*, where pallets (parent license plates) can contain cases (nested license plates).</span></span>

> [!NOTE]
> <span data-ttu-id="d7132-109">Для уменьшения количества складских проводок при использовании структур упаковки, для которых используются вложенные грузоместа, система записывает физические запасы в наличии на родительском грузоместе.</span><span class="sxs-lookup"><span data-stu-id="d7132-109">To reduce the number of inventory transactions when packing structures that have nested license plates are used, the system records the physical on-hand inventory on the parent license plate.</span></span> <span data-ttu-id="d7132-110">Для запуска перемещения физических запасов в наличии с родительского грузоместа во вложенные грузоместа, основанного на данных о структуре упаковки, на мобильном устройстве должен содержаться пункт меню, основанный на процесса создания работы *Упаковывать по вложенным грузоместам*.</span><span class="sxs-lookup"><span data-stu-id="d7132-110">To trigger the movement of the physical on-hand inventory from the parent license plate to the nested license plates, based on the packing structure data, the mobile device must provide a menu item that is based on the *Pack to nested license plates* work creation process.</span></span>

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a><span data-ttu-id="d7132-111">Отображение или пропуск страницы сводки получения</span><span class="sxs-lookup"><span data-stu-id="d7132-111">Show or skip the receiving summary page</span></span>

<span data-ttu-id="d7132-112">Можно использовать функцию *Управление отображением страницы сводки получения на мобильном устройстве*, чтобы воспользоваться преимуществом дополнительного подробного потока приложения склада в рамках процесса получения грузомест.</span><span class="sxs-lookup"><span data-stu-id="d7132-112">You can use the *Control whether to display a receiving summary page on mobile devices* feature to take advantage of an additional detailed Warehouse app flow as part of the license plate receiving process.</span></span>

<span data-ttu-id="d7132-113">Прежде чем использовать эту функцию, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="d7132-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="d7132-114">Администраторы могут использовать параметры [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения.</span><span class="sxs-lookup"><span data-stu-id="d7132-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="d7132-115">В рабочей области **Управление функциями** эта функция перечисляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="d7132-115">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="d7132-116">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="d7132-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d7132-117">**Имя функции:** *Управление отображением страницы сводки получения на мобильном устройстве*</span><span class="sxs-lookup"><span data-stu-id="d7132-117">**Feature name:** *Control whether to display a receiving summary page on mobile devices*</span></span>

<span data-ttu-id="d7132-118">Если эта функция включена, пункты меню мобильного устройства для получения грузомест или получения и размещения грузомест необходимо задать параметр **Отображать страницу сводки получения**.</span><span class="sxs-lookup"><span data-stu-id="d7132-118">When this feature is turned on, mobile device menu items for license plate receiving or license plate receiving and put-away will provide a **Display receiving summary page** setting.</span></span> <span data-ttu-id="d7132-119">Эта настройка имеет следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="d7132-119">This setting has the following options:</span></span>

- <span data-ttu-id="d7132-120">**Отображать подробную сводку** — во время получения грузоместа работники увидят дополнительную страницу, которая показывает полные сведения ASN.</span><span class="sxs-lookup"><span data-stu-id="d7132-120">**Display a detailed summary** – During license plate receiving, workers will see an extra page that shows the full ASN information.</span></span>
- <span data-ttu-id="d7132-121">**Пропустить сводку** — сотрудники не будут видеть полные сведения ASN.</span><span class="sxs-lookup"><span data-stu-id="d7132-121">**Skip the summary** – Workers won't see the full ASN information.</span></span> <span data-ttu-id="d7132-122">Работники склада не смогут задавать код метода обработки или добавлять исключения в ходе процесса приемки.</span><span class="sxs-lookup"><span data-stu-id="d7132-122">Warehouse workers also won't be able to set a disposition code or add exceptions during the receiving process.</span></span>

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a><span data-ttu-id="d7132-123">Блокировать использование грузомест, отправленных по заказам на перемещение, на складах, отличных от склада назначения.</span><span class="sxs-lookup"><span data-stu-id="d7132-123">Prevent transfer order–shipped license plates from being used at warehouses other than the destination warehouse</span></span>

<span data-ttu-id="d7132-124">Процесс получения грузомест не может использоваться, если ASN содержит идентификатор грузоместа, уже существующий и имеющий данные о физическом наличии в местоположении склада, отличном от местоположения склада, где выполняется регистрация этого грузоместа.</span><span class="sxs-lookup"><span data-stu-id="d7132-124">A license plate receiving process can't be used if an ASN contains a license plate ID that already exists and has physical on-hand data at a warehouse location other than the warehouse location where the license plate registration is occurring.</span></span>

<span data-ttu-id="d7132-125">Для сценариев заказов на перемещение, когда транзитный склад не отслеживает грузоместа (и, таким образом, также не отслеживает физические запасы в наличии для каждого грузоместа), можно использовать функцию *Блокировать использование грузомест, отправленных по заказам на перемещение, на складах, отличных от склада назначения*, чтобы предотвратить физические обновления запасов в наличии для грузомест в процессе транзита.</span><span class="sxs-lookup"><span data-stu-id="d7132-125">For transfer order scenarios where the transit warehouse doesn't track license plates (and therefore also doesn't track physical on-hand inventory per license plate), you can use the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature to prevent physical on-hand updates of license plates that are in transit.</span></span>

<span data-ttu-id="d7132-126">Прежде чем использовать эту функцию, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="d7132-126">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="d7132-127">Администраторы могут использовать параметры [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения.</span><span class="sxs-lookup"><span data-stu-id="d7132-127">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="d7132-128">В рабочей области **Управление функциями** эта функция перечисляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="d7132-128">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="d7132-129">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="d7132-129">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d7132-130">**Имя функции:** *Блокировать использование грузомест, отправленных по заказам на перемещение, на складах, отличных от склада назначения*</span><span class="sxs-lookup"><span data-stu-id="d7132-130">**Feature name:** *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse*</span></span>

<span data-ttu-id="d7132-131">Чтобы управлять функциональностью, когда эта функция доступна, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d7132-131">To manage the functionality when this feature is available, follow these steps.</span></span>

1. <span data-ttu-id="d7132-132">Перейдите в раздел **Управление складом \> Настройка \> Параметры управления складом**.</span><span class="sxs-lookup"><span data-stu-id="d7132-132">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="d7132-133">На вкладке **Общие** на экспресс-вкладке **Грузоместа** задайте в поле **Политика грузомест на транзитном складе** одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="d7132-133">On the **General** tab, on the **License plates** FastTab, set the **Transit warehouse license plate policy** field to one of the following values:</span></span>

    - <span data-ttu-id="d7132-134">**Разрешить повторное использование неотслеживаемых грузомест** — система работает так же, как и при недоступности функции *Блокировать использование грузомест, отправленных по заказам на перемещение, на складах, отличных от склада назначения*.</span><span class="sxs-lookup"><span data-stu-id="d7132-134">**Allow reuse of non-tracked license plate** – The system works the same way that it works when the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature isn't available.</span></span> <span data-ttu-id="d7132-135">Это значение является значением по умолчанию при первой активации функции.</span><span class="sxs-lookup"><span data-stu-id="d7132-135">This value is the default setting when you first activate the feature.</span></span>
    - <span data-ttu-id="d7132-136">**Запретить повторное использование неотслеживаемых грузомест** — только обновления запасов в наличии, которые относятся к отгруженному грузоместу, будут разрешены на складе назначения до тех пор, пока не будет получен заказ на перемещение.</span><span class="sxs-lookup"><span data-stu-id="d7132-136">**Prevent reuse of non-tracked license plate** – Only on-hand updates that are related to a shipped license plate will be allowed at the destination warehouse until the transfer order has been received.</span></span>

## <a name="more-information"></a><span data-ttu-id="d7132-137">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="d7132-137">More information</span></span>

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

<span data-ttu-id="d7132-138">Дополнительные сведения о элементах меню для мобильных устройств см. в разделе [Настройка мобильных устройств для работы склада](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="d7132-138">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>
