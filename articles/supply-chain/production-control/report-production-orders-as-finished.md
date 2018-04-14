---
title: "Включение производственных заказов в отчет как завершенных"
description: "Приемка является стадией производства. На этом этапе готовая продукция принимается и перемещается из производственного заказа в запасы."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fa40733e3f1310869ead8b0ac774bb621637e250
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---

# <a name="report-production-orders-as-finished"></a><span data-ttu-id="df7eb-104">Включение производственных заказов в отчет как завершенных</span><span class="sxs-lookup"><span data-stu-id="df7eb-104">Report production orders as finished</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="df7eb-105">Приемка является стадией производства.</span><span class="sxs-lookup"><span data-stu-id="df7eb-105">Report as finished is a production stage.</span></span> <span data-ttu-id="df7eb-106">На этом этапе готовая продукция принимается и перемещается из производственного заказа в запасы.</span><span class="sxs-lookup"><span data-stu-id="df7eb-106">At this stage, a finished product is reported and moved from the production order to the inventory.</span></span>

<span data-ttu-id="df7eb-107">Когда количество готовой продукции для заказа на производство становится завершенным, оно обновляется до статуса "В наличии" в запасах.</span><span class="sxs-lookup"><span data-stu-id="df7eb-107">When a quantity of the finished goods is reported as finished on a production order it is updated as on-hand in the inventory.</span></span> <span data-ttu-id="df7eb-108">Частичные количества первоначально запланированного количества заказа могут быть отмечены как законченные.</span><span class="sxs-lookup"><span data-stu-id="df7eb-108">Partial quantities of the originally planned order quantity can be reported as finished.</span></span> <span data-ttu-id="df7eb-109">При сообщении о завершенных количествах также возможно сообщить количества с ошибками со связанной причиной ошибки.</span><span class="sxs-lookup"><span data-stu-id="df7eb-109">It is also possible to report error quantities with an associated error reason when reporting quantities as finished.</span></span> <span data-ttu-id="df7eb-110">Когда производственный заказ достигает этапа "Принято", это означает, что больше никакое количество не будет показываться в производственном заказе.</span><span class="sxs-lookup"><span data-stu-id="df7eb-110">When the production order reach the stage Reported as finished it indicates that no more quantity is going to be reported at the production  order.</span></span>
<span data-ttu-id="df7eb-111">Следующие характеристики также связаны с процессом **Приемка**:</span><span class="sxs-lookup"><span data-stu-id="df7eb-111">The following characteristics are also associated with the **Report as finished** process:</span></span>
-   <span data-ttu-id="df7eb-112">Возможно настроить потребление сырья и время, которое пропорционально сообщенному количеству (очистка назад)</span><span class="sxs-lookup"><span data-stu-id="df7eb-112">It is possible to set up consumption of raw material and time that are proportional to the reported quantity (back-flushing)</span></span>
-   <span data-ttu-id="df7eb-113">Работа по размещению может быть создана для номенклатур, для которых включены процессы склада.</span><span class="sxs-lookup"><span data-stu-id="df7eb-113">Put-away work can be generated for items that are enabled for warehouse processes.</span></span>
-   <span data-ttu-id="df7eb-114">Можно настроить, чтобы сведения о запланированных или нормативных затратах готовых товаров сообщались на счета ГК.</span><span class="sxs-lookup"><span data-stu-id="df7eb-114">The planned or standard cost value of the finished goods can be set up to be reported to ledger accounts.</span></span>
-   <span data-ttu-id="df7eb-115">Заказ для контроля качества может быть создан для сообщенного количества, основанного на настройке ассоциации качества.</span><span class="sxs-lookup"><span data-stu-id="df7eb-115">A quality order can be created for the reported quantity based on the setup of a quality association.</span></span>

<span data-ttu-id="df7eb-116">Количество сообщается в местонахождение вывода.</span><span class="sxs-lookup"><span data-stu-id="df7eb-116">The quantity is reported to the output location.</span></span> <span data-ttu-id="df7eb-117">После этого создается работа склада, чтобы переместить это количество из положения вывода в конечный пункт, определенный директивой местонахождения для отложенной работы.</span><span class="sxs-lookup"><span data-stu-id="df7eb-117">Warehouse work is then generated to move the quantity from the output location to its final destination defined by the location directive for the put-away work.</span></span>

-   <span data-ttu-id="df7eb-118">Заказ для контроля качества можно создать, когда производственный заказ отмечается как завершенный, если настроена ассоциация качества.</span><span class="sxs-lookup"><span data-stu-id="df7eb-118">A quality order can be created when a production order is reported as finished if a quality association has been set up.</span></span>

## <a name="set-a-production-order-to-reporting-as-finished"></a><span data-ttu-id="df7eb-119">Установка приемки для производственного заказа</span><span class="sxs-lookup"><span data-stu-id="df7eb-119">Set a production order to Reporting as finished</span></span>
<span data-ttu-id="df7eb-120">Можно задать статус производственного заказа **Приемка** с помощью стандартной функции обновления производственного заказа или с помощью журналов маршрута и карты задания, а также с помощью журнала **Приемка**.</span><span class="sxs-lookup"><span data-stu-id="df7eb-120">You can set a production order to **Report as finished** through the standard production order update function, or through the route and job card journals, or through the journal **Report as finished**.</span></span> <span data-ttu-id="df7eb-121">Вы можете также обновить этап до статуса **Приемка** с помощью терминала карточек заданий или страниц устройства карточек задания, когда вы сообщаете о последнем задании производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="df7eb-121">You can also update the stage to **Report as finished** through the job card terminal and job card device pages, when you report on the last job of the production order.</span></span> <span data-ttu-id="df7eb-122">В конце концов, вы можете включить параметр **Приемка** как процесс для решения с ручным складским прибором.</span><span class="sxs-lookup"><span data-stu-id="df7eb-122">Finally, you can enable the **Report as finished** option as a process for the handheld warehouse device solution.</span></span>  




