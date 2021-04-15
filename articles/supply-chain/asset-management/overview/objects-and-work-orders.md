---
title: Активы и заказы на работу
description: В этом разделе описываются активы и заказы на работу в «Управлении активами».
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2fe5523edf46712b17aa7abcad50da44c3eaffd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816774"
---
# <a name="assets-and-work-orders"></a><span data-ttu-id="2d84d-103">Активы и заказы на работу</span><span class="sxs-lookup"><span data-stu-id="2d84d-103">Assets and work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="2d84d-104">В этом разделе описываются активы и заказы на работу в «Управлении активами».</span><span class="sxs-lookup"><span data-stu-id="2d84d-104">This topic describes assets and work orders in Asset Management.</span></span> <span data-ttu-id="2d84d-105">Активы и заказы на работу являются центральными частями «Управления активами».</span><span class="sxs-lookup"><span data-stu-id="2d84d-105">Assets and work orders are the central parts of Asset Management.</span></span> <span data-ttu-id="2d84d-106">*Актив* — это машина или часть машины, которая требует постоянного обслуживания и сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="2d84d-106">An *asset* is a machine or machine part that requires continuous maintenance and service.</span></span> <span data-ttu-id="2d84d-107">Активы могут быть созданы в иерархической структуре, и они могут быть связаны с функциональными местоположениями.</span><span class="sxs-lookup"><span data-stu-id="2d84d-107">Assets can be created in a hierarchical structure, and they can be related to functional locations.</span></span> <span data-ttu-id="2d84d-108">Задания обслуживания могут быть спланированы на всех уровнях в структуре актива.</span><span class="sxs-lookup"><span data-stu-id="2d84d-108">Maintenance jobs can be planned at all levels in the asset structure.</span></span>

<span data-ttu-id="2d84d-109">На каждом активе настраиваются различные данные, такие как информация о продукте и спецификация активов, а также планы требуемого обслуживания.</span><span class="sxs-lookup"><span data-stu-id="2d84d-109">Various data, such as product information and asset specification, and required maintenance plans are set up on each asset.</span></span> <span data-ttu-id="2d84d-110">Нижеприведенный пример показывает обзор данных активов и принадлежности активов к типам заданий.</span><span class="sxs-lookup"><span data-stu-id="2d84d-110">The following illustration shows an overview of asset data and the affiliation of assets to job types.</span></span> <span data-ttu-id="2d84d-111">Красный текст используется для примеров, отображающих наследование и зависимости.</span><span class="sxs-lookup"><span data-stu-id="2d84d-111">Red text is used for examples that show inheritance and dependencies.</span></span>

![Диаграмма, показывающая данные активов, имеющие отношение к типам заданий](media/05-overview-image.png)

<span data-ttu-id="2d84d-113">Каждый заказ на работу имеет тип заказа на работу, такие как профилактическое обслуживание, корректирующее обслуживание или осмотр.</span><span class="sxs-lookup"><span data-stu-id="2d84d-113">Every work order has a work order type, such preventive maintenance, corrective maintenance, or inspection.</span></span> <span data-ttu-id="2d84d-114">Заказ на работу содержит одно или несколько заданий заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="2d84d-114">The work order contains one or more work order jobs.</span></span> <span data-ttu-id="2d84d-115">Каждый заказ на работу определяет задание, которое должно быть выполнено по активу и соответствующему типу задания.</span><span class="sxs-lookup"><span data-stu-id="2d84d-115">Every work order job defines a job that must be performed on an asset and a related job type.</span></span> <span data-ttu-id="2d84d-116">Примеры соответствующих типов задания включают 10 000 км, 50 000 км, 1-летний капитальный ремонт и проверку безопасности.</span><span class="sxs-lookup"><span data-stu-id="2d84d-116">Examples of related job types include 10,000 km, 50,000 km, 1-year overhaul, and safety inspection.</span></span> <span data-ttu-id="2d84d-117">Один заказ на работу может быть связан с несколькими активами.</span><span class="sxs-lookup"><span data-stu-id="2d84d-117">One work order can be related to multiple assets.</span></span>

<span data-ttu-id="2d84d-118">На следующем рисунке показан обзор ключевых данных в заказе на работу.</span><span class="sxs-lookup"><span data-stu-id="2d84d-118">The following illustration shows an overview of the key data in a work order.</span></span>

![Диаграмма, содержащая ключевые данные в заказе на работу](media/06-overview-image.png)

<span data-ttu-id="2d84d-120">Заказ на работу может быть связан с другим заказом на работу, а типы заданий могут содержать последующие задания, создающие заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="2d84d-120">A work order can be related to another work order, and job types can contain succeeding jobs that create a work order.</span></span> <span data-ttu-id="2d84d-121">Как правило, между заказами на работу нет зависимостей.</span><span class="sxs-lookup"><span data-stu-id="2d84d-121">In general, there are no dependencies between work orders.</span></span> <span data-ttu-id="2d84d-122">Таким образом, они могут изменить состояние жизненного цикла заказа на работу и могут быть спланированы независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="2d84d-122">Therefore, they can change their work order lifecycle state and can be scheduled independently of each other.</span></span>

<span data-ttu-id="2d84d-123">Заказы на работу могут создаваться различными способами, связанными с корректирующим, профилактическим или реактивным обслуживанием.</span><span class="sxs-lookup"><span data-stu-id="2d84d-123">Work orders can be created in various ways that are related to corrective, preventive, or reactive maintenance.</span></span> <span data-ttu-id="2d84d-124">Можно также создать заказ на работу вручную.</span><span class="sxs-lookup"><span data-stu-id="2d84d-124">You can also create work orders manually.</span></span> <span data-ttu-id="2d84d-125">Следующий рисунок показывает обзор процесса автоматического или ручного создания заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="2d84d-125">The following illustration shows an overview of the process for automatic or manual creation of work orders.</span></span>

![Диаграмма, в которой показано автоматическое или ручное создание заказов на работу](media/07-overview-image.png)

<span data-ttu-id="2d84d-127">Несколько этапов должны быть завершены, когда вы хотите спланировать и запустить задание обслуживания по заказу на работу.</span><span class="sxs-lookup"><span data-stu-id="2d84d-127">Several steps must be completed when you want to schedule and run a maintenance job on a work order.</span></span> <span data-ttu-id="2d84d-128">На следующем рисунке показан обзор обработки для заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="2d84d-128">The following illustration shows an overview of the processing for a work order.</span></span>

![Диаграмма, показывающая обзор обработки заказа на работу](media/08-overview-image.png)

> [!NOTE]
> <span data-ttu-id="2d84d-130">В целом, когда вы работаете в Dynamics 365 Supply Chain Management и модуле **Управление аткивами**, выберайте **Создать** для создания новой записи, выбирайте **Изменить** для обновления существующей записи и выбирайте **Сохранить**, чтобы сохранить новые или отредактированные данные.</span><span class="sxs-lookup"><span data-stu-id="2d84d-130">In general, when you work in Dynamics 365 Supply Chain Management and the **Asset Management** module, you select **New** to create a new record, you select **Edit** to update an existing record, and you select **Save** to save new or edited data.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]