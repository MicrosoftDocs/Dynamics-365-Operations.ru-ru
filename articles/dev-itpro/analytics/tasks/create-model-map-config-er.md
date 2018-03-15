--- 
title: "Создание конфигурации сопоставлений модели (ER)"
description: "Эта процедура используется для создания новой конфигурации сопоставления модели электронной отчетности (ER) и использования встроенных функций ER для эффективного агрегирования расчетов."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 74606b1378e94e8a6945a408520c8b68648970d8
ms.openlocfilehash: f7206126bfa6150078f1bfb4f7e07c1cf2819ce0
ms.contentlocale: ru-ru
ms.lasthandoff: 02/07/2018

---
# <a name="create-a-model-mapping-configuration-er"></a><span data-ttu-id="2505c-103">Создание конфигурации сопоставлений модели (ER)</span><span class="sxs-lookup"><span data-stu-id="2505c-103">Create a model mapping configuration (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2505c-104">Эта процедура используется для создания новой конфигурации сопоставления модели электронной отчетности (ER) и использования встроенных функций ER для эффективного агрегирования расчетов.</span><span class="sxs-lookup"><span data-stu-id="2505c-104">Use this procedure to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="2505c-105">В этой процедуре вам предстоит создать конфигурацию для компании-образца Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="2505c-105">In this procedure, you will create a configuration for sample company, Litware, Inc.</span></span> 

<span data-ttu-id="2505c-106">Эта процедура предназначена для пользователей, которым назначена роль "Системный администратор" или "Разработчик электронной отчетности".</span><span class="sxs-lookup"><span data-stu-id="2505c-106">This procedure is created for uses with the assigned role of System administrator or Electronic reporting developer.</span></span>

<span data-ttu-id="2505c-107">Эти шаги можно выполнить с использованием любого набора данных.</span><span class="sxs-lookup"><span data-stu-id="2505c-107">These steps can be completed using any dataset.</span></span> <span data-ttu-id="2505c-108">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="2505c-108">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active.”</span></span>

1. <span data-ttu-id="2505c-109">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="2505c-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="2505c-110">Убедитесь, что поставщик конфигурации для демонстрационной компании Litware, Inc. доступен и помечен как активный.</span><span class="sxs-lookup"><span data-stu-id="2505c-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="2505c-111">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и пометка его как активного".</span><span class="sxs-lookup"><span data-stu-id="2505c-111">If you don’t see this configuration provider, complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>  
2. <span data-ttu-id="2505c-112">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="2505c-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="2505c-113">Щелкните "Показать фильтры".</span><span class="sxs-lookup"><span data-stu-id="2505c-113">Click Show filters.</span></span>
4. <span data-ttu-id="2505c-114">В поле "Имя" введите значение фильтра "Интрастат" и используйте оператор фильтра "начинается с".</span><span class="sxs-lookup"><span data-stu-id="2505c-114">In the "Name" field, enter the filter value, "Intrastat" and use the filter operator "begins with".</span></span>
    * <span data-ttu-id="2505c-115">Примените этот фильтр, чтобы найти конфигурацию модели данных "Интрастат".</span><span class="sxs-lookup"><span data-stu-id="2505c-115">Apply this filter to find the ‘Intrastat’ data model configuration.</span></span> <span data-ttu-id="2505c-116">Эта модель может уже существовать в дереве конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2505c-116">This model may already exist in the configurations tree.</span></span> <span data-ttu-id="2505c-117">Если это так, пропустите следующую подзадачу.</span><span class="sxs-lookup"><span data-stu-id="2505c-117">If it does, skip the next sub-task.</span></span>   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a><span data-ttu-id="2505c-118">Получение конфигурации модели Интрастат, предоставленной Майкрософт</span><span class="sxs-lookup"><span data-stu-id="2505c-118">Get the Intrastat model configuration provided by Microsoft</span></span>
1. <span data-ttu-id="2505c-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2505c-119">Close the page.</span></span>
2. <span data-ttu-id="2505c-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2505c-120">Close the page.</span></span>
3. <span data-ttu-id="2505c-121">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="2505c-121">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
4. <span data-ttu-id="2505c-122">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="2505c-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2505c-123">Выберите плитку поставщика Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="2505c-123">Select the Microsoft provider tile.</span></span>  
5. <span data-ttu-id="2505c-124">Щелкните "Репозитории".</span><span class="sxs-lookup"><span data-stu-id="2505c-124">Click Repositories.</span></span>
    * <span data-ttu-id="2505c-125">Щелкните "Репозитории" на плитке поставщика Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="2505c-125">Click Repositories in the Microsoft provider tile.</span></span>  
6. <span data-ttu-id="2505c-126">Щелкните "Показать фильтры".</span><span class="sxs-lookup"><span data-stu-id="2505c-126">Click Show filters.</span></span>
7. <span data-ttu-id="2505c-127">В поле "Имя типа" введите значение фильтра "ресурсы" и используйте оператор фильтра "содержит".</span><span class="sxs-lookup"><span data-stu-id="2505c-127">In the "Type name" field, enter the filter value, “resources” and use the filter operator "contains".</span></span> 
8. <span data-ttu-id="2505c-128">Щелкните Открыть.</span><span class="sxs-lookup"><span data-stu-id="2505c-128">Click Open.</span></span>
9. <span data-ttu-id="2505c-129">В дереве выберите "Модель Интрастат".</span><span class="sxs-lookup"><span data-stu-id="2505c-129">In the tree, select 'Intrastat model'.</span></span>
10. <span data-ttu-id="2505c-130">Нажмите кнопку Импорт.</span><span class="sxs-lookup"><span data-stu-id="2505c-130">Click Import.</span></span>
11. <span data-ttu-id="2505c-131">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="2505c-131">Click Yes.</span></span>
    * <span data-ttu-id="2505c-132">Вы импортировали конфигурацию модели ER, которая содержит модель данных, которая будет использоваться для изучения использования новых функциональных возможностей ER.</span><span class="sxs-lookup"><span data-stu-id="2505c-132">You imported the ER model configuration that contains the data model that you will use to explore how the new ER functionality can be used.</span></span>  
12. <span data-ttu-id="2505c-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2505c-133">Close the page.</span></span>
13. <span data-ttu-id="2505c-134">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2505c-134">Close the page.</span></span>
14. <span data-ttu-id="2505c-135">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="2505c-135">Click Reporting configurations.</span></span>

## <a name="add-a-new-model-mapping-configuration"></a><span data-ttu-id="2505c-136">Добавление новой конфигурации сопоставлений модели</span><span class="sxs-lookup"><span data-stu-id="2505c-136">Add a new model mapping configuration</span></span>
1. <span data-ttu-id="2505c-137">В дереве выберите "Модель Интрастат".</span><span class="sxs-lookup"><span data-stu-id="2505c-137">In the tree, select 'Intrastat model'.</span></span>
2. <span data-ttu-id="2505c-138">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="2505c-138">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="2505c-139">В поле "Создать" введите "Сопоставление модели, основанное на модели данных Интрастат".</span><span class="sxs-lookup"><span data-stu-id="2505c-139">In the New field, enter 'Model Mapping based on data model Intrastat'.</span></span>
4. <span data-ttu-id="2505c-140">В поле "Имя" введите "Сопоставление образца Интрастат".</span><span class="sxs-lookup"><span data-stu-id="2505c-140">In the Name field, type 'Intrastat sample mapping'.</span></span>
    * <span data-ttu-id="2505c-141">Сопоставление образца Интрастат</span><span class="sxs-lookup"><span data-stu-id="2505c-141">Intrastat sample mapping</span></span>  
5. <span data-ttu-id="2505c-142">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="2505c-142">Click Create configuration.</span></span>


