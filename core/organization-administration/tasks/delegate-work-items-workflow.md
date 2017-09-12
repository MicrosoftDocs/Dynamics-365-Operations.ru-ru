--- 
title: "Делегирование рабочих элементов в workflow-процесс"
description: "Если планируется быть не в офисе или по другой причине вы не сможете работать с рабочими элементами, имеется возможность делегировать или переназначить, рабочие элементы для других пользователей."
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6483307ff89ce79a3ef16bb763e3124ac537a5d8
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="ed9c6-103">Делегирование рабочих элементов в workflow-процесс</span><span class="sxs-lookup"><span data-stu-id="ed9c6-103">Delegate work items in a workflow</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ed9c6-104">Если планируется быть не в офисе или по другой причине вы не сможете работать с рабочими элементами, имеется возможность делегировать или переназначить, рабочие элементы для других пользователей.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-104">If you plan to be out of the office or otherwise unavailable to act on work items, you can delegate, or reassign, your work items to other users.</span></span> <span data-ttu-id="ed9c6-105">Эта процедура позволяет настроить систему для автоматического делегирования рабочих элементов другому пользователю.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-105">This procedure helps you configure the system to automatically delegate your work items to another user.</span></span>



<span data-ttu-id="ed9c6-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-automatic-delegation"></a><span data-ttu-id="ed9c6-107">Настройка автоматического делегирования</span><span class="sxs-lookup"><span data-stu-id="ed9c6-107">Set up automatic delegation</span></span>
1. <span data-ttu-id="ed9c6-108">Перейдите в раздел "Общее" > "Настройка" > "Параметры пользователя".</span><span class="sxs-lookup"><span data-stu-id="ed9c6-108">Go to Common > Setup > User options.</span></span>
2. <span data-ttu-id="ed9c6-109">Щелкните вкладку "Workflow-процесс".</span><span class="sxs-lookup"><span data-stu-id="ed9c6-109">Click the Workflow tab.</span></span>
    * <span data-ttu-id="ed9c6-110">Убедитесь, что раздел "Делегирование" развернут.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-110">Make sure the Delegation section is expanded.</span></span>    <span data-ttu-id="ed9c6-111">Для того, чтобы настроить систему на автоматическое делегирование рабочих элементов для других пользователей, необходимо создать правила делегирования, которые определяют какие определенные типы рабочих элементов делегируются.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-111">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="ed9c6-112">Выполните следующие действия, чтобы создать правило делегирования.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-112">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="ed9c6-113">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-113">Click Add.</span></span>
4. <span data-ttu-id="ed9c6-114">В поле "Область" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-114">In the Scope field, select an option.</span></span>
    * <span data-ttu-id="ed9c6-115">Все - делегирование всех назначенных вам задач или рабочих элементов.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-115">All – Delegate all work items that are assigned to you.</span></span>    <span data-ttu-id="ed9c6-116">Модуль — делегирование только рабочих элементов, которые связаны с конкретным типом workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-116">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="ed9c6-117">При выборе этого параметра необходимо выбрать тип workflow-процесса в поле "Имя".</span><span class="sxs-lookup"><span data-stu-id="ed9c6-117">If you select this option, you must select the type of workflow in the Name field.</span></span>    <span data-ttu-id="ed9c6-118">Workflow-процесс — делегирование только рабочих элементов, которые связаны с конкретным workflow-процессом.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-118">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="ed9c6-119">При выборе этого параметра необходимо выбрать workflow-процесс в поле "Имя".</span><span class="sxs-lookup"><span data-stu-id="ed9c6-119">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="ed9c6-120">В поле "Делегат" выберите пользователя, которому требуется делегировать рабочие элементы.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-120">In the Delegate field, select the user to delegate the work items to.</span></span>
    * <span data-ttu-id="ed9c6-121">В полях "Дата и время начала" и "Дата и время окончания" укажите, когда должны автоматически делегироваться рабочие элементы.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-121">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="ed9c6-122">В поле "Дата и время начала" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-122">In the Start date/time field, enter a date and time.</span></span>
7. <span data-ttu-id="ed9c6-123">В поле "Дата и время окончания" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-123">In the End date/time field, enter a date and time.</span></span>
8. <span data-ttu-id="ed9c6-124">Установите флажок "Включено" для активации правила делегирования.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-124">Select the Enabled check box to activate the delegation rule.</span></span>
    * <span data-ttu-id="ed9c6-125">Если вы выбрали значение "Модуль" для параметра "Область", вы должны выбрать модуль в поле "Имя".</span><span class="sxs-lookup"><span data-stu-id="ed9c6-125">If you selected Module as the Scope, then you must select the module in the Name field.</span></span>    <span data-ttu-id="ed9c6-126">Если вы выбрали значение "Workflow-процесс" для параметра "Область", вы должны выбрать определенный workflow-процесс для делегирования в поле "Имя".</span><span class="sxs-lookup"><span data-stu-id="ed9c6-126">If you selected Workflow as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="ed9c6-127">В поле "Комментарий" введите комментарий, который объясняет, почему вы делегируете рабочие элементы.</span><span class="sxs-lookup"><span data-stu-id="ed9c6-127">In the Comment field, enter a comment that explains why you are delegating the work items.</span></span>


