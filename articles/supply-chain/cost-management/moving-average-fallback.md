---
title: Резервная последовательность затрат для скользящего среднего
description: В этой теме представлены сведения о резервных последовательностях затрат для расчета скользящего среднего в Microsoft Dynamics 365 Supply Chain Management.
author: AndersGirke
manager: tfehr
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 541b7ecca5c1c36999f573d6d0f2dc0c9e901631
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967591"
---
# <a name="moving-average-fallback-cost-sequence"></a><span data-ttu-id="e84bb-103">Резервная последовательность затрат для скользящего среднего</span><span class="sxs-lookup"><span data-stu-id="e84bb-103">Moving average fallback cost sequence</span></span>

<span data-ttu-id="e84bb-104">Одним из способов расчета затрат для запасов может быть использование _скользящего среднего_.</span><span class="sxs-lookup"><span data-stu-id="e84bb-104">One way that you can calculate the cost of your inventory is by using a _moving average_.</span></span> <span data-ttu-id="e84bb-105">С каждой складской номенклатурой может быть связано до трех значений затрат:</span><span class="sxs-lookup"><span data-stu-id="e84bb-105">Up to three cost values can be associated with each inventory item:</span></span>

- <span data-ttu-id="e84bb-106">**Последний расход** — затраты на последний расход, которые были назначены до того, как запасы стали отрицательными</span><span class="sxs-lookup"><span data-stu-id="e84bb-106">**Last issue** – The last issue cost that was assigned before inventory went negative</span></span>
- <span data-ttu-id="e84bb-107">**Активные затраты** — последние затраты, которые были активированы в версии учета затрат</span><span class="sxs-lookup"><span data-stu-id="e84bb-107">**Active cost** – The latest cost that was activated in a costing version</span></span>
- <span data-ttu-id="e84bb-108">**Цена номенклатуры** — затраты, которые указываются для выпущенного продукта</span><span class="sxs-lookup"><span data-stu-id="e84bb-108">**Item price** – The cost that is specified for the released product</span></span>

<span data-ttu-id="e84bb-109">Чтобы определить, какое из этих значений затрат следует использовать при расчете скользящего среднего, система использует _резервную последовательность затрат_ для задания порядка предпочтения значений.</span><span class="sxs-lookup"><span data-stu-id="e84bb-109">To determine which of these cost values should be used in moving average calculations, the system uses a _fallback cost sequence_ to establish the order of preference for the values.</span></span> <span data-ttu-id="e84bb-110">Если предпочтительное значение затрат недоступно, система использует следующее предпочтительное значение и т. д.</span><span class="sxs-lookup"><span data-stu-id="e84bb-110">If the preferred cost value isn't available, the system uses the next-preferred value, and so on.</span></span>

<span data-ttu-id="e84bb-111">В предыдущих версиях Microsoft Dynamics 365 Supply Chain Management система использовала фиксированную резервную последовательность затрат (_последний расход — активные затраты — цена номенклатуры_).</span><span class="sxs-lookup"><span data-stu-id="e84bb-111">In previous versions of Microsoft Dynamics 365 Supply Chain Management, the system used a fixed fallback cost sequence (_Last issue – Active cost – Item price_).</span></span> <span data-ttu-id="e84bb-112">В версии 10.0.11 эта последовательность все еще является последовательностью по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e84bb-112">In version 10.0.11, this sequence is still the default sequence.</span></span> <span data-ttu-id="e84bb-113">Однако можно также включить функцию, позволяющую выбрать одну из трех доступных резервных последовательностей затрат.</span><span class="sxs-lookup"><span data-stu-id="e84bb-113">However, you can also turn on a feature that lets you select among three available fallback cost sequences.</span></span> <span data-ttu-id="e84bb-114">Эта возможность особенно полезна для организаций, регулярно использующих отрицательные значения запасов.</span><span class="sxs-lookup"><span data-stu-id="e84bb-114">This feature can be especially useful for organizations that regularly use negative inventory values.</span></span>

<span data-ttu-id="e84bb-115">Чтобы сделать доступным селектор резервной последовательности затрат, пользователь (или администратор) должен использовать [управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), чтобы включить функцию с именем _Резервная последовательность затрат для скользящего среднего_.</span><span class="sxs-lookup"><span data-stu-id="e84bb-115">To make the selector for the fallback cost sequence available, you (or an admin) must use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named _Moving average fallback cost sequence_.</span></span>

<span data-ttu-id="e84bb-116">Чтобы выбрать резервную последовательность затрат для расчета скользящего среднего, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e84bb-116">To select the fallback cost sequence for moving average calculations, follow these steps.</span></span>

1. <span data-ttu-id="e84bb-117">Откройте страницу **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="e84bb-117">Open the **Parameters** page.</span></span>
2. <span data-ttu-id="e84bb-118">На вкладке **Учет запасов** в разделе **Скользящее среднее** задайте в поле **Резервная последовательность затрат** одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="e84bb-118">On the **Inventory accounting** tab, in the **Moving average** section, set the **Fallback cost sequence** field to one of the following values:</span></span>

    - <span data-ttu-id="e84bb-119">**Последний расход — Активные затраты — Цена номенклатуры** — эта последовательность является последовательностью по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e84bb-119">**Last issue – Active cost – Item price** – This sequence is the default sequence.</span></span> <span data-ttu-id="e84bb-120">Это та же последовательность, которая используется, когда функция _Резервная последовательность затрат для скользящего среднего_ не включена.</span><span class="sxs-lookup"><span data-stu-id="e84bb-120">It's the same sequence that is used if the _Moving average fallback cost sequence_ feature isn't turned on.</span></span>
    - <span data-ttu-id="e84bb-121">**Активные затраты — Последний расход**</span><span class="sxs-lookup"><span data-stu-id="e84bb-121">**Active cost – Last issue**</span></span>
    - <span data-ttu-id="e84bb-122">**Активные затраты — Цена номенклатуры** — организации могут столкнуться с проблемами производительности, если они используют бизнес-процессы, в которых запасы регулярно становятся отрицательным и, в то же время, объем проводки имеет высокий уровень.</span><span class="sxs-lookup"><span data-stu-id="e84bb-122">**Active cost – Item price** – Organizations might experience performance issues if they use business processes where inventory regularly goes negative and, at the same time, the transaction volume is high.</span></span> <span data-ttu-id="e84bb-123">Эта настройка может помочь снизить такие проблемы с производительностью.</span><span class="sxs-lookup"><span data-stu-id="e84bb-123">This setting can help mitigate those performance issues.</span></span>

<span data-ttu-id="e84bb-124">![Параметры учета запасов](media/inventory-accounting-parameters.png "Параметры учета запасов")</span><span class="sxs-lookup"><span data-stu-id="e84bb-124">![Inventory accounting parameters](media/inventory-accounting-parameters.png "Inventory accounting parameters")</span></span>
