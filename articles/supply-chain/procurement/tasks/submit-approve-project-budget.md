---
title: Отправка и утверждение бюджета проекта
description: В этой процедуре показано, как создать и отправить бюджет для проекта.
author: RichardLuan
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Service industries
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72ac6705ef8584ef41980a1cc9490227538de365
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222857"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="23df0-103">Отправка и утверждение бюджета проекта</span><span class="sxs-lookup"><span data-stu-id="23df0-103">Submit and approve project budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="23df0-104">В этой процедуре показано, как создать и отправить бюджет для проекта.</span><span class="sxs-lookup"><span data-stu-id="23df0-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="23df0-105">При создании бюджета проекта можно ввести расчетные значения доходов и затрат по проекту, а затем использовать их для контроля фактических проводок по проекту.</span><span class="sxs-lookup"><span data-stu-id="23df0-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="23df0-106">В бюджетировании проекта все исходные бюджеты и изменения должны отправляться в workflow-процесс проекта на утверждение.</span><span class="sxs-lookup"><span data-stu-id="23df0-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="23df0-107">Workflow-процессы обеспечивают более жесткий контроль над процессами и позволяют вести историю изменений.</span><span class="sxs-lookup"><span data-stu-id="23df0-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="23df0-108">Эта задача была создана с использованием набора данных USSI.</span><span class="sxs-lookup"><span data-stu-id="23df0-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="23df0-109">В **области переходов** выберите **Модули > Управление и учет по проектам > Проекты > Все проекты**.</span><span class="sxs-lookup"><span data-stu-id="23df0-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="23df0-110">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="23df0-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="23df0-111">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="23df0-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="23df0-112">В области **Панель операций** щелкните **План**.</span><span class="sxs-lookup"><span data-stu-id="23df0-112">On the **Action Pane**, click **Plan**.</span></span>
5. <span data-ttu-id="23df0-113">Щелкните **Бюджет проекта**.</span><span class="sxs-lookup"><span data-stu-id="23df0-113">Click **Project budget**.</span></span>
6. <span data-ttu-id="23df0-114">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="23df0-114">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="23df0-115">Разверните экспресс-вкладку **Затраты**.</span><span class="sxs-lookup"><span data-stu-id="23df0-115">Expand the **Cost** fastTab.</span></span>
8. <span data-ttu-id="23df0-116">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="23df0-116">Click **New**.</span></span>
9. <span data-ttu-id="23df0-117">В поле **Тип проводки** выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="23df0-117">In the **Transaction type** field, select an option.</span></span>
10. <span data-ttu-id="23df0-118">В поле **Категория** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="23df0-118">In the **Category** field, enter or select a value.</span></span>
11. <span data-ttu-id="23df0-119">В поле **Исходный бюджет** введите число.</span><span class="sxs-lookup"><span data-stu-id="23df0-119">In the **Original budget** field, enter a number.</span></span>
12. <span data-ttu-id="23df0-120">Разверните экспресс-вкладку **Выручка**.</span><span class="sxs-lookup"><span data-stu-id="23df0-120">Expand the **Revenues** fastTab.</span></span>
13. <span data-ttu-id="23df0-121">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="23df0-121">Click **New**.</span></span>
14. <span data-ttu-id="23df0-122">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="23df0-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="23df0-123">В поле **Тип проводки** выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="23df0-123">In the **Transaction type** field, select an option.</span></span>
16. <span data-ttu-id="23df0-124">В поле **Категория** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="23df0-124">In the **Category** field, enter or select a value.</span></span>
17. <span data-ttu-id="23df0-125">В поле **Исходный бюджет** введите число.</span><span class="sxs-lookup"><span data-stu-id="23df0-125">In the **Original budget** field, enter a number.</span></span>
18. <span data-ttu-id="23df0-126">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="23df0-126">Click **Save**.</span></span>
19. <span data-ttu-id="23df0-127">Щелкните **Рабочий процесс**.</span><span class="sxs-lookup"><span data-stu-id="23df0-127">Click **Workflow**.</span></span>
20. <span data-ttu-id="23df0-128">Щелкните **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="23df0-128">Click **Submit**.</span></span>
21. <span data-ttu-id="23df0-129">В поле **Комментарий** введите значение.</span><span class="sxs-lookup"><span data-stu-id="23df0-129">In the **Comment** field, type a value.</span></span>
22. <span data-ttu-id="23df0-130">Щелкните **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="23df0-130">Click **Submit**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]