---
title: Запланированные задания обслуживания заказа на работу
description: В этом разделе описываются запланированные задания обслуживания для заказа на работу в модуле "Управление активами".
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4b3cc32d6ff263967c1ee843702c28968219ac33
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887190"
---
# <a name="scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="197e1-103">Запланированные задания обслуживания заказа на работу</span><span class="sxs-lookup"><span data-stu-id="197e1-103">Scheduled work order maintenance jobs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="197e1-104">Страница **Запланированные задания обслуживания для заказа на работу** используется для получения обзора заказов на работу, назначенных ресурсу.</span><span class="sxs-lookup"><span data-stu-id="197e1-104">The **Scheduled work order maintenance jobs** page is used to get an overview of the work orders allocated to a resource.</span></span> <span data-ttu-id="197e1-105">Заказы на работу с использованием типов ресурсов "Управление персоналом", "Инструмент" и "Станок" отображаются в списке.</span><span class="sxs-lookup"><span data-stu-id="197e1-105">Work orders using resource types "Human resources", "Tool", and "Machine" are shown in the list.</span></span> <span data-ttu-id="197e1-106">Этот список можно использовать для обзора заказов на работу, назначенных конкретному ресурсу.</span><span class="sxs-lookup"><span data-stu-id="197e1-106">The list can be used to get an overview of work orders allocated to a specific resource.</span></span> <span data-ttu-id="197e1-107">Кроме того, его можно использовать для быстрого поиска заказа на работу, назначенного специалисту по обслуживанию, который, например, в это утро сообщил о больничном, а затем быстро выделить другого специалиста по обслуживанию для этого задания.</span><span class="sxs-lookup"><span data-stu-id="197e1-107">You can also use it to quickly find a work order allocated to a maintenance worker who, for example, called in sick this morning, and then quickly allocate another maintenance worker to the job.</span></span>

## <a name="view-scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="197e1-108">Просмотр запланированных заданий обслуживания для заказа на работу</span><span class="sxs-lookup"><span data-stu-id="197e1-108">View scheduled work order maintenance jobs</span></span>

1. <span data-ttu-id="197e1-109">Щелкните **Управление активами** > **Общее** > **Заказы на работу** > **Запланированные задания обслуживания для заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="197e1-109">Click **Asset management** > **Common** > **Work orders** > **Scheduled work order maintenance jobs**.</span></span> <span data-ttu-id="197e1-110">Отображается список всех заказов на работу, которые установлены в состояние жизненного цикла заказа на работу "Запланировано" или "Выполняется".</span><span class="sxs-lookup"><span data-stu-id="197e1-110">You see a list of all work orders set to work order lifecycle state "Scheduled" or "In progress".</span></span>

2. <span data-ttu-id="197e1-111">Можно отсортировать список, например, по специалистам по обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="197e1-111">You can sort the list, for example, by maintenance worker.</span></span> <span data-ttu-id="197e1-112">Можно также использовать фильтр, чтобы ограничить список для показа заказов на работу, назначенных конкретному ресурсу или специалисту по обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="197e1-112">You can also use the filter to limit the list to display work orders allocated to a specific resource or maintenance worker.</span></span>

3. <span data-ttu-id="197e1-113">Можно просмотреть примечания по заказу на работу и, если это необходимо, добавить новые примечания, выбрав задание заказа на работу в списке и щелкнув **Примечания**.</span><span class="sxs-lookup"><span data-stu-id="197e1-113">You can see notes on the work order and, if required, add new notes by selecting the work order job in the list and clicking **Notes**.</span></span>

4. <span data-ttu-id="197e1-114">Если требуется назначить одного специалиста по обслуживанию для заказа на работу, выберите заказ на работу в списке и щелкните **Заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="197e1-114">If you want to allocate one maintenance worker to a work order, select the work order in the list, and click **Work order**.</span></span>

5. <span data-ttu-id="197e1-115">Будет открыта страница **Заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="197e1-115">The **Work order** page opens.</span></span> <span data-ttu-id="197e1-116">Щелкните **Подготовить к отправке**, чтобы запланировать заказ на работу конкретному специалисту по обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="197e1-116">Click **Dispatch** to schedule the work order to a specific maintenance worker.</span></span>

>[!NOTE]
><span data-ttu-id="197e1-117">Более подробную информацию о планировании нескольких заказов на работу или одного заказа на работу см. в разделах [Запланировать заказы на работу](../work-order-scheduling/schedule-work-orders.md) и [Отправка заказа на работу](../work-order-scheduling/dispatch-work-order.md).</span><span class="sxs-lookup"><span data-stu-id="197e1-117">Read more about scheduling several work orders or one work order in [Schedule work orders](../work-order-scheduling/schedule-work-orders.md) and [Dispatch work order](../work-order-scheduling/dispatch-work-order.md).</span></span>

<span data-ttu-id="197e1-118">На следующем рисунке показан пример страницы **Запланированные задания обслуживания для заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="197e1-118">The figure below shows an example of the **Scheduled work order maintenance jobs** page.</span></span>

![Рисунок 1](media/07-work-order-scheduling.png)
