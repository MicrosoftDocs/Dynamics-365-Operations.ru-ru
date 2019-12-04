---
title: Настройка параллельных действий в workflow-процессе
description: Чтобы настроить параллельное мероприятие, необходимо выполнить следующие действия в редакторе workflow-процессов.
author: sericks007
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
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14b4410a0bd177159817cd5116a5a0d959992ad5
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812417"
---
# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="63d9d-103">Настройка параллельных действий в workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="63d9d-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63d9d-104">Чтобы настроить параллельное мероприятие, необходимо выполнить следующие действия в редакторе workflow-процессов.</span><span class="sxs-lookup"><span data-stu-id="63d9d-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="63d9d-105">Параллельное мероприятие состоит из ветвей workflow-процесса, которые выполняются одновременно.</span><span class="sxs-lookup"><span data-stu-id="63d9d-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="63d9d-106">Наименование параллельного действия</span><span class="sxs-lookup"><span data-stu-id="63d9d-106">Name a parallel activity</span></span>

<span data-ttu-id="63d9d-107">Чтобы ввести название параллельного мероприятия, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="63d9d-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="63d9d-108">Щелкните правой кнопкой мыши параллельное мероприятие, затем щелкните **Свойства**, чтобы открыть форму **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="63d9d-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="63d9d-109">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="63d9d-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="63d9d-110">В поле **Имя** введите уникальное имя для параллельного мероприятия.</span><span class="sxs-lookup"><span data-stu-id="63d9d-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="63d9d-111">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="63d9d-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="63d9d-112">Настройте ветви параллельного мероприятия</span><span class="sxs-lookup"><span data-stu-id="63d9d-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="63d9d-113">Выполните следующие действия, чтобы добавить и настроить ветви данного параллельного мероприятия.</span><span class="sxs-lookup"><span data-stu-id="63d9d-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="63d9d-114">Дважды щелкните параллельное мероприятие для отображения ветвей параллельного мероприятия.</span><span class="sxs-lookup"><span data-stu-id="63d9d-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="63d9d-115">Для добавления ветви, перетащите элемент **Ветвь** из зоны **Элементы workflow-процесса** в точку вставки на холст.</span><span class="sxs-lookup"><span data-stu-id="63d9d-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="63d9d-116">На следующем рисунке показана точка вставки.</span><span class="sxs-lookup"><span data-stu-id="63d9d-116">The following figure shows an insertion point.</span></span>

    ![Точка вставки](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="63d9d-118">Порядок ветвлений не важен, поскольку все ветви параллельного мероприятия выполняются одновременно.</span><span class="sxs-lookup"><span data-stu-id="63d9d-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="63d9d-119">Для настройки каждой ветви см. раздел [Настройка параллельных ветвей в workflow-процессе](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="63d9d-119">To configure each branch, see [Configure parallel branches in a workflow](configure-parallel-branch-workflow.md).</span></span>
