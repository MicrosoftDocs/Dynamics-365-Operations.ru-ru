--- 
title: "Создание и выполнение готовых отчетов"
description: "Используйте этот проводник по задаче для формирования готовых отчетов в центральном офисе из различных рабочих областей и отчетов по запросам и продажам из раздела \"Розничная торговля и коммерция\"."
author: ashishmsft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: a2cde359aadd752464a0a5386c78f657db96f13b
ms.contentlocale: ru-ru
ms.lasthandoff: 01/19/2018

---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="e1199-103">Создание и выполнение готовых отчетов</span><span class="sxs-lookup"><span data-stu-id="e1199-103">Generate and run out-of-box reports</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e1199-104">Используйте этот проводник по задаче для формирования готовых отчетов в центральном офисе из различных рабочих областей и отчетов по запросам и продажам из раздела "Розничная торговля и коммерция".</span><span class="sxs-lookup"><span data-stu-id="e1199-104">Use this task guide to run out of box reports in headquarters from different workspaces and Inquiries & Sales reports located under Retail & Commerce.</span></span>



<span data-ttu-id="e1199-105">В качестве компании с демонстрационными данными для создания этой записи используется USRT.</span><span class="sxs-lookup"><span data-stu-id="e1199-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="e1199-106">Эта выверка предназначена для роли системного администратора.</span><span class="sxs-lookup"><span data-stu-id="e1199-106">This recording is intended for the System administrator role.</span></span>


## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="e1199-107">Запуск отчетов из рабочих областей</span><span class="sxs-lookup"><span data-stu-id="e1199-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="e1199-108">Перейдите в раздел "Розничная торговля и коммерция" > "Продукты и категории" > "Управление категориями и продуктами".</span><span class="sxs-lookup"><span data-stu-id="e1199-108">Go to Retail and commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="e1199-109">Щелкните стрелку, чтобы развернуть или свернуть раздел "Отчеты".</span><span class="sxs-lookup"><span data-stu-id="e1199-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="e1199-110">Щелкните «Отчет "Самые популярные продукты"»</span><span class="sxs-lookup"><span data-stu-id="e1199-110">Click Top products report.</span></span>
4. <span data-ttu-id="e1199-111">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="e1199-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="e1199-112">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="e1199-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="e1199-113">В поле "Канал" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e1199-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="e1199-114">В дереве выберите "Contoso Retail\Contoso Retail USA\Central\Houston".</span><span class="sxs-lookup"><span data-stu-id="e1199-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="e1199-115">Отображает иерархию по умолчанию организации розничной торговли для розничной отчетности.</span><span class="sxs-lookup"><span data-stu-id="e1199-115">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="e1199-116">Перейдите в раздел "Управление организацией" > "Организации" > "Цели организационной иерархии", выберите "Отчетность по розничной торговле" и в подразделе "Назначенные иерархии" проверьте имя иерархии, для которой установлен флажок в столбце "По умолчанию".</span><span class="sxs-lookup"><span data-stu-id="e1199-116">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="e1199-117">В демонстрационных данных (используемых для записи этой задачи) вы заметите, что "Розничные магазины по регионам" является организационной иерархией по умолчанию для цели "Отчетность по розничной торговле".</span><span class="sxs-lookup"><span data-stu-id="e1199-117">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
8. <span data-ttu-id="e1199-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e1199-118">Click OK.</span></span>
9. <span data-ttu-id="e1199-119">В поле "Вид" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="e1199-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="e1199-120">В поле "По" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="e1199-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="e1199-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e1199-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports-located-under-retail--commerce-app-link"></a><span data-ttu-id="e1199-122">Запустите отчеты из отчетов по запросам и продажам, доступным по ссылке приложения "Розничная торговля и коммерция".</span><span class="sxs-lookup"><span data-stu-id="e1199-122">Launch reports from the inquiries and sales reports located under Retail & Commerce app link.</span></span>
1. <span data-ttu-id="e1199-123">Перейдите в раздел "Розничная торговля и коммерция" > "Запросы и отчеты" > "Отчеты по продажам" > "Отчет о категориях продаж".</span><span class="sxs-lookup"><span data-stu-id="e1199-123">Go to Retail and commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="e1199-124">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="e1199-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="e1199-125">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="e1199-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="e1199-126">В поле "Канал" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e1199-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e1199-127">В дереве выберите "Contoso Retail\Contoso Retail USA\West\Seattle".</span><span class="sxs-lookup"><span data-stu-id="e1199-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="e1199-128">Отображает иерархию по умолчанию организации розничной торговли для розничной отчетности.</span><span class="sxs-lookup"><span data-stu-id="e1199-128">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="e1199-129">Перейдите в раздел "Управление организацией" > "Организации" > "Цели организационной иерархии", выберите "Отчетность по розничной торговле" и в подразделе "Назначенные иерархии" проверьте имя иерархии, для которой установлен флажок в столбце "По умолчанию".</span><span class="sxs-lookup"><span data-stu-id="e1199-129">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="e1199-130">В демонстрационных данных (используемых для записи этой задачи) вы заметите, что "Розничные магазины по регионам" является организационной иерархией по умолчанию для цели "Отчетность по розничной торговле".</span><span class="sxs-lookup"><span data-stu-id="e1199-130">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
6. <span data-ttu-id="e1199-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e1199-131">Click OK.</span></span>
7. <span data-ttu-id="e1199-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e1199-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="e1199-133">Экспорт отчетов центрального офиса</span><span class="sxs-lookup"><span data-stu-id="e1199-133">Export an HQ reports</span></span>
1. <span data-ttu-id="e1199-134">Перейдите в раздел "Розничная торговля и коммерция" > "Запросы и отчеты" > "Отчеты по продажам" > "Отчет о продажах по организации".</span><span class="sxs-lookup"><span data-stu-id="e1199-134">Go to Retail and commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="e1199-135">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="e1199-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="e1199-136">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="e1199-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="e1199-137">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e1199-137">Click OK.</span></span>
5. <span data-ttu-id="e1199-138">Щелкните "Экспорт".</span><span class="sxs-lookup"><span data-stu-id="e1199-138">Click Export.</span></span>
6. <span data-ttu-id="e1199-139">Щелкните "PDF".</span><span class="sxs-lookup"><span data-stu-id="e1199-139">Click PDF.</span></span>


