---
title: Этапы заказа на обслуживание
description: Определив стадии заказа на сервисное обслуживание и назначив их работникам, можно управлять ходом выполнения заказа на сервисное обслуживание с помощью задач, которые выполняются различными работниками в сервисной организации.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d126b68bea8d2083fcf1d08e168b9ead1511b25c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001257"
---
# <a name="service-order-stages"></a><span data-ttu-id="b2c68-103">Этапы заказа на обслуживание</span><span class="sxs-lookup"><span data-stu-id="b2c68-103">Service order stages</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b2c68-104">Можно настроить стадии заказа на сервисное обслуживание, чтобы определить задачи, которые должны быть выполнены, порядок их выполнения и работников, ответственных за их выполнение.</span><span class="sxs-lookup"><span data-stu-id="b2c68-104">You can set up stages for a service order to define the tasks that must be completed, the order in which they are completed, and the workers who are responsible for completing them.</span></span> <span data-ttu-id="b2c68-105">Определив стадии заказа на сервисное обслуживание и назначив их работникам, можно управлять ходом выполнения заказа на сервисное обслуживание с помощью задач, которые выполняются различными работниками в сервисной организации.</span><span class="sxs-lookup"><span data-stu-id="b2c68-105">By defining the stages for a service order and assigning them to workers, you can control the flow of a service order through the tasks that various people perform in the service organization.</span></span> <span data-ttu-id="b2c68-106">Последовательность стадий должна включать начальную стадию.</span><span class="sxs-lookup"><span data-stu-id="b2c68-106">The sequence of stages must include an initial stage.</span></span>

<span data-ttu-id="b2c68-107">Можно также указать действия, которые можно выполнять на каждой стадии.</span><span class="sxs-lookup"><span data-stu-id="b2c68-107">You can also define the actions that are permitted at each stage.</span></span> <span data-ttu-id="b2c68-108">Например, если снять флажок **Разнести** для всех стадий кроме финальной, заказы на сервисное облуживание будет невозможно разнести, пока не будут пройдены все стадии в последовательности.</span><span class="sxs-lookup"><span data-stu-id="b2c68-108">For example, if you clear the **Post** check box for all stages except the final stage, you prevent any service orders from being posted before the service orders are processed through the complete sequence of stages.</span></span>

## <a name="branching-in-service-order-stages"></a><span data-ttu-id="b2c68-109">Ветвление на стадиях заказа на сервисное обслуживание</span><span class="sxs-lookup"><span data-stu-id="b2c68-109">Branching in service order stages</span></span>

<span data-ttu-id="b2c68-110">При настройке стадии сервисного обслуживания можно создать несколько вариантов или ветвей, которые можно выбрать для перехода на следующую стадию сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="b2c68-110">When you set up a service stage, you can create multiple options, or branches, to select from for the next service stage.</span></span> <span data-ttu-id="b2c68-111">Все созданные ветви будут доступны для выбора по завершении начальной стадии.</span><span class="sxs-lookup"><span data-stu-id="b2c68-111">All the branches that you create are available to select from when the initial stage is completed.</span></span> <span data-ttu-id="b2c68-112">Например, назначьте стадию **Планирование** как начальную стадию.</span><span class="sxs-lookup"><span data-stu-id="b2c68-112">For example, you set up **Planning** as an initial stage.</span></span> <span data-ttu-id="b2c68-113">Создайте две стадии **В работе** и **Отмена** и выберите **Планирование** как родительский объект для них.</span><span class="sxs-lookup"><span data-stu-id="b2c68-113">You create two stages named **In process** and **Cancel**, and then select **Planning** as the parent for them.</span></span> <span data-ttu-id="b2c68-114">Назначьте стадию **Планирование** заказу на продажу.</span><span class="sxs-lookup"><span data-stu-id="b2c68-114">You assign the **Planning** stage to sales order.</span></span> <span data-ttu-id="b2c68-115">По завершении стадии планирования для заказа на продажу можно выбрать стадию **В работе**, если заказ на продажу готов к работе, или стадию **Отмена**, если заказ на продажу отменен.</span><span class="sxs-lookup"><span data-stu-id="b2c68-115">When the planning stage for the sales order is completed, you can select the **In process** stage if the sales order is ready to work on, or you can select the **Cancel** stage if the sales order is canceled.</span></span>

## <a name="see-also"></a><span data-ttu-id="b2c68-116">См. также</span><span class="sxs-lookup"><span data-stu-id="b2c68-116">See also</span></span>

[<span data-ttu-id="b2c68-117">Настройка этапов заказа на обслуживания</span><span class="sxs-lookup"><span data-stu-id="b2c68-117">Set up service order stages</span></span>](set-up-service-order-stages.md)

[<span data-ttu-id="b2c68-118">Изменение этапа заказа на обслуживание</span><span class="sxs-lookup"><span data-stu-id="b2c68-118">Change the service order stage</span></span>](change-service-order-stage.md)

  


