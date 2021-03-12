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
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dfbe78f31082ad0b1272f02e3ae9d7adbd993b1
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797734"
---
# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="caf51-103">Настройка параллельных действий в workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="caf51-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="caf51-104">Чтобы настроить параллельное мероприятие, необходимо выполнить следующие действия в редакторе workflow-процессов.</span><span class="sxs-lookup"><span data-stu-id="caf51-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="caf51-105">Параллельное мероприятие состоит из ветвей workflow-процесса, которые выполняются одновременно.</span><span class="sxs-lookup"><span data-stu-id="caf51-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="caf51-106">Наименование параллельного действия</span><span class="sxs-lookup"><span data-stu-id="caf51-106">Name a parallel activity</span></span>

<span data-ttu-id="caf51-107">Чтобы ввести название параллельного мероприятия, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="caf51-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="caf51-108">Щелкните правой кнопкой мыши параллельное мероприятие, затем щелкните **Свойства**, чтобы открыть форму **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="caf51-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="caf51-109">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="caf51-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="caf51-110">В поле **Имя** введите уникальное имя для параллельного мероприятия.</span><span class="sxs-lookup"><span data-stu-id="caf51-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="caf51-111">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="caf51-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="caf51-112">Настройте ветви параллельного мероприятия</span><span class="sxs-lookup"><span data-stu-id="caf51-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="caf51-113">Выполните следующие действия, чтобы добавить и настроить ветви данного параллельного мероприятия.</span><span class="sxs-lookup"><span data-stu-id="caf51-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="caf51-114">Дважды щелкните параллельное мероприятие для отображения ветвей параллельного мероприятия.</span><span class="sxs-lookup"><span data-stu-id="caf51-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="caf51-115">Для добавления ветви, перетащите элемент **Ветвь** из зоны **Элементы workflow-процесса** в точку вставки на холст.</span><span class="sxs-lookup"><span data-stu-id="caf51-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="caf51-116">На следующем рисунке показана точка вставки.</span><span class="sxs-lookup"><span data-stu-id="caf51-116">The following figure shows an insertion point.</span></span>

    ![Точка вставки](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="caf51-118">Порядок ветвлений не важен, поскольку все ветви параллельного мероприятия выполняются одновременно.</span><span class="sxs-lookup"><span data-stu-id="caf51-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="caf51-119">Для настройки каждой ветви см. раздел [Настройка параллельных ветвей в workflow-процессе](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="caf51-119">To configure each branch, see [Configure parallel branches in a workflow](configure-parallel-branch-workflow.md).</span></span>
