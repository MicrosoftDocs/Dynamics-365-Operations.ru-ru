--- 
title: "Создание номера продукта для заранее определенных вариантов продукта"
description: "На этом руководстве показано, как настроить номенклатуру номера продукта для предопределенных вариантов продукта, и как назначить ее соответствующей группе аналитик продукта."
author: ShylaThompson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 7881701385c802578e5e5c412951a1507efa5acf
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-product-number-for-predefined-product-variants"></a><span data-ttu-id="87944-103">Создание номера продукта для заранее определенных вариантов продукта</span><span class="sxs-lookup"><span data-stu-id="87944-103">Create a product number for predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="87944-104">На этом руководстве показано, как настроить номенклатуру номера продукта для предопределенных вариантов продукта, и как назначить ее соответствующей группе аналитик продукта.</span><span class="sxs-lookup"><span data-stu-id="87944-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="87944-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="87944-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="87944-106">Новая номенклатура номера продукта назначается группе аналитик продукта "Цвет" и "Размер".</span><span class="sxs-lookup"><span data-stu-id="87944-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="87944-107">Эта задача обычно выполняется конструктором продуктов.</span><span class="sxs-lookup"><span data-stu-id="87944-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="87944-108">Создание номенклатуры номеров продуктов</span><span class="sxs-lookup"><span data-stu-id="87944-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="87944-109">Щелкните "Определение модели вариантов продукта".</span><span class="sxs-lookup"><span data-stu-id="87944-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="87944-110">Щелкните "Номенклатура продуктов".</span><span class="sxs-lookup"><span data-stu-id="87944-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="87944-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="87944-111">Click New.</span></span>
4. <span data-ttu-id="87944-112">В поле "Имя" введите имя номенклатуры, которое помогает идентифицировать целевую группу аналитик продукта, например ColorSize.</span><span class="sxs-lookup"><span data-stu-id="87944-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize.</span></span>
5. <span data-ttu-id="87944-113">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="87944-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="87944-114">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="87944-114">Click Add.</span></span>
7. <span data-ttu-id="87944-115">Щелкните "Номер шаблона продукта".</span><span class="sxs-lookup"><span data-stu-id="87944-115">Click Product master number.</span></span>
8. <span data-ttu-id="87944-116">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="87944-116">Click Add.</span></span>
9. <span data-ttu-id="87944-117">Щелкните "Текстовая константа".</span><span class="sxs-lookup"><span data-stu-id="87944-117">Click Text constant.</span></span>
10. <span data-ttu-id="87944-118">В поле "Текст" введите значение.</span><span class="sxs-lookup"><span data-stu-id="87944-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="87944-119">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="87944-119">Click Add.</span></span>
12. <span data-ttu-id="87944-120">Щелкните "Цвет".</span><span class="sxs-lookup"><span data-stu-id="87944-120">Click Color.</span></span>
13. <span data-ttu-id="87944-121">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="87944-121">Click Add.</span></span>
14. <span data-ttu-id="87944-122">Щелкните "Текстовая константа".</span><span class="sxs-lookup"><span data-stu-id="87944-122">Click Text constant.</span></span>
15. <span data-ttu-id="87944-123">В поле "Текст" введите значение.</span><span class="sxs-lookup"><span data-stu-id="87944-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="87944-124">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="87944-124">Click Add.</span></span>
17. <span data-ttu-id="87944-125">Щелкните "Размер".</span><span class="sxs-lookup"><span data-stu-id="87944-125">Click Size.</span></span>
18. <span data-ttu-id="87944-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="87944-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="87944-127">Назначение номенклатуры шаблону продукта</span><span class="sxs-lookup"><span data-stu-id="87944-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="87944-128">Щелкните "Группы аналитик продукта".</span><span class="sxs-lookup"><span data-stu-id="87944-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="87944-129">Выберите группу аналитик продукта SizeCol.</span><span class="sxs-lookup"><span data-stu-id="87944-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="87944-130">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="87944-130">Click Edit.</span></span>
4. <span data-ttu-id="87944-131">Выберите "Да" в поле "Использовать номенклатуру".</span><span class="sxs-lookup"><span data-stu-id="87944-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="87944-132">В поле "Номенклатура номеров вариантов продуктов" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="87944-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="87944-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="87944-133">Close the page.</span></span>


