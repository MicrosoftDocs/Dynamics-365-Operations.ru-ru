---
title: Настройка параллельных ветвей в workflow-процессе
description: Чтобы настроить параллельную ветвь, необходимо выполнить следующие действия в редакторе workflow-процессов.
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
ms.custom: 196043
ms.assetid: dfdae2b8-6a4f-4760-b339-b755c66f3f89
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2339c6f901a3ef39ad4f9586b2f391b966a3df98
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190151"
---
# <a name="configure-parallel-branches-in-a-workflow"></a><span data-ttu-id="e1daa-103">Настройка параллельных ветвей в workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="e1daa-103">Configure parallel branches in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1daa-104">Чтобы настроить параллельную ветвь, необходимо выполнить следующие действия в редакторе workflow-процессов.</span><span class="sxs-lookup"><span data-stu-id="e1daa-104">To configure a parallel branch, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="e1daa-105">Параллельная ветвь — это по сути workflow-процесс, который выполняется в контексте родительского workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="e1daa-105">A parallel branch is essentially a workflow that runs in the context of a parent workflow.</span></span>

## <a name="name-a-branch"></a><span data-ttu-id="e1daa-106">Имя ветви</span><span class="sxs-lookup"><span data-stu-id="e1daa-106">Name a branch</span></span>

<span data-ttu-id="e1daa-107">Чтобы ввести название параллельной ветви, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e1daa-107">Follow these steps to enter a name for a parallel branch.</span></span>

1. <span data-ttu-id="e1daa-108">Щелкните правой кнопкой мыши параллельную ветвь и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="e1daa-108">Right-click the parallel branch, and then click **Properties**.</span></span> <span data-ttu-id="e1daa-109">Будет открыта форма **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="e1daa-109">The **Properties** form is displayed.</span></span>
2. <span data-ttu-id="e1daa-110">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="e1daa-110">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="e1daa-111">В поле **Имя** введите уникальное имя для параллельной ветви.</span><span class="sxs-lookup"><span data-stu-id="e1daa-111">In the **Name** field, enter a unique name for the parallel branch.</span></span>
4. <span data-ttu-id="e1daa-112">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="e1daa-112">Click **Close**.</span></span>

## <a name="design-and-configure-the-elements-of-a-branch"></a><span data-ttu-id="e1daa-113">Создание и настройка элементов ветви</span><span class="sxs-lookup"><span data-stu-id="e1daa-113">Design and configure the elements of a branch</span></span>

<span data-ttu-id="e1daa-114">Выполните следующие действия, чтобы создать и настроить элементы параллельной ветви.</span><span class="sxs-lookup"><span data-stu-id="e1daa-114">Follow these steps to design and configure the elements of a parallel branch.</span></span>

1. <span data-ttu-id="e1daa-115">Дважды щелкните параллельную ветвь.</span><span class="sxs-lookup"><span data-stu-id="e1daa-115">Double-click the parallel branch.</span></span>
2. <span data-ttu-id="e1daa-116">Перетащите элементы workflow-процесса на холст, а затем настройте элементы, как и любой другой workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="e1daa-116">Drag workflow elements onto the canvas, and then configure the elements, just as you would to create any other workflow.</span></span> <span data-ttu-id="e1daa-117">Дополнительные сведения см. в разделе [Создание workflow-процесса](create-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="e1daa-117">For more information, see [Create a workflow](create-workflow.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e1daa-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e1daa-118">Additional resources</span></span>

[<span data-ttu-id="e1daa-119">Создание workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="e1daa-119">Create a workflow</span></span>](create-workflow.md)
