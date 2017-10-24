--- 
title: "Создать одалживаемые номенклатуры"
description: "Номенклатуры временного пользования (одалживаемые номенклатуры) — это записи, позволяющие отслеживать физические номенклатуры, например телефоны или компьютеры, выдаваемые организацией работникам во временное пользование."
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cef1f9b2e3d202d7eea3a967fa8a6c371c6ac3a5
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="create-loan-items"></a><span data-ttu-id="c6346-103">Создать одалживаемые номенклатуры</span><span class="sxs-lookup"><span data-stu-id="c6346-103">Create loan items</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c6346-104">Номенклатуры временного пользования (одалживаемые номенклатуры) — это записи, позволяющие отслеживать физические номенклатуры, например телефоны или компьютеры, выдаваемые организацией работникам во временное пользование.</span><span class="sxs-lookup"><span data-stu-id="c6346-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="c6346-105">Каждая физическая номенклатура должна иметь соответствующую номенклатуру временного пользования.</span><span class="sxs-lookup"><span data-stu-id="c6346-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="c6346-106">В каждой записи арендованной номенклатуры должно быть описано, что было предоставлено в аренду, кто несет ответственность за аренду и количество дней, на которые была предоставлена в аренду номенклатура.</span><span class="sxs-lookup"><span data-stu-id="c6346-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="c6346-107">Одновременно можно создать несколько номенклатур временного пользования, таких как ключи, карточки доступа или комплекты униформы.</span><span class="sxs-lookup"><span data-stu-id="c6346-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="c6346-108">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="c6346-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="c6346-109">Создание типов займов</span><span class="sxs-lookup"><span data-stu-id="c6346-109">Create Loan types</span></span>
1. <span data-ttu-id="c6346-110">Перейдите в раздел "Управление персоналом" > "Работники" > "Одалживаемые номенклатуры" > "Типы займа".</span><span class="sxs-lookup"><span data-stu-id="c6346-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="c6346-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="c6346-111">Click New.</span></span>
3. <span data-ttu-id="c6346-112">В поле "Тип займа" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c6346-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="c6346-113">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c6346-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c6346-114">Введите количество дней, на которое может быть просрочен возврат номенклатур, принадлежащих к этому типу.</span><span class="sxs-lookup"><span data-stu-id="c6346-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="c6346-115">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="c6346-115">Click Save.</span></span>
7. <span data-ttu-id="c6346-116">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c6346-116">Close the page.</span></span>
8. <span data-ttu-id="c6346-117">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="c6346-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="c6346-118">Создание одалживаемых номенклатур</span><span class="sxs-lookup"><span data-stu-id="c6346-118">Create Loan items</span></span>
1. <span data-ttu-id="c6346-119">Перейдите в раздел "Управление персоналом" > "Работники" > "Одалживаемые номенклатуры" > "Одалживаемые номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="c6346-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="c6346-120">Щелкните "Создать одалживаемые номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="c6346-120">Click Create loan items.</span></span>
3. <span data-ttu-id="c6346-121">В поле "Кол-во" введите число.</span><span class="sxs-lookup"><span data-stu-id="c6346-121">In the Qty. field, enter a number.</span></span>
4. <span data-ttu-id="c6346-122">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c6346-122">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c6346-123">В поле "Тип займа" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c6346-123">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="c6346-124">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="c6346-124">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="c6346-125">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c6346-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="c6346-126">Введите количество дней, на которое номенклатура может быть выдана во временное пользование.</span><span class="sxs-lookup"><span data-stu-id="c6346-126">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="c6346-127">Значение по умолчанию в поле "Планируемый возврат" на странице "Одолженное оборудование" вычисляется как текущая дата плюс это число.</span><span class="sxs-lookup"><span data-stu-id="c6346-127">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="c6346-128">В поле "Ответственное лицо" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c6346-128">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="c6346-129">Щелкните Выбрать.</span><span class="sxs-lookup"><span data-stu-id="c6346-129">Click Select.</span></span>
11. <span data-ttu-id="c6346-130">В поле "Начальное значение" введите число.</span><span class="sxs-lookup"><span data-stu-id="c6346-130">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="c6346-131">В поле "Интервал" введите число.</span><span class="sxs-lookup"><span data-stu-id="c6346-131">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="c6346-132">В поле "Формат" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c6346-132">In the Format field, type a value.</span></span>
    * <span data-ttu-id="c6346-133">Например, если начальный номер для номенклатуры временного пользования — 10, в поле "Формат" нужно ввести два символа числа.</span><span class="sxs-lookup"><span data-stu-id="c6346-133">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="c6346-134">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c6346-134">Click OK.</span></span>
15. <span data-ttu-id="c6346-135">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="c6346-135">Refresh the page.</span></span>

