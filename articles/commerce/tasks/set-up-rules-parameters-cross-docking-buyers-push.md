---
title: Настройка правил и параметров для централизованного распределения и кросс-докинга
description: Эта процедура демонстрирует шаги по созданию правил пополнения.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bccd92946783628dce37c3fd018e4dd927efd49
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141145"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a><span data-ttu-id="d548c-103">Настройка правил и параметров для централизованного распределения и кросс-докинга</span><span class="sxs-lookup"><span data-stu-id="d548c-103">Set up rules and parameters for cross docking and buyer's push</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d548c-104">Эта процедура демонстрирует шаги по созданию правил пополнения.</span><span class="sxs-lookup"><span data-stu-id="d548c-104">This procedure demonstrates the steps to create Replenishment rules.</span></span> <span data-ttu-id="d548c-105">Правила пополнения можно использовать для управления тем, как продукты распределяются по магазинам при использовании кросс-докинга и централизованного распределения.</span><span class="sxs-lookup"><span data-stu-id="d548c-105">Replenishment rules can be used to control how products are distributed to stores when using Cross-docking and Buyer´s push.</span></span> <span data-ttu-id="d548c-106">Правила пополнения можно настраивать для магазинов или групп магазинов.</span><span class="sxs-lookup"><span data-stu-id="d548c-106">Replenishment rules can be set up for stores or store groups.</span></span> <span data-ttu-id="d548c-107">Вес, указанный для каждой строки в правиле, будет определять, как количества продуктов будут распределяться между магазинами при использовании правил пополнения в качестве метода распределения для кросс-докинга или централизованного распределения.</span><span class="sxs-lookup"><span data-stu-id="d548c-107">The weight defined for each line in a rule will control how the quantities of products will get distributed between the stores when using Replenishment rules as the distribution method in Cross-docking or Buyer´s push.</span></span> <span data-ttu-id="d548c-108">В данной процедуре используется демонстрационная компания USRT.</span><span class="sxs-lookup"><span data-stu-id="d548c-108">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="d548c-109">Перейдите в раздел "Правила пополнения".</span><span class="sxs-lookup"><span data-stu-id="d548c-109">Go to Replenishment rules.</span></span>
2. <span data-ttu-id="d548c-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d548c-110">Click New.</span></span>
3. <span data-ttu-id="d548c-111">В поле "Правило пополнения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d548c-111">In the Replenishment rule field, type a value.</span></span>
4. <span data-ttu-id="d548c-112">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d548c-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d548c-113">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d548c-113">Click Save.</span></span>
6. <span data-ttu-id="d548c-114">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="d548c-114">Click Add.</span></span>
7. <span data-ttu-id="d548c-115">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="d548c-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d548c-116">Можно выбрать в качестве типа "Иерархия пополнения" или "Канал".</span><span class="sxs-lookup"><span data-stu-id="d548c-116">You can choose Replenishment hierarchy or Channel for the type.</span></span> <span data-ttu-id="d548c-117">Значение определяет, будет в поле "Имя" выбрана иерархия каналов или конкретный канал.</span><span class="sxs-lookup"><span data-stu-id="d548c-117">The value controls whether the selection in Name will be a hierarchy of channels or a specific channel.</span></span>  <span data-ttu-id="d548c-118">В этом примере оставьте значение "Иерархия пополнения".</span><span class="sxs-lookup"><span data-stu-id="d548c-118">For this example, leave it set as Replenishment hierarchy.</span></span>  
8. <span data-ttu-id="d548c-119">В поле "Имя" выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d548c-119">In the Name field, select a value.</span></span>
    * <span data-ttu-id="d548c-120">Значение веса по умолчанию подставляется из веса, определенного на складе.</span><span class="sxs-lookup"><span data-stu-id="d548c-120">The default weight value is populated from the weight defined on the warehouse.</span></span>  <span data-ttu-id="d548c-121">Этот вес можно использовать для правила пополнения или можно ввести в поле "Вес" новый вес.</span><span class="sxs-lookup"><span data-stu-id="d548c-121">This weight can be used for the Replenishment rule or you can enter a new weight in the Weight field.</span></span>  
9. <span data-ttu-id="d548c-122">В поле "Вес" введите число.</span><span class="sxs-lookup"><span data-stu-id="d548c-122">In the Weight field, enter a number.</span></span>
10. <span data-ttu-id="d548c-123">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="d548c-123">Click Add.</span></span>
11. <span data-ttu-id="d548c-124">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="d548c-124">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="d548c-125">В поле "Тип" выберите "Канал".</span><span class="sxs-lookup"><span data-stu-id="d548c-125">In the Type field, select 'Channel'.</span></span>
13. <span data-ttu-id="d548c-126">В поле "Имя" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d548c-126">In the Name field, enter or select a value.</span></span>
14. <span data-ttu-id="d548c-127">В поле "Вес" введите число.</span><span class="sxs-lookup"><span data-stu-id="d548c-127">In the Weight field, enter a number.</span></span>
15. <span data-ttu-id="d548c-128">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d548c-128">Click Save.</span></span>

