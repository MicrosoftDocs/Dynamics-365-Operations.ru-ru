---
title: Ведение спланированных заказов
description: В этой теме содержится информация об управлении спланированными заказами. В ней описывается, как можно обновить статус спланированных заказов, утвердить их и отфильтровать спланированные заказы, которые имеют тот же статус, что и выбранный спланированный заказ.
author: roxanadiaconu
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf578d98abc4825c5607ec031da6ab6737c3183a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560380"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="bdfce-104">Ведение спланированных заказов</span><span class="sxs-lookup"><span data-stu-id="bdfce-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bdfce-105">В этой теме содержится информация об управлении спланированными заказами.</span><span class="sxs-lookup"><span data-stu-id="bdfce-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="bdfce-106">В ней описывается, как можно обновить статус спланированных заказов, утвердить их и отфильтровать спланированные заказы, которые имеют тот же статус, что и выбранный спланированный заказ.</span><span class="sxs-lookup"><span data-stu-id="bdfce-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="bdfce-107">Вы можете управлять запланированными заказами в рабочей области **Сводное планирование**, список **Спланированный заказ** или списки **Спланированный производственный заказ**, **Спланированный заказ на покупку** и **Спланированное перемещение**.</span><span class="sxs-lookup"><span data-stu-id="bdfce-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> <span data-ttu-id="bdfce-108">Можно использовать поле **Статус**, чтобы отслеживать ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="bdfce-108">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="bdfce-109">Используются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bdfce-109">The following values are used:</span></span>

-   <span data-ttu-id="bdfce-110">Когда система сводного планирования создает спланированные заказы, они имеют статус **Не обработано**.</span><span class="sxs-lookup"><span data-stu-id="bdfce-110">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="bdfce-111">Если решено не утверждать спланированный заказ, ему можно присвоить статус **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="bdfce-111">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="bdfce-112">Когда решено не утверждать спланированный заказ, ему можно присвоить статус **Утверждено**.</span><span class="sxs-lookup"><span data-stu-id="bdfce-112">When you decide to firm a planned order, you can give it a status of **Approved**.</span></span> <span data-ttu-id="bdfce-113">Этот статус указывает, что утверждение спланированного заказа утверждено, но заказ еще не утвержден.</span><span class="sxs-lookup"><span data-stu-id="bdfce-113">This status indicates that you approve firming of the planned order, but it isn't firmed yet.</span></span>

<span data-ttu-id="bdfce-114">**Примечание.** Утвержденный спланированный заказ переносится в своем текущем состоянии в следующий расчет сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="bdfce-114">**Note:** An approved planned order is transferred, in its current state, to the next master planning calculation.</span></span> <span data-ttu-id="bdfce-115">Спланированные заказы можно утвердить, последовательно, щелкнув **Утверждение**.</span><span class="sxs-lookup"><span data-stu-id="bdfce-115">You can firm planned orders by clicking **Firm**.</span></span> <span data-ttu-id="bdfce-116">Утвердить можно следующие спланированные заказы:</span><span class="sxs-lookup"><span data-stu-id="bdfce-116">You can firm the following planned orders:</span></span>

-   <span data-ttu-id="bdfce-117">Выбранный спланированный заказ.</span><span class="sxs-lookup"><span data-stu-id="bdfce-117">The planned order that is selected.</span></span>
-   <span data-ttu-id="bdfce-118">Несколько спланированных заказов.</span><span class="sxs-lookup"><span data-stu-id="bdfce-118">Multiple planned orders.</span></span>
-   <span data-ttu-id="bdfce-119">Спланированные заказы, которые создаются посредством развертывания на странице **Развертывание**.</span><span class="sxs-lookup"><span data-stu-id="bdfce-119">Planned orders that are generated by an explosion from the **Explosion** page.</span></span> <span data-ttu-id="bdfce-120">Щелкните **Спланированные заказы**, выберите спланированный заказ, а затем щелкните **Утверждение**.</span><span class="sxs-lookup"><span data-stu-id="bdfce-120">Click **Planned orders**, select the planned order, and then click **Firm**.</span></span>

<span data-ttu-id="bdfce-121">Когда спланированный заказ утвержден, он перемещается в раздел заказов соответствующего модуля.</span><span class="sxs-lookup"><span data-stu-id="bdfce-121">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span> 

<a name="additional-resources"></a><span data-ttu-id="bdfce-122">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bdfce-122">Additional resources</span></span>
--------

[<span data-ttu-id="bdfce-123">Сводные планы</span><span class="sxs-lookup"><span data-stu-id="bdfce-123">Master plans</span></span>](master-plans.md)



