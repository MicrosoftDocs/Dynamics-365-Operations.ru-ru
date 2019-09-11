---
title: Создание заказов на работу
description: В этом разделе описывается, как создавать заказы на работу в модуле "Управление активами".
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b23ed3251b2f6cf4f34b423ce2f85301d6ab31a1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875856"
---
# <a name="creating-work-orders"></a><span data-ttu-id="52611-103">Создание заказов на работу</span><span class="sxs-lookup"><span data-stu-id="52611-103">Creating work orders</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="52611-104">После планирования заданий профилактического обслуживания следующим шагом будет создание заказов на работу для этих заданий.</span><span class="sxs-lookup"><span data-stu-id="52611-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="52611-105">Это делается в одном из графиков обслуживания.</span><span class="sxs-lookup"><span data-stu-id="52611-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="52611-106">Запланированные задания в графике обслуживания могут иметь различные типы ссылок:</span><span class="sxs-lookup"><span data-stu-id="52611-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="52611-107">Тип ссылки</span><span class="sxs-lookup"><span data-stu-id="52611-107">Reference type</span></span> | <span data-ttu-id="52611-108">Описание</span><span class="sxs-lookup"><span data-stu-id="52611-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52611-109">Планы обслуживания</span><span class="sxs-lookup"><span data-stu-id="52611-109">Maintenance plans</span></span>     | <span data-ttu-id="52611-110">Задание профилактического обслуживания должно основываться на типах планов обслуживания "Время" или "Счетчик".</span><span class="sxs-lookup"><span data-stu-id="52611-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="52611-111">Циклы обслуживания</span><span class="sxs-lookup"><span data-stu-id="52611-111">Maintenance rounds</span></span>    | <span data-ttu-id="52611-112">Задания профилактического обслуживания, содержащие несколько активов, требующих подобного типа обслуживания.</span><span class="sxs-lookup"><span data-stu-id="52611-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="52611-113">Запрос на обслуживание</span><span class="sxs-lookup"><span data-stu-id="52611-113">Maintenance request</span></span>   | <span data-ttu-id="52611-114">Запрос, созданный вручную для обслуживания или ремонта актива, который может быть преобразован в заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="52611-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="52611-115">Щелкните **Управление активами** > **Общее** > **Весь график обслуживания**, **Открыть строки графика обслуживания** или **Открыть пулы графиков обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="52611-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="52611-116">Выберите запланированные задания обслуживание, для которых необходимо создать заказ на работу, и щелкните **Заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="52611-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="52611-117">Общее количество часов прогноза для выбранных строк отображается в поле **Прогноз часов обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="52611-117">The total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="52611-118">В разделе **Параметры** выберите количество заказов на работу, которые должны быть созданы.</span><span class="sxs-lookup"><span data-stu-id="52611-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="52611-119">Можно создать один заказ на работу для каждой строки графика обслуживания или несколько заказов на работу на основе выбранных значений в разделе **Один заказ на работу на**.</span><span class="sxs-lookup"><span data-stu-id="52611-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="52611-120">Выберите **Тип заказа на работу**, который будет использоваться для всех создаваемых заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="52611-120">Select a **Work order type** that will be used on all the work orders you create.</span></span>

5. <span data-ttu-id="52611-121">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="52611-121">Click **OK**.</span></span> <span data-ttu-id="52611-122">Создан один или несколько заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="52611-122">One or more work orders are created.</span></span>

![Рисунок 1](media/18-preventive-maintenance.png)

