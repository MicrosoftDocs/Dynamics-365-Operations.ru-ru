---
title: "Настройка параллельной ветви в workflow-процессе"
description: "Чтобы настроить параллельную ветвь, необходимо выполнить следующие действия в редакторе workflow-процессов."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196043
ms.assetid: dfdae2b8-6a4f-4760-b339-b755c66f3f89
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 41bd03757a347a1b5f189bd50dae2545baaddf20
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="configure-a-parallel-branch-in-a-workflow"></a><span data-ttu-id="bf14d-103">Настройка параллельной ветви в workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="bf14d-103">Configure a parallel branch in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bf14d-104">Чтобы настроить параллельную ветвь, необходимо выполнить следующие действия в редакторе workflow-процессов.</span><span class="sxs-lookup"><span data-stu-id="bf14d-104">To configure a parallel branch, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="bf14d-105">Параллельная ветвь — это по сути workflow-процесс, который выполняется в контексте родительского workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="bf14d-105">A parallel branch is essentially a workflow that runs in the context of a parent workflow.</span></span>

## <a name="name-a-branch"></a><span data-ttu-id="bf14d-106">Имя ветви</span><span class="sxs-lookup"><span data-stu-id="bf14d-106">Name a branch</span></span>
<span data-ttu-id="bf14d-107">Чтобы ввести название параллельной ветви, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="bf14d-107">Follow these steps to enter a name for a parallel branch.</span></span>
1.  <span data-ttu-id="bf14d-108">Щелкните правой кнопкой мыши параллельную ветвь и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="bf14d-108">Right-click the parallel branch, and then click **Properties**.</span></span> <span data-ttu-id="bf14d-109">Будет открыта форма **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="bf14d-109">The **Properties** form is displayed.</span></span>
2.  <span data-ttu-id="bf14d-110">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="bf14d-110">In the left pane, click **Basic Settings**.</span></span>
3.  <span data-ttu-id="bf14d-111">В поле **Имя** введите уникальное имя для параллельной ветви.</span><span class="sxs-lookup"><span data-stu-id="bf14d-111">In the **Name** field, enter a unique name for the parallel branch.</span></span>
4.  <span data-ttu-id="bf14d-112">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="bf14d-112">Click **Close**.</span></span>

## <a name="design-and-configure-the-elements-of-a-branch"></a><span data-ttu-id="bf14d-113">Создание и настройка элементов ветви</span><span class="sxs-lookup"><span data-stu-id="bf14d-113">Design and configure the elements of a branch</span></span>
<span data-ttu-id="bf14d-114">Выполните следующие действия, чтобы создать и настроить элементы параллельной ветви.</span><span class="sxs-lookup"><span data-stu-id="bf14d-114">Follow these steps to design and configure the elements of a parallel branch.</span></span>
1.  <span data-ttu-id="bf14d-115">Дважды щелкните параллельную ветвь.</span><span class="sxs-lookup"><span data-stu-id="bf14d-115">Double-click the parallel branch.</span></span>
2.  <span data-ttu-id="bf14d-116">Перетащите элементы workflow-процесса на холст, а затем настройте элементы, как и любой другой workflow-процесс.</span><span class="sxs-lookup"><span data-stu-id="bf14d-116">Drag workflow elements onto the canvas, and then configure the elements, just as you would to create any other workflow.</span></span> <span data-ttu-id="bf14d-117">Дополнительные сведения см. в разделе "Создание workflow-процесса".</span><span class="sxs-lookup"><span data-stu-id="bf14d-117">For more information, see Create a workflow.</span></span>



<a name="see-also"></a><span data-ttu-id="bf14d-118">См. также</span><span class="sxs-lookup"><span data-stu-id="bf14d-118">See also</span></span>
--------

[<span data-ttu-id="bf14d-119">Создайте workflow-процесс</span><span class="sxs-lookup"><span data-stu-id="bf14d-119">Create a workflow</span></span>](create-workflow.md)




