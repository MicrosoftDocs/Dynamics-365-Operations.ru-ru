--- 
title: "Отправка конфигурации в Lifecycle Services для электронной отчетности (ER)"
description: "В следующих шагах поясняется, как пользователь с ролью \"Системный администратор\" или \"Разработчик электронной отчетности\" может создать новую конфигурацию электронной отчетности и отправить ее в Microsoft Lifecycle Services (LCS)."
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
ms.openlocfilehash: d24679a380ec824fe08c56aacb4bc348ff40440a
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="upload-a-configuration-into-lifecycle-services-for-electronic-reporting-er"></a><span data-ttu-id="a4f65-103">Отправка конфигурации в Lifecycle Services для электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="a4f65-103">Upload a configuration into Lifecycle Services for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a4f65-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать новую конфигурацию электронной отчетности и отправить ее в Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a4f65-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration and upload it into Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="a4f65-105">В этом примере вам предстоит создать конфигурацию и отправить ее в LCS для демонстрационной компании Litware, Inc. Эти шаги можно выполнить в любой компании, поскольку конфигурации электронной отчетности являются общими для всех компаний.</span><span class="sxs-lookup"><span data-stu-id="a4f65-105">In this example, you will create a configuration and upload it to LCS for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="a4f65-106">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="a4f65-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="a4f65-107">Доступ к LCS также является обязательным условием для выполнения следующих шагов.</span><span class="sxs-lookup"><span data-stu-id="a4f65-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="a4f65-108">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="a4f65-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="a4f65-109">Выберите "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="a4f65-109">Select ‘Litware, Inc.’</span></span> <span data-ttu-id="a4f65-110">и установите этого поставщика в качестве активного.</span><span class="sxs-lookup"><span data-stu-id="a4f65-110">and set it as active.</span></span>
3. <span data-ttu-id="a4f65-111">Щелкните "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="a4f65-111">Click Configurations.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="a4f65-112">Создать новой конфигурации модели данных</span><span class="sxs-lookup"><span data-stu-id="a4f65-112">Create a new data model configuration</span></span>
1. <span data-ttu-id="a4f65-113">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a4f65-113">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="a4f65-114">Вам предстоит создать конфигурацию, которая содержит пример модели данных для электронных документов.</span><span class="sxs-lookup"><span data-stu-id="a4f65-114">You will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="a4f65-115">Эта конфигурация модели данных будет отправлена в LCS позже.</span><span class="sxs-lookup"><span data-stu-id="a4f65-115">This data model configuration will be uploaded into LCS later.</span></span>  
2. <span data-ttu-id="a4f65-116">В поле "Имя" введите "Пример конфигурации модели".</span><span class="sxs-lookup"><span data-stu-id="a4f65-116">In the Name field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="a4f65-117">Пример конфигурации модели</span><span class="sxs-lookup"><span data-stu-id="a4f65-117">Sample model configuration</span></span>  
3. <span data-ttu-id="a4f65-118">В поле "Описание" введите "Пример конфигурации модели".</span><span class="sxs-lookup"><span data-stu-id="a4f65-118">In the Description field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="a4f65-119">Пример конфигурации модели</span><span class="sxs-lookup"><span data-stu-id="a4f65-119">Sample model configuration</span></span>  
4. <span data-ttu-id="a4f65-120">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="a4f65-120">Click Create configuration.</span></span>
5. <span data-ttu-id="a4f65-121">Щелкните "Конструктор моделей".</span><span class="sxs-lookup"><span data-stu-id="a4f65-121">Click Model designer.</span></span>
6. <span data-ttu-id="a4f65-122">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a4f65-122">Click New.</span></span>
7. <span data-ttu-id="a4f65-123">В поле "Имя" введите "Точка входа".</span><span class="sxs-lookup"><span data-stu-id="a4f65-123">In the Name field, type 'Entry point'.</span></span>
    * <span data-ttu-id="a4f65-124">Точка входа</span><span class="sxs-lookup"><span data-stu-id="a4f65-124">Entry point</span></span>  
8. <span data-ttu-id="a4f65-125">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="a4f65-125">Click Add.</span></span>
9. <span data-ttu-id="a4f65-126">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a4f65-126">Click Save.</span></span>
10. <span data-ttu-id="a4f65-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a4f65-127">Close the page.</span></span>
11. <span data-ttu-id="a4f65-128">Щелкните "Изменить статус".</span><span class="sxs-lookup"><span data-stu-id="a4f65-128">Click Change status.</span></span>
12. <span data-ttu-id="a4f65-129">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="a4f65-129">Click Complete.</span></span>
13. <span data-ttu-id="a4f65-130">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a4f65-130">Click OK.</span></span>

## <a name="register-a-new--repository"></a><span data-ttu-id="a4f65-131">Регистрация нового репозитория</span><span class="sxs-lookup"><span data-stu-id="a4f65-131">Register a new  repository</span></span>
1. <span data-ttu-id="a4f65-132">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a4f65-132">Close the page.</span></span>
2. <span data-ttu-id="a4f65-133">Щелкните "Репозитории".</span><span class="sxs-lookup"><span data-stu-id="a4f65-133">Click Repositories.</span></span>
    * <span data-ttu-id="a4f65-134">Это позволяет открыть список репозиториев для поставщика конфигурации Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="a4f65-134">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
3. <span data-ttu-id="a4f65-135">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a4f65-135">Click Add to open the drop dialog.</span></span>
    * <span data-ttu-id="a4f65-136">Это позволяет добавить новый репозиторий.</span><span class="sxs-lookup"><span data-stu-id="a4f65-136">This allows you to add a new repository.</span></span>  
4. <span data-ttu-id="a4f65-137">В поле "Тип репозитория конфигурации" выберите "LCS".</span><span class="sxs-lookup"><span data-stu-id="a4f65-137">In the Configuration repository type field, select LCS.</span></span>
5. <span data-ttu-id="a4f65-138">Щелкните "Создать репозиторий".</span><span class="sxs-lookup"><span data-stu-id="a4f65-138">Click Create repository.</span></span>
6. <span data-ttu-id="a4f65-139">В поле "Проект" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a4f65-139">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="a4f65-140">Выберите требуемый проект LCS.</span><span class="sxs-lookup"><span data-stu-id="a4f65-140">Select the desired LCS project.</span></span> <span data-ttu-id="a4f65-141">Вы должны иметь доступ к проекту.</span><span class="sxs-lookup"><span data-stu-id="a4f65-141">You must have access to the project.</span></span>  
7. <span data-ttu-id="a4f65-142">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a4f65-142">Click OK.</span></span>
    * <span data-ttu-id="a4f65-143">Заполните новую запись репозитория.</span><span class="sxs-lookup"><span data-stu-id="a4f65-143">Complete a new repository entry.</span></span>  
8. <span data-ttu-id="a4f65-144">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="a4f65-144">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a4f65-145">Выберите запись "Репозиторий LCS".</span><span class="sxs-lookup"><span data-stu-id="a4f65-145">Select the LCS repository record.</span></span>  
    * <span data-ttu-id="a4f65-146">Обратите внимание, что зарегистрированный репозиторий помечен текущим поставщиком, что значит, что только конфигурации, которыми владеет этот поставщик, можно поместить в этот репозиторий и, следовательно, отправить в выбранный проект LCS.</span><span class="sxs-lookup"><span data-stu-id="a4f65-146">Note that a registered repository is marked by the current provider meaning that the only configurations owned by that provider can be placed to this repository and, consequently, uploaded into the selected LCS project.</span></span>  
9. <span data-ttu-id="a4f65-147">Щелкните Открыть.</span><span class="sxs-lookup"><span data-stu-id="a4f65-147">Click Open.</span></span>
    * <span data-ttu-id="a4f65-148">Откройте репозиторий для просмотра списка конфигураций электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="a4f65-148">Open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="a4f65-149">Он будет пустым, если этот проект еще не использовался для совместного использования конфигураций электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="a4f65-149">It will be empty if this project has not yet been used for ER configurations sharing.</span></span>  
10. <span data-ttu-id="a4f65-150">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a4f65-150">Close the page.</span></span>
11. <span data-ttu-id="a4f65-151">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a4f65-151">Close the page.</span></span>

## <a name="upload-configuration-into-lcs"></a><span data-ttu-id="a4f65-152">Отправка конфигурации в LCS</span><span class="sxs-lookup"><span data-stu-id="a4f65-152">Upload configuration into LCS</span></span>
1. <span data-ttu-id="a4f65-153">Щелкните "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="a4f65-153">Click Configurations.</span></span>
2. <span data-ttu-id="a4f65-154">В дереве выберите "Пример конфигурации модели".</span><span class="sxs-lookup"><span data-stu-id="a4f65-154">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="a4f65-155">Выберите созданную конфигурацию, которая уже завершена.</span><span class="sxs-lookup"><span data-stu-id="a4f65-155">Select a created configuration that has been already completed.</span></span>  
3. <span data-ttu-id="a4f65-156">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a4f65-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a4f65-157">Выберите версию выбранной конфигурации со статусом "Завершено".</span><span class="sxs-lookup"><span data-stu-id="a4f65-157">Select the version of the selected configuration with the status of ‘Completed’.</span></span>  
4. <span data-ttu-id="a4f65-158">Щелкните "Изменить статус".</span><span class="sxs-lookup"><span data-stu-id="a4f65-158">Click Change status.</span></span>
5. <span data-ttu-id="a4f65-159">Щелкните "Поделиться".</span><span class="sxs-lookup"><span data-stu-id="a4f65-159">Click Share.</span></span>
    * <span data-ttu-id="a4f65-160">Статус конфигурации изменится с "Завершено" на "Общее" после публикации в LCS.</span><span class="sxs-lookup"><span data-stu-id="a4f65-160">The configuration status will change from ‘Completed’ to ‘Shared’ when it is published in LCS.</span></span>  
6. <span data-ttu-id="a4f65-161">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a4f65-161">Click OK.</span></span>
7. <span data-ttu-id="a4f65-162">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a4f65-162">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a4f65-163">Выберите версию конфигурации со статусом "Общие".</span><span class="sxs-lookup"><span data-stu-id="a4f65-163">Select the configuration version with the status of 'Shared'.</span></span>  
    * <span data-ttu-id="a4f65-164">Обратите внимание, что статус выбранной версии изменился с "Завершено" на "Общее".</span><span class="sxs-lookup"><span data-stu-id="a4f65-164">Note that the status of the selected version has changed from ‘Completed’ to ‘Shared’.</span></span>  
8. <span data-ttu-id="a4f65-165">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a4f65-165">Close the page.</span></span>
9. <span data-ttu-id="a4f65-166">Щелкните "Репозитории".</span><span class="sxs-lookup"><span data-stu-id="a4f65-166">Click Repositories.</span></span>
    * <span data-ttu-id="a4f65-167">Это позволяет открыть список репозиториев для поставщика конфигурации Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="a4f65-167">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
10. <span data-ttu-id="a4f65-168">Щелкните Открыть.</span><span class="sxs-lookup"><span data-stu-id="a4f65-168">Click Open.</span></span>
    * <span data-ttu-id="a4f65-169">Выберите репозиторий LCS и откройте его.</span><span class="sxs-lookup"><span data-stu-id="a4f65-169">Select the LCS repository and open it.</span></span>  
    * <span data-ttu-id="a4f65-170">Обратите внимание, что выбранная конфигурация отображается как актив выбранного проекта LCS.</span><span class="sxs-lookup"><span data-stu-id="a4f65-170">Note that the selected configuration is shown as an asset of the selected LCS project.</span></span>  
    * <span data-ttu-id="a4f65-171">Откройте LCS, используя https://lcs.dynamics.com. Откройте проект, который использовался ранее для регистрации репозитория, откройте библиотеку активов данного проекта и разверните содержимое типа актива "Конфигурация GER". Отправленная конфигурация электронной отчетности станет доступна.</span><span class="sxs-lookup"><span data-stu-id="a4f65-171">Open LCS using https://lcs.dynamics.com. Open a project that was used earlier for repository registration, open the ‘Asset library’ of this project, and expand the content of the ‘GER configuration’ asset type – the uploaded ER configuration will be available.</span></span> <span data-ttu-id="a4f65-172">Обратите внимание, что отправленную конфигурацию LCS можно импортировать в другой экземпляр Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, если поставщики имеют доступ к этому проекту LCS.</span><span class="sxs-lookup"><span data-stu-id="a4f65-172">Note that the uploaded LCS configuration can be imported to another Microsoft Dynamics 365 for Finance and Operations, Enterprise edition instance if providers have access to this LCS project.</span></span>  

