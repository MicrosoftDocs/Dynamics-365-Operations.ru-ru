---
title: Управление сопоставлением модели электронной отчетности в отдельных конфигурациях электронной отчетности
description: В этой теме описывается управление сопоставлениями моделей электронной отчетности (ER) в отдельных конфигурациях электронной отчетности.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fdd6804c33cc153974229c60b64c3bd76426241a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569421"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a><span data-ttu-id="d4883-103">Управление сопоставлениями модели электронной отчетности в отдельных конфигурациях электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="d4883-103">Manage ER model mapping in separate ER configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d4883-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может управлять сопоставлениями модели электронной отчетности в отдельных конфигурациях электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="d4883-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="d4883-105">В этом проводнике по задаче вам предстоит создать необходимые конфигурации ER для демонстрационной компании Litware, Inc. Чтобы выполнить этот проводник по задаче, необходимо сначала выполнить шаги в проводнике по задаче "Электронная отчетность — создание поставщика конфигурации и пометка его как активного".</span><span class="sxs-lookup"><span data-stu-id="d4883-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, "ER Create a configuration provider" and mark it as active.</span></span> 

<span data-ttu-id="d4883-106">Поскольку конфигурации электронной отчетности используются совместно несколькими компаниями, вы можете выполнить этот проводник по задаче, используя набор данных компании на ваш выбор.</span><span class="sxs-lookup"><span data-stu-id="d4883-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="d4883-107">Функциональность для этого руководства по задаче доступна, если установлено одно из следующих исправлений: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 для версии Dynamics AX 7.0 или https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 для версии Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="d4883-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="d4883-108">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="d4883-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="d4883-109">Убедитесь, что поставщик конфигурации для демонстрационной компании Litware, Inc. доступен и помечен как активный.</span><span class="sxs-lookup"><span data-stu-id="d4883-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="d4883-110">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить действия в проводнике по задаче "Создание поставщика конфигурации и пометка его как активного".</span><span class="sxs-lookup"><span data-stu-id="d4883-110">If you don't see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider, and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="d4883-111">Добавление новой конфигурации модели ER</span><span class="sxs-lookup"><span data-stu-id="d4883-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="d4883-112">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="d4883-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="d4883-113">Добавьте новую конфигурацию модели.</span><span class="sxs-lookup"><span data-stu-id="d4883-113">Add a new model configuration.</span></span> <span data-ttu-id="d4883-114">Имя должно быть уникальным в дереве конфигураций.</span><span class="sxs-lookup"><span data-stu-id="d4883-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="d4883-115">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d4883-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="d4883-116">В поле "Имя" введите "Пример модели данных".</span><span class="sxs-lookup"><span data-stu-id="d4883-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="d4883-117">Пример модели данных</span><span class="sxs-lookup"><span data-stu-id="d4883-117">Sample data model</span></span>  
4. <span data-ttu-id="d4883-118">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="d4883-118">Click Create configuration.</span></span>
5. <span data-ttu-id="d4883-119">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="d4883-119">Click Designer.</span></span>
6. <span data-ttu-id="d4883-120">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d4883-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="d4883-121">В поле "Имя" введите "Корень".</span><span class="sxs-lookup"><span data-stu-id="d4883-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="d4883-122">Корневой</span><span class="sxs-lookup"><span data-stu-id="d4883-122">Root</span></span>  
8. <span data-ttu-id="d4883-123">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="d4883-123">Click Add.</span></span>
9. <span data-ttu-id="d4883-124">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d4883-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="d4883-125">В поле "Имя" введите "Компания".</span><span class="sxs-lookup"><span data-stu-id="d4883-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="d4883-126">Организация</span><span class="sxs-lookup"><span data-stu-id="d4883-126">Company</span></span>  
11. <span data-ttu-id="d4883-127">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="d4883-127">Click Add.</span></span>
12. <span data-ttu-id="d4883-128">В поле "Описание" введите текст "Описание юридического лица или компании, в которую вошел пользователь во время выполнения".</span><span class="sxs-lookup"><span data-stu-id="d4883-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="d4883-129">Описание юридического лица или компании, в которую пользователь вошел во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="d4883-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="d4883-130">Щелкните "Корневая ссылка".</span><span class="sxs-lookup"><span data-stu-id="d4883-130">Click Root reference.</span></span>
14. <span data-ttu-id="d4883-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d4883-131">Click OK.</span></span>
15. <span data-ttu-id="d4883-132">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d4883-132">Click Save.</span></span>
16. <span data-ttu-id="d4883-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d4883-133">Close the page.</span></span>
17. <span data-ttu-id="d4883-134">Щелкните "Изменить статус".</span><span class="sxs-lookup"><span data-stu-id="d4883-134">Click Change status.</span></span>
18. <span data-ttu-id="d4883-135">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="d4883-135">Click Complete.</span></span>
19. <span data-ttu-id="d4883-136">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d4883-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="d4883-137">Добавление новой конфигурации сопоставлений модели электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="d4883-137">Add a new ER model-mapping configuration</span></span>
1. <span data-ttu-id="d4883-138">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d4883-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="d4883-139">В поле "Создать" введите "Сопоставление модели, основанное на модели данных Пример модели данных".</span><span class="sxs-lookup"><span data-stu-id="d4883-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="d4883-140">В поле "Имя" введите "Пример сопоставления".</span><span class="sxs-lookup"><span data-stu-id="d4883-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="d4883-141">Пример сопоставления</span><span class="sxs-lookup"><span data-stu-id="d4883-141">Sample mapping</span></span>  
4. <span data-ttu-id="d4883-142">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="d4883-142">Click Create configuration.</span></span>
5. <span data-ttu-id="d4883-143">Разверните раздел "Необходимые условия".</span><span class="sxs-lookup"><span data-stu-id="d4883-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="d4883-144">Группа необходимых условий "Реализации" была добавлена автоматически.</span><span class="sxs-lookup"><span data-stu-id="d4883-144">The Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="d4883-145">Эта группа содержит необходимый компонент, который ссылается на родительскую конфигурацию модели данных, и для которого установлен флаг "Реализация".</span><span class="sxs-lookup"><span data-stu-id="d4883-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="d4883-146">Это означает, что конфигурация сопоставления "Пример сопоставления" считается реализацией модели данных "Пример модели данных".</span><span class="sxs-lookup"><span data-stu-id="d4883-146">This means that this Sample-mapping model-mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="d4883-147">Следовательно, данный компонент будет обеспечивать принудительную загрузку электронной отчетностью конфигураций сопоставлений модели "Пример сопоставления" из репозитория электронной отчетности всякий раз, когда загружается конфигурация модели "Пример модели данных".</span><span class="sxs-lookup"><span data-stu-id="d4883-147">Therefore, this component will force ER to download the model-mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="d4883-148">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="d4883-148">Click Designer.</span></span>
    * <span data-ttu-id="d4883-149">Созданная конфигурация сопоставлений модели содержит новое пустое сопоставление с тем же именем, что и у созданной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d4883-149">The created model-mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="d4883-150">Если выбранная родительская конфигурация модели содержит сопоставления модели, они будут скопированы в новую конфигурацию сопоставлений модели.</span><span class="sxs-lookup"><span data-stu-id="d4883-150">When a selected parent model configuration contains model mappings, they will be copied to a new model-mapping configuration.</span></span>   
7. <span data-ttu-id="d4883-151">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="d4883-151">Click Designer.</span></span>
8. <span data-ttu-id="d4883-152">В дереве выберите узел "Dynamics 365 for Operations\Таблица".</span><span class="sxs-lookup"><span data-stu-id="d4883-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="d4883-153">Щелкните "Добавить корень".</span><span class="sxs-lookup"><span data-stu-id="d4883-153">Click Add root.</span></span>
10. <span data-ttu-id="d4883-154">В поле "Имя" введите "Компания".</span><span class="sxs-lookup"><span data-stu-id="d4883-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="d4883-155">Организация</span><span class="sxs-lookup"><span data-stu-id="d4883-155">Company</span></span>  
11. <span data-ttu-id="d4883-156">В поле "Таблица" введите "CompanyInfo".</span><span class="sxs-lookup"><span data-stu-id="d4883-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="d4883-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="d4883-157">CompanyInfo</span></span>  
12. <span data-ttu-id="d4883-158">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d4883-158">Click OK.</span></span>
13. <span data-ttu-id="d4883-159">В дереве разверните "Компания".</span><span class="sxs-lookup"><span data-stu-id="d4883-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="d4883-160">В дереве разверните "Компания\find()".</span><span class="sxs-lookup"><span data-stu-id="d4883-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="d4883-161">В дереве выберите "Компания\find()\Name".</span><span class="sxs-lookup"><span data-stu-id="d4883-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="d4883-162">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="d4883-162">Click Bind.</span></span>
17. <span data-ttu-id="d4883-163">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d4883-163">Click Save.</span></span>
18. <span data-ttu-id="d4883-164">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d4883-164">Close the page.</span></span>
19. <span data-ttu-id="d4883-165">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d4883-165">Close the page.</span></span>
20. <span data-ttu-id="d4883-166">В области действий щелкните "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="d4883-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="d4883-167">Щелкните "Параметры пользователя".</span><span class="sxs-lookup"><span data-stu-id="d4883-167">Click User parameters.</span></span>
22. <span data-ttu-id="d4883-168">Выберите "Да" в поле "Запустить настройки".</span><span class="sxs-lookup"><span data-stu-id="d4883-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="d4883-169">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d4883-169">Click OK.</span></span>
24. <span data-ttu-id="d4883-170">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="d4883-170">Click Edit.</span></span>
25. <span data-ttu-id="d4883-171">Выберите "Да" в поле "Запустить черновик".</span><span class="sxs-lookup"><span data-stu-id="d4883-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="d4883-172">Добавление новой конфигурации формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="d4883-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="d4883-173">В дереве выберите "Пример модели данных".</span><span class="sxs-lookup"><span data-stu-id="d4883-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="d4883-174">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d4883-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="d4883-175">В поле "Создать" введите "Формат, основанный на модели данных Пример модели данных".</span><span class="sxs-lookup"><span data-stu-id="d4883-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="d4883-176">В поле "Имя" введите "Пример формата".</span><span class="sxs-lookup"><span data-stu-id="d4883-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="d4883-177">Пример формата</span><span class="sxs-lookup"><span data-stu-id="d4883-177">Sample format</span></span>  
5. <span data-ttu-id="d4883-178">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="d4883-178">Click Create configuration.</span></span>
6. <span data-ttu-id="d4883-179">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="d4883-179">Click Designer.</span></span>
7. <span data-ttu-id="d4883-180">Щелкните "Добавить корень", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d4883-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="d4883-181">В дереве выберите "Текст\строка".</span><span class="sxs-lookup"><span data-stu-id="d4883-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="d4883-182">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d4883-182">Click OK.</span></span>
10. <span data-ttu-id="d4883-183">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="d4883-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="d4883-184">В дереве разверните узел "model".</span><span class="sxs-lookup"><span data-stu-id="d4883-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="d4883-185">В дереве выберите "модель\Компания".</span><span class="sxs-lookup"><span data-stu-id="d4883-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="d4883-186">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="d4883-186">Click Bind.</span></span>
14. <span data-ttu-id="d4883-187">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d4883-187">Click Save.</span></span>
15. <span data-ttu-id="d4883-188">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d4883-188">Close the page.</span></span>
    * <span data-ttu-id="d4883-189">Запустите черновую версию созданного формата для целей тестирования.</span><span class="sxs-lookup"><span data-stu-id="d4883-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="d4883-190">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="d4883-190">Click Run.</span></span>
    * <span data-ttu-id="d4883-191">На экспресс-вкладке "Версии" щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="d4883-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="d4883-192">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d4883-192">Click OK.</span></span>
    * <span data-ttu-id="d4883-193">Просмотрите выходные данные, содержащие имя компании, в которую вошел пользователь, запустивший данную конфигурацию формата.</span><span class="sxs-lookup"><span data-stu-id="d4883-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="d4883-194">Созданная конфигурация сопоставлений модели используется в этой конфигурации формата, поскольку доступна только одна конфигурация, содержащая необходимые сопоставления модели.</span><span class="sxs-lookup"><span data-stu-id="d4883-194">The created model-mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="d4883-195">Добавление альтернативной конфигурации сопоставлений модели электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="d4883-195">Add alternative ER model-mapping configuration</span></span>
1. <span data-ttu-id="d4883-196">В дереве выберите "Пример модели данных".</span><span class="sxs-lookup"><span data-stu-id="d4883-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="d4883-197">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d4883-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="d4883-198">В поле "Создать" введите "Сопоставление модели, основанное на модели данных Пример модели данных".</span><span class="sxs-lookup"><span data-stu-id="d4883-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="d4883-199">В поле "Имя" введите "Пример сопоставления (альтернативный)".</span><span class="sxs-lookup"><span data-stu-id="d4883-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="d4883-200">Пример сопоставления (альтернативный)</span><span class="sxs-lookup"><span data-stu-id="d4883-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="d4883-201">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="d4883-201">Click Create configuration.</span></span>
6. <span data-ttu-id="d4883-202">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="d4883-202">Click Designer.</span></span>
7. <span data-ttu-id="d4883-203">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="d4883-203">Click Designer.</span></span>
8. <span data-ttu-id="d4883-204">В дереве выберите узел "Dynamics 365 for Operations\Таблица".</span><span class="sxs-lookup"><span data-stu-id="d4883-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="d4883-205">Щелкните "Добавить корень".</span><span class="sxs-lookup"><span data-stu-id="d4883-205">Click Add root.</span></span>
10. <span data-ttu-id="d4883-206">В поле "Имя" введите "Компания".</span><span class="sxs-lookup"><span data-stu-id="d4883-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="d4883-207">Организация</span><span class="sxs-lookup"><span data-stu-id="d4883-207">Company</span></span>  
11. <span data-ttu-id="d4883-208">В поле "Таблица" введите "CompanyInfo".</span><span class="sxs-lookup"><span data-stu-id="d4883-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="d4883-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="d4883-209">CompanyInfo</span></span>  
12. <span data-ttu-id="d4883-210">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d4883-210">Click OK.</span></span>
13. <span data-ttu-id="d4883-211">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="d4883-211">Click Edit.</span></span>
14. <span data-ttu-id="d4883-212">В дереве выберите "Строка\ОБЪЕДИНИТЬ".</span><span class="sxs-lookup"><span data-stu-id="d4883-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="d4883-213">Щелкните "Добавить функцию".</span><span class="sxs-lookup"><span data-stu-id="d4883-213">Click Add function.</span></span>
16. <span data-ttu-id="d4883-214">В дереве разверните "Компания".</span><span class="sxs-lookup"><span data-stu-id="d4883-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="d4883-215">В дереве разверните "Компания\find()".</span><span class="sxs-lookup"><span data-stu-id="d4883-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="d4883-216">В дереве выберите "Компания\find()\Name".</span><span class="sxs-lookup"><span data-stu-id="d4883-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="d4883-217">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="d4883-217">Click Add data source.</span></span>
20. <span data-ttu-id="d4883-218">В поле "Формула" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d4883-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="d4883-219">CONCATENATE(Компания.'find()'.Имя, ";",</span><span class="sxs-lookup"><span data-stu-id="d4883-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="d4883-220">В дереве выберите "Компания\find()\Компания(DataArea)".</span><span class="sxs-lookup"><span data-stu-id="d4883-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="d4883-221">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="d4883-221">Click Add data source.</span></span>
23. <span data-ttu-id="d4883-222">В поле "Формула" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d4883-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="d4883-223">CONCATENATE(Компания.'find()'.Имя, ";", Компания.'find()'.DataArea)</span><span class="sxs-lookup"><span data-stu-id="d4883-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="d4883-224">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d4883-224">Click Save.</span></span>
25. <span data-ttu-id="d4883-225">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d4883-225">Close the page.</span></span>
26. <span data-ttu-id="d4883-226">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d4883-226">Click Save.</span></span>
27. <span data-ttu-id="d4883-227">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d4883-227">Close the page.</span></span>
28. <span data-ttu-id="d4883-228">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d4883-228">Close the page.</span></span>
29. <span data-ttu-id="d4883-229">Выберите "Да" в поле "Запустить черновик".</span><span class="sxs-lookup"><span data-stu-id="d4883-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="d4883-230">Использование существующей конфигурации сопоставлений модели электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="d4883-230">Use an existing ER model-mapping configuration</span></span>
1. <span data-ttu-id="d4883-231">В дереве выберите "Пример модели данных\Пример формата".</span><span class="sxs-lookup"><span data-stu-id="d4883-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="d4883-232">Щелкните Выполнить.</span><span class="sxs-lookup"><span data-stu-id="d4883-232">Click Run.</span></span>
    * <span data-ttu-id="d4883-233">Выбранную черновую версию конфигурации формата электронной отчетности невозможно выполнить, поскольку для неопределенной модели данных, выбранной в качестве источника данных выполняемого формата электронной отчетности, доступно более одной конфигурации сопоставлений модели.</span><span class="sxs-lookup"><span data-stu-id="d4883-233">The selected draft version of the ER format configuration can't be executed because there is more than one model-mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="d4883-234">Далее вам предстоит определить альтернативную конфигурацию сопоставлений модели в качестве той, сопоставления модели из которой будут использоваться в качестве источников для выполняемого формата электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="d4883-234">Next, you will define the alternative model-mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="d4883-235">В дереве выберите "Пример модели данных\Пример сопоставления (альтернативный)".</span><span class="sxs-lookup"><span data-stu-id="d4883-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="d4883-236">Выберите "Да" в поле "По умолчанию для сопоставления модели".</span><span class="sxs-lookup"><span data-stu-id="d4883-236">Select Yes in the Default for model-mapping field.</span></span>
5. <span data-ttu-id="d4883-237">В дереве выберите "Пример модели данных\Пример формата".</span><span class="sxs-lookup"><span data-stu-id="d4883-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="d4883-238">Щелкните Выполнить.</span><span class="sxs-lookup"><span data-stu-id="d4883-238">Click Run.</span></span>
7. <span data-ttu-id="d4883-239">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d4883-239">Click OK.</span></span>
    * <span data-ttu-id="d4883-240">Конфигурация сопоставлений модели по умолчанию используется в этой конфигурации формата для формирования электронного документа (созданные выходные данные содержат код компании).</span><span class="sxs-lookup"><span data-stu-id="d4883-240">The default model-mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]