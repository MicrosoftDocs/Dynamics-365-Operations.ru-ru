---
title: "Частичный подсчет циклов местонахождений"
description: "Планы подсчета циклов регулируют фактические операции подсчета. Можно запросить, чтобы только конкретные продукты и варианты продуктов подчитывались вместо всех запасов в наличии в местонахождении."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0e0f9d81f4d5943a89d8ac87776e05acb32cb8d9
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="partial-location-cycle-counting"></a><span data-ttu-id="2927e-104">Частичный подсчет циклов местонахождений</span><span class="sxs-lookup"><span data-stu-id="2927e-104">Partial location cycle counting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2927e-105">Планы подсчета циклов регулируют фактические операции подсчета.</span><span class="sxs-lookup"><span data-stu-id="2927e-105">Cycle count plans guide the actual counting operations.</span></span> <span data-ttu-id="2927e-106">Можно запросить, чтобы только конкретные продукты и варианты продуктов подчитывались вместо всех запасов в наличии в местонахождении.</span><span class="sxs-lookup"><span data-stu-id="2927e-106">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span>

<span data-ttu-id="2927e-107">С помощью планов подсчета циклов для создания работы подсчета можно регулировать фактические операции подсчета.</span><span class="sxs-lookup"><span data-stu-id="2927e-107">By using cycle count plans to create counting work, you can guide the actual counting operations.</span></span> <span data-ttu-id="2927e-108">Можно запросить, чтобы только конкретные продукты и варианты продуктов подчитывались вместо всех запасов в наличии в местонахождении.</span><span class="sxs-lookup"><span data-stu-id="2927e-108">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span> <span data-ttu-id="2927e-109">С помощью фильтрации по конкретным продуктам менеджер склада может уменьшить накладные расходы для рассмотрения, избежать ошибок консолидации и сэкономить время.</span><span class="sxs-lookup"><span data-stu-id="2927e-109">By filtering on specific products, the warehouse manager can reduce review overhead, avoid consolidation mistakes, and save time.</span></span>

## <a name="how-to-configure-partial-location-cycle-counting"></a><span data-ttu-id="2927e-110">Настройка частичного цикличного подсчета местонахождений</span><span class="sxs-lookup"><span data-stu-id="2927e-110">How to configure partial location cycle counting</span></span>
<span data-ttu-id="2927e-111">При использовании рабочего процесса склада для операций подсчета для каждого местонахождения создается заголовок работы.</span><span class="sxs-lookup"><span data-stu-id="2927e-111">When you use the warehouse work process for counting operations, a work header is created for each location.</span></span> <span data-ttu-id="2927e-112">При определении плана подсчета циклов можно использовать запрос **Выберите местонахождения** для ограничения создаваемой работы подсчета циклов.</span><span class="sxs-lookup"><span data-stu-id="2927e-112">When you define the cycle count plan, you can use the **Select locations** query to limit the cycle counting work that is created.</span></span> <span data-ttu-id="2927e-113">При выборе продуктов для плана подсчета циклов можно выбрать запросы продукта и вариантов продукта для уточнения того, что подсчитывается.</span><span class="sxs-lookup"><span data-stu-id="2927e-113">When you select products for the cycle count plan, you can select both product and product variant queries to refine what is counted.</span></span> 

<span data-ttu-id="2927e-114">Можно связать **шаблон работы** с план подсчета циклов, чтобы определить способ создания работы подсчета циклов.</span><span class="sxs-lookup"><span data-stu-id="2927e-114">You can associate a **work template** with a cycle count plan to define how the cycle count work should be created.</span></span> <span data-ttu-id="2927e-115">На шаблон работы для операций подсчета напрямую ссылается план подсчета циклов.</span><span class="sxs-lookup"><span data-stu-id="2927e-115">The work template for counting operations is directly referenced from the cycle count plan.</span></span> 

<span data-ttu-id="2927e-116">При определении сведений шаблона работы можно использовать параметр **Разрывы строки работы**, чтобы указать, следует ли группировать строки работы подсчета по номеру номенклатуры или номеру варианта продукта.</span><span class="sxs-lookup"><span data-stu-id="2927e-116">When you define the work template details, you can use the **Work line breaks** option to specify whether the counting work lines must be grouped by item number or product variant number.</span></span> <span data-ttu-id="2927e-117">Эта настройка необходима, если следует выполнить подсчет запасов в наличии только для определенных продуктов в местонахождении.</span><span class="sxs-lookup"><span data-stu-id="2927e-117">This setup is required if you want to count on-hand inventory only for specific products in a location.</span></span> <span data-ttu-id="2927e-118">Создаваемые строки работы подсчета циклов будут иметь уровень информации, определенный здесь, и операция подсчета обрабатывается на основе этого уровня.</span><span class="sxs-lookup"><span data-stu-id="2927e-118">The cycle counting work lines that are created will have the level of information that you define here, and the guided counting operation will be handled based on this level.</span></span> 

<span data-ttu-id="2927e-119">Если связать планы подсчета циклов с шаблонами работ с помощью параметра **Разрывы строки работы** поле **Частичный подсчет циклов** выбирается для создаваемой работы подсчета циклов и несколько строк работы подсчета циклов создается на основе определения шаблона работы.</span><span class="sxs-lookup"><span data-stu-id="2927e-119">If you associate cycle count plans with work templates by using the **Work lines breaks** option, the **Partial cycle count** field is selected for the cycle counting work that is created, and multiple cycle counting work lines will be created based on the definition of the work template.</span></span> 

<span data-ttu-id="2927e-120">Перед обработкой работы частичного подсчета циклов необходимо как минимум выбрать **Отображение кода номенклатуры** для элемента меню мобильного устройства как части настройки подсчета циклов.</span><span class="sxs-lookup"><span data-stu-id="2927e-120">Before partial cycle count work can be processed, you must, at a minimum, select **Display item number** for the mobile device menu item as part of the cycle counting setup.</span></span> <span data-ttu-id="2927e-121">Оператору склада будет предложено записать только сведения о подсчете, относящиеся к строкам подсчета (номера номенклатур и аналитики "продукт").</span><span class="sxs-lookup"><span data-stu-id="2927e-121">The warehouse operator will be asked to record only counting information that is related to the counting lines (item numbers and product dimensions).</span></span> <span data-ttu-id="2927e-122">Все другие складские запасы в наличии будут игнорироваться для этого процесса подсчета.</span><span class="sxs-lookup"><span data-stu-id="2927e-122">All other on-hand inventory will be ignored for this counting process.</span></span> 

<span data-ttu-id="2927e-123">В процессе частичного подсчета циклов дата и время **Последний цикличный подсчет** не будут обновляться для местонахождения.</span><span class="sxs-lookup"><span data-stu-id="2927e-123">For the partial cycle count process, the **Last cycle count** date/time won’t be updated for the location.</span></span>

## <a name="example"></a><span data-ttu-id="2927e-124">Пример</span><span class="sxs-lookup"><span data-stu-id="2927e-124">Example</span></span>
<span data-ttu-id="2927e-125">В этом примере только номер номенклатуры A0001 следует подсчитывать на складе 61.</span><span class="sxs-lookup"><span data-stu-id="2927e-125">For this example, only item number A0001 must be counted in warehouse 61.</span></span>

1.  <span data-ttu-id="2927e-126">Создается новый шаблон работы для подсчета циклов.</span><span class="sxs-lookup"><span data-stu-id="2927e-126">A new work template for cycle counting is created.</span></span> <span data-ttu-id="2927e-127">Параметр **Разрывы строки работы** используется для группировки строк работы подсчета по коду номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="2927e-127">The **Work line breaks** option is used to group counting work lines by item number.</span></span> <span data-ttu-id="2927e-128">Таким образом, создаваемая работа подсчета циклов будет содержать строки по коду номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="2927e-128">Therefore, the cycle counting work that is created will have lines per item number.</span></span> <span data-ttu-id="2927e-129">Можно также сгруппировать строки по номеру варианта продукта.</span><span class="sxs-lookup"><span data-stu-id="2927e-129">You can also group the lines by product variant number.</span></span>
2.  <span data-ttu-id="2927e-130">Создается новый план подсчета циклов, который ссылается на только что созданный шаблон работы.</span><span class="sxs-lookup"><span data-stu-id="2927e-130">A new cycle counting plan is created that references the newly created work template.</span></span> <span data-ttu-id="2927e-131">План подсчета циклов включает в себя все местонахождения на складе 61 (запрос **Выберите местонахождения** запрос), содержащие запасов для кода номенклатуры A0001.</span><span class="sxs-lookup"><span data-stu-id="2927e-131">The cycle counting plan includes all locations in warehouse 61 (**Select locations** query) that hold inventory for item number A0001.</span></span> <span data-ttu-id="2927e-132">Выбор конкретных продуктов определяется в разделе **Выбор продуктов плана подсчета циклов**.</span><span class="sxs-lookup"><span data-stu-id="2927e-132">The selection of specific products is defined in the **Cycle count product selections** section.</span></span>
3.  <span data-ttu-id="2927e-133">Можно выбрать продукты для планов подсчета циклов, установив в поле **Пустые местоположения** значение **Исключить пустые**.</span><span class="sxs-lookup"><span data-stu-id="2927e-133">You can select products for cycle counting plans by setting the **Empty locations** field to **Exclude empty**.</span></span> <span data-ttu-id="2927e-134">При обработке плана подсчета циклов создается работа частичного подсчета циклов для номера номенклатуры A0001.</span><span class="sxs-lookup"><span data-stu-id="2927e-134">When the cycle counting plan is processed, partial cycle count work for item number A0001 is created.</span></span> <span data-ttu-id="2927e-135">Фактический процесс подсчета можно выполнить с помощью пункта меню мобильного устройства для подсчета циклов.</span><span class="sxs-lookup"><span data-stu-id="2927e-135">The actual counting process can be performed by using a mobile device menu item for guided cycle counting.</span></span>



<a name="see-also"></a><span data-ttu-id="2927e-136">См. также</span><span class="sxs-lookup"><span data-stu-id="2927e-136">See also</span></span>
--------

[<span data-ttu-id="2927e-137">Подсчет циклов</span><span class="sxs-lookup"><span data-stu-id="2927e-137">Cycle counting</span></span>](cycle-counting.md)


