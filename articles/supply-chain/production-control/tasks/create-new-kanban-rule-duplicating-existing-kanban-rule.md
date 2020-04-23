---
title: Создание правила канбана путем копирования имеющегося правила канбана
description: Эта процедура описывает создание дубликата существующего правила канбана.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 84a0093d95c2f7084c7a0ed17f8b2f86d654b5d7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212226"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="0b715-103">Создание правила канбана путем копирования имеющегося правила канбана</span><span class="sxs-lookup"><span data-stu-id="0b715-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b715-104">Эта процедура описывает создание дубликата существующего правила канбана.</span><span class="sxs-lookup"><span data-stu-id="0b715-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="0b715-105">Это полезно, если нужно создать новые правила канбана на основе существующих правил канбана.</span><span class="sxs-lookup"><span data-stu-id="0b715-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="0b715-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="0b715-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0b715-107">Эта процедура предназначена для инженер-технолога или менеджера потока создания ценности, так как он подготавливает производство измененного производственного потока нового или нового правила пополнения.</span><span class="sxs-lookup"><span data-stu-id="0b715-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="0b715-108">Выберите правило канбана</span><span class="sxs-lookup"><span data-stu-id="0b715-108">Select a kanban rule</span></span>
1. <span data-ttu-id="0b715-109">Перейти к правилам канбана.</span><span class="sxs-lookup"><span data-stu-id="0b715-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="0b715-110">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="0b715-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0b715-111">Выберите правило канбана 000017 для продукта M0006.</span><span class="sxs-lookup"><span data-stu-id="0b715-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="0b715-112">Дублировать правило канбана</span><span class="sxs-lookup"><span data-stu-id="0b715-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="0b715-113">Щелкните "Дублировать правило канбана".</span><span class="sxs-lookup"><span data-stu-id="0b715-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="0b715-114">Дублируя правило канбана, можно изменить тип, даты, мероприятия и выбор продукта.</span><span class="sxs-lookup"><span data-stu-id="0b715-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="0b715-115">Изменение продукта для этой процедуры выполняется на следующем этапе.</span><span class="sxs-lookup"><span data-stu-id="0b715-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="0b715-116">В поле "Продукт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="0b715-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="0b715-117">Выберите M0007.</span><span class="sxs-lookup"><span data-stu-id="0b715-117">Select M0007.</span></span>  
3. <span data-ttu-id="0b715-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="0b715-118">Click OK.</span></span>
    * <span data-ttu-id="0b715-119">Обратите внимание, что создается дубликат правила канбана 000017.</span><span class="sxs-lookup"><span data-stu-id="0b715-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    

