---
title: Виртуальные номенклатуры
description: В этой теме подробно рассматривается, как использовать тип строки "виртуальная" для строк спецификаций и формул в Dynamics 365 Supply Chain Management.
author: ShylaThompson
manager: tfehr
ms.date: 06/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: shylaw
ms.search.validfrom: ''
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: dc69687b1dd94407b28209178e923fe5169bcdac
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211338"
---
# <a name="phantom-items"></a><span data-ttu-id="746db-103">Виртуальные номенклатуры</span><span class="sxs-lookup"><span data-stu-id="746db-103">Phantom items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="746db-104">В этой теме подробно рассматривается, как использовать тип строки "виртуальная" для строк спецификаций и формул.</span><span class="sxs-lookup"><span data-stu-id="746db-104">This topic describes, in detail, how the Phantom line type can be used for the lines of a bill of materials (BOM) and a formula.</span></span> <span data-ttu-id="746db-105">На следующем рисунке (a) — это спецификация на продукт H и детали F и G, а (b) — маршрутный лист для продуктов H и детали F.</span><span class="sxs-lookup"><span data-stu-id="746db-105">In the following illustration, (a) is the BOM for product H and parts F and G, and (b) is the route sheet for products H and part F.</span></span>

![Продукт H и деталь F](media/product-H-part-F.png)


<span data-ttu-id="746db-107">На этом рисунке показан пример структуры спецификации на двух уровнях.</span><span class="sxs-lookup"><span data-stu-id="746db-107">This illustration shows an example of a BOM structure in two levels.</span></span> <span data-ttu-id="746db-108">Готовый продукт H представляет собой продукт — машинный агрегат.</span><span class="sxs-lookup"><span data-stu-id="746db-108">Finished product H represents a product for a machine assembly.</span></span> <span data-ttu-id="746db-109">Машинный агрегат состоит из двух деталей: электрического блока (F), в который входит два материала (A и B), и группы упаковочных материалов (G), в которую также входит два материала (C и D).</span><span class="sxs-lookup"><span data-stu-id="746db-109">The machine assembly consists of two parts, an electrical unit (F) that has two materials (A and B) and a group of packaging materials (G) that also has two materials (C and D).</span></span> <span data-ttu-id="746db-110">Еще один материал (E) используется в процессе сборки машины в целом.</span><span class="sxs-lookup"><span data-stu-id="746db-110">Another material (E) is used during the general assembly of the machine.</span></span>

![Продукт H и деталь F](media/product-H-part-B.png)

<span data-ttu-id="746db-112">На рисунке выше показана техническая спецификация на продукт H. Эта структура позволяет получить представление о деталях и компонентах, входящих в машинный агрегат в целом.</span><span class="sxs-lookup"><span data-stu-id="746db-112">The preceding illustration represents the Engineering BOM for product H. This structure provides a good overview of the parts and components of the overall machine assembly.</span></span> <span data-ttu-id="746db-113">Тем не менее, хотя конструкторам продукта было бы удобно видеть спецификацию в таком виде, эта структура может неправильно иллюстрировать порядок сборки машины в цехе.</span><span class="sxs-lookup"><span data-stu-id="746db-113">However, although product designers might prefer to see the BOM represented in this way, this structure might not correctly represent the way that the machine is built on the shop floor.</span></span> 

<span data-ttu-id="746db-114">Например, техническая спецификация на предыдущем рисунке указывает, что электрический блок F собирается как отдельная деталь по отдельному заказу на выполнение работ.</span><span class="sxs-lookup"><span data-stu-id="746db-114">For example, the Engineering BOM in the preceding illustration indicates that electrical unit F is assembled as a separate part on a separate work order.</span></span> <span data-ttu-id="746db-115">Однако в цехе могут посчитать более рациональным собирать электрический блок в ходе сборки машины в целом, а не в виде отдельного заказа на выполнение работ.</span><span class="sxs-lookup"><span data-stu-id="746db-115">However, on the shop floor, it might be judged more optimal to assemble the electrical unit as part of the overall machine assembly, not as a separate work order.</span></span>

<span data-ttu-id="746db-116">В этой технической спецификации также указано, что деталь G — это отдельная деталь.</span><span class="sxs-lookup"><span data-stu-id="746db-116">This Engineering BOM also indicates that part G is a separate part.</span></span> <span data-ttu-id="746db-117">Однако в этой структуре деталь G представляет не физическую деталь, а совокупность упаковочных материалов.</span><span class="sxs-lookup"><span data-stu-id="746db-117">However, in this structure, part G doesn’t represent a physical part but a collection of packaging materials.</span></span> 

<span data-ttu-id="746db-118">Таким образом, несмотря на всю ценность технической спецификации для разработки продукта и его обслуживания, это не самый логичный способ представить процесс производства продукта.</span><span class="sxs-lookup"><span data-stu-id="746db-118">Therefore, although an Engineering BOM provides great value for the design of a product and maintenance of that design, it might not be the most logical way to support the manufacturing execution process of the product.</span></span> <span data-ttu-id="746db-119">И наоборот, производственная спецификация представляет оптимальный способ сборки продукта.</span><span class="sxs-lookup"><span data-stu-id="746db-119">By contrast, a Manufacturing BOM represents the best way to build a product.</span></span>

<span data-ttu-id="746db-120">На следующем рисунке показано, как предыдущая техническая спецификация превращается в производственную спецификацию.</span><span class="sxs-lookup"><span data-stu-id="746db-120">The following illustration shows how the preceding Engineering BOM is transitioned into a Manufacturing BOM.</span></span> <span data-ttu-id="746db-121">На этом рисунке (a) — спецификация на продукт H, а (b) — маршрутный лист для продукта H.</span><span class="sxs-lookup"><span data-stu-id="746db-121">In this illustration, (a) is the BOM for product H, and b is the route sheet for product H.</span></span>

<span data-ttu-id="746db-122">В этой структуре детали F и G не упоминаются, а материалы, из которых состоят эти детали, перенесены на следующий уровень спецификации.</span><span class="sxs-lookup"><span data-stu-id="746db-122">In this structure, you can see that there is no notion of parts F and G, and the materials that these parts consist of have been elevated to the next BOM level.</span></span> 

<span data-ttu-id="746db-123">В отличие от технической спецификации, в которой было две операционные карты, в производственной спецификации операционная карта только одна.</span><span class="sxs-lookup"><span data-stu-id="746db-123">Unlike the Engineering BOM, which had two operations sheets, the Manufacturing BOM has only one operations sheet.</span></span> <span data-ttu-id="746db-124">Операции упаковки, которая была связана с деталью G, также была перенесена на следующий уровень и теперь находится в операционной карте для продукта H. Сборка электрического блока представляет собой первую операцию.</span><span class="sxs-lookup"><span data-stu-id="746db-124">The packaging operation that was linked to part G has also been elevated and is now part of the operations sheet for product H. The assembly of the electrical unit is the first operation.</span></span> <span data-ttu-id="746db-125">Этот порядок представляется разумным, потому что этот блок используется на следующей операции, т. е. сборке машины.</span><span class="sxs-lookup"><span data-stu-id="746db-125">This order makes good sense, because this unit is used in the next operation, which is the machine assembly.</span></span> <span data-ttu-id="746db-126">Последняя операция — это операция упаковки, при которой потребляется два упаковочных материала (C и D).</span><span class="sxs-lookup"><span data-stu-id="746db-126">The last operation is the packaging operation, which consumes two packing materials (C and D).</span></span>

<span data-ttu-id="746db-127">Переход от технической спецификации к производственной спецификации обеспечивается типом строки "виртуальная спецификация".</span><span class="sxs-lookup"><span data-stu-id="746db-127">The transition between the Engineering BOM and the Manufacturing BOM is enabled through the Phantom BOM line type.</span></span> <span data-ttu-id="746db-128">Как предполагает слово "виртуальная", детали F и G исчезли во время перехода от одного типа спецификации к другому.</span><span class="sxs-lookup"><span data-stu-id="746db-128">As the term “phantom” indicates, parts F and G have disappeared during the transition between the two BOM types.</span></span> <span data-ttu-id="746db-129">В этом примере тип строки "виртуальная" применяется к строкам спецификации для деталей F и G в технической спецификации.</span><span class="sxs-lookup"><span data-stu-id="746db-129">In this example, the Phantom line type is applied to the BOM lines for parts F and G in the Engineering BOM.</span></span> <span data-ttu-id="746db-130">При создании производственного заказа или заказа партии техническая спецификация копируется в производственный заказ или заказ партии.</span><span class="sxs-lookup"><span data-stu-id="746db-130">When a production or batch order is created, the Engineering BOM is copied to the production or batch order.</span></span> <span data-ttu-id="746db-131">Затем, когда производится оценка заказа, происходит переход от технической спецификации к производственной спецификации, как показано на рисунках выше.</span><span class="sxs-lookup"><span data-stu-id="746db-131">Then, when the order is estimated, the transition from the Engineering BOM to the Manufacturing BOM occurs, as shown in the preceding illustrations.</span></span> <span data-ttu-id="746db-132">С операционной карты на втором рисунке упаковочные материалы C и D представляют собой вход для операции.</span><span class="sxs-lookup"><span data-stu-id="746db-132">From the operations sheet in the second illustration, packaging materials C and D are input for the operation.</span></span> 

## <a name="multilevel-phantom-bom-structures"></a><span data-ttu-id="746db-133">Многоуровневые структуры виртуальных спецификаций</span><span class="sxs-lookup"><span data-stu-id="746db-133">Multilevel phantom BOM structures</span></span>
<span data-ttu-id="746db-134">Тип строки "виртуальная" может использоваться в многоуровневых структурах спецификаций, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="746db-134">The Phantom line type can be used in multilevel BOM structures, as shown in the following illustration.</span></span> <span data-ttu-id="746db-135">На этом рисунке (a) — это спецификация на продукт G, а (b) — маршрутный лист для деталей E и F и продукта G.</span><span class="sxs-lookup"><span data-stu-id="746db-135">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for parts E and F and product G.</span></span> 

![Продукт G и деталь F с маршрутными листами](media/product-G-route-sheet-G.png)


<span data-ttu-id="746db-137">На следующем рисунке показаны результирующие производственная спецификация и маршрутный лист, если настроить строки спецификации для деталей E и F так, что тип строки — "виртуальная".</span><span class="sxs-lookup"><span data-stu-id="746db-137">The following illustration shows the resulting Manufacturing BOM and route sheet if the BOM lines for parts E and F are configured so that the line type is Phantom.</span></span> <span data-ttu-id="746db-138">На этом рисунке (a) — спецификация на продукт G, а (b) — маршрутный лист для продукта G.</span><span class="sxs-lookup"><span data-stu-id="746db-138">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for product G.</span></span>

![Продукт G](media/product-G.png)


## <a name="phantom-and-route-network"></a><span data-ttu-id="746db-140">Виртуальная спецификация и маршрутная сеть</span><span class="sxs-lookup"><span data-stu-id="746db-140">Phantom and route network</span></span>
<span data-ttu-id="746db-141">Виртуальные спецификации также могут использоваться для спецификации, у которой есть маршрутная сеть.</span><span class="sxs-lookup"><span data-stu-id="746db-141">Phantom BOMs can also be used for a BOM that has a route network.</span></span> <span data-ttu-id="746db-142">В маршрутной сети одна или несколько операций выполняется параллельно.</span><span class="sxs-lookup"><span data-stu-id="746db-142">In a route network, one or more operations run in parallel.</span></span> <span data-ttu-id="746db-143">На следующем рисунке показан пример маршрутной сети, используемой в многоуровневой спецификации.</span><span class="sxs-lookup"><span data-stu-id="746db-143">The following illustration shows an example of a route network that is used in a multilevel BOM.</span></span> <span data-ttu-id="746db-144">На этом рисунке (a) — это спецификация на продукт G и деталь F, а (b) — маршрутный лист для продукта G и детали F, имеющей маршрутную сеть.</span><span class="sxs-lookup"><span data-stu-id="746db-144">In this illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F, which has a route network.</span></span>

![Продукт G и деталь F](media/product-G-part-F.png)


<span data-ttu-id="746db-146">На следующем рисунке (a) — это спецификация на продукт G и деталь F, а (b) — маршрутный лист для продукта G и детали F.</span><span class="sxs-lookup"><span data-stu-id="746db-146">In the following illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F.</span></span>

![Продукт G и деталь F с маршрутными листами](media/product-G-part-F-with-route-sheet.png)
