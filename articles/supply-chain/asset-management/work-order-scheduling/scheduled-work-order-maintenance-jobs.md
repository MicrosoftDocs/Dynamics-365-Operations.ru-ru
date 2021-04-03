---
title: Запланированные задания обслуживания заказа на работу
description: В этом разделе описываются запланированные задания обслуживания для заказа на работу в модуле "Управление активами".
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c8cea81d27f1671b54c4947b05bbc387667247c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263814"
---
# <a name="scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="f8b6e-103">Запланированные задания обслуживания заказа на работу</span><span class="sxs-lookup"><span data-stu-id="f8b6e-103">Scheduled work order maintenance jobs</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f8b6e-104">Страница **Запланированные задания обслуживания для заказа на работу** отображает обзор заказов на работу, назначенных ресурсу.</span><span class="sxs-lookup"><span data-stu-id="f8b6e-104">The **Scheduled work order maintenance jobs** page shows an overview of the work orders allocated to a resource.</span></span> <span data-ttu-id="f8b6e-105">Заказы на работу с использованием типов ресурсов "Управление персоналом", "Инструмент" и "Станок" отображаются.</span><span class="sxs-lookup"><span data-stu-id="f8b6e-105">Work orders using resource types "Human resources", "Tool", and "Machine" are shown.</span></span> <span data-ttu-id="f8b6e-106">Например, если специалист по обслуживанию сообщил, что заболел, вы можете использовать эту страницу, чтобы быстро найти заказы на работу, назначенные этому работнику, а затем выделить другого специалиста по обслуживанию для этого задания.</span><span class="sxs-lookup"><span data-stu-id="f8b6e-106">For example, if a maintenance worker calls in sick, you can use this page to quickly find work orders allocated to the worker, and then allocate another maintenance worker to the job.</span></span>

## <a name="view-scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="f8b6e-107">Просмотр запланированных заданий обслуживания для заказа на работу</span><span class="sxs-lookup"><span data-stu-id="f8b6e-107">View scheduled work order maintenance jobs</span></span>

1. <span data-ttu-id="f8b6e-108">Щелкните **Управление активами** > **Общее** > **Заказы на работу** > **Запланированные задания обслуживания для заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="f8b6e-108">Click **Asset management** > **Common** > **Work orders** > **Scheduled work order maintenance jobs**.</span></span> <span data-ttu-id="f8b6e-109">Отображается список всех заказов на работу, которые установлены в состояние жизненного цикла заказа на работу "Запланировано" или "Выполняется".</span><span class="sxs-lookup"><span data-stu-id="f8b6e-109">You see a list of all work orders set to work order lifecycle state "Scheduled" or "In progress".</span></span>

2. <span data-ttu-id="f8b6e-110">Можно отсортировать список, например, по специалистам по обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="f8b6e-110">You can sort the list, for example, by maintenance worker.</span></span> <span data-ttu-id="f8b6e-111">Можно также использовать фильтр, чтобы ограничить список для показа заказов на работу, назначенных конкретному ресурсу или специалисту по обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="f8b6e-111">You can also use the filter to limit the list to display work orders allocated to a specific resource or maintenance worker.</span></span>

3. <span data-ttu-id="f8b6e-112">Можно просмотреть примечания по заказу на работу и, если это необходимо, добавить новые примечания, выбрав задание заказа на работу и щелкнув **Примечания**.</span><span class="sxs-lookup"><span data-stu-id="f8b6e-112">You can see notes on the work order and, if required, add new notes by selecting the work order job, and then click **Notes**.</span></span>

4. <span data-ttu-id="f8b6e-113">Если требуется назначить одного специалиста по обслуживанию для заказа на работу, выберите заказ на работу и щелкните **Заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="f8b6e-113">If you want to allocate one maintenance worker to a work order, select the work order, and then click **Work order**.</span></span>

5. <span data-ttu-id="f8b6e-114">Будет открыта страница **Заказ на работу**.</span><span class="sxs-lookup"><span data-stu-id="f8b6e-114">The **Work order** page opens.</span></span> <span data-ttu-id="f8b6e-115">Щелкните **Подготовить к отправке**, чтобы запланировать заказ на работу конкретному специалисту по обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="f8b6e-115">Click **Dispatch** to schedule the work order to a specific maintenance worker.</span></span>

>[!NOTE]
><span data-ttu-id="f8b6e-116">Более подробную информацию о планировании нескольких заказов на работу или одного заказа на работу см. в разделах [Запланировать заказы на работу](../work-order-scheduling/schedule-work-orders.md) и [Отправка заказа на работу](../work-order-scheduling/dispatch-work-order.md).</span><span class="sxs-lookup"><span data-stu-id="f8b6e-116">Read more about scheduling several work orders or one work order in [Schedule work orders](../work-order-scheduling/schedule-work-orders.md) and [Dispatch work order](../work-order-scheduling/dispatch-work-order.md).</span></span>

<span data-ttu-id="f8b6e-117">На следующем снимке экрана показан пример страницы **Запланированные задания обслуживания для заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="f8b6e-117">The following screenshot shows an example of the **Scheduled work order maintenance jobs** page.</span></span>

![Рисунок 1](media/07-work-order-scheduling.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]