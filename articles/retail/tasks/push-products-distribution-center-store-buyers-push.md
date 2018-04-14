--- 
title: "Распределение продуктов из центров распространения в магазины через централизованное распределение"
description: "Эта процедура содержит инструкции по созданию и обработке централизованного распределения для распределения продуктов из одного местоположения между одним или несколькими магазинами."
author: rubencdelgado
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f827cae291644bea0e6a1af8af9f692b118534ad
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a><span data-ttu-id="9ac87-103">Распределение продуктов из центров распространения в магазины через централизованное распределение</span><span class="sxs-lookup"><span data-stu-id="9ac87-103">Push products from distribution center to store using buyer's push</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9ac87-104">Эта процедура содержит инструкции по созданию и обработке централизованного распределения для распределения продуктов из одного местоположения между одним или несколькими магазинами.</span><span class="sxs-lookup"><span data-stu-id="9ac87-104">This procedure walks through the steps to create and process a Buyer´s push to distribute products from one location to one or many stores.</span></span> <span data-ttu-id="9ac87-105">Пользователь может определить несколько конфигураций и получать о системы предложения по распределению продуктов или вручную указывать, куда нужно распределять продукты и какое количество должно быть распределено в каждый из магазинов.</span><span class="sxs-lookup"><span data-stu-id="9ac87-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="9ac87-106">Процедура не включает настройку данных, которые можно использовать при централизованном распределении, например правила пополнения, организационные иерархии и веса магазинов.</span><span class="sxs-lookup"><span data-stu-id="9ac87-106">This procedure doesn't include setup of data that can be used in the Buyer´s push, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="9ac87-107">В данной процедуре используется демонстрационная компания USRT.</span><span class="sxs-lookup"><span data-stu-id="9ac87-107">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="9ac87-108">Перейдите в раздел "Централизованное распределение"</span><span class="sxs-lookup"><span data-stu-id="9ac87-108">Go to Buyer's push.</span></span>
2. <span data-ttu-id="9ac87-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9ac87-109">Click New.</span></span>
3. <span data-ttu-id="9ac87-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="9ac87-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="9ac87-111">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9ac87-111">In the Site field, enter or select a value.</span></span>
5. <span data-ttu-id="9ac87-112">В поле "Склад" введите или выберите склад, который имеет продукты с нужными количествами в наличии.</span><span class="sxs-lookup"><span data-stu-id="9ac87-112">In the Warehouse field, enter or select a warehouse that has products with on-hand quantities.</span></span>
6. <span data-ttu-id="9ac87-113">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="9ac87-113">Click Add.</span></span>
7. <span data-ttu-id="9ac87-114">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="9ac87-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="9ac87-115">В поле "Код номенклатуры" введите или выберите продукт.</span><span class="sxs-lookup"><span data-stu-id="9ac87-115">In the Item number field, enter or select a product.</span></span>
9. <span data-ttu-id="9ac87-116">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="9ac87-116">Click Add.</span></span>
10. <span data-ttu-id="9ac87-117">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="9ac87-117">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="9ac87-118">В поле "Код номенклатуры" введите или выберите вариант продукта.</span><span class="sxs-lookup"><span data-stu-id="9ac87-118">In the Item number field, enter or select a variant product.</span></span>
    * <span data-ttu-id="9ac87-119">При вводе варианта продукта строки будут созданы для каждого варианта.</span><span class="sxs-lookup"><span data-stu-id="9ac87-119">When entering a variant product, lines will be created for each variant.</span></span>  
12. <span data-ttu-id="9ac87-120">В списке пометьте строку.</span><span class="sxs-lookup"><span data-stu-id="9ac87-120">In the list, mark a row.</span></span>
13. <span data-ttu-id="9ac87-121">В поле "Количество принудительной отправки" введите выбранного продукта, которое вы хотите распределять.</span><span class="sxs-lookup"><span data-stu-id="9ac87-121">In the Pushed quantity field, type how many of the selected product you want to distribute.</span></span>
14. <span data-ttu-id="9ac87-122">В поле "Дополнительное количество" введите количество продуктов, которые имеются в достаточном для распределения количестве.</span><span class="sxs-lookup"><span data-stu-id="9ac87-122">In the Additional quantity to push field, enter the quantity of the products that have available quantity to distribute.</span></span>
15. <span data-ttu-id="9ac87-123">В поле "Распределение" введите "Вес местоположения".</span><span class="sxs-lookup"><span data-stu-id="9ac87-123">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="9ac87-124">Можно выбрать другие типы для использования других правил распределения.</span><span class="sxs-lookup"><span data-stu-id="9ac87-124">You can select the other types to use other rules for the distribution.</span></span>  
16. <span data-ttu-id="9ac87-125">В поле "Иерархия пополнения" выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9ac87-125">In the Replenishment hierarchy field, select a value.</span></span>
17. <span data-ttu-id="9ac87-126">Выберите "Да" в поле "Учитывать ассортименты".</span><span class="sxs-lookup"><span data-stu-id="9ac87-126">Select Yes in the Respect assortments field.</span></span>
18. <span data-ttu-id="9ac87-127">Щелкните "Вычисление количеств" и проверьте количества, добавленные в строки в разделе "Склад".</span><span class="sxs-lookup"><span data-stu-id="9ac87-127">Click Calculate quantities and review the quantities that are added to the rows in the Warehouse section.</span></span>
19. <span data-ttu-id="9ac87-128">Щелкните "Создать заказ".</span><span class="sxs-lookup"><span data-stu-id="9ac87-128">Click Create order.</span></span>
20. <span data-ttu-id="9ac87-129">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="9ac87-129">Click Yes.</span></span>


