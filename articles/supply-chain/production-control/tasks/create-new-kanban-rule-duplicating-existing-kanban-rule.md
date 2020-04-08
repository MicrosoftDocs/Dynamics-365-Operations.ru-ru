---
title: Создание правила канбана путем копирования имеющегося правила канбана
description: Эта процедура описывает создание дубликата существующего правила канбана.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bc65dd80221cedd25890037afcb3d2617f22793
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149221"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="69f59-103">Создание правила канбана путем копирования имеющегося правила канбана</span><span class="sxs-lookup"><span data-stu-id="69f59-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="69f59-104">Эта процедура описывает создание дубликата существующего правила канбана.</span><span class="sxs-lookup"><span data-stu-id="69f59-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="69f59-105">Это полезно, если нужно создать новые правила канбана на основе существующих правил канбана.</span><span class="sxs-lookup"><span data-stu-id="69f59-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="69f59-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="69f59-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="69f59-107">Эта процедура предназначена для инженер-технолога или менеджера потока создания ценности, так как он подготавливает производство измененного производственного потока нового или нового правила пополнения.</span><span class="sxs-lookup"><span data-stu-id="69f59-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="69f59-108">Выберите правило канбана</span><span class="sxs-lookup"><span data-stu-id="69f59-108">Select a kanban rule</span></span>
1. <span data-ttu-id="69f59-109">Перейти к правилам канбана.</span><span class="sxs-lookup"><span data-stu-id="69f59-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="69f59-110">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="69f59-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="69f59-111">Выберите правило канбана 000017 для продукта M0006.</span><span class="sxs-lookup"><span data-stu-id="69f59-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="69f59-112">Дублировать правило канбана</span><span class="sxs-lookup"><span data-stu-id="69f59-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="69f59-113">Щелкните "Дублировать правило канбана".</span><span class="sxs-lookup"><span data-stu-id="69f59-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="69f59-114">Дублируя правило канбана, можно изменить тип, даты, мероприятия и выбор продукта.</span><span class="sxs-lookup"><span data-stu-id="69f59-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="69f59-115">Изменение продукта для этой процедуры выполняется на следующем этапе.</span><span class="sxs-lookup"><span data-stu-id="69f59-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="69f59-116">В поле "Продукт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="69f59-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="69f59-117">Выберите M0007.</span><span class="sxs-lookup"><span data-stu-id="69f59-117">Select M0007.</span></span>  
3. <span data-ttu-id="69f59-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="69f59-118">Click OK.</span></span>
    * <span data-ttu-id="69f59-119">Обратите внимание, что создается дубликат правила канбана 000017.</span><span class="sxs-lookup"><span data-stu-id="69f59-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    

