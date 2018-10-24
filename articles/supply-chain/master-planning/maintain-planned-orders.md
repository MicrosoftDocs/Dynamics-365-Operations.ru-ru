---
title: "Ведение спланированных заказов"
description: "В этой теме содержится информация об управлении спланированными заказами. В ней описывается, как можно обновить статус спланированных заказов, утвердить их и отфильтровать спланированные заказы, которые имеют тот же статус, что и выбранный спланированный заказ."
author: roxanadiaconu
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 657c19896b20a514dc5308bf7fb086085b482fec
ms.openlocfilehash: bf578d98abc4825c5607ec031da6ab6737c3183a
ms.contentlocale: ru-ru
ms.lasthandoff: 10/08/2018

---

# <a name="maintain-planned-orders"></a><span data-ttu-id="d847a-104">Ведение спланированных заказов</span><span class="sxs-lookup"><span data-stu-id="d847a-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d847a-105">В этой теме содержится информация об управлении спланированными заказами.</span><span class="sxs-lookup"><span data-stu-id="d847a-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="d847a-106">В ней описывается, как можно обновить статус спланированных заказов, утвердить их и отфильтровать спланированные заказы, которые имеют тот же статус, что и выбранный спланированный заказ.</span><span class="sxs-lookup"><span data-stu-id="d847a-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="d847a-107">Вы можете управлять запланированными заказами в рабочей области **Сводное планирование**, список **Спланированный заказ** или списки **Спланированный производственный заказ**, **Спланированный заказ на покупку** и **Спланированное перемещение**.</span><span class="sxs-lookup"><span data-stu-id="d847a-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> <span data-ttu-id="d847a-108">Можно использовать поле **Статус**, чтобы отслеживать ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="d847a-108">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="d847a-109">Используются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d847a-109">The following values are used:</span></span>

-   <span data-ttu-id="d847a-110">Когда система сводного планирования создает спланированные заказы, они имеют статус **Не обработано**.</span><span class="sxs-lookup"><span data-stu-id="d847a-110">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="d847a-111">Если решено не утверждать спланированный заказ, ему можно присвоить статус **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="d847a-111">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="d847a-112">Когда решено не утверждать спланированный заказ, ему можно присвоить статус **Утверждено**.</span><span class="sxs-lookup"><span data-stu-id="d847a-112">When you decide to firm a planned order, you can give it a status of **Approved**.</span></span> <span data-ttu-id="d847a-113">Этот статус указывает, что утверждение спланированного заказа утверждено, но заказ еще не утвержден.</span><span class="sxs-lookup"><span data-stu-id="d847a-113">This status indicates that you approve firming of the planned order, but it isn't firmed yet.</span></span>

<span data-ttu-id="d847a-114">**Примечание.** Утвержденный спланированный заказ переносится в своем текущем состоянии в следующий расчет сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="d847a-114">**Note:** An approved planned order is transferred, in its current state, to the next master planning calculation.</span></span> <span data-ttu-id="d847a-115">Спланированные заказы можно утвердить, последовательно, щелкнув **Утверждение**.</span><span class="sxs-lookup"><span data-stu-id="d847a-115">You can firm planned orders by clicking **Firm**.</span></span> <span data-ttu-id="d847a-116">Утвердить можно следующие спланированные заказы:</span><span class="sxs-lookup"><span data-stu-id="d847a-116">You can firm the following planned orders:</span></span>

-   <span data-ttu-id="d847a-117">Выбранный спланированный заказ.</span><span class="sxs-lookup"><span data-stu-id="d847a-117">The planned order that is selected.</span></span>
-   <span data-ttu-id="d847a-118">Несколько спланированных заказов.</span><span class="sxs-lookup"><span data-stu-id="d847a-118">Multiple planned orders.</span></span>
-   <span data-ttu-id="d847a-119">Спланированные заказы, которые создаются посредством развертывания на странице **Развертывание**.</span><span class="sxs-lookup"><span data-stu-id="d847a-119">Planned orders that are generated by an explosion from the **Explosion** page.</span></span> <span data-ttu-id="d847a-120">Щелкните **Спланированные заказы**, выберите спланированный заказ, а затем щелкните **Утверждение**.</span><span class="sxs-lookup"><span data-stu-id="d847a-120">Click **Planned orders**, select the planned order, and then click **Firm**.</span></span>

<span data-ttu-id="d847a-121">Когда спланированный заказ утвержден, он перемещается в раздел заказов соответствующего модуля.</span><span class="sxs-lookup"><span data-stu-id="d847a-121">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span> 

<a name="additional-resources"></a><span data-ttu-id="d847a-122">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d847a-122">Additional resources</span></span>
--------

[<span data-ttu-id="d847a-123">Сводные планы</span><span class="sxs-lookup"><span data-stu-id="d847a-123">Master plans</span></span>](master-plans.md)




