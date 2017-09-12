--- 
title: "Создание правил конфигурации"
description: "Эта процедура заключается в создании правил конфигурации, которые можно использовать для конфигурации на основе аналитик, чтобы принудительно устанавливать или запрещать определенные сочетания строк спецификации."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c901ebea4fd7423db61ef2c33689e606e33e2434
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="create-configuration-rules"></a><span data-ttu-id="ad222-103">Создание правил конфигурации</span><span class="sxs-lookup"><span data-stu-id="ad222-103">Create configuration rules</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ad222-104">Эта процедура заключается в создании правил конфигурации, которые можно использовать для конфигурации на основе аналитик, чтобы принудительно устанавливать или запрещать определенные сочетания строк спецификации.</span><span class="sxs-lookup"><span data-stu-id="ad222-104">This procedure creates configuration rules that can be used for dimension-based configuration to enforce or prevent certain combinations of BOM lines.</span></span> <span data-ttu-id="ad222-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="ad222-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ad222-106">Это седьмая из восьми процедур, в которых поясняется, как строить сочетания для конфигурации на основе аналитик.</span><span class="sxs-lookup"><span data-stu-id="ad222-106">This is the seventh procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="ad222-107">Перейдите в раздел "Управление сведениями о продукте" > "Спецификации и формулы" > "Спецификации".</span><span class="sxs-lookup"><span data-stu-id="ad222-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="ad222-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="ad222-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ad222-109">Найдите и выберите спецификацию для конфигурации на основе аналитик.</span><span class="sxs-lookup"><span data-stu-id="ad222-109">Find and select the BOM for the dimension-based configuration.</span></span>  
3. <span data-ttu-id="ad222-110">В области действий щелкните "Параметры".</span><span class="sxs-lookup"><span data-stu-id="ad222-110">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="ad222-111">Щелкните "Изменить режим просмотра".</span><span class="sxs-lookup"><span data-stu-id="ad222-111">Click Change view.</span></span>
5. <span data-ttu-id="ad222-112">Щелкните Вид заголовка.</span><span class="sxs-lookup"><span data-stu-id="ad222-112">Click Header view.</span></span>
    * <span data-ttu-id="ad222-113">Откройте представление заголовка для доступа к экспресс-вкладке "Конфигурационный маршрут".</span><span class="sxs-lookup"><span data-stu-id="ad222-113">Open the header view to access the Configuration route FastTab.</span></span>  
6. <span data-ttu-id="ad222-114">Разверните или сверните раздел "Конфигурационный маршрут".</span><span class="sxs-lookup"><span data-stu-id="ad222-114">Expand or collapse the Configuration route section.</span></span>
    * <span data-ttu-id="ad222-115">Экспресс-вкладка "Конфигурационный маршрут" должна находиться в развернутом режиме.</span><span class="sxs-lookup"><span data-stu-id="ad222-115">The Configuration route FastTab must be in the expanded mode.</span></span>  
7. <span data-ttu-id="ad222-116">Щелкните "Правила конфигурации".</span><span class="sxs-lookup"><span data-stu-id="ad222-116">Click Configuration rules.</span></span>
8. <span data-ttu-id="ad222-117">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="ad222-117">Click New.</span></span>
9. <span data-ttu-id="ad222-118">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="ad222-118">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="ad222-119">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="ad222-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ad222-120">Отображаются номенклатуры в текущей конфигурационной группе.</span><span class="sxs-lookup"><span data-stu-id="ad222-120">The items in the current configuration group are displayed.</span></span> <span data-ttu-id="ad222-121">Выберите одну, представляющую условие в правиле.</span><span class="sxs-lookup"><span data-stu-id="ad222-121">Select the one that represents the condition in the rule.</span></span>  
11. <span data-ttu-id="ad222-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="ad222-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="ad222-123">В поле "Метод" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="ad222-123">In the Method field, select an option.</span></span>
    * <span data-ttu-id="ad222-124">Можно принудительно выбирать или снимать выбор с номенклатур из другой конфигурационной группы.</span><span class="sxs-lookup"><span data-stu-id="ad222-124">It is possible to enforce either a selection or a deselection of an item from another configuration group.</span></span>  
13. <span data-ttu-id="ad222-125">В поле "Производная группа" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="ad222-125">In the Derived group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="ad222-126">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="ad222-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="ad222-127">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="ad222-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ad222-128">Выберите требуемую конфигурационную группу.</span><span class="sxs-lookup"><span data-stu-id="ad222-128">Select the desired configuration group.</span></span>  
16. <span data-ttu-id="ad222-129">В поле "Код производной номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="ad222-129">In the Derived item number field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="ad222-130">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="ad222-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ad222-131">Выберите номер номенклатуры, которая будет выбираться или выбор с которой будет сниматься в зависимости от выбранного метода.</span><span class="sxs-lookup"><span data-stu-id="ad222-131">Select the item number that will be either selected or deselected depending on the chosen method.</span></span>  
18. <span data-ttu-id="ad222-132">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ad222-132">Close the page.</span></span>


