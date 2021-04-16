---
title: Создание и выполнение готовых отчетов
description: Используйте этот проводник по задаче для формирования готовых отчетов в Headquarters из различных рабочих областей и отчетов по запросам и продажам в Commerce.
author: ashishmsft
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db75b09f1ae1f83a88a5e5eaef0c8c1b8eab5901
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804145"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="657a5-103">Создание и выполнение готовых отчетов</span><span class="sxs-lookup"><span data-stu-id="657a5-103">Generate and run out of box reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="657a5-104">Используйте этот проводник по задаче для формирования готовых отчетов в Headquarters из различных рабочих областей и отчетов по запросам и продажам в Commerce.</span><span class="sxs-lookup"><span data-stu-id="657a5-104">Use this task guide to run out of box reports in Headquarters from different workspaces and Inquiries & Sales reports located in Commerce.</span></span>

<span data-ttu-id="657a5-105">В качестве компании с демонстрационными данными для создания этой записи используется USRT.</span><span class="sxs-lookup"><span data-stu-id="657a5-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="657a5-106">Эта выверка предназначена для роли системного администратора.</span><span class="sxs-lookup"><span data-stu-id="657a5-106">This recording is intended for the System administrator role.</span></span>

## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="657a5-107">Запуск отчетов из рабочих областей</span><span class="sxs-lookup"><span data-stu-id="657a5-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="657a5-108">Перейдите в раздел "Retail и Commerce" > "Продукты и категории" > "Управление категориями и продуктами".</span><span class="sxs-lookup"><span data-stu-id="657a5-108">Go to Retail and Commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="657a5-109">Щелкните стрелку, чтобы развернуть или свернуть раздел "Отчеты".</span><span class="sxs-lookup"><span data-stu-id="657a5-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="657a5-110">Щелкните «Отчет "Самые популярные продукты"»</span><span class="sxs-lookup"><span data-stu-id="657a5-110">Click Top products report.</span></span>
4. <span data-ttu-id="657a5-111">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="657a5-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="657a5-112">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="657a5-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="657a5-113">В поле "Канал" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="657a5-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="657a5-114">В дереве выберите "Contoso Retail\Contoso Retail USA\Central\Houston".</span><span class="sxs-lookup"><span data-stu-id="657a5-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="657a5-115">Отображает иерархию по умолчанию организации для отчетности Commerce.</span><span class="sxs-lookup"><span data-stu-id="657a5-115">This shows the default organization hierarchy for Commerce reporting purpose.</span></span>   <span data-ttu-id="657a5-116">Перейдите в раздел "Управление организацией > Организации > Цели организационной иерархии", выберите "Отчетность Commerce" и в подразделе "Назначенные иерархии" проверьте имя иерархии, для которой установлен флажок в столбце "По умолчанию".</span><span class="sxs-lookup"><span data-stu-id="657a5-116">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="657a5-117">В демонстрационных данных (используемых для записи этой задачи) вы заметите, что "Магазины по регионам" является организационной иерархией по умолчанию для цели "Отчетность".</span><span class="sxs-lookup"><span data-stu-id="657a5-117">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
8. <span data-ttu-id="657a5-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="657a5-118">Click OK.</span></span>
9. <span data-ttu-id="657a5-119">В поле "Вид" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="657a5-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="657a5-120">В поле "По" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="657a5-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="657a5-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="657a5-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a><span data-ttu-id="657a5-122">Запуск отчетов из отчетов по запросам и продажам</span><span class="sxs-lookup"><span data-stu-id="657a5-122">Launch reports from the inquiries and sales reports</span></span>
1. <span data-ttu-id="657a5-123">Перейдите в раздел "Retail и Commerce" > "Запросы и отчеты" > "Отчеты по продажам" > "Отчет о категориях продаж".</span><span class="sxs-lookup"><span data-stu-id="657a5-123">Go to Retail and Commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="657a5-124">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="657a5-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="657a5-125">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="657a5-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="657a5-126">В поле "Канал" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="657a5-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="657a5-127">В дереве выберите "Contoso Retail\Contoso Retail USA\West\Seattle".</span><span class="sxs-lookup"><span data-stu-id="657a5-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="657a5-128">Отображает иерархию по умолчанию организации для отчетности Commerce.</span><span class="sxs-lookup"><span data-stu-id="657a5-128">This shows the default organization hierarchy for Commerce reporting purpose.</span></span> <span data-ttu-id="657a5-129">Перейдите в раздел "Управление организацией > Организации > Цели организационной иерархии", выберите "Отчетность Commerce" и в подразделе "Назначенные иерархии" проверьте имя иерархии, для которой установлен флажок в столбце "По умолчанию".</span><span class="sxs-lookup"><span data-stu-id="657a5-129">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="657a5-130">В демонстрационных данных (используемых для записи этой задачи) вы заметите, что "Магазины по регионам" является организационной иерархией по умолчанию для цели "Отчетность".</span><span class="sxs-lookup"><span data-stu-id="657a5-130">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
6. <span data-ttu-id="657a5-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="657a5-131">Click OK.</span></span>
7. <span data-ttu-id="657a5-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="657a5-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="657a5-133">Экспорт отчетов центрального офиса</span><span class="sxs-lookup"><span data-stu-id="657a5-133">Export an HQ reports</span></span>
1. <span data-ttu-id="657a5-134">Перейдите в раздел "Retail и Commerce" > "Запросы и отчеты" > "Отчеты по продажам" > "Отчет о продажах по организации".</span><span class="sxs-lookup"><span data-stu-id="657a5-134">Go to Retail and Commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="657a5-135">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="657a5-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="657a5-136">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="657a5-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="657a5-137">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="657a5-137">Click OK.</span></span>
5. <span data-ttu-id="657a5-138">Щелкните "Экспорт".</span><span class="sxs-lookup"><span data-stu-id="657a5-138">Click Export.</span></span>
6. <span data-ttu-id="657a5-139">Щелкните "PDF".</span><span class="sxs-lookup"><span data-stu-id="657a5-139">Click PDF.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]