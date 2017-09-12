---
title: "Частичный подсчет циклов местонахождений"
description: "Планы подсчета циклов регулируют фактические операции подсчета. Можно запросить, чтобы только конкретные продукты и варианты продуктов подчитывались вместо всех запасов в наличии в местонахождении."
author: perlynne
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
keywords: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 2ee4de8eabc55271e272ca3026746787353f5fc3
ms.contentlocale: ru-ru
ms.lasthandoff: 07/18/2017

---

# <a name="partial-location-cycle-counting"></a><span data-ttu-id="5929d-105">Частичный подсчет циклов местонахождений</span><span class="sxs-lookup"><span data-stu-id="5929d-105">Partial location cycle counting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5929d-106">Планы подсчета циклов регулируют фактические операции подсчета.</span><span class="sxs-lookup"><span data-stu-id="5929d-106">Cycle count plans guide the actual counting operations.</span></span> <span data-ttu-id="5929d-107">Можно запросить, чтобы только конкретные продукты и варианты продуктов подчитывались вместо всех запасов в наличии в местонахождении.</span><span class="sxs-lookup"><span data-stu-id="5929d-107">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span>

<span data-ttu-id="5929d-108">С помощью планов подсчета циклов для создания работы подсчета можно регулировать фактические операции подсчета.</span><span class="sxs-lookup"><span data-stu-id="5929d-108">By using cycle count plans to create counting work, you can guide the actual counting operations.</span></span> <span data-ttu-id="5929d-109">Можно запросить, чтобы только конкретные продукты и варианты продуктов подчитывались вместо всех запасов в наличии в местонахождении.</span><span class="sxs-lookup"><span data-stu-id="5929d-109">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span> <span data-ttu-id="5929d-110">С помощью фильтрации по конкретным продуктам менеджер склада может уменьшить накладные расходы для рассмотрения, избежать ошибок консолидации и сэкономить время.</span><span class="sxs-lookup"><span data-stu-id="5929d-110">By filtering on specific products, the warehouse manager can reduce review overhead, avoid consolidation mistakes, and save time.</span></span>

## <a name="how-to-configure-partial-location-cycle-counting"></a><span data-ttu-id="5929d-111">Настройка частичного цикличного подсчета местонахождений</span><span class="sxs-lookup"><span data-stu-id="5929d-111">How to configure partial location cycle counting</span></span>
<span data-ttu-id="5929d-112">При использовании рабочего процесса склада для операций подсчета для каждого местонахождения создается заголовок работы.</span><span class="sxs-lookup"><span data-stu-id="5929d-112">When you use the warehouse work process for counting operations, a work header is created for each location.</span></span> <span data-ttu-id="5929d-113">При определении плана подсчета циклов можно использовать запрос **Выберите местонахождения** для ограничения создаваемой работы подсчета циклов.</span><span class="sxs-lookup"><span data-stu-id="5929d-113">When you define the cycle count plan, you can use the **Select locations** query to limit the cycle counting work that is created.</span></span> <span data-ttu-id="5929d-114">При выборе продуктов для плана подсчета циклов можно выбрать запросы продукта и вариантов продукта для уточнения того, что подсчитывается.</span><span class="sxs-lookup"><span data-stu-id="5929d-114">When you select products for the cycle count plan, you can select both product and product variant queries to refine what is counted.</span></span> 

<span data-ttu-id="5929d-115">Можно связать **шаблон работы** с план подсчета циклов, чтобы определить способ создания работы подсчета циклов.</span><span class="sxs-lookup"><span data-stu-id="5929d-115">You can associate a **work template** with a cycle count plan to define how the cycle count work should be created.</span></span> <span data-ttu-id="5929d-116">На шаблон работы для операций подсчета напрямую ссылается план подсчета циклов.</span><span class="sxs-lookup"><span data-stu-id="5929d-116">The work template for counting operations is directly referenced from the cycle count plan.</span></span> 

<span data-ttu-id="5929d-117">При определении сведений шаблона работы можно использовать параметр **Разрывы строки работы**, чтобы указать, следует ли группировать строки работы подсчета по номеру номенклатуры или номеру варианта продукта.</span><span class="sxs-lookup"><span data-stu-id="5929d-117">When you define the work template details, you can use the **Work line breaks** option to specify whether the counting work lines must be grouped by item number or product variant number.</span></span> <span data-ttu-id="5929d-118">Эта настройка необходима, если следует выполнить подсчет запасов в наличии только для определенных продуктов в местонахождении.</span><span class="sxs-lookup"><span data-stu-id="5929d-118">This setup is required if you want to count on-hand inventory only for specific products in a location.</span></span> <span data-ttu-id="5929d-119">Создаваемые строки работы подсчета циклов будут иметь уровень информации, определенный здесь, и операция подсчета обрабатывается на основе этого уровня.</span><span class="sxs-lookup"><span data-stu-id="5929d-119">The cycle counting work lines that are created will have the level of information that you define here, and the guided counting operation will be handled based on this level.</span></span> 

<span data-ttu-id="5929d-120">Если связать планы подсчета циклов с шаблонами работ с помощью параметра **Разрывы строки работы** поле **Частичный подсчет циклов** выбирается для создаваемой работы подсчета циклов и несколько строк работы подсчета циклов создается на основе определения шаблона работы.</span><span class="sxs-lookup"><span data-stu-id="5929d-120">If you associate cycle count plans with work templates by using the **Work lines breaks** option, the **Partial cycle count** field is selected for the cycle counting work that is created, and multiple cycle counting work lines will be created based on the definition of the work template.</span></span> 

<span data-ttu-id="5929d-121">Перед обработкой работы частичного подсчета циклов необходимо как минимум выбрать **Отображение кода номенклатуры** для элемента меню мобильного устройства как части настройки подсчета циклов.</span><span class="sxs-lookup"><span data-stu-id="5929d-121">Before partial cycle count work can be processed, you must, at a minimum, select **Display item number** for the mobile device menu item as part of the cycle counting setup.</span></span> <span data-ttu-id="5929d-122">Оператору склада будет предложено записать только сведения о подсчете, относящиеся к строкам подсчета (номера номенклатур и аналитики "продукт").</span><span class="sxs-lookup"><span data-stu-id="5929d-122">The warehouse operator will be asked to record only counting information that is related to the counting lines (item numbers and product dimensions).</span></span> <span data-ttu-id="5929d-123">Все другие складские запасы в наличии будут игнорироваться для этого процесса подсчета.</span><span class="sxs-lookup"><span data-stu-id="5929d-123">All other on-hand inventory will be ignored for this counting process.</span></span> 

<span data-ttu-id="5929d-124">В процессе частичного подсчета циклов дата и время **Последний цикличный подсчет** не будут обновляться для местонахождения.</span><span class="sxs-lookup"><span data-stu-id="5929d-124">For the partial cycle count process, the **Last cycle count** date/time won’t be updated for the location.</span></span>

## <a name="example"></a><span data-ttu-id="5929d-125">Пример</span><span class="sxs-lookup"><span data-stu-id="5929d-125">Example</span></span>
<span data-ttu-id="5929d-126">В этом примере только номер номенклатуры A0001 следует подсчитывать на складе 61.</span><span class="sxs-lookup"><span data-stu-id="5929d-126">For this example, only item number A0001 must be counted in warehouse 61.</span></span>

1.  <span data-ttu-id="5929d-127">Создается новый шаблон работы для подсчета циклов.</span><span class="sxs-lookup"><span data-stu-id="5929d-127">A new work template for cycle counting is created.</span></span> <span data-ttu-id="5929d-128">Параметр **Разрывы строки работы** используется для группировки строк работы подсчета по коду номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="5929d-128">The **Work line breaks** option is used to group counting work lines by item number.</span></span> <span data-ttu-id="5929d-129">Таким образом, создаваемая работа подсчета циклов будет содержать строки по коду номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="5929d-129">Therefore, the cycle counting work that is created will have lines per item number.</span></span> <span data-ttu-id="5929d-130">Можно также сгруппировать строки по номеру варианта продукта.</span><span class="sxs-lookup"><span data-stu-id="5929d-130">You can also group the lines by product variant number.</span></span>
2.  <span data-ttu-id="5929d-131">Создается новый план подсчета циклов, который ссылается на только что созданный шаблон работы.</span><span class="sxs-lookup"><span data-stu-id="5929d-131">A new cycle counting plan is created that references the newly created work template.</span></span> <span data-ttu-id="5929d-132">План подсчета циклов включает в себя все местонахождения на складе 61 (запрос **Выберите местонахождения** запрос), содержащие запасов для кода номенклатуры A0001.</span><span class="sxs-lookup"><span data-stu-id="5929d-132">The cycle counting plan includes all locations in warehouse 61 (**Select locations** query) that hold inventory for item number A0001.</span></span> <span data-ttu-id="5929d-133">Выбор конкретных продуктов определяется в разделе **Выбор продуктов плана подсчета циклов**.</span><span class="sxs-lookup"><span data-stu-id="5929d-133">The selection of specific products is defined in the **Cycle count product selections** section.</span></span>
3.  <span data-ttu-id="5929d-134">Можно выбрать продукты для планов подсчета циклов, задав в поле **Пустые местоположения** значение **Исключить пустые**. При обработке плана подсчета циклов создается работа частичного подсчета циклов для кода номенклатуры A0001.</span><span class="sxs-lookup"><span data-stu-id="5929d-134">You can select products for cycle counting plans by setting the **Empty locations** field to **Exclude empty**.When the cycle counting plan is processed, partial cycle count work for item number A0001 is created.</span></span> <span data-ttu-id="5929d-135">Фактический процесс подсчета можно выполнить с помощью пункта меню мобильного устройства для подсчета циклов.</span><span class="sxs-lookup"><span data-stu-id="5929d-135">The actual counting process can be performed by using a mobile device menu item for guided cycle counting.</span></span>



<a name="see-also"></a><span data-ttu-id="5929d-136">См. также</span><span class="sxs-lookup"><span data-stu-id="5929d-136">See also</span></span>
--------

[<span data-ttu-id="5929d-137">Подсчет циклов</span><span class="sxs-lookup"><span data-stu-id="5929d-137">Cycle counting</span></span>](cycle-counting.md)


