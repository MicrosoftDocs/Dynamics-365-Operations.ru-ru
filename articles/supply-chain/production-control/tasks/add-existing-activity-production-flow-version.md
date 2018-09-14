--- 
title: "Добавление имеющегося мероприятия в версию производственного потока"
description: "При создании новых версий производственных потоков можно выбрать добавление мероприятий, созданных для более старых версий, в новую версию."
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 032855125ccd14fbdc1e1bdb735c92ce70853fb0
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a><span data-ttu-id="3ba5c-103">Добавление имеющегося мероприятия в версию производственного потока</span><span class="sxs-lookup"><span data-stu-id="3ba5c-103">Add an existing activity to a production flow version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3ba5c-104">При создании новых версий производственных потоков можно выбрать добавление мероприятий, созданных для более старых версий, в новую версию.</span><span class="sxs-lookup"><span data-stu-id="3ba5c-104">When creating new versions of production flows, you can choose to add activities created for the older versions, to the new version.</span></span> <span data-ttu-id="3ba5c-105">Эта процедура демонстрирует порядок создания новой версии для существующего производственного потока без копирования мероприятий.</span><span class="sxs-lookup"><span data-stu-id="3ba5c-105">This procedure shows how a new version is created for an existing production flow, without copying the activities.</span></span> <span data-ttu-id="3ba5c-106">В следующем шаге существующее мероприятие добавляется в новую версию.</span><span class="sxs-lookup"><span data-stu-id="3ba5c-106">In the next step, an existing activity is added to the new version.</span></span> 

<span data-ttu-id="3ba5c-107">Эта задача требует производственного потока с уже созданными версией и мероприятиями.</span><span class="sxs-lookup"><span data-stu-id="3ba5c-107">This task requires production flow with version and activities already created.</span></span>


## <a name="create-a-new-production-flow-version"></a><span data-ttu-id="3ba5c-108">Создание новой версии производственного потока</span><span class="sxs-lookup"><span data-stu-id="3ba5c-108">Create a new production flow version</span></span>
1. <span data-ttu-id="3ba5c-109">Перейдите в раздел "Управление производством" > "Настройка" > "Поток бережливого производства" > "Производственные потоки".</span><span class="sxs-lookup"><span data-stu-id="3ba5c-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="3ba5c-110">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3ba5c-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3ba5c-111">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3ba5c-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3ba5c-112">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="3ba5c-112">Click Edit.</span></span>
5. <span data-ttu-id="3ba5c-113">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="3ba5c-113">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="3ba5c-114">В поле "Дата окончания срока действия" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="3ba5c-114">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="3ba5c-115">Обратите внимание, что перед созданием новой версии производственного потока необходимо проверить дату окончания срока действия и время активной версии.</span><span class="sxs-lookup"><span data-stu-id="3ba5c-115">Note that before you create a new production flow version, make sure to check the expiration date and time of the active version.</span></span> <span data-ttu-id="3ba5c-116">Новая версия будет создана с эффективной датой начала, которая связывается с датой окончания срока действия выбранной версии.</span><span class="sxs-lookup"><span data-stu-id="3ba5c-116">The new version will be created with an effective start date, which connects to the expiry date of the selected version.</span></span>  
7. <span data-ttu-id="3ba5c-117">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="3ba5c-117">Click Add.</span></span>
8. <span data-ttu-id="3ba5c-118">Выберите значение "Нет" в поле "Копировать из версии".</span><span class="sxs-lookup"><span data-stu-id="3ba5c-118">Select No in the Copy from version field.</span></span>
    * <span data-ttu-id="3ba5c-119">Выберите "Нет", чтобы начать с пустой версии, если большинство мероприятий скопированной версии будет заменено новыми мероприятиями.</span><span class="sxs-lookup"><span data-stu-id="3ba5c-119">Select No to start with an empty version if most of the activities of the copied version will be replaced by new activities.</span></span> <span data-ttu-id="3ba5c-120">Добавьте неизменные мероприятия к функции "Добавить существующее" в форме мероприятия вручную.</span><span class="sxs-lookup"><span data-stu-id="3ba5c-120">Add the unchanged activities to the Add existing function in the activity form manually.</span></span>  
9. <span data-ttu-id="3ba5c-121">Выберите "Нет" в поле "Дублировать правила канбана".</span><span class="sxs-lookup"><span data-stu-id="3ba5c-121">Select No in the Duplicate kanban rules field.</span></span>
    * <span data-ttu-id="3ba5c-122">Когда мероприятия не копируются в новую версию, невозможно скопировать правила канбана во время создания новой версии.</span><span class="sxs-lookup"><span data-stu-id="3ba5c-122">When the activities are not copied to the new version, it is not possible to copy the kanban rules at the time of creation of the new version.</span></span>   <span data-ttu-id="3ba5c-123">Вместо этого вы будете использовать функцию создания заменяющего канбана в форме правила канбана для замены правил канбана старой версии производственного потока на правила канбана с использованием мероприятий новой версии.</span><span class="sxs-lookup"><span data-stu-id="3ba5c-123">Instead you will use the create replacement kanban function later in the kanban rule form, to replace kanban rules of the old production flow version with kanban rules using the activities of the new version.</span></span>  
10. <span data-ttu-id="3ba5c-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3ba5c-124">Click OK.</span></span>
11. <span data-ttu-id="3ba5c-125">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3ba5c-125">In the list, find and select the desired record.</span></span>

## <a name="add-an-existing-activity"></a><span data-ttu-id="3ba5c-126">Добавление существующего мероприятия</span><span class="sxs-lookup"><span data-stu-id="3ba5c-126">Add an existing activity</span></span>
1. <span data-ttu-id="3ba5c-127">Щелкните "Мероприятия".</span><span class="sxs-lookup"><span data-stu-id="3ba5c-127">Click Activities.</span></span>
2. <span data-ttu-id="3ba5c-128">Щелкните "Добавить существующее", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3ba5c-128">Click Add existing to open the drop dialog.</span></span>
    * <span data-ttu-id="3ba5c-129">Найдите и выберите существующее мероприятие для добавления в новую версию производственного потока.</span><span class="sxs-lookup"><span data-stu-id="3ba5c-129">Find and select an existing activity to be added to the new production flow version.</span></span>  <span data-ttu-id="3ba5c-130">Обратите внимание, что в списке отображаются все мероприятия, которые были созданы для этого производственного потока для всех предыдущих версий потока.</span><span class="sxs-lookup"><span data-stu-id="3ba5c-130">Note that the list shows all activities that have been created for this production flow for all previous versions of the flow.</span></span>  
3. <span data-ttu-id="3ba5c-131">В поле "Мероприятие" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3ba5c-131">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="3ba5c-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3ba5c-132">Click OK.</span></span>


