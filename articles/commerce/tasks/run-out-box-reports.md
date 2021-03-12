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
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e11bca1e6850f401f52c2ccbea1089a4e71591c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003723"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="34df0-103">Создание и выполнение готовых отчетов</span><span class="sxs-lookup"><span data-stu-id="34df0-103">Generate and run out of box reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34df0-104">Используйте этот проводник по задаче для формирования готовых отчетов в Headquarters из различных рабочих областей и отчетов по запросам и продажам в Commerce.</span><span class="sxs-lookup"><span data-stu-id="34df0-104">Use this task guide to run out of box reports in Headquarters from different workspaces and Inquiries & Sales reports located in Commerce.</span></span>

<span data-ttu-id="34df0-105">В качестве компании с демонстрационными данными для создания этой записи используется USRT.</span><span class="sxs-lookup"><span data-stu-id="34df0-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="34df0-106">Эта выверка предназначена для роли системного администратора.</span><span class="sxs-lookup"><span data-stu-id="34df0-106">This recording is intended for the System administrator role.</span></span>

## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="34df0-107">Запуск отчетов из рабочих областей</span><span class="sxs-lookup"><span data-stu-id="34df0-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="34df0-108">Перейдите в раздел "Retail и Commerce" > "Продукты и категории" > "Управление категориями и продуктами".</span><span class="sxs-lookup"><span data-stu-id="34df0-108">Go to Retail and Commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="34df0-109">Щелкните стрелку, чтобы развернуть или свернуть раздел "Отчеты".</span><span class="sxs-lookup"><span data-stu-id="34df0-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="34df0-110">Щелкните «Отчет "Самые популярные продукты"»</span><span class="sxs-lookup"><span data-stu-id="34df0-110">Click Top products report.</span></span>
4. <span data-ttu-id="34df0-111">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="34df0-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="34df0-112">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="34df0-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="34df0-113">В поле "Канал" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="34df0-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="34df0-114">В дереве выберите "Contoso Retail\Contoso Retail USA\Central\Houston".</span><span class="sxs-lookup"><span data-stu-id="34df0-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="34df0-115">Отображает иерархию по умолчанию организации для отчетности Commerce.</span><span class="sxs-lookup"><span data-stu-id="34df0-115">This shows the default organization hierarchy for Commerce reporting purpose.</span></span>   <span data-ttu-id="34df0-116">Перейдите в раздел "Управление организацией > Организации > Цели организационной иерархии", выберите "Отчетность Commerce" и в подразделе "Назначенные иерархии" проверьте имя иерархии, для которой установлен флажок в столбце "По умолчанию".</span><span class="sxs-lookup"><span data-stu-id="34df0-116">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="34df0-117">В демонстрационных данных (используемых для записи этой задачи) вы заметите, что "Магазины по регионам" является организационной иерархией по умолчанию для цели "Отчетность".</span><span class="sxs-lookup"><span data-stu-id="34df0-117">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
8. <span data-ttu-id="34df0-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="34df0-118">Click OK.</span></span>
9. <span data-ttu-id="34df0-119">В поле "Вид" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="34df0-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="34df0-120">В поле "По" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="34df0-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="34df0-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="34df0-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a><span data-ttu-id="34df0-122">Запуск отчетов из отчетов по запросам и продажам</span><span class="sxs-lookup"><span data-stu-id="34df0-122">Launch reports from the inquiries and sales reports</span></span>
1. <span data-ttu-id="34df0-123">Перейдите в раздел "Retail и Commerce" > "Запросы и отчеты" > "Отчеты по продажам" > "Отчет о категориях продаж".</span><span class="sxs-lookup"><span data-stu-id="34df0-123">Go to Retail and Commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="34df0-124">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="34df0-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="34df0-125">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="34df0-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="34df0-126">В поле "Канал" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="34df0-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="34df0-127">В дереве выберите "Contoso Retail\Contoso Retail USA\West\Seattle".</span><span class="sxs-lookup"><span data-stu-id="34df0-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="34df0-128">Отображает иерархию по умолчанию организации для отчетности Commerce.</span><span class="sxs-lookup"><span data-stu-id="34df0-128">This shows the default organization hierarchy for Commerce reporting purpose.</span></span> <span data-ttu-id="34df0-129">Перейдите в раздел "Управление организацией > Организации > Цели организационной иерархии", выберите "Отчетность Commerce" и в подразделе "Назначенные иерархии" проверьте имя иерархии, для которой установлен флажок в столбце "По умолчанию".</span><span class="sxs-lookup"><span data-stu-id="34df0-129">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="34df0-130">В демонстрационных данных (используемых для записи этой задачи) вы заметите, что "Магазины по регионам" является организационной иерархией по умолчанию для цели "Отчетность".</span><span class="sxs-lookup"><span data-stu-id="34df0-130">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
6. <span data-ttu-id="34df0-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="34df0-131">Click OK.</span></span>
7. <span data-ttu-id="34df0-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="34df0-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="34df0-133">Экспорт отчетов центрального офиса</span><span class="sxs-lookup"><span data-stu-id="34df0-133">Export an HQ reports</span></span>
1. <span data-ttu-id="34df0-134">Перейдите в раздел "Retail и Commerce" > "Запросы и отчеты" > "Отчеты по продажам" > "Отчет о продажах по организации".</span><span class="sxs-lookup"><span data-stu-id="34df0-134">Go to Retail and Commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="34df0-135">В поле "Дата начала" введите дату.</span><span class="sxs-lookup"><span data-stu-id="34df0-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="34df0-136">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="34df0-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="34df0-137">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="34df0-137">Click OK.</span></span>
5. <span data-ttu-id="34df0-138">Щелкните "Экспорт".</span><span class="sxs-lookup"><span data-stu-id="34df0-138">Click Export.</span></span>
6. <span data-ttu-id="34df0-139">Щелкните "PDF".</span><span class="sxs-lookup"><span data-stu-id="34df0-139">Click PDF.</span></span>

