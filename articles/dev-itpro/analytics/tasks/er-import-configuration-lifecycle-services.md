--- 
title: "Импорт конфигурации из Lifecycle Services для электронной отчетности (ER)"
description: "В следующих шагах поясняется, как пользователь с ролью \"Системный администратор\" или \"Разработчик электронной отчетности\" может импортировать новую конфигурацию электронной отчетности из Microsoft Lifecycle Services (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 9eb4f54897c84b98828c927f0f93613583fd4599
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="import-a-configuration-from-lifecycle-services-for-electronic-reporting-er"></a><span data-ttu-id="28a95-103">Импорт конфигурации из Lifecycle Services для электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="28a95-103">Import a configuration from Lifecycle Services for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="28a95-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может импортировать новую конфигурацию электронной отчетности из Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="28a95-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="28a95-105">В этом примере вам предстоит выбрать желаемую версию конфигурации электронной отчетности для демонстрационной компании Litware, Inc. Эти шаги можно выполнить в любой компании, поскольку конфигурации электронной отчетности являются общими для всех компаний.</span><span class="sxs-lookup"><span data-stu-id="28a95-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="28a95-106">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Отправка конфигурации электронной отчетности в Lifecycle Services".</span><span class="sxs-lookup"><span data-stu-id="28a95-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="28a95-107">Доступ к LCS также является обязательным условием для выполнения следующих шагов.</span><span class="sxs-lookup"><span data-stu-id="28a95-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="28a95-108">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="28a95-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="28a95-109">Щелкните "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="28a95-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="28a95-110">Удаление общей версии конфигурации модели данных</span><span class="sxs-lookup"><span data-stu-id="28a95-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="28a95-111">В дереве выберите "Пример конфигурации модели".</span><span class="sxs-lookup"><span data-stu-id="28a95-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="28a95-112">Первая версия конфигурации примера модели данных создана и опубликована в LCS во время выполнения процедуры "Отправка конфигурации электронной отчетности в Lifecycle Services".</span><span class="sxs-lookup"><span data-stu-id="28a95-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="28a95-113">В этой процедуре мы удалим эту версию конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="28a95-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="28a95-114">Эта версия примера конфигурации модели данных будет позднее импортирована из LCS.</span><span class="sxs-lookup"><span data-stu-id="28a95-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="28a95-115">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="28a95-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="28a95-116">Выберите версию этой конфигурации со статусом "Общие".</span><span class="sxs-lookup"><span data-stu-id="28a95-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="28a95-117">Этот статус указывает, что конфигурация была опубликована в LCS.</span><span class="sxs-lookup"><span data-stu-id="28a95-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="28a95-118">Щелкните "Изменить статус".</span><span class="sxs-lookup"><span data-stu-id="28a95-118">Click Change status.</span></span>
4. <span data-ttu-id="28a95-119">Щелкните "Отменить".</span><span class="sxs-lookup"><span data-stu-id="28a95-119">Click Discontinue.</span></span>
    * <span data-ttu-id="28a95-120">Измените статус выбранной версии с "Общее" на "Отменено", чтобы сделать ее доступной для удаления.</span><span class="sxs-lookup"><span data-stu-id="28a95-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="28a95-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="28a95-121">Click OK.</span></span>
6. <span data-ttu-id="28a95-122">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="28a95-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="28a95-123">Выберите версию этой конфигурации со статусом "Отменено".</span><span class="sxs-lookup"><span data-stu-id="28a95-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="28a95-124">Нажмите кнопку Удалить.</span><span class="sxs-lookup"><span data-stu-id="28a95-124">Click Delete.</span></span>
8. <span data-ttu-id="28a95-125">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="28a95-125">Click Yes.</span></span>
    * <span data-ttu-id="28a95-126">Обратите внимание, что доступна только черновая версия 2 выбранной конфигурации модели данных.</span><span class="sxs-lookup"><span data-stu-id="28a95-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="28a95-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="28a95-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="28a95-128">Импорт общей версии конфигурации модели данных из LCS</span><span class="sxs-lookup"><span data-stu-id="28a95-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="28a95-129">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="28a95-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="28a95-130">Откройте список репозиториев для Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="28a95-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="28a95-131">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="28a95-131">configuration provider.</span></span>  
2. <span data-ttu-id="28a95-132">Щелкните "Репозитории".</span><span class="sxs-lookup"><span data-stu-id="28a95-132">Click Repositories.</span></span>
3. <span data-ttu-id="28a95-133">Щелкните Открыть.</span><span class="sxs-lookup"><span data-stu-id="28a95-133">Click Open.</span></span>
    * <span data-ttu-id="28a95-134">Выберите репозиторий LCS и откройте его.</span><span class="sxs-lookup"><span data-stu-id="28a95-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="28a95-135">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="28a95-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="28a95-136">Выберите первую версию примере конфигурации модели в списке версий.</span><span class="sxs-lookup"><span data-stu-id="28a95-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="28a95-137">Нажмите кнопку Импорт.</span><span class="sxs-lookup"><span data-stu-id="28a95-137">Click Import.</span></span>
6. <span data-ttu-id="28a95-138">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="28a95-138">Click Yes.</span></span>
    * <span data-ttu-id="28a95-139">Подтвердите импорт выбранной версии из LCS.</span><span class="sxs-lookup"><span data-stu-id="28a95-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="28a95-140">Обратите внимание, что информационное сообщение (над формой) подтверждает успешное завершение импорта выбранной версии.</span><span class="sxs-lookup"><span data-stu-id="28a95-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="28a95-141">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="28a95-141">Close the page.</span></span>
8. <span data-ttu-id="28a95-142">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="28a95-142">Close the page.</span></span>
9. <span data-ttu-id="28a95-143">Щелкните "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="28a95-143">Click Configurations.</span></span>
10. <span data-ttu-id="28a95-144">В дереве выберите "Пример конфигурации модели".</span><span class="sxs-lookup"><span data-stu-id="28a95-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="28a95-145">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="28a95-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="28a95-146">Выберите версию этой конфигурации со статусом "Общее".</span><span class="sxs-lookup"><span data-stu-id="28a95-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="28a95-147">Обратите внимание, что общая версия 1 выбранной конфигурации модели данных теперь также доступна.</span><span class="sxs-lookup"><span data-stu-id="28a95-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  


