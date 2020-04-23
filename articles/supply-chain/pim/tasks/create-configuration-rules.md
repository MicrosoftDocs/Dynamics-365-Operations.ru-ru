---
title: Создание правил конфигурации
description: Эта процедура заключается в создании правил конфигурации, которые можно использовать для конфигурации на основе аналитик, чтобы принудительно устанавливать или запрещать определенные сочетания строк спецификации.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c53ea2eea7dfe3c02d1b21964decc6630d3a41cf
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208279"
---
# <a name="create-configuration-rules"></a><span data-ttu-id="28425-103">Создание правил конфигурации</span><span class="sxs-lookup"><span data-stu-id="28425-103">Create configuration rules</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="28425-104">Эта процедура заключается в создании правил конфигурации, которые можно использовать для конфигурации на основе аналитик, чтобы принудительно устанавливать или запрещать определенные сочетания строк спецификации.</span><span class="sxs-lookup"><span data-stu-id="28425-104">This procedure creates configuration rules that can be used for dimension-based configuration to enforce or prevent certain combinations of BOM lines.</span></span> <span data-ttu-id="28425-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="28425-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="28425-106">Это седьмая из восьми процедур, в которых поясняется, как строить сочетания для конфигурации на основе аналитик.</span><span class="sxs-lookup"><span data-stu-id="28425-106">This is the seventh procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="28425-107">Перейдите в раздел "Управление сведениями о продукте" > "Спецификации и формулы" > "Спецификации".</span><span class="sxs-lookup"><span data-stu-id="28425-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="28425-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="28425-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="28425-109">Найдите и выберите спецификацию для конфигурации на основе аналитик.</span><span class="sxs-lookup"><span data-stu-id="28425-109">Find and select the BOM for the dimension-based configuration.</span></span>  
3. <span data-ttu-id="28425-110">В области действий щелкните "Параметры".</span><span class="sxs-lookup"><span data-stu-id="28425-110">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="28425-111">Щелкните "Изменить режим просмотра".</span><span class="sxs-lookup"><span data-stu-id="28425-111">Click Change view.</span></span>
5. <span data-ttu-id="28425-112">Щелкните Вид заголовка.</span><span class="sxs-lookup"><span data-stu-id="28425-112">Click Header view.</span></span>
    * <span data-ttu-id="28425-113">Откройте представление заголовка для доступа к экспресс-вкладке "Конфигурационный маршрут".</span><span class="sxs-lookup"><span data-stu-id="28425-113">Open the header view to access the Configuration route FastTab.</span></span>  
6. <span data-ttu-id="28425-114">Разверните или сверните раздел "Конфигурационный маршрут".</span><span class="sxs-lookup"><span data-stu-id="28425-114">Expand or collapse the Configuration route section.</span></span>
    * <span data-ttu-id="28425-115">Экспресс-вкладка "Конфигурационный маршрут" должна находиться в развернутом режиме.</span><span class="sxs-lookup"><span data-stu-id="28425-115">The Configuration route FastTab must be in the expanded mode.</span></span>  
7. <span data-ttu-id="28425-116">Щелкните "Правила конфигурации".</span><span class="sxs-lookup"><span data-stu-id="28425-116">Click Configuration rules.</span></span>
8. <span data-ttu-id="28425-117">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="28425-117">Click New.</span></span>
9. <span data-ttu-id="28425-118">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="28425-118">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="28425-119">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="28425-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="28425-120">Отображаются номенклатуры в текущей конфигурационной группе.</span><span class="sxs-lookup"><span data-stu-id="28425-120">The items in the current configuration group are displayed.</span></span> <span data-ttu-id="28425-121">Выберите одну, представляющую условие в правиле.</span><span class="sxs-lookup"><span data-stu-id="28425-121">Select the one that represents the condition in the rule.</span></span>  
11. <span data-ttu-id="28425-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="28425-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="28425-123">В поле "Метод" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="28425-123">In the Method field, select an option.</span></span>
    * <span data-ttu-id="28425-124">Можно принудительно выбирать или снимать выбор с номенклатур из другой конфигурационной группы.</span><span class="sxs-lookup"><span data-stu-id="28425-124">It is possible to enforce either a selection or a deselection of an item from another configuration group.</span></span>  
13. <span data-ttu-id="28425-125">В поле "Производная группа" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="28425-125">In the Derived group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="28425-126">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="28425-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="28425-127">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="28425-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="28425-128">Выберите требуемую конфигурационную группу.</span><span class="sxs-lookup"><span data-stu-id="28425-128">Select the desired configuration group.</span></span>  
16. <span data-ttu-id="28425-129">В поле "Код производной номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="28425-129">In the Derived item number field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="28425-130">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="28425-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="28425-131">Выберите номер номенклатуры, которая будет выбираться или выбор с которой будет сниматься в зависимости от выбранного метода.</span><span class="sxs-lookup"><span data-stu-id="28425-131">Select the item number that will be either selected or deselected depending on the chosen method.</span></span>  
18. <span data-ttu-id="28425-132">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="28425-132">Close the page.</span></span>

