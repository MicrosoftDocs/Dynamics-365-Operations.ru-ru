---
title: Определение возможностей ресурса
description: Возможности ресурса описывают, что могут делать операционные ресурсы.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6bd3f2b1efc1e6a883ad2a25d127e74a8925de8f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146798"
---
# <a name="define-resource-capabilities"></a><span data-ttu-id="d2ecb-103">Определение возможностей ресурса</span><span class="sxs-lookup"><span data-stu-id="d2ecb-103">Define resource capabilities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d2ecb-104">Возможности ресурса описывают, что могут делать операционные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-104">Resource capabilities describe what operations resources can do.</span></span> <span data-ttu-id="d2ecb-105">Во время планирования требования каждого задания и операции сопоставляются с возможностями доступных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-105">During scheduling, the requirements of each job and operation are matched against the capabilities of the available resources.</span></span> <span data-ttu-id="d2ecb-106">Это руководство по задаче поможет создать способность ресурса и назначить ее ресурсу.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-106">This task guide will help you create a resource capability and assign it to a resource.</span></span> <span data-ttu-id="d2ecb-107">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-107">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-resource-capability"></a><span data-ttu-id="d2ecb-108">Создание возможности ресурса</span><span class="sxs-lookup"><span data-stu-id="d2ecb-108">Create a resource capability</span></span>
1. <span data-ttu-id="d2ecb-109">Перейдите в раздел "Возможности ресурса".</span><span class="sxs-lookup"><span data-stu-id="d2ecb-109">Go to Resource capabilities.</span></span>
2. <span data-ttu-id="d2ecb-110">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-110">Click New.</span></span>
3. <span data-ttu-id="d2ecb-111">В поле "Возможность" введите код возможности ресурса.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-111">In the Capability field, type the ID of the resource capability.</span></span>
    * <span data-ttu-id="d2ecb-112">Для данной операций используйте код возможности, чтобы указать, что ресурсы должны иметь эту возможность для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-112">For a given operation, you use the capability ID to specify that resources must have this capability to perform the operation.</span></span>  
4. <span data-ttu-id="d2ecb-113">В поле "Описание" введите описание возможности.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-113">In the Description field, enter a description of the capability.</span></span>

## <a name="assign-capability-to-a-resource"></a><span data-ttu-id="d2ecb-114">Назначение возможности ресурсу</span><span class="sxs-lookup"><span data-stu-id="d2ecb-114">Assign capability to a resource</span></span>
1. <span data-ttu-id="d2ecb-115">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-115">Click Add.</span></span>
2. <span data-ttu-id="d2ecb-116">В поле "Ресурс" введите код ресурса.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-116">In the Resource field, type the ID of the resource.</span></span>
    * <span data-ttu-id="d2ecb-117">Возможность ресурса можно назначить одному или нескольким ресурсам.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-117">A resource capability can be assigned to one or more resources.</span></span>  
3. <span data-ttu-id="d2ecb-118">В поле "Истечение срока" введите дату.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-118">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="d2ecb-119">Это поле можно использовать для указания того, что ресурс имеет возможность только на ограниченное время.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-119">You can use this field to specify that a resource has the capability for only a limited time.</span></span>  
4. <span data-ttu-id="d2ecb-120">В поле "Приоритет" введите число.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-120">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="d2ecb-121">При планировании заданий и операций можно указать, следует ли выбирать ресурсы по приоритету.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-121">When you schedule jobs and operations, you can specify whether to select resources by priority.</span></span> <span data-ttu-id="d2ecb-122">Если выбрать этот параметр и если нескольких ресурсов могут выполнить задание либо операцию к запрашиваемой дате, будет выбран ресурс с наименьшим приоритетом по отношению к необходимой возможности.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-122">If you choose to do this, and more than one resource can perform the job or operation by the requested date, the resource that has the lowest priority with respect to the required capability is selected.</span></span>  
5. <span data-ttu-id="d2ecb-123">В поле "Уровень" введите число.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-123">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="d2ecb-124">Если указать, что для задания или операции требуется определенная возможность, можно также указать минимальный необходимый уровень.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-124">When you specify that a job or operation requires a particular capability, you can also specify the minimum level that is required.</span></span> <span data-ttu-id="d2ecb-125">Используйте уровень возможности для дифференциации ресурсов, которые могут выполнить одно задание, но различаются по скорости, сильным сторонам, размерам и т. д.</span><span class="sxs-lookup"><span data-stu-id="d2ecb-125">Use the capability level to differentiate resources that can perform the same job, but at different speeds, strengths, sizes, and so on.</span></span>  

