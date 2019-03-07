---
title: Создание правил конфигурации
description: Эта процедура заключается в создании правил конфигурации, которые можно использовать для конфигурации на основе аналитик, чтобы принудительно устанавливать или запрещать определенные сочетания строк спецификации.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a315ddecd2e10f508b86ac8ea18a36df71616963
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "314747"
---
# <a name="create-configuration-rules"></a><span data-ttu-id="9de0b-103">Создание правил конфигурации</span><span class="sxs-lookup"><span data-stu-id="9de0b-103">Create configuration rules</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9de0b-104">Эта процедура заключается в создании правил конфигурации, которые можно использовать для конфигурации на основе аналитик, чтобы принудительно устанавливать или запрещать определенные сочетания строк спецификации.</span><span class="sxs-lookup"><span data-stu-id="9de0b-104">This procedure creates configuration rules that can be used for dimension-based configuration to enforce or prevent certain combinations of BOM lines.</span></span> <span data-ttu-id="9de0b-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="9de0b-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9de0b-106">Это седьмая из восьми процедур, в которых поясняется, как строить сочетания для конфигурации на основе аналитик.</span><span class="sxs-lookup"><span data-stu-id="9de0b-106">This is the seventh procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="9de0b-107">Перейдите в раздел "Управление сведениями о продукте" > "Спецификации и формулы" > "Спецификации".</span><span class="sxs-lookup"><span data-stu-id="9de0b-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="9de0b-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="9de0b-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9de0b-109">Найдите и выберите спецификацию для конфигурации на основе аналитик.</span><span class="sxs-lookup"><span data-stu-id="9de0b-109">Find and select the BOM for the dimension-based configuration.</span></span>  
3. <span data-ttu-id="9de0b-110">В области действий щелкните "Параметры".</span><span class="sxs-lookup"><span data-stu-id="9de0b-110">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="9de0b-111">Щелкните "Изменить режим просмотра".</span><span class="sxs-lookup"><span data-stu-id="9de0b-111">Click Change view.</span></span>
5. <span data-ttu-id="9de0b-112">Щелкните Вид заголовка.</span><span class="sxs-lookup"><span data-stu-id="9de0b-112">Click Header view.</span></span>
    * <span data-ttu-id="9de0b-113">Откройте представление заголовка для доступа к экспресс-вкладке "Конфигурационный маршрут".</span><span class="sxs-lookup"><span data-stu-id="9de0b-113">Open the header view to access the Configuration route FastTab.</span></span>  
6. <span data-ttu-id="9de0b-114">Разверните или сверните раздел "Конфигурационный маршрут".</span><span class="sxs-lookup"><span data-stu-id="9de0b-114">Expand or collapse the Configuration route section.</span></span>
    * <span data-ttu-id="9de0b-115">Экспресс-вкладка "Конфигурационный маршрут" должна находиться в развернутом режиме.</span><span class="sxs-lookup"><span data-stu-id="9de0b-115">The Configuration route FastTab must be in the expanded mode.</span></span>  
7. <span data-ttu-id="9de0b-116">Щелкните "Правила конфигурации".</span><span class="sxs-lookup"><span data-stu-id="9de0b-116">Click Configuration rules.</span></span>
8. <span data-ttu-id="9de0b-117">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9de0b-117">Click New.</span></span>
9. <span data-ttu-id="9de0b-118">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="9de0b-118">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="9de0b-119">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="9de0b-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9de0b-120">Отображаются номенклатуры в текущей конфигурационной группе.</span><span class="sxs-lookup"><span data-stu-id="9de0b-120">The items in the current configuration group are displayed.</span></span> <span data-ttu-id="9de0b-121">Выберите одну, представляющую условие в правиле.</span><span class="sxs-lookup"><span data-stu-id="9de0b-121">Select the one that represents the condition in the rule.</span></span>  
11. <span data-ttu-id="9de0b-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="9de0b-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="9de0b-123">В поле "Метод" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="9de0b-123">In the Method field, select an option.</span></span>
    * <span data-ttu-id="9de0b-124">Можно принудительно выбирать или снимать выбор с номенклатур из другой конфигурационной группы.</span><span class="sxs-lookup"><span data-stu-id="9de0b-124">It is possible to enforce either a selection or a deselection of an item from another configuration group.</span></span>  
13. <span data-ttu-id="9de0b-125">В поле "Производная группа" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="9de0b-125">In the Derived group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="9de0b-126">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="9de0b-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="9de0b-127">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="9de0b-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9de0b-128">Выберите требуемую конфигурационную группу.</span><span class="sxs-lookup"><span data-stu-id="9de0b-128">Select the desired configuration group.</span></span>  
16. <span data-ttu-id="9de0b-129">В поле "Код производной номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="9de0b-129">In the Derived item number field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="9de0b-130">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="9de0b-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9de0b-131">Выберите номер номенклатуры, которая будет выбираться или выбор с которой будет сниматься в зависимости от выбранного метода.</span><span class="sxs-lookup"><span data-stu-id="9de0b-131">Select the item number that will be either selected or deselected depending on the chosen method.</span></span>  
18. <span data-ttu-id="9de0b-132">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9de0b-132">Close the page.</span></span>

