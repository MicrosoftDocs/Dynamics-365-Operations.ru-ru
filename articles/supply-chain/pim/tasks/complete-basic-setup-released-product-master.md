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
ms.openlocfilehash: f93f3db022b7b338bfa18ff6aea79f8086ea997f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147948"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="8a140-103">Завершение базовой настройки шаблона запущенных в производство продуктов</span><span class="sxs-lookup"><span data-stu-id="8a140-103">Complete basic setup of a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8a140-104">В этой теме показано, как выполнить минимальную настройку, необходимую, прежде чем шаблон продукта можно будет использовать в версиях спецификаций.</span><span class="sxs-lookup"><span data-stu-id="8a140-104">This topic shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="8a140-105">Это третья процедура из восьми, в которых поясняется, как строить сочетания для конфигурации на основе аналитик.</span><span class="sxs-lookup"><span data-stu-id="8a140-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="8a140-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="8a140-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="8a140-107">Перейдите в раздел **Область переходов > Модули > Управление сведениями о продукте > Продукты > Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="8a140-107">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="8a140-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8a140-108">In the list, find and select the desired record.</span></span> <span data-ttu-id="8a140-109">Выберите шаблон продукта, который вы запустили в производство во второй процедуре.</span><span class="sxs-lookup"><span data-stu-id="8a140-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="8a140-110">Этот шаблон продукта создан с использованием технологии конфигурации на основе аналитик.</span><span class="sxs-lookup"><span data-stu-id="8a140-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="8a140-111">В области панели операций выберите **Продукт**.</span><span class="sxs-lookup"><span data-stu-id="8a140-111">On the Action Pane, select **Product**.</span></span>
4. <span data-ttu-id="8a140-112">Выберите **Группы аналитики**, чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8a140-112">Select **Dimension groups** to open the drop dialog.</span></span>
5. <span data-ttu-id="8a140-113">В поле **Группа аналитик хранения** выберите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8a140-113">In the **Storage dimension group** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="8a140-114">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8a140-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="8a140-115">Группа аналитик хранения определяет, какие аналитики хранения используются для проводки продукта.</span><span class="sxs-lookup"><span data-stu-id="8a140-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="8a140-116">Для этой процедуры выберите **Сайт**.</span><span class="sxs-lookup"><span data-stu-id="8a140-116">Select **Site** for this procedure.</span></span>  
7. <span data-ttu-id="8a140-117">В поле **Группа аналитик отслеживания** выберите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8a140-117">In the **Tracking dimension group** field, select the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="8a140-118">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8a140-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="8a140-119">Группа аналитик отслеживания определяет, какие аналитики отслеживания используются для проводки продукта.</span><span class="sxs-lookup"><span data-stu-id="8a140-119">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="8a140-120">Для этой процедуры выберите **Нет**.</span><span class="sxs-lookup"><span data-stu-id="8a140-120">Select **None** for this procedure.</span></span>  
9. <span data-ttu-id="8a140-121">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a140-121">Click **OK**.</span></span>
10. <span data-ttu-id="8a140-122">Выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="8a140-122">Click **Edit**.</span></span>
11. <span data-ttu-id="8a140-123">В поле **Группа номенклатурных моделей** выберите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8a140-123">In the **Item model group** field, select the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="8a140-124">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8a140-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="8a140-125">В группе номенклатурных моделей содержатся настройки, определяющие порядок контроля и управления приходом и расходом номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="8a140-125">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="8a140-126">Они также определяют расчет потребления номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="8a140-126">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="8a140-127">Для этой процедуры выберите **ФИФО**.</span><span class="sxs-lookup"><span data-stu-id="8a140-127">Select **FIFO** for this procedure.</span></span>  
13. <span data-ttu-id="8a140-128">Разверните раздел **Управление затратами**.</span><span class="sxs-lookup"><span data-stu-id="8a140-128">Expand the **Manage costs** section.</span></span>
14. <span data-ttu-id="8a140-129">В поле **Группа номенклатур** выберите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8a140-129">In the **Item group** field, select the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="8a140-130">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8a140-130">In the list, find and select the desired record.</span></span> <span data-ttu-id="8a140-131">Номенклатурные группы используются для управления запасами, распределенными по группам.</span><span class="sxs-lookup"><span data-stu-id="8a140-131">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="8a140-132">Для этой процедуры выберите **CarAudio**.</span><span class="sxs-lookup"><span data-stu-id="8a140-132">Select **CarAudio** for this procedure.</span></span>  
16. <span data-ttu-id="8a140-133">В области действий выберите **План**.</span><span class="sxs-lookup"><span data-stu-id="8a140-133">On the Action Pane, select **Plan**.</span></span>
17. <span data-ttu-id="8a140-134">Выберите **Параметры заказа по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="8a140-134">Select **Default order settings**.</span></span>
18. <span data-ttu-id="8a140-135">В поле **Тип заказа по умолчанию** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="8a140-135">In the **Default order type field**, select an option.</span></span> <span data-ttu-id="8a140-136">Выберите **Производство**, чтобы указать, что вариант поставки по умолчанию для данного шаблона продукта по умолчанию — это его производство.</span><span class="sxs-lookup"><span data-stu-id="8a140-136">Select **Production** to specify that the default supply option for this product master is to produce it.</span></span>  
19. <span data-ttu-id="8a140-137">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="8a140-137">Select **Save**.</span></span>
20. <span data-ttu-id="8a140-138">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8a140-138">Close the page.</span></span>
21. <span data-ttu-id="8a140-139">Закройте форму **Сведения о выпущенном продукте**.</span><span class="sxs-lookup"><span data-stu-id="8a140-139">Close the **Released product details** form.</span></span>

