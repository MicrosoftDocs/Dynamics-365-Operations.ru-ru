---
title: Резервирование такой же партии для заказа на продажу
description: В этой статье описывается, как настроить продукт, чтобы разрешить резервирование запасов относительно одной партии запасов.
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 067dd6d3c337378a610ee1fcf6a7812716813bab
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251738"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="a6a09-103">Резервирование такой же партии для заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="a6a09-103">Reserve the same batch for a sales order</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6a09-104">В этой статье описывается, как настроить продукт, чтобы разрешить резервирование запасов относительно одной партии запасов.</span><span class="sxs-lookup"><span data-stu-id="a6a09-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="a6a09-105">Резервирование из одной и той же партии позволяет резервировать запасы для строки заказа на продажу из одной партии складских запасов.</span><span class="sxs-lookup"><span data-stu-id="a6a09-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="a6a09-106">Например, клиенту, заказывающему обои, может потребоваться выполнение всего заказа из одной и той же партии, чтобы все рулоны обоев были одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="a6a09-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="a6a09-107">Чтобы настроить для продукта резервирование из одной и той же партии, эти параметры должны быть активными в настройках группы моделей номенклатур, группы аналитик отслеживания и группы аналитик хранения, которые назначаются продукту:</span><span class="sxs-lookup"><span data-stu-id="a6a09-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

-   <span data-ttu-id="a6a09-108">**Группы моделей номенклатур** — для группы моделей номенклатур должны быть выбраны поля **Выбор из той же партии** и **Консолидировать требование** в группе полей **Резервирование** для политик запасов.</span><span class="sxs-lookup"><span data-stu-id="a6a09-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
-   <span data-ttu-id="a6a09-109">**Группы аналитик отслеживания** — у группы аналитик отслеживания должно иметься поле **План покрытия по аналитикам**, выбранное для номера партии.</span><span class="sxs-lookup"><span data-stu-id="a6a09-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
-   <span data-ttu-id="a6a09-110">**Группы аналитик хранения** — у группы аналитик хранения должно иметься поле **План покрытия по аналитикам**, выбранное для настроек **Сайт** и **Склад**.</span><span class="sxs-lookup"><span data-stu-id="a6a09-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="a6a09-111">При резервировании запасов для продукта в строке заказа на продажу, для которой настроен выбор из той же партии, система пытается зарезервировать заказываемое количество из одной партии складских запасов.</span><span class="sxs-lookup"><span data-stu-id="a6a09-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, the system tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="a6a09-112">Во внимание принимаются также все особые требования к атрибутам партии.</span><span class="sxs-lookup"><span data-stu-id="a6a09-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="a6a09-113">Если количество не может быть скомплектовано из одной партии, отобразится страница **Конфликт резервирования из той же партии**.</span><span class="sxs-lookup"><span data-stu-id="a6a09-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="a6a09-114">Эта страница описывает вопросы и действия, которые вы можете предпринять, чтобы продолжить резервирование.</span><span class="sxs-lookup"><span data-stu-id="a6a09-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="a6a09-115">Следующие условия могут помешать резервированию партии:</span><span class="sxs-lookup"><span data-stu-id="a6a09-115">The following conditions might prevent the batch from being reserved:</span></span>

-   <span data-ttu-id="a6a09-116">Код расстановки партии имеет настройку **Резервирование блока** для продаж со значением **Заблокировано**.</span><span class="sxs-lookup"><span data-stu-id="a6a09-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
-   <span data-ttu-id="a6a09-117">Срок годности партии определяется на основе даты окончания срока годности и всех применимых дней продажи клиента.</span><span class="sxs-lookup"><span data-stu-id="a6a09-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="a6a09-118">Номенклатура может по-прежнему рассматриваться как доступная для резервирования, если группа складских моделей для номенклатуры является управлением датой по принципу FEFO и в качестве критерия комплектации выбран срок годности.</span><span class="sxs-lookup"><span data-stu-id="a6a09-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
-   <span data-ttu-id="a6a09-119">Партия имеет недостаточное количество оставшихся дней срока хранения на основании даты окончания срока годности и даты, до которой желательно использовать продукцию, плюс все дни продаж клиента.</span><span class="sxs-lookup"><span data-stu-id="a6a09-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>




