---
title: "Атрибуты партии"
description: "В этом разделе представлена информация об атрибутах партии. Атрибуты партии являются характеристиками сырья и готовых продуктов, которые образуют партии складских запасов. В разделе также описывается, как назначать атрибуты партии, и как можно производить по ним поиск при резервировании партий."
author: YuyuScheller
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 255cb8f530b1906409c54dc446872802214482e8
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="batch-attributes"></a><span data-ttu-id="4a4e6-105">Атрибуты партии</span><span class="sxs-lookup"><span data-stu-id="4a4e6-105">Batch attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a4e6-106">В этом разделе представлена информация об атрибутах партии.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-106">This topic provides information about batch attributes.</span></span> <span data-ttu-id="4a4e6-107">Атрибуты партии являются характеристиками сырья и готовых продуктов, которые образуют партии складских запасов.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-107">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="4a4e6-108">В разделе также описывается, как назначать атрибуты партии, и как можно производить по ним поиск при резервировании партий.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-108">The topic also explains how to assign batch attributes, and how you can search on them when you reserve batches.</span></span>

<span data-ttu-id="4a4e6-109">Атрибуты партии являются характеристиками сырья и готовых продуктов, которые образуют партии складских запасов.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-109">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="4a4e6-110">Атрибуты партии могут различаться в зависимости от ряда факторов, включающих условия окружающей среды или качество сырья, использованного для создания партии, или выхода готового продукта.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-110">Batch attributes can vary, depending on factors such as environmental conditions, the quality of the raw materials that are used to produce the batch, or the outcome of the finished product.</span></span> <span data-ttu-id="4a4e6-111">Число и типы используемых атрибутов партии сильно отличаются для различных отраслей.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-111">The number and types of batch attributes that are used can vary widely from one industry to another.</span></span> <span data-ttu-id="4a4e6-112">Здесь приводятся два примера использования атрибутов партий:</span><span class="sxs-lookup"><span data-stu-id="4a4e6-112">Here are two examples that show how to use batch attributes:</span></span>

-   <span data-ttu-id="4a4e6-113">При производстве сыра молоко как сырье может характеризоваться такими атрибутами как содержание жира и процентное содержание.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-113">In the cheese industry, milk, which is one of the raw materials that are used to produce the cheese, can have attributes such as fat content and percentage weight.</span></span> <span data-ttu-id="4a4e6-114">Сыр, производимый из молока, может иметь другие атрибуты, например, влажность и срок вызревания.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-114">The cheese that is produced from the milk can have other attributes, such as moisture and age.</span></span>
-   <span data-ttu-id="4a4e6-115">При производстве стали производимое железо может характеризоваться такими атрибутами как содержание магния, содержание серебра и содержание цинка.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-115">In the steel industry, the iron that is produced might have attributes such as the percentages of magnesium content, silver content, and zinc content.</span></span>

<span data-ttu-id="4a4e6-116">Чтобы лучше управлять числом и типами атрибутов, вы можете использовать группы атрибутов партии.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-116">To better manage the number and types of attributes, you can use batch attribute groups.</span></span> <span data-ttu-id="4a4e6-117">Таким образом вам не придется добавлять каждый атрибут индивидуально.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-117">In this way, you don't have to add each attribute individually.</span></span>

## <a name="assign-batch-attributes"></a><span data-ttu-id="4a4e6-118">Назначение атрибутов партии</span><span class="sxs-lookup"><span data-stu-id="4a4e6-118">Assign batch attributes</span></span>
<span data-ttu-id="4a4e6-119">Атрибуты партии можно назначать отдельным продуктам, входящим в партии складских запасов, или можно назначать их продуктам, связанным с конкретными клиентами.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-119">You can assign batch attributes to individual products that are held in inventory batches, or you can assign them to products that are associated with specific customers.</span></span> <span data-ttu-id="4a4e6-120">Прежде чем атрибут партии можно будет назначить на уровне клиентов, его необходимо назначить на уровне продукта.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-120">Before you can assign a batch attribute at the customer level, you must assign it at the product level.</span></span> <span data-ttu-id="4a4e6-121">Продукт должен иметь аналитику партии, установленную в состояние **Активная** в группе аналитик отслеживания.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-121">The product must have the batch dimension set to **Active** in the tracking dimension group.</span></span> <span data-ttu-id="4a4e6-122">Чтобы назначить атрибут партии отдельному продукту, используйте страницу для определенного продукта.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-122">To assign a batch attribute to an individual product, use the product-specific page.</span></span> <span data-ttu-id="4a4e6-123">Если атрибут является специфическим для продукта для клиента, используйте форму для определенного клиента.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-123">If the attribute is specific to a product for a customer, use the customer-specific page.</span></span> <span data-ttu-id="4a4e6-124">Когда вы добавляете атрибут к продукту, вы также определяете другие параметры.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-124">When you add an attribute to a product, you also define other parameters.</span></span> <span data-ttu-id="4a4e6-125">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-125">Here are some examples:</span></span>

-   <span data-ttu-id="4a4e6-126">Минимальный и максимальный диапазоны для атрибута типа **Целое число** или **Дробь**.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-126">The minimum and maximum ranges for an attribute of the **Integer** or **Fraction** type.</span></span>
-   <span data-ttu-id="4a4e6-127">Действия, выполняемые при превышении допуска, для атрибута типа **Целое число** или **Дробь**.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-127">The tolerance actions for an attribute of the **Integer** or **Fraction** type.</span></span> <span data-ttu-id="4a4e6-128">Если значение атрибута выходит за пределы минимального и максимального диапазонов, действие может быть или предупреждением, или сообщением об ошибке.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-128">If the value of the attribute falls outside the minimum and maximum range, the action can be either a warning message or an error message.</span></span>
-   <span data-ttu-id="4a4e6-129">Целевое значение для атрибута.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-129">The target value for the attribute.</span></span> <span data-ttu-id="4a4e6-130">Данное значение является оптимальным значением атрибута и применяется к атрибутам всех типов.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-130">This value is the optimal value of the attribute, and it applies to all attribute types.</span></span>

<span data-ttu-id="4a4e6-131">Доступ к страницам для продуктов, выбираемых на странице **Запущенные в производство продукты**, предоставляется в разделе "Управление сведениями о продуктах".</span><span class="sxs-lookup"><span data-stu-id="4a4e6-131">You can access the pages for products that you select on the **Released products** page in Product information management.</span></span> <span data-ttu-id="4a4e6-132">После того как продукту назначены атрибуты партии, можно затем добавить отдельные значения атрибутам на странице **Атрибуты партии складских запасов**.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-132">After you assign batch attributes to a product, you can add specific values to the attributes on the **Inventory batch attributes** page.</span></span>

## <a name="reserve-batches"></a><span data-ttu-id="4a4e6-133">Резервирование партий</span><span class="sxs-lookup"><span data-stu-id="4a4e6-133">Reserve batches</span></span>
<span data-ttu-id="4a4e6-134">Вы можете искать по атрибутам партии, когда вы резервируете партию для заказа на продажу, чтобы выполнить заказ клиента, или когда вы комплектуете и резервируете партии для производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-134">You can search on batch attributes when you do batch reservations for a sales order to fulfill a customer's order, or when you pick and reserve batches for a production order.</span></span> <span data-ttu-id="4a4e6-135">Поиск помогает найти партию складских запасов, в которой содержится продукт с требуемыми атрибутами партии.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-135">The search helps locate an inventory batch that contains the product that has the batch attribute that you want.</span></span> <span data-ttu-id="4a4e6-136">После того как партия или партии найдены, можно затем зарезервировать продукт для создаваемой строки складской проводки.</span><span class="sxs-lookup"><span data-stu-id="4a4e6-136">After you locate the batch or batches, you can reserve the product to the originating inventory transaction line.</span></span>




