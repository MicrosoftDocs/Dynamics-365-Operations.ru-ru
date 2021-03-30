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
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f8348283a05ce9acb1dbbcd1a4b9b97ea1d337f1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251993"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="a57e2-104">Ведение спланированных заказов</span><span class="sxs-lookup"><span data-stu-id="a57e2-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a57e2-105">В этой теме содержится информация об управлении спланированными заказами.</span><span class="sxs-lookup"><span data-stu-id="a57e2-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="a57e2-106">В ней описывается, как можно обновить статус спланированных заказов, утвердить их и отфильтровать спланированные заказы, которые имеют тот же статус, что и выбранный спланированный заказ.</span><span class="sxs-lookup"><span data-stu-id="a57e2-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="a57e2-107">Вы можете управлять запланированными заказами в рабочей области **Сводное планирование**, список **Спланированный заказ** или списки **Спланированный производственный заказ**, **Спланированный заказ на покупку** и **Спланированное перемещение**.</span><span class="sxs-lookup"><span data-stu-id="a57e2-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="a57e2-108">Статус спланированного заказа</span><span class="sxs-lookup"><span data-stu-id="a57e2-108">Planned order status</span></span>
<span data-ttu-id="a57e2-109">Можно использовать поле **Статус**, чтобы отслеживать ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="a57e2-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="a57e2-110">Используются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a57e2-110">The following values are used:</span></span>

-   <span data-ttu-id="a57e2-111">Когда система сводного планирования создает спланированные заказы, они имеют статус **Не обработано**.</span><span class="sxs-lookup"><span data-stu-id="a57e2-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="a57e2-112">Если решено не утверждать спланированный заказ, ему можно присвоить статус **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="a57e2-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="a57e2-113">Если необходимо утвердить спланированный заказ, можно изменить статус на **Утверждено**.</span><span class="sxs-lookup"><span data-stu-id="a57e2-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="a57e2-114">Спланированные заказы со статусом **Утверждено** учитываются в сводном планировании, поэтому они не изменяются и не удаляются во время последующего запуска сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="a57e2-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted during a later master planning run.</span></span> <span data-ttu-id="a57e2-115">Для достижения этой цели логика планирования копирует спланированные заказы **Одобрено** из старой версии плана в новую версию плана во время сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="a57e2-115">To achieve this, the planning logic copies the **Approved** planned orders from the old plan version to the new plan version during master planning.</span></span>

## <a name="firming-planned-orders"></a><span data-ttu-id="a57e2-116">Утверждение спланированных заказов</span><span class="sxs-lookup"><span data-stu-id="a57e2-116">Firming planned orders</span></span> 
<span data-ttu-id="a57e2-117">При утверждении спланированных заказов создаются реальные заказы.</span><span class="sxs-lookup"><span data-stu-id="a57e2-117">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="a57e2-118">Они также известны как *выпущенные* или *открытые заказы*.</span><span class="sxs-lookup"><span data-stu-id="a57e2-118">These are also known as *released* or *open orders*.</span></span> <span data-ttu-id="a57e2-119">Когда спланированный заказ утвержден, он перемещается в раздел заказов соответствующего модуля.</span><span class="sxs-lookup"><span data-stu-id="a57e2-119">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="a57e2-120">Можно выбрать два варианта утверждения на странице **Спланированные заказы**:</span><span class="sxs-lookup"><span data-stu-id="a57e2-120">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="a57e2-121">**Утвердить** — будет утвержден один или несколько выбранных спланированных заказов.</span><span class="sxs-lookup"><span data-stu-id="a57e2-121">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="a57e2-122">**Утвердить все** — все спланированные заказы будут утверждены в фильтре.</span><span class="sxs-lookup"><span data-stu-id="a57e2-122">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="a57e2-123">При использовании варианта **Утвердить все** вам не придется выбирать спланированный заказ, все спланированные заказы в фильтре будут утверждены.</span><span class="sxs-lookup"><span data-stu-id="a57e2-123">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="a57e2-124">Этот параметр может быть полезен при утверждении большого количества спланированных заказов.</span><span class="sxs-lookup"><span data-stu-id="a57e2-124">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="a57e2-125">Можно отследить утвержденный спланированный из пункта **История утверждений** в форме **Спланированные заказы > Просмотреть > История утверждений**.</span><span class="sxs-lookup"><span data-stu-id="a57e2-125">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="a57e2-126">Использовать параллельное утверждение</span><span class="sxs-lookup"><span data-stu-id="a57e2-126">Parallelize firming</span></span>
<span data-ttu-id="a57e2-127">Если планируется утверждение многих заказов одновременно, параллельное выполнение может улучшить время выполнения или производительность.</span><span class="sxs-lookup"><span data-stu-id="a57e2-127">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="a57e2-128">Этот параметр доступен при утверждении нескольких спланированных заказов с помощью команды **Утвердить** или **Утвердить все**.</span><span class="sxs-lookup"><span data-stu-id="a57e2-128">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="a57e2-129">Доступны следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="a57e2-129">The following parameters are available:</span></span>

-   <span data-ttu-id="a57e2-130">**Параллельное утверждение** — если **Да**, процесс утверждения будет выполняться параллельно с количеством потоков, определенных в параметре **Количество потоков**.</span><span class="sxs-lookup"><span data-stu-id="a57e2-130">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="a57e2-131">**Количество потоков** — управляет количеством потоков, используемых для параллельной обработки процесса утверждения.</span><span class="sxs-lookup"><span data-stu-id="a57e2-131">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="a57e2-132">Этот параметр отображается только в том случае, если для параметра **Параллельное утверждение** задано значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="a57e2-132">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>

> [!NOTE]
> <span data-ttu-id="a57e2-133">Вариант **Использовать параллельное утверждение** отображается только в том случае, если у вас есть более одного спланированного заказа, выбранного для утверждения.</span><span class="sxs-lookup"><span data-stu-id="a57e2-133">The option for **Parallelize firming** is only shown when you have more than one planned order selected for firming.</span></span>

<a name="additional-resources"></a><span data-ttu-id="a57e2-134">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a57e2-134">Additional resources</span></span>
--------

[<span data-ttu-id="a57e2-135">Обзор сводных планов</span><span class="sxs-lookup"><span data-stu-id="a57e2-135">Master plans overview</span></span>](master-plans.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]