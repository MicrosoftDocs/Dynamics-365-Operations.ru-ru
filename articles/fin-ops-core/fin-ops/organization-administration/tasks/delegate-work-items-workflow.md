---
title: Делегирование рабочих элементов в workflow-процесс
description: Если планируется быть не в офисе или по другой причине вы не сможете работать с рабочими элементами, имеется возможность делегировать или переназначить, рабочие элементы для других пользователей.
author: ChrisGarty
ms.date: 07/07/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed21f6d32cdcf74eb153daba32c20b7cef94d4e4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747377"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="79194-103">Делегирование рабочих элементов в бизнес-правиле</span><span class="sxs-lookup"><span data-stu-id="79194-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="79194-104">Делегирование рабочего элемента вручную</span><span class="sxs-lookup"><span data-stu-id="79194-104">Manually delegate a work item</span></span>

<span data-ttu-id="79194-105">Чтобы делегировать отдельный рабочий элемент, выберите параметр **Делегировать** в меню **Рабочий процесс**, затем введите пользователя для делегирования вместе с комментарием.</span><span class="sxs-lookup"><span data-stu-id="79194-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="79194-106">В результате рабочий элемент будет переназначен этому пользователю для его выполнения.</span><span class="sxs-lookup"><span data-stu-id="79194-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="manually-delegate-multiple-work-items"></a><span data-ttu-id="79194-107">Делегирование нескольких рабочих элементов вручную</span><span class="sxs-lookup"><span data-stu-id="79194-107">Manually delegate multiple work items</span></span>

<span data-ttu-id="79194-108">Несколько рабочих элементов могут быть делегированы вместе со страницы **Рабочие элементы, назначенные мне**.</span><span class="sxs-lookup"><span data-stu-id="79194-108">Multiple work items can be delegated together from the **Work items assigned to me** page.</span></span> <span data-ttu-id="79194-109">Следующие типы рабочих процессов подходят для массового делегирования: рабочей процесс утверждения договора покупки, рабочий процесс заказов на покупку, анализ заявки на покупку и рабочий процесс накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="79194-109">The following workflow types are eligible for mass delegation: Purchase agreement approval workflow, Purchase order workflow, Purchase requisition review, and Vendor invoice workflow.</span></span> <span data-ttu-id="79194-110">Функция **Делегирование нескольких рабочих элементов** по умолчанию отключена и может быть включена в пункте **Рабочие области > Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="79194-110">The **Delegate multiple work items** feature is disabled by default and can be enabled in **Workspaces > Feature management**.</span></span> <span data-ttu-id="79194-111">Обратитесь за помощью к системному администратору, чтобы включить эту функцию.</span><span class="sxs-lookup"><span data-stu-id="79194-111">Contact your system administrator for help with enabling this feature.</span></span>
1.  <span data-ttu-id="79194-112">Перейдите к пункту **Общие > Общие > Рабочие элементы > Рабочие элементы, назначенные мне**.</span><span class="sxs-lookup"><span data-stu-id="79194-112">Go to **Common > Common > Work items > Work items assigned to me**.</span></span>
2.  <span data-ttu-id="79194-113">Выберите рабочие элементы, которые будут делегированы.</span><span class="sxs-lookup"><span data-stu-id="79194-113">Select the work items that will be delegated.</span></span>
3.  <span data-ttu-id="79194-114">Щелкните меню **Делегирование рабочих элементов**.</span><span class="sxs-lookup"><span data-stu-id="79194-114">Click the **Delegate work items** menu.</span></span>
4.  <span data-ttu-id="79194-115">В поле **Пользователь** выберите пользователя, которому требуется делегировать рабочие элементы.</span><span class="sxs-lookup"><span data-stu-id="79194-115">In the **User** field, select the user to delegate the work items to.</span></span>
5.  <span data-ttu-id="79194-116">В поле **Комментарий** введите комментарий, который объясняет, почему вы делегируете рабочие элементы.</span><span class="sxs-lookup"><span data-stu-id="79194-116">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>
6.  <span data-ttu-id="79194-117">Нажмите кнопку **Делегирование рабочих элементов**, чтобы завершить делегирование рабочего элемента.</span><span class="sxs-lookup"><span data-stu-id="79194-117">Click the **Delegate work items** button to complete the work item delegation.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="79194-118">Автоматическое делегирование рабочих элементов</span><span class="sxs-lookup"><span data-stu-id="79194-118">Automatically delegate work items</span></span>

<span data-ttu-id="79194-119">Если вы собираетесь отсутствовать в офисе или по другим причинам будете недоступны для действий над рабочими элементами в течение периода времени, вы можете автоматически делегировать новые рабочие элементы другим пользователям с помощью страницы **Параметры пользователя**.</span><span class="sxs-lookup"><span data-stu-id="79194-119">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="79194-120">Настройка автоматического делегирования</span><span class="sxs-lookup"><span data-stu-id="79194-120">Set up automatic delegation</span></span>
1. <span data-ttu-id="79194-121">Перейдите в раздел **Общее > Настройка > Параметры пользователя**.</span><span class="sxs-lookup"><span data-stu-id="79194-121">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="79194-122">Перейдите на вкладку **Рабочий процесс**. Убедитесь, что раздел делегирования развернут.</span><span class="sxs-lookup"><span data-stu-id="79194-122">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="79194-123">Для того, чтобы настроить систему на автоматическое делегирование рабочих элементов для других пользователей, необходимо создать правила делегирования, которые определяют какие определенные типы рабочих элементов делегируются.</span><span class="sxs-lookup"><span data-stu-id="79194-123">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="79194-124">Выполните следующие действия, чтобы создать правило делегирования.</span><span class="sxs-lookup"><span data-stu-id="79194-124">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="79194-125">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="79194-125">Click **Add**.</span></span>
4. <span data-ttu-id="79194-126">В поле **Область** выберите вариант:</span><span class="sxs-lookup"><span data-stu-id="79194-126">In the **Scope** field, select an option:</span></span>
    - <span data-ttu-id="79194-127">Все - делегирование всех назначенных вам задач или рабочих элементов.</span><span class="sxs-lookup"><span data-stu-id="79194-127">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="79194-128">Модуль — делегирование только рабочих элементов, которые связаны с конкретным типом workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="79194-128">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="79194-129">При выборе этого параметра необходимо выбрать тип рабочего процесса в поле **Имя**.</span><span class="sxs-lookup"><span data-stu-id="79194-129">If you select this option, you must select the type of workflow in the **Name** field.</span></span>
    - <span data-ttu-id="79194-130">Workflow-процесс — делегирование только рабочих элементов, которые связаны с конкретным workflow-процессом.</span><span class="sxs-lookup"><span data-stu-id="79194-130">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="79194-131">При выборе этого параметра необходимо выбрать рабочий процесс в поле **Имя**.</span><span class="sxs-lookup"><span data-stu-id="79194-131">If you select this option, you must select the workflow in the **Name** field.</span></span>  
5. <span data-ttu-id="79194-132">В поле **Имя**:</span><span class="sxs-lookup"><span data-stu-id="79194-132">In the **Name** field:</span></span>
    - <span data-ttu-id="79194-133">Для области **Модуль** выберите целевой модуль.</span><span class="sxs-lookup"><span data-stu-id="79194-133">For **Module** scope, select the target module.</span></span>
    - <span data-ttu-id="79194-134">Для области **Рабочий процесс** выберите целевой рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="79194-134">For **Workflow** scope, select the target workflow.</span></span>
6. <span data-ttu-id="79194-135">В поле **Делегат** выберите пользователя, которому требуется делегировать рабочие элементы.</span><span class="sxs-lookup"><span data-stu-id="79194-135">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="79194-136">В полях **Дата и время начала** и **Дата и время окончания** укажите, когда должны автоматически делегироваться рабочие элементы.</span><span class="sxs-lookup"><span data-stu-id="79194-136">Use the **Start date/time** and **End date/time** fields to specify when you want the work items to be automatically delegated.</span></span>  
7. <span data-ttu-id="79194-137">В поле **Дата и время начала** введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="79194-137">In the **Start date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="79194-138">В поле **Дата и время окончания** введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="79194-138">In the **End date/time** field, enter a date and time.</span></span>
9. <span data-ttu-id="79194-139">Установите флажок **Включено** для активации правила делегирования.</span><span class="sxs-lookup"><span data-stu-id="79194-139">Select the **Enabled** check box to activate the delegation rule.</span></span> 
10. <span data-ttu-id="79194-140">В поле **Комментарий** введите комментарий, который объясняет, почему вы делегируете рабочие элементы.</span><span class="sxs-lookup"><span data-stu-id="79194-140">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]