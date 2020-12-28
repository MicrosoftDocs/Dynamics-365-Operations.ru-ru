---
title: Управление задачами в POS
description: В этом разделе описывается управление задачами в приложении POS Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cc685fcd584fe2ab5cd9282e8fbefbd284d5b2a2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4415300"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="3b4c1-103">Управление задачами в POS</span><span class="sxs-lookup"><span data-stu-id="3b4c1-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3b4c1-104">В этом разделе описывается управление задачами в приложении POS Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3b4c1-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

## <a name="overview"></a><span data-ttu-id="3b4c1-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="3b4c1-105">Overview</span></span>

<span data-ttu-id="3b4c1-106">Приложение POS Dynamics 365 Commerce содержит функции управления задачами, которые позволяют руководителям и работникам магазинов управлять задачами и обновлять статус задач.</span><span class="sxs-lookup"><span data-stu-id="3b4c1-106">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="3b4c1-107">Работники магазина могут получить доступ к задачам, выбирая плитку **задачи** на домашней странице POS или выбирая уведомления о задачах.</span><span class="sxs-lookup"><span data-stu-id="3b4c1-107">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="3b4c1-108">По умолчанию работники магазина переносятся на вкладку **Мои задачи**, где они могут просматривать назначенные им задачи.</span><span class="sxs-lookup"><span data-stu-id="3b4c1-108">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="3b4c1-109">Однако они могут легко переключаться на **просроченные задачи**, **Открытые задачи** и **Списки задач**.</span><span class="sxs-lookup"><span data-stu-id="3b4c1-109">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="3b4c1-110">Операции задач для руководителей магазинов</span><span class="sxs-lookup"><span data-stu-id="3b4c1-110">Task operations for store managers</span></span>

<span data-ttu-id="3b4c1-111">С помощью кнопок на панели команд руководители магазинов могут выполнять следующие операции задач в приложении POS:</span><span class="sxs-lookup"><span data-stu-id="3b4c1-111">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="3b4c1-112">**Назначить** — назначьте выбранные задачи работнику магазина.</span><span class="sxs-lookup"><span data-stu-id="3b4c1-112">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="3b4c1-113">**Статус задачи** — изменение статуса выбранных задач.</span><span class="sxs-lookup"><span data-stu-id="3b4c1-113">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="3b4c1-114">**Фильтр** — по умолчанию отображаются только активные задачи.</span><span class="sxs-lookup"><span data-stu-id="3b4c1-114">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="3b4c1-115">Однако с помощью фильтров руководители могут просматривать все задачи, даже выполненные или отмененные.</span><span class="sxs-lookup"><span data-stu-id="3b4c1-115">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="3b4c1-116">**Новая задача** — создание задачи в рамках существующего списка задач или создание одноцелевой задачи.</span><span class="sxs-lookup"><span data-stu-id="3b4c1-116">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="3b4c1-117">С помощью кнопок на панели команд работники магазинов могут выполнять следующие операции задач в приложении POS:</span><span class="sxs-lookup"><span data-stu-id="3b4c1-117">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="3b4c1-118">**Статус задачи** — изменение статуса выбранных задач.</span><span class="sxs-lookup"><span data-stu-id="3b4c1-118">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="3b4c1-119">**Фильтр** — по умолчанию отображаются только активные задачи.</span><span class="sxs-lookup"><span data-stu-id="3b4c1-119">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="3b4c1-120">Однако с помощью фильтров работники могут просматривать все задачи, даже выполненные или отмененные.</span><span class="sxs-lookup"><span data-stu-id="3b4c1-120">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="3b4c1-121">На следующем рисунке показана вкладка **мои задачи** в приложении Commerce POS.</span><span class="sxs-lookup"><span data-stu-id="3b4c1-121">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![Вкладка «мои задачи» в приложении Commerce POS](media/POS-task-management.png)

<span data-ttu-id="3b4c1-123">На следующем рисунке показана вкладка **Списки задач**.</span><span class="sxs-lookup"><span data-stu-id="3b4c1-123">The following illustration shows the **Task lists** tab.</span></span>

![Вкладка «Списки задач» в приложении Commerce POS](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="3b4c1-125">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3b4c1-125">Additional resources</span></span>

[<span data-ttu-id="3b4c1-126">Обзор управления задачами</span><span class="sxs-lookup"><span data-stu-id="3b4c1-126">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="3b4c1-127">Настройка управления задачами</span><span class="sxs-lookup"><span data-stu-id="3b4c1-127">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="3b4c1-128">Создание списков задач и добавление задач</span><span class="sxs-lookup"><span data-stu-id="3b4c1-128">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="3b4c1-129">Назначение списков задач магазинам или сотрудникам</span><span class="sxs-lookup"><span data-stu-id="3b4c1-129">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)
