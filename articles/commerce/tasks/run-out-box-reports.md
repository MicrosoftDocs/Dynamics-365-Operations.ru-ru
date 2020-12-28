---
title: Создание и выполнение готовых отчетов
description: Используйте этот проводник по задаче для формирования готовых отчетов в Headquarters из различных рабочих областей и отчетов по запросам и продажам в Commerce.
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d148fa36a116860af8c44043d90759b8a2d76fb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4415269"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="17d29-103">Создание и выполнение готовых отчетов</span><span class="sxs-lookup"><span data-stu-id="17d29-103">Generate and run out of box reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17d29-104">Используйте этот проводник по задаче для формирования готовых отчетов в Headquarters из различных рабочих областей и отчетов по запросам и продажам в Commerce.</span><span class="sxs-lookup"><span data-stu-id="17d29-104">Use this task guide to run out of box reports in Headquarters from different workspaces and Inquiries & Sales reports located in Commerce.</span></span>

<span data-ttu-id="17d29-105">В качестве компании с демонстрационными данными для создания этой записи используется USRT.</span><span class="sxs-lookup"><span data-stu-id="17d29-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="17d29-106">Эта выверка предназначена для роли системного администратора.</span><span class="sxs-lookup"><span data-stu-id="17d29-106">This recording is intended for the System administrator role.</span></span>

## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="17d29-107">Запуск отчетов из рабочих областей</span><span class="sxs-lookup"><span data-stu-id="17d29-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="17d29-108">Перейдите в раздел "Retail и Commerce" > "Продукты и категории" > "Управление категориями и продуктами".</span><span class="sxs-lookup"><span data-stu-id="17d29-108">Go to Retail and Commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="17d29-109">Щелкните стрелку, чтобы развернуть или свернуть раздел "Отчеты".</span><span class="sxs-lookup"><span data-stu-id="17d29-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="17d29-110">Щелкните «Отчет "Самые популярные продукты"»</span><span class="sxs-lookup"><span data-stu-id="17d29-110">Click Top products report.</span></span>
4. <span data-ttu-id="17d29-111">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="17d29-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="17d29-112">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="17d29-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="17d29-113">В поле "Канал" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="17d29-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="17d29-114">В дереве выберите "Contoso Retail\Contoso Retail USA\Central\Houston".</span><span class="sxs-lookup"><span data-stu-id="17d29-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="17d29-115">Отображает иерархию по умолчанию организации для отчетности Commerce.</span><span class="sxs-lookup"><span data-stu-id="17d29-115">This shows the default organization hierarchy for Commerce reporting purpose.</span></span>   <span data-ttu-id="17d29-116">Перейдите в раздел "Управление организацией > Организации > Цели организационной иерархии", выберите "Отчетность Commerce" и в подразделе "Назначенные иерархии" проверьте имя иерархии, для которой установлен флажок в столбце "По умолчанию".</span><span class="sxs-lookup"><span data-stu-id="17d29-116">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="17d29-117">В демонстрационных данных (используемых для записи этой задачи) вы заметите, что "Магазины по регионам" является организационной иерархией по умолчанию для цели "Отчетность".</span><span class="sxs-lookup"><span data-stu-id="17d29-117">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
8. <span data-ttu-id="17d29-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="17d29-118">Click OK.</span></span>
9. <span data-ttu-id="17d29-119">В поле "Вид" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="17d29-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="17d29-120">В поле "По" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="17d29-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="17d29-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="17d29-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a><span data-ttu-id="17d29-122">Запуск отчетов из отчетов по запросам и продажам</span><span class="sxs-lookup"><span data-stu-id="17d29-122">Launch reports from the inquiries and sales reports</span></span>
1. <span data-ttu-id="17d29-123">Перейдите в раздел "Retail и Commerce" > "Запросы и отчеты" > "Отчеты по продажам" > "Отчет о категориях продаж".</span><span class="sxs-lookup"><span data-stu-id="17d29-123">Go to Retail and Commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="17d29-124">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="17d29-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="17d29-125">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="17d29-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="17d29-126">В поле "Канал" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="17d29-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="17d29-127">В дереве выберите "Contoso Retail\Contoso Retail USA\West\Seattle".</span><span class="sxs-lookup"><span data-stu-id="17d29-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="17d29-128">Отображает иерархию по умолчанию организации для отчетности Commerce.</span><span class="sxs-lookup"><span data-stu-id="17d29-128">This shows the default organization hierarchy for Commerce reporting purpose.</span></span> <span data-ttu-id="17d29-129">Перейдите в раздел "Управление организацией > Организации > Цели организационной иерархии", выберите "Отчетность Commerce" и в подразделе "Назначенные иерархии" проверьте имя иерархии, для которой установлен флажок в столбце "По умолчанию".</span><span class="sxs-lookup"><span data-stu-id="17d29-129">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="17d29-130">В демонстрационных данных (используемых для записи этой задачи) вы заметите, что "Магазины по регионам" является организационной иерархией по умолчанию для цели "Отчетность".</span><span class="sxs-lookup"><span data-stu-id="17d29-130">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
6. <span data-ttu-id="17d29-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="17d29-131">Click OK.</span></span>
7. <span data-ttu-id="17d29-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="17d29-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="17d29-133">Экспорт отчетов центрального офиса</span><span class="sxs-lookup"><span data-stu-id="17d29-133">Export an HQ reports</span></span>
1. <span data-ttu-id="17d29-134">Перейдите в раздел "Retail и Commerce" > "Запросы и отчеты" > "Отчеты по продажам" > "Отчет о продажах по организации".</span><span class="sxs-lookup"><span data-stu-id="17d29-134">Go to Retail and Commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="17d29-135">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="17d29-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="17d29-136">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="17d29-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="17d29-137">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="17d29-137">Click OK.</span></span>
5. <span data-ttu-id="17d29-138">Щелкните "Экспорт".</span><span class="sxs-lookup"><span data-stu-id="17d29-138">Click Export.</span></span>
6. <span data-ttu-id="17d29-139">Щелкните "PDF".</span><span class="sxs-lookup"><span data-stu-id="17d29-139">Click PDF.</span></span>

