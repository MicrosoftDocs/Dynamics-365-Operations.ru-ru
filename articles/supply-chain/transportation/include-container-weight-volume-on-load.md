---
title: "Включение веса и объема контейнера при загрузке"
description: "В этой теме описывается, как настроить и использовать функциональность для включения в загрузки веса и объема контейнера."
author: pjacobse
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
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b137db6f67da30d6ac3a973940c1df1fd7268a1a
ms.openlocfilehash: ac1df9b430feb025e4a544a7ecd7baa0c919cbe4
ms.contentlocale: ru-ru
ms.lasthandoff: 10/02/2017

---

# <a name="include-container-weight-and-volume-on-load"></a><span data-ttu-id="3b815-103">Включение веса и объема контейнера при загрузке</span><span class="sxs-lookup"><span data-stu-id="3b815-103">Include container weight and volume on load</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3b815-104">Функциональность для включения в загрузку веса и объема контейнера дает четкое представление об общем весе и объеме контейнеров и номенклатур, входящих в загрузку.</span><span class="sxs-lookup"><span data-stu-id="3b815-104">The functionality for including the container weight and volume on a load gives a clear representation of the total weight and volume of containers and items that are going on a load.</span></span>

<span data-ttu-id="3b815-105">Загрузка содержит одну отгрузку или несколько отгрузок, и эти отгрузки содержат различные номенклатуры, которые относятся к одному заказу на продажу или к нескольким заказам на продажу.</span><span class="sxs-lookup"><span data-stu-id="3b815-105">A load contains a single shipment or multiple shipments, and these shipments contain distinct items that belong to a single sales order or multiple sales orders.</span></span> <span data-ttu-id="3b815-106">Номенклатуры хранятся внутри контейнера, а контейнеры загружаются в загрузку.</span><span class="sxs-lookup"><span data-stu-id="3b815-106">The items are stored inside a container, and containers are loaded on a load.</span></span> <span data-ttu-id="3b815-107">Элементы, которые находятся за пределами контейнера, также могут входить в загрузку.</span><span class="sxs-lookup"><span data-stu-id="3b815-107">Items that are outside a container can also be part of a load.</span></span> <span data-ttu-id="3b815-108">На основании этих условий система вычисляет значения для веса и объема загрузки, учитывая вес и объем и контейнеров, и номенклатур.</span><span class="sxs-lookup"><span data-stu-id="3b815-108">Based on these conditions, the system calculates values for the weight and volume on the load by considering the weight and volume of both containers and items.</span></span>

<span data-ttu-id="3b815-109">Если вычисленные значения неточные, вы можете откорректировать их, введя фактические значения веса и объема в загрузке.</span><span class="sxs-lookup"><span data-stu-id="3b815-109">If the calculated values aren’t precise, you can adjust them by entering the actual values for the weight and volume on the load.</span></span> <span data-ttu-id="3b815-110">Значения веса и объема используются в процессах управления транспортировкой.</span><span class="sxs-lookup"><span data-stu-id="3b815-110">The values for the weight and volume are used in transportation management processes.</span></span> <span data-ttu-id="3b815-111">Например, эти значения используются на рабочем месте ставок и маршрутов, где они определяют ставку и маршрут для загрузок, а также используются для определения способов доставки и прибытия водителей.</span><span class="sxs-lookup"><span data-stu-id="3b815-111">For example, the values are used in the rate route workbench, where they help define the rate and route for loads, and they are also used for transportation tenders and driver check-in.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="3b815-112">Где это применяется</span><span class="sxs-lookup"><span data-stu-id="3b815-112">Where it applies</span></span>

<span data-ttu-id="3b815-113">Функциональность для включения в загрузку веса и объема контейнера применяется в процессах управления транспортировкой, таких как рабочее место ставок и маршрутов, способы доставки транспортировки и прибытие водителей.</span><span class="sxs-lookup"><span data-stu-id="3b815-113">The functionality for including the container weight and volume on a load applies in transportation management processes, such as the rate route workbench, transportation tenders, and driver check-in.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="3b815-114">Порядок настройки</span><span class="sxs-lookup"><span data-stu-id="3b815-114">How it is set up</span></span>

<span data-ttu-id="3b815-115">Количество контейнеров, которое должно учитываться для загрузки, вычисляется на основании веса и объема контейнера, а также процента использования контейнера.</span><span class="sxs-lookup"><span data-stu-id="3b815-115">The number of containers that should be considered for a load is calculated based on the weight and volume of the container, and on the percentage of the container is used.</span></span>

-   <span data-ttu-id="3b815-116">Чтобы задать вес и объем для контейнера, выберите **Управление складом** \> **Настройка** \> **Контейнеры** \> **Типы контейнеров**.</span><span class="sxs-lookup"><span data-stu-id="3b815-116">To set the weight and volume for a container, click **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>

-   <span data-ttu-id="3b815-117">Чтобы задать процент использования контейнера, выберите **Управление складом** \> **Настройка** \> **Контейнеры** \> **Группы контейнеров**, а затем введите значение в поле **Процент загрузки контейнера**.</span><span class="sxs-lookup"><span data-stu-id="3b815-117">To set the container utilization percentage, click **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**, and then enter a value in the **Container utilization percentage** field.</span></span>
