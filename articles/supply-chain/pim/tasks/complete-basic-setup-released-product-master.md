---
title: Завершение базовой настройки шаблона запущенных в производство продуктов
description: В этой теме показано, как выполнить минимальную настройку, необходимую, прежде чем шаблон продукта можно будет использовать в версиях спецификаций.
author: ShylaThompson
manager: AnnBe
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bd7e02c9aea17fbc3312660d0e50cd8bbf39aa3d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845025"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="a05a3-103">Завершение базовой настройки шаблона запущенных в производство продуктов</span><span class="sxs-lookup"><span data-stu-id="a05a3-103">Complete basic setup of a released product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a05a3-104">В этой теме показано, как выполнить минимальную настройку, необходимую, прежде чем шаблон продукта можно будет использовать в версиях спецификаций.</span><span class="sxs-lookup"><span data-stu-id="a05a3-104">This topic shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="a05a3-105">Это третья процедура из восьми, в которых поясняется, как строить сочетания для конфигурации на основе аналитик.</span><span class="sxs-lookup"><span data-stu-id="a05a3-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="a05a3-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="a05a3-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="a05a3-107">Перейдите в раздел **Область переходов > Модули > Управление сведениями о продукте > Продукты > Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="a05a3-107">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="a05a3-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a05a3-108">In the list, find and select the desired record.</span></span> <span data-ttu-id="a05a3-109">Выберите шаблон продукта, который вы запустили в производство во второй процедуре.</span><span class="sxs-lookup"><span data-stu-id="a05a3-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="a05a3-110">Этот шаблон продукта создан с использованием технологии конфигурации на основе аналитик.</span><span class="sxs-lookup"><span data-stu-id="a05a3-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="a05a3-111">В области панели операций выберите **Продукт**.</span><span class="sxs-lookup"><span data-stu-id="a05a3-111">On the Action Pane, select **Product**.</span></span>
4. <span data-ttu-id="a05a3-112">Выберите **Группы аналитики**, чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a05a3-112">Select **Dimension groups** to open the drop dialog.</span></span>
5. <span data-ttu-id="a05a3-113">В поле **Группа аналитик хранения** выберите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a05a3-113">In the **Storage dimension group** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a05a3-114">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a05a3-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="a05a3-115">Группа аналитик хранения определяет, какие аналитики хранения используются для проводки продукта.</span><span class="sxs-lookup"><span data-stu-id="a05a3-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="a05a3-116">Для этой процедуры выберите **Сайт**.</span><span class="sxs-lookup"><span data-stu-id="a05a3-116">Select **Site** for this procedure.</span></span>  
7. <span data-ttu-id="a05a3-117">В поле **Группа аналитик отслеживания** выберите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a05a3-117">In the **Tracking dimension group** field, select the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="a05a3-118">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a05a3-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="a05a3-119">Группа аналитик отслеживания определяет, какие аналитики отслеживания используются для проводки продукта.</span><span class="sxs-lookup"><span data-stu-id="a05a3-119">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="a05a3-120">Для этой процедуры выберите **Нет**.</span><span class="sxs-lookup"><span data-stu-id="a05a3-120">Select **None** for this procedure.</span></span>  
9. <span data-ttu-id="a05a3-121">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="a05a3-121">Click **OK**.</span></span>
10. <span data-ttu-id="a05a3-122">Выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="a05a3-122">Click **Edit**.</span></span>
11. <span data-ttu-id="a05a3-123">В поле **Группа номенклатурных моделей** выберите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a05a3-123">In the **Item model group** field, select the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="a05a3-124">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a05a3-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="a05a3-125">В группе номенклатурных моделей содержатся настройки, определяющие порядок контроля и управления приходом и расходом номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="a05a3-125">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="a05a3-126">Они также определяют расчет потребления номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="a05a3-126">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="a05a3-127">Для этой процедуры выберите **ФИФО**.</span><span class="sxs-lookup"><span data-stu-id="a05a3-127">Select **FIFO** for this procedure.</span></span>  
13. <span data-ttu-id="a05a3-128">Разверните раздел **Управление затратами**.</span><span class="sxs-lookup"><span data-stu-id="a05a3-128">Expand the **Manage costs** section.</span></span>
14. <span data-ttu-id="a05a3-129">В поле **Группа номенклатур** выберите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a05a3-129">In the **Item group** field, select the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="a05a3-130">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a05a3-130">In the list, find and select the desired record.</span></span> <span data-ttu-id="a05a3-131">Номенклатурные группы используются для управления запасами, распределенными по группам.</span><span class="sxs-lookup"><span data-stu-id="a05a3-131">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="a05a3-132">Для этой процедуры выберите **CarAudio**.</span><span class="sxs-lookup"><span data-stu-id="a05a3-132">Select **CarAudio** for this procedure.</span></span>  
16. <span data-ttu-id="a05a3-133">В области действий выберите **План**.</span><span class="sxs-lookup"><span data-stu-id="a05a3-133">On the Action Pane, select **Plan**.</span></span>
17. <span data-ttu-id="a05a3-134">Выберите **Параметры заказа по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="a05a3-134">Select **Default order settings**.</span></span>
18. <span data-ttu-id="a05a3-135">В поле **Тип заказа по умолчанию** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="a05a3-135">In the **Default order type field**, select an option.</span></span> <span data-ttu-id="a05a3-136">Выберите **Производство**, чтобы указать, что вариант поставки по умолчанию для данного шаблона продукта по умолчанию — это его производство.</span><span class="sxs-lookup"><span data-stu-id="a05a3-136">Select **Production** to specify that the default supply option for this product master is to produce it.</span></span>  
19. <span data-ttu-id="a05a3-137">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="a05a3-137">Select **Save**.</span></span>
20. <span data-ttu-id="a05a3-138">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a05a3-138">Close the page.</span></span>
21. <span data-ttu-id="a05a3-139">Закройте форму **Сведения о выпущенном продукте**.</span><span class="sxs-lookup"><span data-stu-id="a05a3-139">Close the **Released product details** form.</span></span>

