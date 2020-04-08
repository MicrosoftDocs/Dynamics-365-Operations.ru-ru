---
title: Инициализация уровней запасов на складе
description: В этой процедуре показано, как вручную загружать обновлять запасы в наличии с использованием журнала складских проводок.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f922620c7aeeafd8560316239875c1ec5486191
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145694"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a><span data-ttu-id="6d30f-103">Инициализация уровней запасов на складе</span><span class="sxs-lookup"><span data-stu-id="6d30f-103">Initialize stock levels in the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6d30f-104">В этой процедуре показано, как вручную загружать обновлять запасы в наличии с использованием журнала складских проводок.</span><span class="sxs-lookup"><span data-stu-id="6d30f-104">This procedure shows you how to get the on-hand inventory updated manually using an Inventory movement journal.</span></span> <span data-ttu-id="6d30f-105">(Также можно обновить запасы в наличии, импортируя проводки в информационных объектах.) Это руководство можно выполнить в компании USMF для демонстрационных данных, где все условия, такие как наименование журнала, настройка номенклатуры, профили разносок и счета, доступны.</span><span class="sxs-lookup"><span data-stu-id="6d30f-105">(It's also possible to update on-hand inventory by importing transactions in data entities.) You can run this guide in demo data company USMF where all the prerequisites like journal name, item setup, posting profiles, and accounts are available.</span></span> <span data-ttu-id="6d30f-106">В руководство имеются конкретные значения для номенклатуры и аналитик, которые используются.</span><span class="sxs-lookup"><span data-stu-id="6d30f-106">The guide suggests specific values for the item and dimensions that are used.</span></span> <span data-ttu-id="6d30f-107">При выборе другой номенклатуры может потребоваться ввести значения для других аналитик.</span><span class="sxs-lookup"><span data-stu-id="6d30f-107">If you choose a different item, you may need to enter values for different dimensions.</span></span>

1. <span data-ttu-id="6d30f-108">Перейдите в раздел "Управление запасами" > "Записи журнала" > "Номенклатуры" > "Движение".</span><span class="sxs-lookup"><span data-stu-id="6d30f-108">Go to Inventory management > Journal entries > Items > Movement.</span></span>
2. <span data-ttu-id="6d30f-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6d30f-109">Click New.</span></span>
3. <span data-ttu-id="6d30f-110">В поле "Имя" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="6d30f-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6d30f-111">Выберите IMov.</span><span class="sxs-lookup"><span data-stu-id="6d30f-111">Select IMov.</span></span>
    * <span data-ttu-id="6d30f-112">Рекомендуется использовать разные шаблоны имен журналов для разных деловых целей.</span><span class="sxs-lookup"><span data-stu-id="6d30f-112">It's a good practice to use different journal name templates for the different business purposes.</span></span>  
5. <span data-ttu-id="6d30f-113">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="6d30f-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="6d30f-114">В поле "Корр.счет" укажите требуемые значения "140200".</span><span class="sxs-lookup"><span data-stu-id="6d30f-114">In the Offset account field, specify the values '140200'.</span></span>
    * <span data-ttu-id="6d30f-115">Это корреспондирующий счет, который будет счетом по умолчанию в строках журнала.</span><span class="sxs-lookup"><span data-stu-id="6d30f-115">This is the offset account that will be the default account on the journal lines.</span></span> <span data-ttu-id="6d30f-116">Можно переопределить значение по умолчанию, чтобы назначить разные корр. счета в строках.</span><span class="sxs-lookup"><span data-stu-id="6d30f-116">It's possible to override the default to assign different offset accounts per line.</span></span>  
7. <span data-ttu-id="6d30f-117">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="6d30f-117">Click OK.</span></span>
8. <span data-ttu-id="6d30f-118">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6d30f-118">Click New.</span></span>
9. <span data-ttu-id="6d30f-119">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="6d30f-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="6d30f-120">Выберите номенклатуру A0001.</span><span class="sxs-lookup"><span data-stu-id="6d30f-120">Select item A0001.</span></span>
11. <span data-ttu-id="6d30f-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="6d30f-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="6d30f-122">Перейдите на вкладку "Складские аналитики".</span><span class="sxs-lookup"><span data-stu-id="6d30f-122">Click the Inventory dimensions tab.</span></span>
13. <span data-ttu-id="6d30f-123">В поле "Сайт" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="6d30f-123">In the Site field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="6d30f-124">Выберите сайт 1.</span><span class="sxs-lookup"><span data-stu-id="6d30f-124">Select site 1.</span></span>
15. <span data-ttu-id="6d30f-125">В поле "Склад" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="6d30f-125">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="6d30f-126">Выберите склад 13.</span><span class="sxs-lookup"><span data-stu-id="6d30f-126">Select warehouse 13.</span></span>
17. <span data-ttu-id="6d30f-127">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="6d30f-127">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="6d30f-128">В поле "Местонахождение" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="6d30f-128">In the Location field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="6d30f-129">Выберите местонахождение 13.</span><span class="sxs-lookup"><span data-stu-id="6d30f-129">Select location 13.</span></span>
20. <span data-ttu-id="6d30f-130">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="6d30f-130">In the Quantity field, enter a number.</span></span>
21. <span data-ttu-id="6d30f-131">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6d30f-131">Click Save.</span></span>
22. <span data-ttu-id="6d30f-132">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="6d30f-132">Click Post.</span></span>
23. <span data-ttu-id="6d30f-133">Установите или снимите флажок "Перенести все ошибки разноски в новый журнал".</span><span class="sxs-lookup"><span data-stu-id="6d30f-133">Check or uncheck the Transfer all posting errors to a new journal check box.</span></span>
    * <span data-ttu-id="6d30f-134">При включении этого параметра строки, которые не могут быть разнесены, будут скопированы в новый журнал.</span><span class="sxs-lookup"><span data-stu-id="6d30f-134">If you enable this option, any lines that fail to post will be copied to a new journal.</span></span> <span data-ttu-id="6d30f-135">Можно использовать сведения в журнале, чтобы скорректировать проблемы, а затем повторно разнести строки.</span><span class="sxs-lookup"><span data-stu-id="6d30f-135">You can use the information in the log to correct the issues and then re-post the lines.</span></span>  
24. <span data-ttu-id="6d30f-136">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="6d30f-136">Click OK.</span></span>
25. <span data-ttu-id="6d30f-137">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6d30f-137">Close the page.</span></span>
26. <span data-ttu-id="6d30f-138">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6d30f-138">Close the page.</span></span>

