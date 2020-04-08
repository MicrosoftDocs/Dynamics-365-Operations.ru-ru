---
title: Проверка хода выполнения на мобильном устройстве задания
description: В этой процедуры показано, как запустить производственное задание в регистрационной форме устройства задания и как сообщать о ходе выполнения задания.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationTouch, JmgRegistrationTouchUserConfiguration, JmgRegistrationTouchStart, JmgRegistrationTouchReportFeedback, JmgRegistrationTouchAssignedJobs, JmgRegistrationTouchBreak, JmgRegistrationTouchLeave, JmgRegistrationTouchIndirectActivity, JmgDialogForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 70cdd5aff68581af29984e88a16339de921c8ff0
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146660"
---
# <a name="report-progress-on-a-mobile-job-device"></a><span data-ttu-id="722b4-103">Проверка хода выполнения на мобильном устройстве задания</span><span class="sxs-lookup"><span data-stu-id="722b4-103">Report progress on a mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="722b4-104">В этой процедуры показано, как запустить производственное задание в регистрационной форме устройства задания и как сообщать о ходе выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="722b4-104">This procedure shows you how to start and report progress on a production job in the job device registration form.</span></span>



<span data-ttu-id="722b4-105">Для выполнения этой процедуры необходимо иметь роль администратора системы или оператора станка, связанную с учетной записью пользователя.</span><span class="sxs-lookup"><span data-stu-id="722b4-105">To be able to run this procedure you must have the System administator or Machine Operator role associated with the user account.</span></span>

1. <span data-ttu-id="722b4-106">Перейдите в раздел "Управление производством" > "Управление производством" > "Карта задания — устройство".</span><span class="sxs-lookup"><span data-stu-id="722b4-106">Go to Production control > Manufacturing execution > Job card device.</span></span>
2. <span data-ttu-id="722b4-107">В поле WorkerTextField введите значок работника.</span><span class="sxs-lookup"><span data-stu-id="722b4-107">In the WorkerTextField field, enter the badge of a worker.</span></span> <span data-ttu-id="722b4-108">В демонстрационных данных USMF для пользователя Christina Portra введите "123".</span><span class="sxs-lookup"><span data-stu-id="722b4-108">In the USMF demo data type '123' for Christina Portra..</span></span>
3. <span data-ttu-id="722b4-109">Щелкните "Войти в систему".</span><span class="sxs-lookup"><span data-stu-id="722b4-109">Click Log in.</span></span>
4. <span data-ttu-id="722b4-110">Нажмите кнопку "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="722b4-110">Click the Filter button.</span></span>
5. <span data-ttu-id="722b4-111">Установите или снимите флажок "Применить фильтр конфигурации".</span><span class="sxs-lookup"><span data-stu-id="722b4-111">Check or uncheck the Apply configuration filter check box.</span></span> <span data-ttu-id="722b4-112">Если установить фильтр, можно использовать производственное подразделение 110 в USMF.</span><span class="sxs-lookup"><span data-stu-id="722b4-112">If you set a filter you can use production unit 110 in USMF.</span></span>
6. <span data-ttu-id="722b4-113">В поле "Производственное подразделение" выберите группу ресурсов, над производственными заданиями которой может работать работник.</span><span class="sxs-lookup"><span data-stu-id="722b4-113">In the Production unit field, select the ressource group for which production jobs the worker can work on.</span></span>
7. <span data-ttu-id="722b4-114">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="722b4-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="722b4-115">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="722b4-115">Click OK.</span></span>
9. <span data-ttu-id="722b4-116">Нажмите кнопку "Запустить задание".</span><span class="sxs-lookup"><span data-stu-id="722b4-116">Click the Start job button.</span></span>
10. <span data-ttu-id="722b4-117">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="722b4-117">Click OK.</span></span>
11. <span data-ttu-id="722b4-118">Нажмите кнопку "Проверить ход выполнения".</span><span class="sxs-lookup"><span data-stu-id="722b4-118">Click the Report progress button.</span></span>
12. <span data-ttu-id="722b4-119">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="722b4-119">Click OK.</span></span>
13. <span data-ttu-id="722b4-120">Нажмите кнопку "Следующее задание".</span><span class="sxs-lookup"><span data-stu-id="722b4-120">Click the Next job button.</span></span>
14. <span data-ttu-id="722b4-121">Нажмите "Распределено" для просмотра обзора всех производственных заданий.</span><span class="sxs-lookup"><span data-stu-id="722b4-121">Click the Assigned to see an overview of all production jobs button.</span></span>
15. <span data-ttu-id="722b4-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="722b4-122">Close the page.</span></span>
16. <span data-ttu-id="722b4-123">Нажмите кнопку "Прерывание".</span><span class="sxs-lookup"><span data-stu-id="722b4-123">Click the Break button.</span></span>
17. <span data-ttu-id="722b4-124">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="722b4-124">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="722b4-125">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="722b4-125">Click OK.</span></span>
19. <span data-ttu-id="722b4-126">Нажмите кнопку "Уход".</span><span class="sxs-lookup"><span data-stu-id="722b4-126">Click the Leaving button.</span></span>
20. <span data-ttu-id="722b4-127">Выберите команду выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="722b4-127">Select to log out.</span></span>
21. <span data-ttu-id="722b4-128">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="722b4-128">Click OK.</span></span>
22. <span data-ttu-id="722b4-129">В поле WorkerTextField снова войдите в систему.</span><span class="sxs-lookup"><span data-stu-id="722b4-129">In the WorkerTextField field, log in again.</span></span> <span data-ttu-id="722b4-130">Можно выбрать работника "123" в демонстрационных данных USMF.</span><span class="sxs-lookup"><span data-stu-id="722b4-130">You can select worker '123' in USMF demo data.</span></span>
23. <span data-ttu-id="722b4-131">Щелкните "Войти в систему".</span><span class="sxs-lookup"><span data-stu-id="722b4-131">Click Log in.</span></span>
24. <span data-ttu-id="722b4-132">Нажмите "Остановить прерывание".</span><span class="sxs-lookup"><span data-stu-id="722b4-132">Click Stop break.</span></span>
25. <span data-ttu-id="722b4-133">Нажмите кнопку "Действие".</span><span class="sxs-lookup"><span data-stu-id="722b4-133">Click the Activity button.</span></span>
26. <span data-ttu-id="722b4-134">Щелкните "Отмена".</span><span class="sxs-lookup"><span data-stu-id="722b4-134">Click Cancel.</span></span>
27. <span data-ttu-id="722b4-135">Нажмите кнопку "Уход".</span><span class="sxs-lookup"><span data-stu-id="722b4-135">Click the Leaving button.</span></span>
28. <span data-ttu-id="722b4-136">Выберите команду времени ухода.</span><span class="sxs-lookup"><span data-stu-id="722b4-136">Select to clock out.</span></span>
29. <span data-ttu-id="722b4-137">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="722b4-137">Click OK.</span></span>
30. <span data-ttu-id="722b4-138">Выберите причину, по которой вы уходите раньше.</span><span class="sxs-lookup"><span data-stu-id="722b4-138">Select a reason why you are clocking out early.</span></span>

