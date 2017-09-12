--- 
title: "Сообщение о завершении производственного заказа"
description: "В этой процедуре показано, как составить отчет по производственному заказу как \"завершено\"."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 17b2285e4669f1ad8fa6cea1250693a2a70c7dfa
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="report-a-production-order-as-finished"></a><span data-ttu-id="91ac9-103">Сообщение о завершении производственного заказа</span><span class="sxs-lookup"><span data-stu-id="91ac9-103">Report a production order as finished</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="91ac9-104">В этой процедуре показано, как составить отчет по производственному заказу как "завершено".</span><span class="sxs-lookup"><span data-stu-id="91ac9-104">This procedure shows how to report a production order as finished.</span></span> <span data-ttu-id="91ac9-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="91ac9-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="91ac9-106">Это шестая из семи процедур, которая объясняет жизненный цикл производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="91ac9-106">This is the sixth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="report-a-production-order-as-finished"></a><span data-ttu-id="91ac9-107">Сообщение о завершении производственного заказа</span><span class="sxs-lookup"><span data-stu-id="91ac9-107">Report a production order as finished</span></span>
1. <span data-ttu-id="91ac9-108">Перейдите в раздел "Управление производством" > "Производственные заказы" > "Все производственные заказы".</span><span class="sxs-lookup"><span data-stu-id="91ac9-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="91ac9-109">Выберите производственный заказ со статусом "Начато".</span><span class="sxs-lookup"><span data-stu-id="91ac9-109">Select a production order that has the Started status.</span></span>  
2. <span data-ttu-id="91ac9-110">В области действий щелкните "Производственный заказ".</span><span class="sxs-lookup"><span data-stu-id="91ac9-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="91ac9-111">Щелкните "Приемка".</span><span class="sxs-lookup"><span data-stu-id="91ac9-111">Click Report as finished.</span></span>
    * <span data-ttu-id="91ac9-112">На этой странице можно подтвердить количество готовой продукции как "принято".</span><span class="sxs-lookup"><span data-stu-id="91ac9-112">On this page, you can confirm the quantity of the finished product to be reported as finished.</span></span>  
4. <span data-ttu-id="91ac9-113">Перейдите на вкладку "Общие".</span><span class="sxs-lookup"><span data-stu-id="91ac9-113">Click the General tab.</span></span>
5. <span data-ttu-id="91ac9-114">Установите "Количество правильных" равным "18".</span><span class="sxs-lookup"><span data-stu-id="91ac9-114">Set Good quantity to '18'.</span></span>
6. <span data-ttu-id="91ac9-115">Установите "Количество ошибочных" равным "2".</span><span class="sxs-lookup"><span data-stu-id="91ac9-115">Set Error quantity to '2'.</span></span>
7. <span data-ttu-id="91ac9-116">В поле "Причина ошибки" выберите "Материал".</span><span class="sxs-lookup"><span data-stu-id="91ac9-116">In the Error cause field, select 'Material'.</span></span>
8. <span data-ttu-id="91ac9-117">Установите или снимите флажок "Заключительное задание".</span><span class="sxs-lookup"><span data-stu-id="91ac9-117">Select or clear the End job check box.</span></span>
9. <span data-ttu-id="91ac9-118">Установите или снимите флажок "Ошибка приема".</span><span class="sxs-lookup"><span data-stu-id="91ac9-118">Select or clear the Accept error check box.</span></span>
10. <span data-ttu-id="91ac9-119">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="91ac9-119">Click OK.</span></span>

## <a name="verify-the-report-as-finished-journal"></a><span data-ttu-id="91ac9-120">Проверка журнала "Приемка"</span><span class="sxs-lookup"><span data-stu-id="91ac9-120">Verify the Report as finished journal</span></span>
1. <span data-ttu-id="91ac9-121">В области действий щелкните "Показать".</span><span class="sxs-lookup"><span data-stu-id="91ac9-121">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="91ac9-122">Щелкните "Принятые".</span><span class="sxs-lookup"><span data-stu-id="91ac9-122">Click Reported as finished.</span></span>
3. <span data-ttu-id="91ac9-123">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="91ac9-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="91ac9-124">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="91ac9-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="91ac9-125">Выполняется разноска журнала "Приемка".</span><span class="sxs-lookup"><span data-stu-id="91ac9-125">The Report as finished journal is posted.</span></span> <span data-ttu-id="91ac9-126">Если вы хотите выполнить корректировки в журнале, можно вручную создать новый журнал, в котором можно внести изменения.</span><span class="sxs-lookup"><span data-stu-id="91ac9-126">If you want to make adjustments to the journal, you can manually create  a new journal where you can make changes.</span></span>  


