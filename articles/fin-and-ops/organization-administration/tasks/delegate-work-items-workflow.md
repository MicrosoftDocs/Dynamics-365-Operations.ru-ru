---
title: Делегирование рабочих элементов в workflow-процесс
description: Если планируется быть не в офисе или по другой причине вы не сможете работать с рабочими элементами, имеется возможность делегировать или переназначить, рабочие элементы для других пользователей.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44dc747543e32b54729d12c89a401b0187e25a61
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916423"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="dafb7-103">Делегирование рабочих элементов в бизнес-правиле</span><span class="sxs-lookup"><span data-stu-id="dafb7-103">Delegate work items in a workflow</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="dafb7-104">Делегирование рабочего элемента вручную</span><span class="sxs-lookup"><span data-stu-id="dafb7-104">Manually delegate a work item</span></span>

<span data-ttu-id="dafb7-105">Чтобы делегировать отдельный рабочий элемент, выберите параметр **Делегировать** в меню **Рабочий процесс**, затем введите пользователя для делегирования вместе с комментарием.</span><span class="sxs-lookup"><span data-stu-id="dafb7-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="dafb7-106">В результате рабочий элемент будет переназначен этому пользователю для его выполнения.</span><span class="sxs-lookup"><span data-stu-id="dafb7-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="dafb7-107">Автоматическое делегирование рабочих элементов</span><span class="sxs-lookup"><span data-stu-id="dafb7-107">Automatically delegate work items</span></span>

<span data-ttu-id="dafb7-108">Если вы собираетесь отсутствовать в офисе или по другим причинам будете недоступны для действий над рабочими элементами в течение периода времени, вы можете автоматически делегировать новые рабочие элементы другим пользователям с помощью страницы **Параметры пользователя**.</span><span class="sxs-lookup"><span data-stu-id="dafb7-108">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="dafb7-109">Настройка автоматического делегирования</span><span class="sxs-lookup"><span data-stu-id="dafb7-109">Set up automatic delegation</span></span>
1. <span data-ttu-id="dafb7-110">Перейдите в раздел **Общее > Настройка > Параметры пользователя**.</span><span class="sxs-lookup"><span data-stu-id="dafb7-110">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="dafb7-111">Перейдите на вкладку **Рабочий процесс**. Убедитесь, что раздел делегирования развернут.</span><span class="sxs-lookup"><span data-stu-id="dafb7-111">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="dafb7-112">Для того, чтобы настроить систему на автоматическое делегирование рабочих элементов для других пользователей, необходимо создать правила делегирования, которые определяют какие определенные типы рабочих элементов делегируются.</span><span class="sxs-lookup"><span data-stu-id="dafb7-112">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="dafb7-113">Выполните следующие действия, чтобы создать правило делегирования.</span><span class="sxs-lookup"><span data-stu-id="dafb7-113">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="dafb7-114">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="dafb7-114">Click **Add**.</span></span>
4. <span data-ttu-id="dafb7-115">В поле **Область** выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="dafb7-115">In the **Scope** field, select an option.</span></span>
    - <span data-ttu-id="dafb7-116">Все - делегирование всех назначенных вам задач или рабочих элементов.</span><span class="sxs-lookup"><span data-stu-id="dafb7-116">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="dafb7-117">Модуль — делегирование только рабочих элементов, которые связаны с конкретным типом workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="dafb7-117">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="dafb7-118">При выборе этого параметра необходимо выбрать тип workflow-процесса в поле "Имя".</span><span class="sxs-lookup"><span data-stu-id="dafb7-118">If you select this option, you must select the type of workflow in the Name field.</span></span>
    - <span data-ttu-id="dafb7-119">Workflow-процесс — делегирование только рабочих элементов, которые связаны с конкретным workflow-процессом.</span><span class="sxs-lookup"><span data-stu-id="dafb7-119">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="dafb7-120">При выборе этого параметра необходимо выбрать workflow-процесс в поле "Имя".</span><span class="sxs-lookup"><span data-stu-id="dafb7-120">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="dafb7-121">В поле **Делегат** выберите пользователя, которому требуется делегировать рабочие элементы.</span><span class="sxs-lookup"><span data-stu-id="dafb7-121">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="dafb7-122">В полях "Дата и время начала" и "Дата и время окончания" укажите, когда должны автоматически делегироваться рабочие элементы.</span><span class="sxs-lookup"><span data-stu-id="dafb7-122">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="dafb7-123">В поле **Дата и время начала** введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="dafb7-123">In the **Start date/time** field, enter a date and time.</span></span>
7. <span data-ttu-id="dafb7-124">В поле **Дата и время окончания** введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="dafb7-124">In the **End date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="dafb7-125">Установите флажок **Включено** для активации правила делегирования.</span><span class="sxs-lookup"><span data-stu-id="dafb7-125">Select the **Enabled** check box to activate the delegation rule.</span></span> <span data-ttu-id="dafb7-126">Если вы выбрали значение **Модуль** для параметра "Область", вы должны выбрать модуль в поле "Имя".</span><span class="sxs-lookup"><span data-stu-id="dafb7-126">If you selected **Module** as the Scope, then you must select the module in the Name field.</span></span> <span data-ttu-id="dafb7-127">Если вы выбрали значение **Workflow-процесс** для параметра "Область", вы должны выбрать определенный рабочий процесс для делегирования в поле "Имя".</span><span class="sxs-lookup"><span data-stu-id="dafb7-127">If you selected **Workflow** as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="dafb7-128">В поле **Комментарий** введите комментарий, который объясняет, почему вы делегируете рабочие элементы.</span><span class="sxs-lookup"><span data-stu-id="dafb7-128">In the **Comment** field, enter a comment that explains why you are delegating the work items.</span></span>

