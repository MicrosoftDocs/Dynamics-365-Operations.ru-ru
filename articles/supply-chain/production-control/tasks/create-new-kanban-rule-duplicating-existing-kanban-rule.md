--- 
title: "Создание правила канбана путем копирования имеющегося правила канбана"
description: "Эта процедура описывает создание дубликата существующего правила канбана."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6bdd79de9f7dd71c3acbfa32c4decbf0b4593798
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="728b9-103">Создание правила канбана путем копирования имеющегося правила канбана</span><span class="sxs-lookup"><span data-stu-id="728b9-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="728b9-104">Эта процедура описывает создание дубликата существующего правила канбана.</span><span class="sxs-lookup"><span data-stu-id="728b9-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="728b9-105">Это полезно, если нужно создать новые правила канбана на основе существующих правил канбана.</span><span class="sxs-lookup"><span data-stu-id="728b9-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="728b9-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="728b9-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="728b9-107">Эта процедура предназначена для инженер-технолога или менеджера потока создания ценности, так как он подготавливает производство измененного производственного потока нового или нового правила пополнения.</span><span class="sxs-lookup"><span data-stu-id="728b9-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="728b9-108">Выберите правило канбана</span><span class="sxs-lookup"><span data-stu-id="728b9-108">Select a kanban rule</span></span>
1. <span data-ttu-id="728b9-109">Перейти к правилам канбана.</span><span class="sxs-lookup"><span data-stu-id="728b9-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="728b9-110">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="728b9-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="728b9-111">Выберите правило канбана 000017 для продукта M0006.</span><span class="sxs-lookup"><span data-stu-id="728b9-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="728b9-112">Дублировать правило канбана</span><span class="sxs-lookup"><span data-stu-id="728b9-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="728b9-113">Щелкните "Дублировать правило канбана".</span><span class="sxs-lookup"><span data-stu-id="728b9-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="728b9-114">Дублируя правило канбана, можно изменить тип, даты, мероприятия и выбор продукта.</span><span class="sxs-lookup"><span data-stu-id="728b9-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="728b9-115">Изменение продукта для этой процедуры выполняется на следующем этапе.</span><span class="sxs-lookup"><span data-stu-id="728b9-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="728b9-116">В поле "Продукт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="728b9-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="728b9-117">Выберите M0007.</span><span class="sxs-lookup"><span data-stu-id="728b9-117">Select M0007.</span></span>  
3. <span data-ttu-id="728b9-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="728b9-118">Click OK.</span></span>
    * <span data-ttu-id="728b9-119">Обратите внимание, что создается дубликат правила канбана 000017.</span><span class="sxs-lookup"><span data-stu-id="728b9-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    


