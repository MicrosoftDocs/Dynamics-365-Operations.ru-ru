---
title: Отправка и утверждение бюджета проекта
description: В этой процедуре показано, как создать и отправить бюджет для проекта.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f727e19d3f8c424b1c59e52602b7e907151f4492
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569853"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="b00cb-103">Отправка и утверждение бюджета проекта</span><span class="sxs-lookup"><span data-stu-id="b00cb-103">Submit and approve project budget</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b00cb-104">В этой процедуре показано, как создать и отправить бюджет для проекта.</span><span class="sxs-lookup"><span data-stu-id="b00cb-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="b00cb-105">При создании бюджета проекта можно ввести расчетные значения доходов и затрат по проекту, а затем использовать их для контроля фактических проводок по проекту.</span><span class="sxs-lookup"><span data-stu-id="b00cb-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="b00cb-106">В бюджетировании проекта все исходные бюджеты и изменения должны отправляться в workflow-процесс проекта на утверждение.</span><span class="sxs-lookup"><span data-stu-id="b00cb-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="b00cb-107">Workflow-процессы обеспечивают более жесткий контроль над процессами и позволяют вести историю изменений.</span><span class="sxs-lookup"><span data-stu-id="b00cb-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="b00cb-108">Эта задача была создана с использованием набора данных USSI.</span><span class="sxs-lookup"><span data-stu-id="b00cb-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="b00cb-109">Перейдите в раздел "Управление и учет по проектам" > "Проекты" > "Все проекты".</span><span class="sxs-lookup"><span data-stu-id="b00cb-109">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="b00cb-110">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="b00cb-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b00cb-111">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="b00cb-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b00cb-112">В области действий щелкните "План".</span><span class="sxs-lookup"><span data-stu-id="b00cb-112">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="b00cb-113">Щелкните "Бюджет проекта".</span><span class="sxs-lookup"><span data-stu-id="b00cb-113">Click Project budget.</span></span>
6. <span data-ttu-id="b00cb-114">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b00cb-114">In the Description field, type a value.</span></span>
7. <span data-ttu-id="b00cb-115">Разверните раздел "Стоимость".</span><span class="sxs-lookup"><span data-stu-id="b00cb-115">Expand the Cost section</span></span>
8. <span data-ttu-id="b00cb-116">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b00cb-116">Click New.</span></span>
9. <span data-ttu-id="b00cb-117">В поле "Тип проводки" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="b00cb-117">In the Transaction type field, select an option.</span></span>
10. <span data-ttu-id="b00cb-118">В поле "Категория" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b00cb-118">In the Category field, enter or select a value.</span></span>
11. <span data-ttu-id="b00cb-119">В поле "Исходный бюджет" введите число.</span><span class="sxs-lookup"><span data-stu-id="b00cb-119">In the Original budget field, enter a number.</span></span>
12. <span data-ttu-id="b00cb-120">Разверните раздел "Выручка".</span><span class="sxs-lookup"><span data-stu-id="b00cb-120">Expand the Revenues section.</span></span>
13. <span data-ttu-id="b00cb-121">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b00cb-121">Click New.</span></span>
14. <span data-ttu-id="b00cb-122">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="b00cb-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="b00cb-123">В поле "Тип проводки" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="b00cb-123">In the Transaction type field, select an option.</span></span>
16. <span data-ttu-id="b00cb-124">В поле "Категория" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b00cb-124">In the Category field, enter or select a value.</span></span>
17. <span data-ttu-id="b00cb-125">В поле "Исходный бюджет" введите число.</span><span class="sxs-lookup"><span data-stu-id="b00cb-125">In the Original budget field, enter a number.</span></span>
18. <span data-ttu-id="b00cb-126">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="b00cb-126">Click Save.</span></span>
19. <span data-ttu-id="b00cb-127">Щелкните "Бизнес-правило".</span><span class="sxs-lookup"><span data-stu-id="b00cb-127">Click Workflow.</span></span>
20. <span data-ttu-id="b00cb-128">Щелкните Отправить.</span><span class="sxs-lookup"><span data-stu-id="b00cb-128">Click Submit.</span></span>
21. <span data-ttu-id="b00cb-129">В поле "Комментарий" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b00cb-129">In the Comment field, type a value.</span></span>
22. <span data-ttu-id="b00cb-130">Щелкните Отправить.</span><span class="sxs-lookup"><span data-stu-id="b00cb-130">Click Submit.</span></span>

