---
title: Дополнительные зоны местонахождения
description: В этом разделе представлен обзор новых зон местонахождения, которые были добавлены в Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 32114db4cf202870bae5ce307517170d3e618762
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597150"
---
# <a name="additional-location-zones"></a><span data-ttu-id="5da7e-103">Дополнительные зоны местонахождения</span><span class="sxs-lookup"><span data-stu-id="5da7e-103">Additional location zones</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5da7e-104">В Microsoft Dynamics 365 Supply Chain Management имеются три новых поля зоны.</span><span class="sxs-lookup"><span data-stu-id="5da7e-104">Three new zone fields are available in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="5da7e-105">Менеджеры склада могут использовать их для определения дополнительных складских организаций или макетов.</span><span class="sxs-lookup"><span data-stu-id="5da7e-105">Warehouse managers can use them to define additional warehouse organizations or layouts.</span></span> <span data-ttu-id="5da7e-106">Новые поля зоны можно установить либо вручную, либо с помощью мастера **Настройка местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="5da7e-106">The new zone fields can be set either manually or by using the **Location setup** wizard.</span></span> <span data-ttu-id="5da7e-107">Они могут использоваться в любом запросе или в фильтрации, использующей таблицу "Местонахождения".</span><span class="sxs-lookup"><span data-stu-id="5da7e-107">They can be used in any query or filtering that uses the Locations table.</span></span>

<span data-ttu-id="5da7e-108">Для использования полей зон дополнительная настройка не требуется.</span><span class="sxs-lookup"><span data-stu-id="5da7e-108">No additional setup is required to use the zone fields.</span></span>

## <a name="turn-on-the-additional-location-zone-feature"></a><span data-ttu-id="5da7e-109">Включение функции дополнительных зон местоположения</span><span class="sxs-lookup"><span data-stu-id="5da7e-109">Turn on the Additional location zone feature</span></span>

<span data-ttu-id="5da7e-110">Прежде чем использовать функцию *Дополнительная зона местонахождения*, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="5da7e-110">Before you can use the *Additional location zone* feature, it must be turned on in your system.</span></span> <span data-ttu-id="5da7e-111">Администраторы могут использовать параметры [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="5da7e-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="5da7e-112">В рабочей области **Управление функциями** эта функция перечисляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="5da7e-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="5da7e-113">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="5da7e-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="5da7e-114">**Название функции:** *Дополнительная зона местонахождения*</span><span class="sxs-lookup"><span data-stu-id="5da7e-114">**Feature name:** *Additional location zone*</span></span>

## <a name="use-location-zones"></a><span data-ttu-id="5da7e-115">Использование зон местонахождения</span><span class="sxs-lookup"><span data-stu-id="5da7e-115">Use location zones</span></span>

1. <span data-ttu-id="5da7e-116">Перейдите в раздел **Управление складом \> Настройка \> Склад \> Мастер настройки местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="5da7e-116">Go to **Warehouse management \> Setup \> Warehouse \> Location setup wizard**.</span></span>
2. <span data-ttu-id="5da7e-117">Задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5da7e-117">Set the following values:</span></span>

    - <span data-ttu-id="5da7e-118">В поле **Склад** выберите _62_.</span><span class="sxs-lookup"><span data-stu-id="5da7e-118">In the **Warehouse** field, select _62_.</span></span>
    - <span data-ttu-id="5da7e-119">В поле **Код зоны** выберите _ЭТАЖ_.</span><span class="sxs-lookup"><span data-stu-id="5da7e-119">In the **Zone ID** field, select _FLOOR_.</span></span>
    - <span data-ttu-id="5da7e-120">В поле **Дополнительная зона 1** выберите _PICKZONE1_.</span><span class="sxs-lookup"><span data-stu-id="5da7e-120">In the **Additional Zone 1** field, select _PICKZONE1_.</span></span>
    - <span data-ttu-id="5da7e-121">В поле **Дополнительная зона 2** выберите _WEBSHOP1_.</span><span class="sxs-lookup"><span data-stu-id="5da7e-121">In the **Additional Zone 2** field, select _WEBSHOP1_.</span></span>
    - <span data-ttu-id="5da7e-122">В поле **Код профиля местонахождения** выберите _ЭТАЖ_.</span><span class="sxs-lookup"><span data-stu-id="5da7e-122">In the **Location profile ID** field, select _FLOOR_.</span></span>

3. <span data-ttu-id="5da7e-123">Выберите строку **Этаж**.</span><span class="sxs-lookup"><span data-stu-id="5da7e-123">Select the **Floor** line.</span></span>
4. <span data-ttu-id="5da7e-124">В поле **С номера** введите значение _1_.</span><span class="sxs-lookup"><span data-stu-id="5da7e-124">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="5da7e-125">В поле **До номера** введите значение _3_.</span><span class="sxs-lookup"><span data-stu-id="5da7e-125">In the **To number** field, enter _3_.</span></span>
5. <span data-ttu-id="5da7e-126">Выберите строку **Проход**.</span><span class="sxs-lookup"><span data-stu-id="5da7e-126">Select the **Aisle** line.</span></span>
6. <span data-ttu-id="5da7e-127">В поле **С номера** введите значение _1_.</span><span class="sxs-lookup"><span data-stu-id="5da7e-127">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="5da7e-128">В поле **До номера** введите значение _5_.</span><span class="sxs-lookup"><span data-stu-id="5da7e-128">In the **To number** field, enter _5_.</span></span>
7. <span data-ttu-id="5da7e-129">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="5da7e-129">Select **Create**.</span></span>
8. <span data-ttu-id="5da7e-130">Вы получите сообщения о том, что были добавлены новые местоположения.</span><span class="sxs-lookup"><span data-stu-id="5da7e-130">You receive messages that state that new locations have been added.</span></span> <span data-ttu-id="5da7e-131">Чтобы просмотреть сообщения, выберите кнопку **Показать сообщения**.</span><span class="sxs-lookup"><span data-stu-id="5da7e-131">Select the **Show messages** button to view the messages.</span></span>
9. <span data-ttu-id="5da7e-132">Перейдите в раздел **Управление складом \> Настройка \> Склад \> Местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="5da7e-132">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span> <span data-ttu-id="5da7e-133">В списке отобразятся новые местоположения, а все поля зон будут доступны (то есть, поле существующей зоны и новые поля дополнительных зон).</span><span class="sxs-lookup"><span data-stu-id="5da7e-133">The new locations appear in the list, and all zone fields are available (that is, the existing zone field and the new additional zone fields).</span></span>
