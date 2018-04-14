--- 
title: "Создание готового продукта (только для версии от февраля 2016 г.)"
description: "Эта задача рассматривает создание готовой продукции."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 4e01d45c9f1e2a4ec866f18e18827f6dab2cdbd1
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-finished-product-february-2016-only"></a><span data-ttu-id="e9c41-103">Создание готового продукта (только для версии от февраля 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="e9c41-103">Create a finished product (February 2016 only)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e9c41-104">Эта задача рассматривает создание готовой продукции.</span><span class="sxs-lookup"><span data-stu-id="e9c41-104">This task focuses on creating a finished product.</span></span> <span data-ttu-id="e9c41-105">Это первая задача в серии расчетов спецификации.</span><span class="sxs-lookup"><span data-stu-id="e9c41-105">It is the first task in the BOM calculation series.</span></span> <span data-ttu-id="e9c41-106">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="e9c41-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="e9c41-107">Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="e9c41-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="e9c41-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="e9c41-108">Click New.</span></span>
3. <span data-ttu-id="e9c41-109">В поле "Номер продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="e9c41-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="e9c41-110">В целя демонстрации введите BOM_1.</span><span class="sxs-lookup"><span data-stu-id="e9c41-110">For the demonstration, type BOM_1.</span></span>  
4. <span data-ttu-id="e9c41-111">В поле "Группа номенклатурных моделей" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="e9c41-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="e9c41-112">Выберите STD.</span><span class="sxs-lookup"><span data-stu-id="e9c41-112">Select STD.</span></span> <span data-ttu-id="e9c41-113">STD означает "стандартная себестоимость" и является наиболее часто используемой моделью при работе с расчетами затрат.</span><span class="sxs-lookup"><span data-stu-id="e9c41-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="e9c41-114">В поле "Номенклатурная группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="e9c41-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="e9c41-115">Например, выберите "Аудио".</span><span class="sxs-lookup"><span data-stu-id="e9c41-115">For example, select Audio.</span></span> <span data-ttu-id="e9c41-116">Это не окажет влияния на расчеты затрат.</span><span class="sxs-lookup"><span data-stu-id="e9c41-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="e9c41-117">В поле "Группа аналитик хранения" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="e9c41-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e9c41-118">Выберите SiteWH.</span><span class="sxs-lookup"><span data-stu-id="e9c41-118">Select SiteWH.</span></span> <span data-ttu-id="e9c41-119">Только сайт и склад будут использоваться для демонстрации.</span><span class="sxs-lookup"><span data-stu-id="e9c41-119">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="e9c41-120">В поле "Группа аналитик отслеживания" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="e9c41-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e9c41-121">Аналитики отслеживания не будут использоваться для данного примера, выберите "Нет".</span><span class="sxs-lookup"><span data-stu-id="e9c41-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="e9c41-122">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e9c41-122">Click OK.</span></span>
9. <span data-ttu-id="e9c41-123">В области действий щелкните "Управление запасами".</span><span class="sxs-lookup"><span data-stu-id="e9c41-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="e9c41-124">Щелкните "Параметры заказа по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="e9c41-124">Click Default order settings.</span></span>
11. <span data-ttu-id="e9c41-125">В поле "Тип заказа по умолчанию" выберите "Производство".</span><span class="sxs-lookup"><span data-stu-id="e9c41-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="e9c41-126">Поскольку это готовая продукция, которая будет произведена, выберите "Производство".</span><span class="sxs-lookup"><span data-stu-id="e9c41-126">Because this is a finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="e9c41-127">В поле "Сайт покупок" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="e9c41-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="e9c41-128">В целях демонстрации выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="e9c41-128">For the demonstration, select Site 1.</span></span>  
13. <span data-ttu-id="e9c41-129">В поле "Сайт запасов" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="e9c41-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="e9c41-130">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="e9c41-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="e9c41-131">В поле "Сайт продаж" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="e9c41-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="e9c41-132">В этом примере выберите "Cайт 1".</span><span class="sxs-lookup"><span data-stu-id="e9c41-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="e9c41-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e9c41-133">Close the page.</span></span>


