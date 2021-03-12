---
title: Настройка параллельных ветвей в workflow-процессе
description: Чтобы настроить параллельную ветвь, необходимо выполнить следующие действия в редакторе workflow-процессов.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196043
ms.assetid: dfdae2b8-6a4f-4760-b339-b755c66f3f89
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d23e981526fd17a3cb856fffcc39e76cf24da68
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797709"
---
# <a name="configure-parallel-branches-in-a-workflow"></a><span data-ttu-id="eca53-103">Настройка параллельных ветвей в workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="eca53-103">Configure parallel branches in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eca53-104">Чтобы настроить параллельную ветвь, необходимо выполнить следующие действия в редакторе workflow-процессов.</span><span class="sxs-lookup"><span data-stu-id="eca53-104">To configure a parallel branch, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="eca53-105">Параллельная ветвь — это по сути workflow-процесс, который выполняется в контексте родительского workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="eca53-105">A parallel branch is essentially a workflow that runs in the context of a parent workflow.</span></span>

## <a name="name-a-branch"></a><span data-ttu-id="eca53-106">Имя ветви</span><span class="sxs-lookup"><span data-stu-id="eca53-106">Name a branch</span></span>

<span data-ttu-id="eca53-107">Чтобы ввести название параллельной ветви, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="eca53-107">Follow these steps to enter a name for a parallel branch.</span></span>

1. <span data-ttu-id="eca53-108">Щелкните правой кнопкой мыши параллельную ветвь и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="eca53-108">Right-click the parallel branch, and then click **Properties**.</span></span> <span data-ttu-id="eca53-109">Будет открыта форма **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="eca53-109">The **Properties** form is displayed.</span></span>
2. <span data-ttu-id="eca53-110">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="eca53-110">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="eca53-111">В поле **Имя** введите уникальное имя для параллельной ветви.</span><span class="sxs-lookup"><span data-stu-id="eca53-111">In the **Name** field, enter a unique name for the parallel branch.</span></span>
4. <span data-ttu-id="eca53-112">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="eca53-112">Click **Close**.</span></span>

## <a name="design-and-configure-the-elements-of-a-branch"></a><span data-ttu-id="eca53-113">Создание и настройка элементов ветви</span><span class="sxs-lookup"><span data-stu-id="eca53-113">Design and configure the elements of a branch</span></span>

<span data-ttu-id="eca53-114">Выполните следующие действия, чтобы создать и настроить элементы параллельной ветви.</span><span class="sxs-lookup"><span data-stu-id="eca53-114">Follow these steps to design and configure the elements of a parallel branch.</span></span>

1. <span data-ttu-id="eca53-115">Дважды щелкните параллельную ветвь.</span><span class="sxs-lookup"><span data-stu-id="eca53-115">Double-click the parallel branch.</span></span>
2. <span data-ttu-id="eca53-116">Перетащите элементы workflow-процесса на холст, а затем настройте элементы, как и любой другой workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="eca53-116">Drag workflow elements onto the canvas, and then configure the elements, just as you would to create any other workflow.</span></span> <span data-ttu-id="eca53-117">Дополнительные сведения см. в разделе [Обзор создания бизнес-правил](create-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="eca53-117">For more information, see [Create workflows overview](create-workflow.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eca53-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="eca53-118">Additional resources</span></span>

[<span data-ttu-id="eca53-119">Обзор создания бизнес-правил</span><span class="sxs-lookup"><span data-stu-id="eca53-119">Create workflows overview</span></span>](create-workflow.md)
