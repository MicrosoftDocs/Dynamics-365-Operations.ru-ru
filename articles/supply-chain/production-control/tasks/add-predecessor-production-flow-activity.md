--- 
title: "Добавление предшествующего элемента к мероприятию производственного потока"
description: "В версии производственного потока все мероприятия должны быть последовательными."
author: cvocph
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: bab99189fdd1980600612aaca9c6eb70cd976e2d
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a><span data-ttu-id="c871f-103">Добавление предшествующего элемента к мероприятию производственного потока</span><span class="sxs-lookup"><span data-stu-id="c871f-103">Add a predecessor to a production flow activity</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c871f-104">В версии производственного потока все мероприятия должны быть последовательными.</span><span class="sxs-lookup"><span data-stu-id="c871f-104">In a production flow version, all activities must be sequenced.</span></span> <span data-ttu-id="c871f-105">Мероприятие может иметь один или несколько предыдущих или последующих мероприятий.</span><span class="sxs-lookup"><span data-stu-id="c871f-105">An activity can have one or multiple predecessors or successors.</span></span> 

<span data-ttu-id="c871f-106">Эта процедура демонстрирует порядок связывания предшествующего элемента с мероприятием.</span><span class="sxs-lookup"><span data-stu-id="c871f-106">This procedure shows how to associate a predecessor to an activity.</span></span> 

<span data-ttu-id="c871f-107">Для выполнения этой задачи требуется производственный поток, который имеет черновую версию, содержащую хотя бы два мероприятия, которые можно подключить.</span><span class="sxs-lookup"><span data-stu-id="c871f-107">To perform this task, you need a production flow that has the Draft version with at least two activities that can be connected.</span></span> 

<span data-ttu-id="c871f-108">Дополнительные сведения см. в официальном документе "Производственные потоки и мероприятия в бережливом производстве".</span><span class="sxs-lookup"><span data-stu-id="c871f-108">To learn more, read the white paper "Production flows and activities in lean manufacturing."</span></span>


## <a name="find-the-production-flow-and-version"></a><span data-ttu-id="c871f-109">Поиск производственного потока и версии</span><span class="sxs-lookup"><span data-stu-id="c871f-109">Find the production flow and version</span></span>
1. <span data-ttu-id="c871f-110">Перейдите в раздел "Управление производством" > "Настройка" > "Поток бережливого производства" > "Производственные потоки".</span><span class="sxs-lookup"><span data-stu-id="c871f-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="c871f-111">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c871f-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c871f-112">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c871f-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c871f-113">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c871f-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c871f-114">Щелкните "Мероприятия".</span><span class="sxs-lookup"><span data-stu-id="c871f-114">Click Activities.</span></span>

## <a name="select-an-activity-and-add-a-predecessor"></a><span data-ttu-id="c871f-115">Выберите мероприятие и добавьте предшествующий элемент</span><span class="sxs-lookup"><span data-stu-id="c871f-115">Select an activity and add a predecessor</span></span>
1. <span data-ttu-id="c871f-116">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c871f-116">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="c871f-117">Щелкните "Добавить предшествующий элемент".</span><span class="sxs-lookup"><span data-stu-id="c871f-117">Click Add predecessor.</span></span>
3. <span data-ttu-id="c871f-118">В поле "Мероприятие" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c871f-118">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="c871f-119">В поле "Коэффициент времени цикла" введите число.</span><span class="sxs-lookup"><span data-stu-id="c871f-119">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="c871f-120">Коэффициент времени цикла по умолчанию для связи мероприятий равен 1.</span><span class="sxs-lookup"><span data-stu-id="c871f-120">The default cycle time ratio of an activity relation is 1.</span></span> <span data-ttu-id="c871f-121">Это предполагает, что оба мероприятия выполняются в одном темпе или с одинаковым временем такта.</span><span class="sxs-lookup"><span data-stu-id="c871f-121">This assumes that both activities run at the same pace or takt time.</span></span> <span data-ttu-id="c871f-122">Если предшествующий элемент работает в более высоком темпе (с меньшим временем такта), коэффициент должен быть меньше 1, если предшествующий элемент работает в более медленном темпе (с большим временем такта) коэффициент времени цикла будет больше 1.</span><span class="sxs-lookup"><span data-stu-id="c871f-122">If the predecessor runs at a higher pace (lower takt time), the ratio should be lower than 1, if the predecessor runs at a slower pace (higher takt time) the cycle time ratio is greater than 1.</span></span>  
5. <span data-ttu-id="c871f-123">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c871f-123">Click OK.</span></span>


