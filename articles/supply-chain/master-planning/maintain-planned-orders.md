---
title: Ведение спланированных заказов
description: В этой теме содержится информация об управлении спланированными заказами. В ней описывается, как можно обновить статус спланированных заказов, утвердить их и отфильтровать спланированные заказы, которые имеют тот же статус, что и выбранный спланированный заказ.
author: roxanadiaconu
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ecda1c113a0663ff430aa15a0023668097078ad1
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213822"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="47682-104">Ведение спланированных заказов</span><span class="sxs-lookup"><span data-stu-id="47682-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47682-105">В этой теме содержится информация об управлении спланированными заказами.</span><span class="sxs-lookup"><span data-stu-id="47682-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="47682-106">В ней описывается, как можно обновить статус спланированных заказов, утвердить их и отфильтровать спланированные заказы, которые имеют тот же статус, что и выбранный спланированный заказ.</span><span class="sxs-lookup"><span data-stu-id="47682-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="47682-107">Вы можете управлять запланированными заказами в рабочей области **Сводное планирование**, список **Спланированный заказ** или списки **Спланированный производственный заказ**, **Спланированный заказ на покупку** и **Спланированное перемещение**.</span><span class="sxs-lookup"><span data-stu-id="47682-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="47682-108">Статус спланированного заказа</span><span class="sxs-lookup"><span data-stu-id="47682-108">Planned order status</span></span>
<span data-ttu-id="47682-109">Можно использовать поле **Статус**, чтобы отслеживать ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="47682-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="47682-110">Используются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="47682-110">The following values are used:</span></span>

-   <span data-ttu-id="47682-111">Когда система сводного планирования создает спланированные заказы, они имеют статус **Не обработано**.</span><span class="sxs-lookup"><span data-stu-id="47682-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="47682-112">Если решено не утверждать спланированный заказ, ему можно присвоить статус **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="47682-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="47682-113">Если необходимо утвердить спланированный заказ, можно изменить статус на **Утверждено**.</span><span class="sxs-lookup"><span data-stu-id="47682-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="47682-114">Спланированные заказы со статусом **Утверждено** учитываются в сводном планировании, поэтому они не изменяются и не удаляются во время последующего запуска сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="47682-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted during a later master planning run.</span></span> <span data-ttu-id="47682-115">Для достижения этой цели логика планирования копирует спланированные заказы **Одобрено** из старой версии плана в новую версию плана во время сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="47682-115">To achieve this, the planning logic copies the **Approved** planned orders from the old plan version to the new plan version during master planning.</span></span>

## <a name="firming-planned-orders"></a><span data-ttu-id="47682-116">Утверждение спланированных заказов</span><span class="sxs-lookup"><span data-stu-id="47682-116">Firming planned orders</span></span> 
<span data-ttu-id="47682-117">При утверждении спланированных заказов создаются реальные заказы.</span><span class="sxs-lookup"><span data-stu-id="47682-117">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="47682-118">Они также известны как *выпущенные* или *открытые заказы*.</span><span class="sxs-lookup"><span data-stu-id="47682-118">These are also known as *released* or *open orders*.</span></span> <span data-ttu-id="47682-119">Когда спланированный заказ утвержден, он перемещается в раздел заказов соответствующего модуля.</span><span class="sxs-lookup"><span data-stu-id="47682-119">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="47682-120">Можно выбрать два варианта утверждения на странице **Спланированные заказы**:</span><span class="sxs-lookup"><span data-stu-id="47682-120">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="47682-121">**Утвердить** — будет утвержден один или несколько выбранных спланированных заказов.</span><span class="sxs-lookup"><span data-stu-id="47682-121">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="47682-122">**Утвердить все** — все спланированные заказы будут утверждены в фильтре.</span><span class="sxs-lookup"><span data-stu-id="47682-122">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="47682-123">При использовании варианта **Утвердить все** вам не придется выбирать спланированный заказ, все спланированные заказы в фильтре будут утверждены.</span><span class="sxs-lookup"><span data-stu-id="47682-123">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="47682-124">Этот параметр может быть полезен при утверждении большого количества спланированных заказов.</span><span class="sxs-lookup"><span data-stu-id="47682-124">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="47682-125">Можно отследить утвержденный спланированный из пункта **История утверждений** в форме **Спланированные заказы > Просмотреть > История утверждений**.</span><span class="sxs-lookup"><span data-stu-id="47682-125">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="47682-126">Использовать параллельное утверждение</span><span class="sxs-lookup"><span data-stu-id="47682-126">Parallelize firming</span></span>
<span data-ttu-id="47682-127">Если планируется утверждение многих заказов одновременно, параллельное выполнение может улучшить время выполнения или производительность.</span><span class="sxs-lookup"><span data-stu-id="47682-127">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="47682-128">Этот параметр доступен при утверждении нескольких спланированных заказов с помощью команды **Утвердить** или **Утвердить все**.</span><span class="sxs-lookup"><span data-stu-id="47682-128">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="47682-129">Доступны следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="47682-129">The following parameters are available:</span></span>

-   <span data-ttu-id="47682-130">**Параллельное утверждение** — если **Да**, процесс утверждения будет выполняться параллельно с количеством потоков, определенных в параметре **Количество потоков**.</span><span class="sxs-lookup"><span data-stu-id="47682-130">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="47682-131">**Количество потоков** — управляет количеством потоков, используемых для параллельной обработки процесса утверждения.</span><span class="sxs-lookup"><span data-stu-id="47682-131">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="47682-132">Этот параметр отображается только в том случае, если для параметра **Параллельное утверждение** задано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="47682-132">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>

> [!NOTE]
> <span data-ttu-id="47682-133">Вариант **Использовать параллельное утверждение** отображается только в том случае, если у вас есть более одного спланированного заказа, выбранного для утверждения.</span><span class="sxs-lookup"><span data-stu-id="47682-133">The option for **Parallelize firming** is only shown when you have more than one planned order selected for firming.</span></span>

<a name="additional-resources"></a><span data-ttu-id="47682-134">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="47682-134">Additional resources</span></span>
--------

[<span data-ttu-id="47682-135">Обзор сводных планов</span><span class="sxs-lookup"><span data-stu-id="47682-135">Master plans overview</span></span>](master-plans.md)



