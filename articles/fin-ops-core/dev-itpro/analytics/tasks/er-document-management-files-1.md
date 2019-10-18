---
title: Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 1. Подготовка модели данных)
description: В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для использования файлов управления документами (вложений) в выходных данных электронной отчетности.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d3bd01f7aa1ef95230c37458a5676111a5efa23c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182562"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1-prepare-data-model"></a><span data-ttu-id="1e950-103">Электронная отчетность — Использование файлов управления документами в выходных данных формата (Часть 1. Подготовка модели данных)</span><span class="sxs-lookup"><span data-stu-id="1e950-103">ER Use Document Management files in format outputs (Part 1: Prepare data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1e950-104">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для использования файлов управления документами (вложений) в выходных данных электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="1e950-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="1e950-105">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="1e950-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="1e950-106">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="1e950-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="1e950-107">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="1e950-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="1e950-108">Получение доступа к списку конфигураций, предоставленных компанией Microsoft</span><span class="sxs-lookup"><span data-stu-id="1e950-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="1e950-109">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="1e950-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="1e950-110">Убедитесь, что поставщик Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="1e950-110">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="1e950-111">доступен и помечен как активный.</span><span class="sxs-lookup"><span data-stu-id="1e950-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="1e950-112">Выберите "Litware, Inc".</span><span class="sxs-lookup"><span data-stu-id="1e950-112">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="1e950-113">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="1e950-113">provider.</span></span>
3. <span data-ttu-id="1e950-114">Щелкните "Репозитории".</span><span class="sxs-lookup"><span data-stu-id="1e950-114">Click Repositories.</span></span>
    * <span data-ttu-id="1e950-115">Если репозиторий типа "Операционные ресурсы" уже существует, пропустите остальные шаги текущей подзадачи.</span><span class="sxs-lookup"><span data-stu-id="1e950-115">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="1e950-116">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="1e950-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="1e950-117">В поле "Тип репозитория конфигурации" введите "Операционные ресурсы".</span><span class="sxs-lookup"><span data-stu-id="1e950-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="1e950-118">Щелкните "Создать репозиторий".</span><span class="sxs-lookup"><span data-stu-id="1e950-118">Click Create repository.</span></span>
7. <span data-ttu-id="1e950-119">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1e950-119">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="1e950-120">Получите конфигурации "Модель накладной клиента", предоставленные Microsoft</span><span class="sxs-lookup"><span data-stu-id="1e950-120">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="1e950-121">Щелкните "Показать фильтры".</span><span class="sxs-lookup"><span data-stu-id="1e950-121">Click Show filters.</span></span>
2. <span data-ttu-id="1e950-122">Примените следующие фильтры: введите значение фильтра "Операционные ресурсы" в поле "Имя", используя оператор фильтра "начинается с"; введите значение фильтра "" по полю "Описание", используя оператор фильтра "начинается с"</span><span class="sxs-lookup"><span data-stu-id="1e950-122">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="1e950-123">Щелкните "Показать фильтры".</span><span class="sxs-lookup"><span data-stu-id="1e950-123">Click Show filters.</span></span>
4. <span data-ttu-id="1e950-124">Щелкните Открыть.</span><span class="sxs-lookup"><span data-stu-id="1e950-124">Click Open.</span></span>
5. <span data-ttu-id="1e950-125">В дереве выберите "Модель накладной клиента".</span><span class="sxs-lookup"><span data-stu-id="1e950-125">In the tree, select 'Customer invoice model'.</span></span>
    * <span data-ttu-id="1e950-126">Выберите модель конфигурации "Модель накладной клиента", чтобы импортировать ее.</span><span class="sxs-lookup"><span data-stu-id="1e950-126">Select the model configuration 'Customer invoice model' to import it.</span></span>  
6. <span data-ttu-id="1e950-127">Нажмите кнопку Импорт.</span><span class="sxs-lookup"><span data-stu-id="1e950-127">Click Import.</span></span>
    * <span data-ttu-id="1e950-128">Щелкните "Импорт" для версии 1 выбранной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1e950-128">Click Import for version 1 of the selected configuration.</span></span>  
7. <span data-ttu-id="1e950-129">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="1e950-129">Click Yes.</span></span>
8. <span data-ttu-id="1e950-130">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1e950-130">Close the page.</span></span>
9. <span data-ttu-id="1e950-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1e950-131">Close the page.</span></span>
10. <span data-ttu-id="1e950-132">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="1e950-132">Click Reporting configurations.</span></span>
11. <span data-ttu-id="1e950-133">В дереве выберите "Модель накладной клиента".</span><span class="sxs-lookup"><span data-stu-id="1e950-133">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="1e950-134">Создайте производную модель для поддержки доступа к файлам управления документами.</span><span class="sxs-lookup"><span data-stu-id="1e950-134">Create the derived model to support access to the Document Management files.</span></span>
    * <span data-ttu-id="1e950-135">Вы создадите нашу собственную конфигурацию модели накладной клиента на основе конфигурации, предоставленной компанией Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1e950-135">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="1e950-136">Вы будет использовать эту конфигурация для реализации доступа к файлам управления документами и для того, чтобы сделать их доступными для электронных документов, которые будут созданы на основе этой модели.</span><span class="sxs-lookup"><span data-stu-id="1e950-136">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="1e950-137">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="1e950-137">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="1e950-138">В поле "Создать" введите "Производное от имени: Модель накладной клиента, Microsoft".</span><span class="sxs-lookup"><span data-stu-id="1e950-138">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="1e950-139">В поле "Имя" введите "Модель накладной клиента (настраиваемая)".</span><span class="sxs-lookup"><span data-stu-id="1e950-139">In the Name field, type 'Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="1e950-140">Модель накладной клиента (настраиваемая)</span><span class="sxs-lookup"><span data-stu-id="1e950-140">Customer invoice model (custom)</span></span>  
4. <span data-ttu-id="1e950-141">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="1e950-141">Click Create configuration.</span></span>

