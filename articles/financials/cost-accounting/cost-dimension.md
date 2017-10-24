---
title: "Создание аналитик и импорт элементов аналитик"
description: "Учет затрат — это независимый модуль, для работы которого требуются данные справочников из других модулей."
author: YuyuScheller
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0fb276e7d62e2f7c02934e74741c8cf74778fc12
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="create-dimensions-and-import-dimension-members"></a><span data-ttu-id="cf97c-103">Создание аналитик и импорт элементов аналитик</span><span class="sxs-lookup"><span data-stu-id="cf97c-103">Create dimensions and import dimension members</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cf97c-104">Учет затрат — это независимый модуль, для работы которого требуются данные из других модулей.</span><span class="sxs-lookup"><span data-stu-id="cf97c-104">Cost accounting is an independent module that requires data from other modules.</span></span> <span data-ttu-id="cf97c-105">Эти данные подразделяется на следующие:</span><span class="sxs-lookup"><span data-stu-id="cf97c-105">This data is categorized into the following:</span></span>

-  <span data-ttu-id="cf97c-106">Элементы затрат</span><span class="sxs-lookup"><span data-stu-id="cf97c-106">Cost elements</span></span>
-  <span data-ttu-id="cf97c-107">Объекты затрат</span><span class="sxs-lookup"><span data-stu-id="cf97c-107">Cost objects</span></span>
-  <span data-ttu-id="cf97c-108">Статистические аналитики</span><span class="sxs-lookup"><span data-stu-id="cf97c-108">Statistical dimensions</span></span>

<span data-ttu-id="cf97c-109">**Элемент затрат** соответствует связанному с затратами элементу в плане счетов.</span><span class="sxs-lookup"><span data-stu-id="cf97c-109">A **Cost element** corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="cf97c-110">**Объект затрат** соответствует любому типу финансовой аналитики, такому как продукты, центры затрат и проекты, которые вы хотите оценивать, затраты на которые вы хотите распределять или изменять непосредственно.</span><span class="sxs-lookup"><span data-stu-id="cf97c-110">A **Cost object** corresponds to any type of financial dimension, such as products, cost centers, and projects that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="cf97c-111">**Статистическая аналитика** и ее элементы используются для регистрации немонетарных записей.</span><span class="sxs-lookup"><span data-stu-id="cf97c-111">A **Statistical dimension** and its members are used to register non-monetary entries.</span></span> <span data-ttu-id="cf97c-112">Элементы статистической аналитики могут использоваться в качестве базы распределения в распределении затрат и распределении стоимости.</span><span class="sxs-lookup"><span data-stu-id="cf97c-112">Statistical dimension members can be used as an allocation base in cost distribution and allocation</span></span> 

<span data-ttu-id="cf97c-113">На следующей схеме показаны аналитики, которые используются в модуле "Учет затрат".</span><span class="sxs-lookup"><span data-stu-id="cf97c-113">The following diagram illustrates the dimensions that are used in Cost accounting.</span></span>

<span data-ttu-id="cf97c-114">[![Аналитики учета затрат](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="cf97c-114">[![Cost accounting dimensions](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span></span>

<span data-ttu-id="cf97c-115">После импорта данных в модуль "Учет затрат" их можно использовать для построения различных перспектив, позволяющих руководителям на всех уровнях организации делать обоснованные выводы.</span><span class="sxs-lookup"><span data-stu-id="cf97c-115">After the data is imported into Cost accounting, you can use it to build various perspectives that provide insights to managers at all levels of the organization.</span></span> <span data-ttu-id="cf97c-116">В следующих темах содержатся сведения о создании аналитик и импорте элементов аналитик.</span><span class="sxs-lookup"><span data-stu-id="cf97c-116">The following topics provide information about creating dimensions and importing dimension members.</span></span> 

-  [<span data-ttu-id="cf97c-117">Аналитики элемента затрат</span><span class="sxs-lookup"><span data-stu-id="cf97c-117">Cost element dimensions</span></span>](cost-elements.md)
-  [<span data-ttu-id="cf97c-118">Создание элементов затрат (проводник по задаче)</span><span class="sxs-lookup"><span data-stu-id="cf97c-118">Create cost elements (Task guide)</span></span>](./tasks/create-cost-elements.md)
-  [<span data-ttu-id="cf97c-119">Аналитики объекта затрат</span><span class="sxs-lookup"><span data-stu-id="cf97c-119">Cost object dimensions</span></span>](cost-objects.md)
-  [<span data-ttu-id="cf97c-120">Создание элементов затрат (проводник по задаче)</span><span class="sxs-lookup"><span data-stu-id="cf97c-120">Create cost elements (Task guide)</span></span>](./tasks/create-cost-objects.md)
-  [<span data-ttu-id="cf97c-121">Сопоставление элементов аналитики элемента затрат с общим набором элементов аналитики</span><span class="sxs-lookup"><span data-stu-id="cf97c-121">Map cost element dimension members to a common set of dimension members</span></span>](map-cost-elements-dimension-members.md)
-  [<span data-ttu-id="cf97c-122">Сопоставление измерения элементов затрат (проводник по задаче)</span><span class="sxs-lookup"><span data-stu-id="cf97c-122">Map a cost element dimension (Task guide)</span></span>](./tasks/map-cost-element-dimension.md)
-  [<span data-ttu-id="cf97c-123">Элементы статистической аналитики и шаблоны поставщика статистической меры</span><span class="sxs-lookup"><span data-stu-id="cf97c-123">Statistical dimension members and statistical measure provider templates</span></span>](statistical-measure-provider-template.md)







