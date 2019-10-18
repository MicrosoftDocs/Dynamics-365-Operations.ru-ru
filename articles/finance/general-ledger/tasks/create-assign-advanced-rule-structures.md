---
title: Создание и назначение структур дополнительных правил
description: В этой теме объясняется, как создать и назначить структуру дополнительных правил в структуру счетов.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cff07c13553ea140f537160da7f93820d5e3f77a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175605"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="74b86-103">Создание и назначение структур дополнительных правил</span><span class="sxs-lookup"><span data-stu-id="74b86-103">Create and assign advanced rule structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="74b86-104">В этой теме объясняется, как создать и назначить структуру дополнительных правил в структуру счетов.</span><span class="sxs-lookup"><span data-stu-id="74b86-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="74b86-105">В данном руководстве используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="74b86-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="74b86-106">Создание новой структуры дополнительного правила</span><span class="sxs-lookup"><span data-stu-id="74b86-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="74b86-107">Выберите **Область переходов > Модули > Главная книга > План счетов > Структуры > Структуры дополнительных правил**.</span><span class="sxs-lookup"><span data-stu-id="74b86-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="74b86-108">Выберите **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="74b86-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="74b86-109">В поле **Структура дополнительных правил** введите имя для описания структуры правил.</span><span class="sxs-lookup"><span data-stu-id="74b86-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="74b86-110">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="74b86-110">Select **OK**.</span></span>
5. <span data-ttu-id="74b86-111">Выберите **Добавить сегмент**.</span><span class="sxs-lookup"><span data-stu-id="74b86-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="74b86-112">В списке сегментов выберите финансовую аналитику.</span><span class="sxs-lookup"><span data-stu-id="74b86-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="74b86-113">Например, **Магазин**.</span><span class="sxs-lookup"><span data-stu-id="74b86-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="74b86-114">Выберите **Добавить сегмент**.</span><span class="sxs-lookup"><span data-stu-id="74b86-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="74b86-115">Выберите **Активировать**.</span><span class="sxs-lookup"><span data-stu-id="74b86-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="74b86-116">Применение структуры дополнительного правила к структуре счета</span><span class="sxs-lookup"><span data-stu-id="74b86-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="74b86-117">Выберите **область переходов > Модули > Главная книга > План счетов > Структуры > Настройка структур счетов**.</span><span class="sxs-lookup"><span data-stu-id="74b86-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="74b86-118">В списке найдите и выберите структуру счета, к которой необходимо применить дополнительное правило.</span><span class="sxs-lookup"><span data-stu-id="74b86-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="74b86-119">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="74b86-119">Select **Edit**.</span></span> <span data-ttu-id="74b86-120">Можно также выбрать **Дополнительные правила**, и будет предложено перевести структуру счета в **Режим черновика**.</span><span class="sxs-lookup"><span data-stu-id="74b86-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="74b86-121">Выберите **Дополнительные правила**.</span><span class="sxs-lookup"><span data-stu-id="74b86-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="74b86-122">Выберите **Создать**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="74b86-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="74b86-123">В поле **Дополнительное правило** введите значение.</span><span class="sxs-lookup"><span data-stu-id="74b86-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="74b86-124">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="74b86-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="74b86-125">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="74b86-125">Select **Create**.</span></span>
9. <span data-ttu-id="74b86-126">Выберите **Добавить новые критерии**.</span><span class="sxs-lookup"><span data-stu-id="74b86-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="74b86-127">В поле **Где** выберите счет ГК или финансовую аналитику.</span><span class="sxs-lookup"><span data-stu-id="74b86-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="74b86-128">В поле **Оператор** выберите параметр, например **находится в диапазоне** и **включает**.</span><span class="sxs-lookup"><span data-stu-id="74b86-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="74b86-129">В поле **Значение** введите значение.</span><span class="sxs-lookup"><span data-stu-id="74b86-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="74b86-130">В поле **через** введите значение.</span><span class="sxs-lookup"><span data-stu-id="74b86-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="74b86-131">Выберите **Добавить**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="74b86-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="74b86-132">В списке найдите структуру дополнительного правила, которая должна использоваться при соответствии указанных критериев.</span><span class="sxs-lookup"><span data-stu-id="74b86-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="74b86-133">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="74b86-133">Select **Add**.</span></span>
17. <span data-ttu-id="74b86-134">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="74b86-134">Close the page.</span></span>
18. <span data-ttu-id="74b86-135">Выберите **Активировать**.</span><span class="sxs-lookup"><span data-stu-id="74b86-135">Select **Activate**.</span></span>

