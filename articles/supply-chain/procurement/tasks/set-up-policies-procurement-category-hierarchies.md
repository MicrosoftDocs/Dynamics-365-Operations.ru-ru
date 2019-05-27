---
title: Настройка политик для иерархий категорий закупаемой продукции
description: Эта процедура используется, чтобы настроить для заказа продукции в категории.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1fdf357466de12bd0188fc43cd266c67af762c7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569922"
---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a><span data-ttu-id="bb32b-103">Настройка политик для иерархий категорий закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="bb32b-103">Set up policies for procurement category hierarchies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bb32b-104">Эта процедура используется, чтобы настроить для заказа продукции в категории.</span><span class="sxs-lookup"><span data-stu-id="bb32b-104">Use this procedure to set up rules for ordering products in a category.</span></span> <span data-ttu-id="bb32b-105">Правила определяются для определенной политики закупок.</span><span class="sxs-lookup"><span data-stu-id="bb32b-105">The rules are defined for a specific purchasing policy.</span></span> <span data-ttu-id="bb32b-106">Правило доступа к категориям определяет, к каким категориям закупок имеют доступ сотрудники, когда они создают заявку.</span><span class="sxs-lookup"><span data-stu-id="bb32b-106">The category access rule controls which procurement categories employees have access to when they create a requisition.</span></span> <span data-ttu-id="bb32b-107">При создании заявки политика закупок и правило доступа к категориям, которые требуется применить, определяются на основании юридического лица и операционной единицы, к которым принадлежит сотрудник.</span><span class="sxs-lookup"><span data-stu-id="bb32b-107">When a requisition is being created, the purchasing policy and category access rule that should be applied are determined by the legal entity and the operational unit that the employee belongs to.</span></span> <span data-ttu-id="bb32b-108">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="bb32b-108">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="bb32b-109">Обычно эту задачу выполняет менеджер по закупкам.</span><span class="sxs-lookup"><span data-stu-id="bb32b-109">This task would typically be carried out by a purchasing manager.</span></span>


## <a name="find-the-procurement-policy"></a><span data-ttu-id="bb32b-110">Поиск политики закупок</span><span class="sxs-lookup"><span data-stu-id="bb32b-110">Find the procurement policy</span></span>
1. <span data-ttu-id="bb32b-111">Перейдите в раздел "Закупки и источники" > "Настройка" > "Политики" > "Политики закупок".</span><span class="sxs-lookup"><span data-stu-id="bb32b-111">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="bb32b-112">Перейдите по ссылке в политике USMF "Политика закупок".</span><span class="sxs-lookup"><span data-stu-id="bb32b-112">Click the link on the Procurement Policy USMF policy.</span></span>
    * <span data-ttu-id="bb32b-113">Это политика, в которую будет добавлено правило.</span><span class="sxs-lookup"><span data-stu-id="bb32b-113">This is the policy that you’ll add a rule to.</span></span> <span data-ttu-id="bb32b-114">Она должна быть активной.</span><span class="sxs-lookup"><span data-stu-id="bb32b-114">It must be an Active policy.</span></span>  

## <a name="create-a-category-access-rule"></a><span data-ttu-id="bb32b-115">Создать правило доступа для категории</span><span class="sxs-lookup"><span data-stu-id="bb32b-115">Create a category access rule</span></span>
1. <span data-ttu-id="bb32b-116">Выберите "Правило политики доступа к категории".</span><span class="sxs-lookup"><span data-stu-id="bb32b-116">Select the Category access policy rule.</span></span>
    * <span data-ttu-id="bb32b-117">Если кнопка "Создать правило политики" затемнена, это значит, что уже имеется активное правило политики для доступа к категории.</span><span class="sxs-lookup"><span data-stu-id="bb32b-117">If the Create policy rule button is dimmed, it’s because there’s already an active policy rule for Category access.</span></span> <span data-ttu-id="bb32b-118">Проверьте поле "Дата начала срока действия" и "Дата окончания срока действия", чтобы определить это правило, и щелкните "Отменить правило политики".</span><span class="sxs-lookup"><span data-stu-id="bb32b-118">Check the Effective and Expiration date fields to determine which it is, then select it, and click Retire policy rule.</span></span> <span data-ttu-id="bb32b-119">Если кнопка "Создать правило политики" доступна, выполнять действия не требуется.</span><span class="sxs-lookup"><span data-stu-id="bb32b-119">If the Create policy rule button is available, you don’t need to do anything.</span></span>  
2. <span data-ttu-id="bb32b-120">Щелкните "Создать правило политики".</span><span class="sxs-lookup"><span data-stu-id="bb32b-120">Click Create policy rule.</span></span>
3. <span data-ttu-id="bb32b-121">В поле "Действует с" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="bb32b-121">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="bb32b-122">Время не должно перекрываться с другим правилом, которое уже активно.</span><span class="sxs-lookup"><span data-stu-id="bb32b-122">The time must not overlap with another rule that’s already active.</span></span>  
    * <span data-ttu-id="bb32b-123">Выберите категорию, к которой применяется правило.</span><span class="sxs-lookup"><span data-stu-id="bb32b-123">Select a category that the rule will apply to.</span></span> <span data-ttu-id="bb32b-124">Обратите внимание, какая это категория — эта информация потребуется позже.</span><span class="sxs-lookup"><span data-stu-id="bb32b-124">Make a note of which category this is – you’ll need it later.</span></span> <span data-ttu-id="bb32b-125">При выборе категории ее родительская категория или категории также добавляются в список категорий "Выбрано".</span><span class="sxs-lookup"><span data-stu-id="bb32b-125">When you select a category, its parent category or categories will also be added to the Selected categories list.</span></span>  
    * <span data-ttu-id="bb32b-126">Чтобы применить правило ко всем подкатегориям выбранной категории, установите флажок "Включить подкатегории".</span><span class="sxs-lookup"><span data-stu-id="bb32b-126">If you want the rule to apply to all subcategories of the selected category, select the Include subcategories check box.</span></span>  
4. <span data-ttu-id="bb32b-127">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="bb32b-127">Click Add.</span></span>
    * <span data-ttu-id="bb32b-128">Если задать для параметра "Включить родительское правило" значение "Да", правило политики, определенное для родительской категории, также назначается ее дочерним категориям, если для них не было определено правило политики.</span><span class="sxs-lookup"><span data-stu-id="bb32b-128">If you set the Include parent rule option to Yes, the policy rule that you define for a parent category is also assigned to its child categories, if no policy rule has been defined for the child categories.</span></span>  
5. <span data-ttu-id="bb32b-129">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="bb32b-129">Click OK.</span></span>

## <a name="create-a-category-policy-rule"></a><span data-ttu-id="bb32b-130">Создать правило политики для категории</span><span class="sxs-lookup"><span data-stu-id="bb32b-130">Create a category policy rule</span></span>
1. <span data-ttu-id="bb32b-131">Выберите "Правило политики категории".</span><span class="sxs-lookup"><span data-stu-id="bb32b-131">Select the Category policy rule</span></span>
    * <span data-ttu-id="bb32b-132">Если кнопка "Создать правило политики" затемнена, выберите активное правило политики и щелкните "Отменить правило политики".</span><span class="sxs-lookup"><span data-stu-id="bb32b-132">If the Create policy rule button is dimmed, select the active policy rule, and then click Retire policy rule.</span></span>  
2. <span data-ttu-id="bb32b-133">Щелкните "Создать правило политики".</span><span class="sxs-lookup"><span data-stu-id="bb32b-133">Click Create policy rule.</span></span>
3. <span data-ttu-id="bb32b-134">В поле "Действует с" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="bb32b-134">In the Effective date field, enter a date and time.</span></span>
4. <span data-ttu-id="bb32b-135">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="bb32b-135">Click Add.</span></span>
5. <span data-ttu-id="bb32b-136">Выберите ту же категорию, которую вы использовали для правила доступа к категории.</span><span class="sxs-lookup"><span data-stu-id="bb32b-136">Select the same category that you used for the Category access rule.</span></span>
6. <span data-ttu-id="bb32b-137">В поле "Выбор поставщика" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="bb32b-137">In the Vendor selection field, select an option.</span></span>
    * <span data-ttu-id="bb32b-138">Выберите правило для управления тем, каких поставщиков можно выбрать для категории при создании заявок.</span><span class="sxs-lookup"><span data-stu-id="bb32b-138">Select a rule to control which kind of vendors can be selected for the category when requisitions are created.</span></span>  
7. <span data-ttu-id="bb32b-139">Щелкните "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="bb32b-139">Click Close.</span></span>
    * <span data-ttu-id="bb32b-140">Определенные правила политики предназначаются для заявок типа "Потребление".</span><span class="sxs-lookup"><span data-stu-id="bb32b-140">The policy rules that you have defined have been for requisitions of type Consumption.</span></span> <span data-ttu-id="bb32b-141">Если бы вы хотели определять политики для заявок типа "Пополнение", вы бы создали правило для типа правила политики "Правило политики доступа к категории пополнения".</span><span class="sxs-lookup"><span data-stu-id="bb32b-141">If you wanted to define policies for requisitions of type Replenishment, you would create a rule for the Policy rule type called “Replenishment category access policy rule”.</span></span>  

