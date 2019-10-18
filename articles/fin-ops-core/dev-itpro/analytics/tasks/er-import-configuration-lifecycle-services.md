---
title: Электронная отчетность — Импорт конфигурации из Lifecycle Services
description: В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может импортировать новую конфигурацию электронной отчетности из Microsoft Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0830707885e8ed52581aa789df0279d78e3a9c10
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184838"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="6b7b2-103">Электронная отчетность — Импорт конфигурации из Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="6b7b2-103">ER Import a configuration from Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6b7b2-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может импортировать новую конфигурацию электронной отчетности из Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6b7b2-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="6b7b2-105">В этом примере вам предстоит выбрать желаемую версию конфигурации электронной отчетности для демонстрационной компании Litware, Inc. Эти шаги можно выполнить в любой компании, поскольку конфигурации электронной отчетности являются общими для всех компаний.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="6b7b2-106">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Отправка конфигурации электронной отчетности в Lifecycle Services".</span><span class="sxs-lookup"><span data-stu-id="6b7b2-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="6b7b2-107">Доступ к LCS также является обязательным условием для выполнения следующих шагов.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="6b7b2-108">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="6b7b2-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="6b7b2-109">Щелкните "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="6b7b2-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="6b7b2-110">Удаление общей версии конфигурации модели данных</span><span class="sxs-lookup"><span data-stu-id="6b7b2-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="6b7b2-111">В дереве выберите "Пример конфигурации модели".</span><span class="sxs-lookup"><span data-stu-id="6b7b2-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="6b7b2-112">Первая версия конфигурации примера модели данных создана и опубликована в LCS во время выполнения процедуры "Отправка конфигурации электронной отчетности в Lifecycle Services".</span><span class="sxs-lookup"><span data-stu-id="6b7b2-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="6b7b2-113">В этой процедуре мы удалим эту версию конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="6b7b2-114">Эта версия примера конфигурации модели данных будет позднее импортирована из LCS.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="6b7b2-115">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6b7b2-116">Выберите версию этой конфигурации со статусом "Общие".</span><span class="sxs-lookup"><span data-stu-id="6b7b2-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="6b7b2-117">Этот статус указывает, что конфигурация была опубликована в LCS.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="6b7b2-118">Щелкните "Изменить статус".</span><span class="sxs-lookup"><span data-stu-id="6b7b2-118">Click Change status.</span></span>
4. <span data-ttu-id="6b7b2-119">Щелкните "Отменить".</span><span class="sxs-lookup"><span data-stu-id="6b7b2-119">Click Discontinue.</span></span>
    * <span data-ttu-id="6b7b2-120">Измените статус выбранной версии с "Общее" на "Отменено", чтобы сделать ее доступной для удаления.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="6b7b2-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="6b7b2-121">Click OK.</span></span>
6. <span data-ttu-id="6b7b2-122">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6b7b2-123">Выберите версию этой конфигурации со статусом "Отменено".</span><span class="sxs-lookup"><span data-stu-id="6b7b2-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="6b7b2-124">Нажмите кнопку Удалить.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-124">Click Delete.</span></span>
8. <span data-ttu-id="6b7b2-125">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-125">Click Yes.</span></span>
    * <span data-ttu-id="6b7b2-126">Обратите внимание, что доступна только черновая версия 2 выбранной конфигурации модели данных.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="6b7b2-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="6b7b2-128">Импорт общей версии конфигурации модели данных из LCS</span><span class="sxs-lookup"><span data-stu-id="6b7b2-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="6b7b2-129">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6b7b2-130">Откройте список репозиториев для Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="6b7b2-131">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-131">configuration provider.</span></span>  
2. <span data-ttu-id="6b7b2-132">Щелкните "Репозитории".</span><span class="sxs-lookup"><span data-stu-id="6b7b2-132">Click Repositories.</span></span>
3. <span data-ttu-id="6b7b2-133">Щелкните Открыть.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-133">Click Open.</span></span>
    * <span data-ttu-id="6b7b2-134">Выберите репозиторий LCS и откройте его.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="6b7b2-135">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6b7b2-136">Выберите первую версию примере конфигурации модели в списке версий.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="6b7b2-137">Нажмите кнопку Импорт.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-137">Click Import.</span></span>
6. <span data-ttu-id="6b7b2-138">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-138">Click Yes.</span></span>
    * <span data-ttu-id="6b7b2-139">Подтвердите импорт выбранной версии из LCS.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="6b7b2-140">Обратите внимание, что информационное сообщение (над формой) подтверждает успешное завершение импорта выбранной версии.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="6b7b2-141">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-141">Close the page.</span></span>
8. <span data-ttu-id="6b7b2-142">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-142">Close the page.</span></span>
9. <span data-ttu-id="6b7b2-143">Щелкните "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="6b7b2-143">Click Configurations.</span></span>
10. <span data-ttu-id="6b7b2-144">В дереве выберите "Пример конфигурации модели".</span><span class="sxs-lookup"><span data-stu-id="6b7b2-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="6b7b2-145">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6b7b2-146">Выберите версию этой конфигурации со статусом "Общее".</span><span class="sxs-lookup"><span data-stu-id="6b7b2-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="6b7b2-147">Обратите внимание, что общая версия 1 выбранной конфигурации модели данных теперь также доступна.</span><span class="sxs-lookup"><span data-stu-id="6b7b2-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  

