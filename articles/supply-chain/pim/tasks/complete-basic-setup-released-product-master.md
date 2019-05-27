---
title: Завершение базовой настройки шаблона запущенных в производство продуктов
description: В этой процедуре показано, как выполнить минимальную настройку, необходимую, прежде чем шаблон продукта можно будет использовать в версиях спецификаций.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d3a91977c38c0ce0f9fe114bec943c7cb32a5d4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568782"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="3a73c-103">Завершение базовой настройки шаблона запущенных в производство продуктов</span><span class="sxs-lookup"><span data-stu-id="3a73c-103">Complete basic setup of a released product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3a73c-104">В этой процедуре показано, как выполнить минимальную настройку, необходимую, прежде чем шаблон продукта можно будет использовать в версиях спецификаций.</span><span class="sxs-lookup"><span data-stu-id="3a73c-104">This procedure shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="3a73c-105">Это третья процедура из восьми, в которых поясняется, как строить сочетания для конфигурации на основе аналитик.</span><span class="sxs-lookup"><span data-stu-id="3a73c-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="3a73c-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="3a73c-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="3a73c-107">Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="3a73c-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="3a73c-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3a73c-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3a73c-109">Выберите шаблон продукта, который вы запустили в производство во второй процедуре.</span><span class="sxs-lookup"><span data-stu-id="3a73c-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="3a73c-110">Этот шаблон продукта создан с использованием технологии конфигурации на основе аналитик.</span><span class="sxs-lookup"><span data-stu-id="3a73c-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="3a73c-111">В области действий щелкните "Продукт".</span><span class="sxs-lookup"><span data-stu-id="3a73c-111">On the Action Pane, click Product.</span></span>
4. <span data-ttu-id="3a73c-112">Щелкните "Группы аналитики", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3a73c-112">Click Dimension groups to open the drop dialog.</span></span>
5. <span data-ttu-id="3a73c-113">В поле "Группа аналитик хранения" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3a73c-113">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="3a73c-114">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3a73c-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3a73c-115">Группа аналитик хранения определяет, какие аналитики хранения используются для проводки продукта.</span><span class="sxs-lookup"><span data-stu-id="3a73c-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="3a73c-116">Для этой процедуры выберите "Сайт".</span><span class="sxs-lookup"><span data-stu-id="3a73c-116">Select Site for this procedure.</span></span>  
7. <span data-ttu-id="3a73c-117">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3a73c-117">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="3a73c-118">В поле "Группа аналитик отслеживания" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3a73c-118">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="3a73c-119">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3a73c-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3a73c-120">Группа аналитик отслеживания определяет, какие аналитики отслеживания используются для проводки продукта.</span><span class="sxs-lookup"><span data-stu-id="3a73c-120">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="3a73c-121">Для этой процедуры выберите "Нет".</span><span class="sxs-lookup"><span data-stu-id="3a73c-121">Select None for this procedure.</span></span>  
10. <span data-ttu-id="3a73c-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3a73c-122">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="3a73c-123">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3a73c-123">Click OK.</span></span>
12. <span data-ttu-id="3a73c-124">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3a73c-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="3a73c-125">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="3a73c-125">Click Edit.</span></span>
    * <span data-ttu-id="3a73c-126">Откройте форму "Сведения о выпущенном продукте", чтобы продолжить выполнение задачи настройки.</span><span class="sxs-lookup"><span data-stu-id="3a73c-126">Open the Released product details form to continue the setup task.</span></span>  
14. <span data-ttu-id="3a73c-127">В поле "Группа номенклатурных моделей" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3a73c-127">In the Item model group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="3a73c-128">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3a73c-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3a73c-129">В группе номенклатурных моделей содержатся настройки, определяющие порядок контроля и управления приходом и расходом номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="3a73c-129">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="3a73c-130">Они также определяют расчет потребления номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="3a73c-130">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="3a73c-131">Для этой процедуры выберите "ФИФО".</span><span class="sxs-lookup"><span data-stu-id="3a73c-131">Select   FIFO for this procedure.</span></span>  
16. <span data-ttu-id="3a73c-132">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3a73c-132">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="3a73c-133">Разверните или сверните раздел "Управление затратами".</span><span class="sxs-lookup"><span data-stu-id="3a73c-133">Expand or collapse the Manage costs section.</span></span>
18. <span data-ttu-id="3a73c-134">В поле "Номенклатурная группа" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="3a73c-134">In the Item group field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="3a73c-135">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3a73c-135">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3a73c-136">Номенклатурные группы используются для управления запасами, распределенными по группам.</span><span class="sxs-lookup"><span data-stu-id="3a73c-136">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="3a73c-137">Для этой процедуры выберите "CarAudio".</span><span class="sxs-lookup"><span data-stu-id="3a73c-137">Select   CarAudio for this procedure.</span></span>  
20. <span data-ttu-id="3a73c-138">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3a73c-138">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="3a73c-139">В области действий щелкните "План".</span><span class="sxs-lookup"><span data-stu-id="3a73c-139">On the Action Pane, click Plan.</span></span>
22. <span data-ttu-id="3a73c-140">Щелкните "Параметры заказа по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="3a73c-140">Click Default order settings.</span></span>
23. <span data-ttu-id="3a73c-141">В поле "Тип заказа по умолчанию" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="3a73c-141">In the Default order type field, select an option.</span></span>
    * <span data-ttu-id="3a73c-142">Выберите "Производство", чтобы указать, что вариант поставки по умолчанию для данного шаблона продукта по умолчанию — это его производство.</span><span class="sxs-lookup"><span data-stu-id="3a73c-142">Select Production to specify that the default supply option for this product master is to produce it.</span></span>  
24. <span data-ttu-id="3a73c-143">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3a73c-143">Close the page.</span></span>
25. <span data-ttu-id="3a73c-144">Закройте форму "Сведения о выпущенном продукте".</span><span class="sxs-lookup"><span data-stu-id="3a73c-144">Close the Released product details form.</span></span>

