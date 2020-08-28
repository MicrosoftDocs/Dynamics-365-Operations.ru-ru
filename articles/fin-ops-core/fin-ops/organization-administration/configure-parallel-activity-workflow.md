---
title: Настройка параллельных действий в workflow-процессе
description: Чтобы настроить параллельное мероприятие, необходимо выполнить следующие действия в редакторе workflow-процессов.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 998ee559a092c4acd34a6df05e893bdbf4289099
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698323"
---
# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="d7454-103">Настройка параллельных действий в workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="d7454-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7454-104">Чтобы настроить параллельное мероприятие, необходимо выполнить следующие действия в редакторе workflow-процессов.</span><span class="sxs-lookup"><span data-stu-id="d7454-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="d7454-105">Параллельное мероприятие состоит из ветвей workflow-процесса, которые выполняются одновременно.</span><span class="sxs-lookup"><span data-stu-id="d7454-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="d7454-106">Наименование параллельного действия</span><span class="sxs-lookup"><span data-stu-id="d7454-106">Name a parallel activity</span></span>

<span data-ttu-id="d7454-107">Чтобы ввести название параллельного мероприятия, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d7454-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="d7454-108">Щелкните правой кнопкой мыши параллельное мероприятие, затем щелкните **Свойства**, чтобы открыть форму **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="d7454-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="d7454-109">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="d7454-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="d7454-110">В поле **Имя** введите уникальное имя для параллельного мероприятия.</span><span class="sxs-lookup"><span data-stu-id="d7454-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="d7454-111">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="d7454-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="d7454-112">Настройте ветви параллельного мероприятия</span><span class="sxs-lookup"><span data-stu-id="d7454-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="d7454-113">Выполните следующие действия, чтобы добавить и настроить ветви данного параллельного мероприятия.</span><span class="sxs-lookup"><span data-stu-id="d7454-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="d7454-114">Дважды щелкните параллельное мероприятие для отображения ветвей параллельного мероприятия.</span><span class="sxs-lookup"><span data-stu-id="d7454-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="d7454-115">Для добавления ветви, перетащите элемент **Ветвь** из зоны **Элементы workflow-процесса** в точку вставки на холст.</span><span class="sxs-lookup"><span data-stu-id="d7454-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="d7454-116">На следующем рисунке показана точка вставки.</span><span class="sxs-lookup"><span data-stu-id="d7454-116">The following figure shows an insertion point.</span></span>

    ![Точка вставки](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="d7454-118">Порядок ветвлений не важен, поскольку все ветви параллельного мероприятия выполняются одновременно.</span><span class="sxs-lookup"><span data-stu-id="d7454-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="d7454-119">Для настройки каждой ветви см. раздел [Настройка параллельных ветвей в workflow-процессе](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="d7454-119">To configure each branch, see [Configure parallel branches in a workflow](configure-parallel-branch-workflow.md).</span></span>
