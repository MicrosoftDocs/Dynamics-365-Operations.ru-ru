---
title: "Трассировка номенклатуры или сырья"
description: "Эта процедура демонстрирует способ использования трассировки номенклатуры, чтобы указать, где номенклатуры или сырье использовались или используются."
author: pjacobse
manager: AnnBe
ms.date: 06/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 86868fc3a5d1543e46b3ebd4dcc31cbc3a78479b
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---
# <a name="trace-an-item-or-raw-material"></a><span data-ttu-id="956eb-103">Трассировка номенклатуры или сырья</span><span class="sxs-lookup"><span data-stu-id="956eb-103">Trace an item or raw material</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="956eb-104">Эта процедура демонстрирует способ использования трассировки номенклатуры, чтобы указать, где номенклатуры или сырье использовались или используются.</span><span class="sxs-lookup"><span data-stu-id="956eb-104">This procedure demonstrates how to use item tracing to identify where items or raw materials have been used or are being used.</span></span> <span data-ttu-id="956eb-105">С помощью этой процедуры можно определить номенклатуру, отследить ее до источника, а затем выполнить трассировку вперед до производства и продажи готовой продукции.</span><span class="sxs-lookup"><span data-stu-id="956eb-105">With this procedure, you can identify an item, trace it back to the source, and then trace forward through the production and sale of the finished product.</span></span> <span data-ttu-id="956eb-106">Процесс можно использовать для изучения клиентов, на которых это повлияло, затронутые заказы на продажу и т. д.</span><span class="sxs-lookup"><span data-stu-id="956eb-106">The process can be used to investigate the customers impacted, the sales orders affected, and more.</span></span> <span data-ttu-id="956eb-107">В этой процедуре используется компания с демонстрационными данными USP2.</span><span class="sxs-lookup"><span data-stu-id="956eb-107">This procedure uses demo data company USP2.</span></span>


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a><span data-ttu-id="956eb-108">Трассировка номенклатуры назад с использованием известного номера партии</span><span class="sxs-lookup"><span data-stu-id="956eb-108">Trace an item backwards using a known batch number</span></span>
1. <span data-ttu-id="956eb-109">Перейдите в раздел "Управление запасами" > "Запросы и отчеты" > "Аналитики отслеживания" > "Трассировка номенклатур".</span><span class="sxs-lookup"><span data-stu-id="956eb-109">Go to Inventory management > Inquiries and reports > Tracking dimensions > Item tracing.</span></span>
2. <span data-ttu-id="956eb-110">В поле "Код номенклатуры" выберите "P9100".</span><span class="sxs-lookup"><span data-stu-id="956eb-110">In the Item number field, select P9100.</span></span>
3. <span data-ttu-id="956eb-111">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="956eb-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="956eb-112">В поле "Вперед или назад" выберите "Назад".</span><span class="sxs-lookup"><span data-stu-id="956eb-112">In the Forward or backward field, select 'Backward'.</span></span>
5. <span data-ttu-id="956eb-113">В поле "Номер партии" выберите "as-12-344-01".</span><span class="sxs-lookup"><span data-stu-id="956eb-113">In the Batch number field, select as-12-344-01.</span></span>
6. <span data-ttu-id="956eb-114">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="956eb-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="956eb-115">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="956eb-115">Click OK.</span></span>

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a><span data-ttu-id="956eb-116">Указание номенклатуры, ее трассировка вперед и создание анализа</span><span class="sxs-lookup"><span data-stu-id="956eb-116">Identify an item, trace it forward, and make an analysis</span></span>
    * <span data-ttu-id="956eb-117">Верхний узел дерева представляет количество выбранной номенклатуры и партии, имеющееся в наличии.</span><span class="sxs-lookup"><span data-stu-id="956eb-117">The top node of the tree represents the on hand quantity of the selected item and batch.</span></span> <span data-ttu-id="956eb-118">Необходимо развернуть узлы дерева для поиска номенклатуры, для которой должна быть выполнена прямая трассировка.</span><span class="sxs-lookup"><span data-stu-id="956eb-118">You need to expand the nodes of the tree to find the item that the forward trace should be executed on.</span></span>   
1. <span data-ttu-id="956eb-119">В дереве разверните описанные ниже узлы и выберите последний узел.</span><span class="sxs-lookup"><span data-stu-id="956eb-119">In the tree, expand 'the nodes described below, and then select the last node'.</span></span>
    * <span data-ttu-id="956eb-120">Разверните узел "P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015 ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101" и выберите его.</span><span class="sxs-lookup"><span data-stu-id="956eb-120">Expand: 'P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101' and then select that node.</span></span>     
2. <span data-ttu-id="956eb-121">В дереве разверните описанный ниже узел и выберите этот узел.</span><span class="sxs-lookup"><span data-stu-id="956eb-121">In the tree, expand 'the node described below and then select that node'.</span></span>
    * <span data-ttu-id="956eb-122">Начиная с только что выбранного узла, разверните узел "M9103 ● Production line B-000050 ● 12/9/2015 ● -160.00 lb ● Size=70, Color=OK, Site=1, Warehouse=10, Batch number=App01" и выберите его.</span><span class="sxs-lookup"><span data-stu-id="956eb-122">Starting from the node that you’ve just selected,  expand 'M9103 ● Production line B-000050 ● 12/9/2015  ● -160.00 lb ● Size=70, Color=OK, Site=1, Warehouse=10, Batch number=App01' and then select that node.</span></span>  
3. <span data-ttu-id="956eb-123">Щелкните "Трассировать от узла".</span><span class="sxs-lookup"><span data-stu-id="956eb-123">Click Trace from node.</span></span>
4. <span data-ttu-id="956eb-124">Щелкните "Вперед".</span><span class="sxs-lookup"><span data-stu-id="956eb-124">Click Forward.</span></span>
5. <span data-ttu-id="956eb-125">В области действий щелкните "Трассировка".</span><span class="sxs-lookup"><span data-stu-id="956eb-125">On the Action Pane, click Tracing.</span></span>
    * <span data-ttu-id="956eb-126">Существует несколько параметров трассировки, которые предоставляют сведения о клиентах, на которых повлияла отслеживаемая номенклатура, и заказах на продажу, связанных с номенклатурой, которая была или не была отгружена.</span><span class="sxs-lookup"><span data-stu-id="956eb-126">There are several tracing options which provide information about the customers impacted by the item that you’re tracing, and the sales orders related to the item which have and haven’t been shipped.</span></span>   
6. <span data-ttu-id="956eb-127">Щелкните "Клиенты".</span><span class="sxs-lookup"><span data-stu-id="956eb-127">Click Customers.</span></span>
7. <span data-ttu-id="956eb-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="956eb-128">Close the page.</span></span>
8. <span data-ttu-id="956eb-129">В области действий щелкните "Трассировка".</span><span class="sxs-lookup"><span data-stu-id="956eb-129">On the Action Pane, click Tracing.</span></span>
9. <span data-ttu-id="956eb-130">Щелкните "Отгруженные заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="956eb-130">Click Shipped sales orders.</span></span>
10. <span data-ttu-id="956eb-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="956eb-131">Close the page.</span></span>

