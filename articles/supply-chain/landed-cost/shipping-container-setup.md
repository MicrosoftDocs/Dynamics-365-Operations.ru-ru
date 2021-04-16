---
title: Грузовые контейнеры
description: В этой теме описывается, как настроить контейнеры отгрузки для модуля "Стоимость на складе".
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 2f7e9435aa3d0d06e1cc51457a6343b807d76dc7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833721"
---
# <a name="shipping-container-setup"></a><span data-ttu-id="998b7-103">Настройка контейнера отгрузки</span><span class="sxs-lookup"><span data-stu-id="998b7-103">Shipping container setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="998b7-104">В этой теме описывается, как настроить контейнеры отгрузки для модуля **Стоимость на складе**.</span><span class="sxs-lookup"><span data-stu-id="998b7-104">This topic describes how to set up shipping containers for the **Landed cost** module.</span></span>

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a><span data-ttu-id="998b7-105">Настройка типов контейнеров отгрузки</span><span class="sxs-lookup"><span data-stu-id="998b7-105">Set up shipping container types</span></span>

<span data-ttu-id="998b7-106">Типы контейнеров отгрузки определяют типы контейнеров отгрузки, которые доступны для использования во время отгрузки и рейсов.</span><span class="sxs-lookup"><span data-stu-id="998b7-106">Shipping container types define the types of shipping containers that are available for use during shipping and voyages.</span></span>

<span data-ttu-id="998b7-107">Для работы с типами контейнеров отгрузки перейдите **Стоимость на складе \> Настройка контейнеров \> Типы контейнеров отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="998b7-107">To work with the shipping container types, go to **Landed cost \> Containers setup \> Shipping container types**.</span></span> <span data-ttu-id="998b7-108">Там можно просматривать, добавлять и удалять записи для типов контейнеров.</span><span class="sxs-lookup"><span data-stu-id="998b7-108">There, you can view, add, and remove records for your container types.</span></span> <span data-ttu-id="998b7-109">В следующей таблице описываются поля, которые доступны для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="998b7-109">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="998b7-110">Поле</span><span class="sxs-lookup"><span data-stu-id="998b7-110">Field</span></span> | <span data-ttu-id="998b7-111">описание</span><span class="sxs-lookup"><span data-stu-id="998b7-111">Description</span></span> |
|---|---|
| <span data-ttu-id="998b7-112">Тип грузового контейнера</span><span class="sxs-lookup"><span data-stu-id="998b7-112">Shipping container type</span></span> | <span data-ttu-id="998b7-113">Введите уникальное идентификационное имя/номер для типа контейнера отгрузки.</span><span class="sxs-lookup"><span data-stu-id="998b7-113">Enter a unique identification name/number for the shipping container type.</span></span> |
| <span data-ttu-id="998b7-114">описание</span><span class="sxs-lookup"><span data-stu-id="998b7-114">Description</span></span> | <span data-ttu-id="998b7-115">Введите описание типа контейнера отгрузки.</span><span class="sxs-lookup"><span data-stu-id="998b7-115">Enter a description of the shipping container type.</span></span> |
| <span data-ttu-id="998b7-116">Объем</span><span class="sxs-lookup"><span data-stu-id="998b7-116">Volume</span></span> | <span data-ttu-id="998b7-117">Введите максимальный объем, разрешенный в контейнерах отгрузки этого типа.</span><span class="sxs-lookup"><span data-stu-id="998b7-117">Enter the maximum volume that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="998b7-118">Вес</span><span class="sxs-lookup"><span data-stu-id="998b7-118">Weight</span></span> | <span data-ttu-id="998b7-119">Введите максимальный вес, разрешенный в контейнерах отгрузки этого типа.</span><span class="sxs-lookup"><span data-stu-id="998b7-119">Enter the maximum weight that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="998b7-120">Возвращаемые</span><span class="sxs-lookup"><span data-stu-id="998b7-120">Returnable</span></span> | <span data-ttu-id="998b7-121">Укажите, могут ли контейнеры отгрузки этого типа возвращаться поставщику после их использования во время рейса.</span><span class="sxs-lookup"><span data-stu-id="998b7-121">Specify whether shipping containers of this type can be returned to the vendor after they are used during a voyage.</span></span> <span data-ttu-id="998b7-122">Если этот параметр задан как *Да*, то для возврата контейнеров отгрузки этого типа в порт происхождения могут применяться дополнительные затраты.</span><span class="sxs-lookup"><span data-stu-id="998b7-122">If this option is set to *Yes*, additional costs might apply for the return of shipping containers of this type to the port of origin.</span></span> |

## <a name="set-up-shipping-containers"></a><span data-ttu-id="998b7-123">Настройка контейнеров отгрузки</span><span class="sxs-lookup"><span data-stu-id="998b7-123">Set up shipping containers</span></span>

<span data-ttu-id="998b7-124">Записи контейнеров отгрузки используются для определения всех контейнеров, используемых во время рейса.</span><span class="sxs-lookup"><span data-stu-id="998b7-124">You use shipping container records to identify each container that you use during voyages.</span></span> <span data-ttu-id="998b7-125">При создании рейса можно выбрать конкретный контейнер для него в списке всех записей контейнера отгрузки, которые были определены здесь.</span><span class="sxs-lookup"><span data-stu-id="998b7-125">When you create a voyage, you can select a specific container for it in the list of all the shipping container records that you've defined here.</span></span> <span data-ttu-id="998b7-126">Эта функция особенно полезна, если ваша компания владеет собственными контейнерами отгрузки.</span><span class="sxs-lookup"><span data-stu-id="998b7-126">This feature is especially useful if your company owns its own shipping containers.</span></span>

<span data-ttu-id="998b7-127">Нет необходимости вводить номера контейнеров отгрузки для контейнеров отгрузки, которые будут использоваться только один раз.</span><span class="sxs-lookup"><span data-stu-id="998b7-127">You don't have to enter shipping container numbers for shipping containers that will be used only one time.</span></span> <span data-ttu-id="998b7-128">Вместо этого можно добавить номер контейнера отгрузки при создании рейса.</span><span class="sxs-lookup"><span data-stu-id="998b7-128">Instead, you can add the shipping container number when you create a voyage.</span></span>

<span data-ttu-id="998b7-129">Записи контейнеров отгрузки используются только в стоимости на складе.</span><span class="sxs-lookup"><span data-stu-id="998b7-129">Shipping container records are used only in Landed cost.</span></span> <span data-ttu-id="998b7-130">Они недоступны в стандартном модуле **Управление транспортировкой** (TMS).</span><span class="sxs-lookup"><span data-stu-id="998b7-130">They aren't available in the standard **Transportation management** module (TMS).</span></span>

<span data-ttu-id="998b7-131">Для работы с контейнерами отгрузки перейдите **Стоимость на складе \> Настройка контейнеров \> Контейнеры отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="998b7-131">To work with shipping containers, go to **Landed cost \> Containers setup \> Shipping containers**.</span></span> <span data-ttu-id="998b7-132">Там можно просматривать, добавлять и удалять записи для контейнеров отгрузки.</span><span class="sxs-lookup"><span data-stu-id="998b7-132">There, you can view, add, and remove records your shipping containers.</span></span> <span data-ttu-id="998b7-133">В следующей таблице описываются поля, которые доступны для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="998b7-133">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="998b7-134">Поле</span><span class="sxs-lookup"><span data-stu-id="998b7-134">Field</span></span> | <span data-ttu-id="998b7-135">описание</span><span class="sxs-lookup"><span data-stu-id="998b7-135">Description</span></span> |
|---|---|
| <span data-ttu-id="998b7-136">Грузовой контейнер</span><span class="sxs-lookup"><span data-stu-id="998b7-136">Shipping container</span></span> | <span data-ttu-id="998b7-137">Введите уникальное идентификационное имя/номер для контейнера отгрузки.</span><span class="sxs-lookup"><span data-stu-id="998b7-137">Enter a unique identification name/number for the shipping container.</span></span> |
| <span data-ttu-id="998b7-138">Тип грузового контейнера</span><span class="sxs-lookup"><span data-stu-id="998b7-138">Shipping container type</span></span> | <span data-ttu-id="998b7-139">Выберите тип контейнера отгрузки.</span><span class="sxs-lookup"><span data-stu-id="998b7-139">Select the type of shipping container.</span></span> <span data-ttu-id="998b7-140">Дополнительные сведения см. в разделе [Настройка типов контейнеров отгрузки](#shipping-container-types) ранее в данной теме.</span><span class="sxs-lookup"><span data-stu-id="998b7-140">For more information, see the [Set up shipping container types](#shipping-container-types) section earlier in this topic.</span></span> |

> [!NOTE]
> - <span data-ttu-id="998b7-141">Настройка контейнера отгрузки необязательная.</span><span class="sxs-lookup"><span data-stu-id="998b7-141">The shipping container setup is optional.</span></span> <span data-ttu-id="998b7-142">Обычно она используется только в том случае, если компания владеет собственными контейнерами отгрузки или часто использует одни и те же контейнеры отгрузки.</span><span class="sxs-lookup"><span data-stu-id="998b7-142">Typically, you will use it only if your company owns its own shipping containers or often reuses the same shipping containers.</span></span>
> - <span data-ttu-id="998b7-143">Для номеров контейнеров отгрузки не вычисляются контрольные разряды.</span><span class="sxs-lookup"><span data-stu-id="998b7-143">No check digits are calculated for shipping container numbers.</span></span>

## <a name="set-up-unit-types"></a><a name="unit-types"></a><span data-ttu-id="998b7-144">Настройка типов единиц</span><span class="sxs-lookup"><span data-stu-id="998b7-144">Set up unit types</span></span>

<span data-ttu-id="998b7-145">Типы единиц измерения определяют дополнительные методы группирования и идентификации для контейнеров отгрузки.</span><span class="sxs-lookup"><span data-stu-id="998b7-145">Unit types establish additional groupings and identification methods for shipping containers.</span></span> <span data-ttu-id="998b7-146">Тип единицы измерения обычно используется для определения типа контейнера, в котором упакованы товары, например, палеты или барабаны.</span><span class="sxs-lookup"><span data-stu-id="998b7-146">The unit type is typically used to identify the type of container that goods are packaged in, such as pallets or drums.</span></span> <span data-ttu-id="998b7-147">Тип единицы можно выбрать при настройке контейнера на странице **Все контейнеры отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="998b7-147">You can select a unit type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="998b7-148">Типы единиц используются только в стоимости на складе.</span><span class="sxs-lookup"><span data-stu-id="998b7-148">Unit types are used only in Landed cost.</span></span> <span data-ttu-id="998b7-149">Они недоступны в TMS.</span><span class="sxs-lookup"><span data-stu-id="998b7-149">They aren't available in TMS.</span></span>

<span data-ttu-id="998b7-150">Для работы с типами единиц перейдите **Стоимость на складе \> Настройка контейнеров \> Типы единиц**.</span><span class="sxs-lookup"><span data-stu-id="998b7-150">To work with unit types, go to **Landed cost \> Containers setup \> Unit types**.</span></span> <span data-ttu-id="998b7-151">Там можно просматривать, добавлять и удалять записи для типов единиц.</span><span class="sxs-lookup"><span data-stu-id="998b7-151">There, you can view, add, and remove records for your unit types.</span></span> <span data-ttu-id="998b7-152">В следующей таблице описываются поля, которые доступны для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="998b7-152">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="998b7-153">Поле</span><span class="sxs-lookup"><span data-stu-id="998b7-153">Field</span></span> | <span data-ttu-id="998b7-154">описание</span><span class="sxs-lookup"><span data-stu-id="998b7-154">Description</span></span> |
|---|---|
| <span data-ttu-id="998b7-155">Тип подразделения</span><span class="sxs-lookup"><span data-stu-id="998b7-155">Unit type</span></span> | <span data-ttu-id="998b7-156">Введите уникальное идентификационное имя/номер для типа единиц.</span><span class="sxs-lookup"><span data-stu-id="998b7-156">Enter a unique identification name/number for the unit type.</span></span> |
| <span data-ttu-id="998b7-157">описание</span><span class="sxs-lookup"><span data-stu-id="998b7-157">Description</span></span> | <span data-ttu-id="998b7-158">Введите описание типа единиц.</span><span class="sxs-lookup"><span data-stu-id="998b7-158">Enter a description of the unit type.</span></span> |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a><span data-ttu-id="998b7-159">Настройка типов холодильников</span><span class="sxs-lookup"><span data-stu-id="998b7-159">Set up refrigeration types</span></span>

<span data-ttu-id="998b7-160">Типы холодильников задают методы группирования и определения контейнеров отгрузки (обычно это контейнеры-рефрижераторы).</span><span class="sxs-lookup"><span data-stu-id="998b7-160">Refrigeration types establish additional groupings and identification methods for shipping containers (usually refrigerated containers).</span></span> <span data-ttu-id="998b7-161">Тип холодильников можно выбрать при настройке контейнера на странице **Все контейнеры отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="998b7-161">You can select a refrigeration type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="998b7-162">Для работы с типами холодильников перейдите **Стоимость на складе \> Настройка контейнеров \> Типы холодильников**.</span><span class="sxs-lookup"><span data-stu-id="998b7-162">To work with refrigeration types, go to **Landed cost \> Containers setup \> Refrigeration types**.</span></span> <span data-ttu-id="998b7-163">Там можно просматривать, добавлять и удалять записи для типов холодильников.</span><span class="sxs-lookup"><span data-stu-id="998b7-163">There, you can view, add, and remove records for your refrigeration types.</span></span> <span data-ttu-id="998b7-164">В следующей таблице описываются поля, которые доступны для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="998b7-164">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="998b7-165">Поле</span><span class="sxs-lookup"><span data-stu-id="998b7-165">Field</span></span> | <span data-ttu-id="998b7-166">описание</span><span class="sxs-lookup"><span data-stu-id="998b7-166">Description</span></span> |
|---|---|
| <span data-ttu-id="998b7-167">Тип охлаждения</span><span class="sxs-lookup"><span data-stu-id="998b7-167">Refrigeration type</span></span> | <span data-ttu-id="998b7-168">Введите уникальное идентификационное имя/номер для типа холодильников.</span><span class="sxs-lookup"><span data-stu-id="998b7-168">Enter a unique identification name/number for the refrigeration type.</span></span> |
| <span data-ttu-id="998b7-169">описание</span><span class="sxs-lookup"><span data-stu-id="998b7-169">Description</span></span> | <span data-ttu-id="998b7-170">Введите описание типа холодильников.</span><span class="sxs-lookup"><span data-stu-id="998b7-170">Enter a description of the refrigeration type.</span></span> |
