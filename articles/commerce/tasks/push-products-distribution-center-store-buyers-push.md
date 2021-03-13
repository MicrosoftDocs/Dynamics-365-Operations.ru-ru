---
title: Распределение продуктов из центров распространения в магазины через централизованное распределение
description: Эта процедура содержит инструкции по созданию и обработке централизованного распределения для распределения продуктов из одного местоположения между одним или несколькими магазинами.
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailBuyersPush, InventLocationIdLookup, InventItemIdLookupSimple, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3720945823cf127f776a9ea6a6ad75a72ceec00c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012349"
---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a><span data-ttu-id="77ee6-103">Распределение продуктов из центров распространения в магазины через централизованное распределение</span><span class="sxs-lookup"><span data-stu-id="77ee6-103">Push products from distribution center to store using buyer's push</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77ee6-104">Эта процедура содержит инструкции по созданию и обработке централизованного распределения для распределения продуктов из одного местоположения между одним или несколькими магазинами.</span><span class="sxs-lookup"><span data-stu-id="77ee6-104">This procedure walks through the steps to create and process a Buyer´s push to distribute products from one location to one or many stores.</span></span> <span data-ttu-id="77ee6-105">Пользователь может определить несколько конфигураций и получать о системы предложения по распределению продуктов или вручную указывать, куда нужно распределять продукты и какое количество должно быть распределено в каждый из магазинов.</span><span class="sxs-lookup"><span data-stu-id="77ee6-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="77ee6-106">Процедура не включает настройку данных, которые можно использовать при централизованном распределении, например правила пополнения, организационные иерархии и веса магазинов.</span><span class="sxs-lookup"><span data-stu-id="77ee6-106">This procedure doesn't include setup of data that can be used in the Buyer´s push, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="77ee6-107">В данной процедуре используется демонстрационная компания USRT.</span><span class="sxs-lookup"><span data-stu-id="77ee6-107">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="77ee6-108">Перейдите в раздел "Централизованное распределение"</span><span class="sxs-lookup"><span data-stu-id="77ee6-108">Go to Buyer's push.</span></span>
2. <span data-ttu-id="77ee6-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="77ee6-109">Click New.</span></span>
3. <span data-ttu-id="77ee6-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="77ee6-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="77ee6-111">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="77ee6-111">In the Site field, enter or select a value.</span></span>
5. <span data-ttu-id="77ee6-112">В поле "Склад" введите или выберите склад, который имеет продукты с нужными количествами в наличии.</span><span class="sxs-lookup"><span data-stu-id="77ee6-112">In the Warehouse field, enter or select a warehouse that has products with on-hand quantities.</span></span>
6. <span data-ttu-id="77ee6-113">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="77ee6-113">Click Add.</span></span>
7. <span data-ttu-id="77ee6-114">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="77ee6-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="77ee6-115">В поле "Код номенклатуры" введите или выберите продукт.</span><span class="sxs-lookup"><span data-stu-id="77ee6-115">In the Item number field, enter or select a product.</span></span>
9. <span data-ttu-id="77ee6-116">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="77ee6-116">Click Add.</span></span>
10. <span data-ttu-id="77ee6-117">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="77ee6-117">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="77ee6-118">В поле "Код номенклатуры" введите или выберите вариант продукта.</span><span class="sxs-lookup"><span data-stu-id="77ee6-118">In the Item number field, enter or select a variant product.</span></span>
    * <span data-ttu-id="77ee6-119">При вводе варианта продукта строки будут созданы для каждого варианта.</span><span class="sxs-lookup"><span data-stu-id="77ee6-119">When entering a variant product, lines will be created for each variant.</span></span>  
12. <span data-ttu-id="77ee6-120">В списке пометьте строку.</span><span class="sxs-lookup"><span data-stu-id="77ee6-120">In the list, mark a row.</span></span>
13. <span data-ttu-id="77ee6-121">В поле "Количество принудительной отправки" введите выбранного продукта, которое вы хотите распределять.</span><span class="sxs-lookup"><span data-stu-id="77ee6-121">In the Pushed quantity field, type how many of the selected product you want to distribute.</span></span>
14. <span data-ttu-id="77ee6-122">В поле "Дополнительное количество" введите количество продуктов, которые имеются в достаточном для распределения количестве.</span><span class="sxs-lookup"><span data-stu-id="77ee6-122">In the Additional quantity to push field, enter the quantity of the products that have available quantity to distribute.</span></span>
15. <span data-ttu-id="77ee6-123">В поле "Распределение" введите "Вес местоположения".</span><span class="sxs-lookup"><span data-stu-id="77ee6-123">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="77ee6-124">Можно выбрать другие типы для использования других правил распределения.</span><span class="sxs-lookup"><span data-stu-id="77ee6-124">You can select the other types to use other rules for the distribution.</span></span>  
16. <span data-ttu-id="77ee6-125">В поле "Иерархия пополнения" выберите значение.</span><span class="sxs-lookup"><span data-stu-id="77ee6-125">In the Replenishment hierarchy field, select a value.</span></span>
17. <span data-ttu-id="77ee6-126">Выберите "Да" в поле "Учитывать ассортименты".</span><span class="sxs-lookup"><span data-stu-id="77ee6-126">Select Yes in the Respect assortments field.</span></span>
18. <span data-ttu-id="77ee6-127">Щелкните "Вычисление количеств" и проверьте количества, добавленные в строки в разделе "Склад".</span><span class="sxs-lookup"><span data-stu-id="77ee6-127">Click Calculate quantities and review the quantities that are added to the rows in the Warehouse section.</span></span>
19. <span data-ttu-id="77ee6-128">Щелкните "Создать заказ".</span><span class="sxs-lookup"><span data-stu-id="77ee6-128">Click Create order.</span></span>
20. <span data-ttu-id="77ee6-129">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="77ee6-129">Click Yes.</span></span>

