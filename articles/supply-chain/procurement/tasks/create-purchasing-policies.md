---
title: Создание политик закупок
description: В этой процедуре показано, как создать политики закупок для соответствия бизнес-процессам закупок.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3bd4d6f8625c91f2190e994f04cbec4548272f04
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557833"
---
# <a name="create-purchasing-policies"></a><span data-ttu-id="b5b6e-103">Создание политик закупок</span><span class="sxs-lookup"><span data-stu-id="b5b6e-103">Create purchasing policies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b5b6e-104">В этой процедуре показано, как создать политики закупок для соответствия бизнес-процессам закупок.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-104">This procedure shows you how to create purchasing policies to align with your business processes for purchasing.</span></span> <span data-ttu-id="b5b6e-105">Прежде чем создавать политики закупок, необходимо настроить параметры политики закупок.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-105">Before you can create purchasing policies, you must set up the purchasing policy parameters.</span></span> <span data-ttu-id="b5b6e-106">Можно создавать, изменять и отменять политики закупок, но невозможно удалить политики закупок.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-106">It’s possible to create, modify, and retire a purchasing policy, but you can’t delete a purchasing policy.</span></span> <span data-ttu-id="b5b6e-107">Обычно эту процедуру выполняет менеджер по закупкам.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-107">This procedure would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="b5b6e-108">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-108">You can use this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-policy-parameters"></a><span data-ttu-id="b5b6e-109">Настройка параметров политики</span><span class="sxs-lookup"><span data-stu-id="b5b6e-109">Set up policy parameters</span></span>
1. <span data-ttu-id="b5b6e-110">Перейдите в раздел "Политики закупок".</span><span class="sxs-lookup"><span data-stu-id="b5b6e-110">Go to Purchasing policies.</span></span>
2. <span data-ttu-id="b5b6e-111">Щелкните "Параметры".</span><span class="sxs-lookup"><span data-stu-id="b5b6e-111">Click Parameters.</span></span>
    * <span data-ttu-id="b5b6e-112">Правила приоритета политик применяются к различным уровням в организации.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-112">Policy precedence rules apply to different levels in your organization.</span></span> <span data-ttu-id="b5b6e-113">Отображаемые подразделения зависят от организационной иерархии и от того, на каких уровнях в иерархии присвоено назначение "Внутренний контроль закупаемой продукции".</span><span class="sxs-lookup"><span data-stu-id="b5b6e-113">The organizational units that are shown depend on your organizational hierarchy, and on which levels in the hierarchy have been assigned the purpose of Procurement internal control.</span></span> <span data-ttu-id="b5b6e-114">Например, ваша организация может иметь юридические лица, центры затрат, регионы и подразделения, но может быть так, что только некоторые из них будут иметь назначение иерархии "Внутренний контроль закупаемой продукции".</span><span class="sxs-lookup"><span data-stu-id="b5b6e-114">For example, your organization might have legal entities, cost centers, regions, and departments, but it may be that only some of these have a hierarchy purpose of Procurement internal control.</span></span> <span data-ttu-id="b5b6e-115">По умолчанию доступна организация типа "Компания".</span><span class="sxs-lookup"><span data-stu-id="b5b6e-115">As a default, the organization of type Company is available.</span></span>  
3. <span data-ttu-id="b5b6e-116">Перейдите на вкладку "Параметры типа правила политики".</span><span class="sxs-lookup"><span data-stu-id="b5b6e-116">Click the Policy rule type parameters tab.</span></span>
4. <span data-ttu-id="b5b6e-117">В дереве выберите "Политика закупок\Правило управления заявками на покупку".</span><span class="sxs-lookup"><span data-stu-id="b5b6e-117">In the tree, select 'Purchasing policy\Purchase requisition control rule'.</span></span>
    * <span data-ttu-id="b5b6e-118">Определите порядок приоритета выполнения политики на уровне политики.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-118">You define the order of precedence for policy resolution at the policy level.</span></span> <span data-ttu-id="b5b6e-119">Однако для некоторых типов политики можно переопределить порядок приоритета для отдельных типов правил политики.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-119">However, for some policy types, you can override the order of precedence for individual policy rule types.</span></span> <span data-ttu-id="b5b6e-120">Например, можно определить следующий порядок приоритета для политик закупки: центр затрат, подразделение, компания.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-120">For example, you might define the order of precedence for purchasing policies to be: cost center, department, company.</span></span> <span data-ttu-id="b5b6e-121">Для правила политики каталога может потребоваться установить следующий порядок приоритета: подразделение, центр затрат, компания.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-121">For the catalog policy rule, you might want the order of precedence to be: department, cost center, company.</span></span> <span data-ttu-id="b5b6e-122">Можно изменить порядок приоритета для правила политики каталога.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-122">You can change the order of precedence for the Catalog policy rule.</span></span> <span data-ttu-id="b5b6e-123">Когда работник создает заявку, отображаемый каталог определяется политиками, связанными с подразделением работника, затем с центром затрат, а затем с компанией.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-123">When a worker creates a requisition, the catalog that is displayed is determined by the policies that are associated with the worker’s department, then their cost center, and then their company.</span></span>  
    * <span data-ttu-id="b5b6e-124">При наличии нескольких перечисленных уровней организации можно использовать стрелки "Вверх/вниз", чтобы настроить порядок приоритета для правила "Внутренний контроль закупаемой продукции".</span><span class="sxs-lookup"><span data-stu-id="b5b6e-124">If there’s more than one organizational level listed, you can use the Up/Down arrows to set the order of precedence for the Purchase requisition control rule.</span></span>  
5. <span data-ttu-id="b5b6e-125">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-125">Close the page.</span></span>

## <a name="create-a-new-policy"></a><span data-ttu-id="b5b6e-126">Создание новой политики</span><span class="sxs-lookup"><span data-stu-id="b5b6e-126">Create a new policy</span></span>
1. <span data-ttu-id="b5b6e-127">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b5b6e-127">Click New.</span></span>
2. <span data-ttu-id="b5b6e-128">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-128">In the Name field, type a value.</span></span>
3. <span data-ttu-id="b5b6e-129">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-129">In the Description field, type a value.</span></span>
    * <span data-ttu-id="b5b6e-130">Одна политика закупок может применяться только к одной организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-130">A single purchasing policy can only apply to one organization hierarchy.</span></span> <span data-ttu-id="b5b6e-131">Например, можно иметь одну иерархию с именем "Географическая" и одну с именем "Подразделение", но для каждой иерархии будут заданы разные политики закупок.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-131">For example, you could have one hierarchy called “Geographic” and one called “Department”, and have a different purchasing policy for each.</span></span>  
    * <span data-ttu-id="b5b6e-132">Выберите организацию, к которой должна применяться политика.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-132">Select an organization that the policy should apply to.</span></span>  
4. <span data-ttu-id="b5b6e-133">Щелкните стрелку для добавления выбранной организации.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-133">Click the arrow to add the selected organization.</span></span>
    * <span data-ttu-id="b5b6e-134">Можно повторить эту процедуру для добавления нескольких организаций.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-134">You can repeat this process to add more organizations.</span></span>  

## <a name="add-a-policy-rule"></a><span data-ttu-id="b5b6e-135">Добавление правила политики</span><span class="sxs-lookup"><span data-stu-id="b5b6e-135">Add a policy rule</span></span>
1. <span data-ttu-id="b5b6e-136">В списке "Тип правила политики" выберите "Правило назначения заявки".</span><span class="sxs-lookup"><span data-stu-id="b5b6e-136">In the Policy rule type list, select Requisition purpose rule.</span></span>
    * <span data-ttu-id="b5b6e-137">Вы создаете правило, согласно которому для назначения заявки по умолчанию задается тип "Потребление", но вместо этого можно выбрать тип "Пополнение".</span><span class="sxs-lookup"><span data-stu-id="b5b6e-137">You’ll create a rule that sets the default requisition purpose to type Consumption but allows the Replenishment type to be selected instead.</span></span>  
2. <span data-ttu-id="b5b6e-138">Щелкните "Создать правило политики".</span><span class="sxs-lookup"><span data-stu-id="b5b6e-138">Click Create policy rule.</span></span>
3. <span data-ttu-id="b5b6e-139">Выберите "Да" в поле "Разрешить переопределение вручную".</span><span class="sxs-lookup"><span data-stu-id="b5b6e-139">Select Yes in the Allow manual override field.</span></span>
4. <span data-ttu-id="b5b6e-140">Щелкните "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="b5b6e-140">Click Close.</span></span>
    * <span data-ttu-id="b5b6e-141">Теперь можно настроить другие правила политики для политики закупок.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-141">Now you can set up other policy rules for the purchasing policy.</span></span>   <span data-ttu-id="b5b6e-142">Обратите внимание, что тип "Правило политики" не может иметь перекрывающиеся правила, активные одновременно в пределах одной политики закупок.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-142">Note that a Policy rule type cannot have overlapping rules that are active at the same time within a single procurement policy.</span></span>  
5. <span data-ttu-id="b5b6e-143">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-143">Close the page.</span></span>
6. <span data-ttu-id="b5b6e-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b5b6e-144">Close the page.</span></span>

