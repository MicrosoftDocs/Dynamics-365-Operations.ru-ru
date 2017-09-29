--- 
title: "Кросс-докинг продуктов со склада приемки в магазины"
description: "Эта процедура содержит инструкции по созданию и обработке кросс-докинга для распределения продуктов из получающего местоположения заказа на покупку между одним или несколькими магазинами."
author: BibiSp
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: daa42bb83d6b988e8fd18db6ad8386c67fd3e6e5
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a><span data-ttu-id="4b1cd-103">Кросс-докинг продуктов со склада приемки в магазины</span><span class="sxs-lookup"><span data-stu-id="4b1cd-103">Cross-dock products from receiving warehouse to stores</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4b1cd-104">Эта процедура содержит инструкции по созданию и обработке кросс-докинга для распределения продуктов из получающего местоположения заказа на покупку между одним или несколькими магазинами.</span><span class="sxs-lookup"><span data-stu-id="4b1cd-104">This procedure walks through the steps to create and process a Cross-dock to distribute products from the receiving location of a purchase order to one or many stores.</span></span> <span data-ttu-id="4b1cd-105">Пользователь может определить несколько конфигураций и получать о системы предложения по распределению продуктов или вручную указывать, куда нужно распределять продукты и какое количество должно быть распределено в каждый из магазинов.</span><span class="sxs-lookup"><span data-stu-id="4b1cd-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="4b1cd-106">Процедура не включает настройку данных, которые можно использовать в кросс-докинге, например правила пополнения, организационные иерархии и веса магазинов.</span><span class="sxs-lookup"><span data-stu-id="4b1cd-106">The procedure doesn't include setup of data that can be used in the Cross-dock, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="4b1cd-107">В данной процедуре используется демонстрационная компания USRT.</span><span class="sxs-lookup"><span data-stu-id="4b1cd-107">The procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="4b1cd-108">Перейдите в раздел "Все заказы на покупку".</span><span class="sxs-lookup"><span data-stu-id="4b1cd-108">Go to All purchase orders.</span></span>
2. <span data-ttu-id="4b1cd-109">Выберите в списке заказ на покупку и щелкните ссылку, чтобы открыть заказ.</span><span class="sxs-lookup"><span data-stu-id="4b1cd-109">Select a purchase order in the list and click the link to open the order.</span></span>
3. <span data-ttu-id="4b1cd-110">В области действий щелкните "Розница".</span><span class="sxs-lookup"><span data-stu-id="4b1cd-110">On the Action Pane, click Retail.</span></span>
4. <span data-ttu-id="4b1cd-111">Щелкните "Кросс-докинг".</span><span class="sxs-lookup"><span data-stu-id="4b1cd-111">Click Cross docking.</span></span>
5. <span data-ttu-id="4b1cd-112">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="4b1cd-112">Click Edit.</span></span>
    * <span data-ttu-id="4b1cd-113">Категории можно использовать для фильтрации номенклатуры в разделе "Строки".</span><span class="sxs-lookup"><span data-stu-id="4b1cd-113">The category can be used to filter the items in the Lines section.</span></span>  
6. <span data-ttu-id="4b1cd-114">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4b1cd-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="4b1cd-115">В поле "Количество для кросс-докинга" введите значение для определения того, какое количество приобретенного выбранного продукта будет распределено.</span><span class="sxs-lookup"><span data-stu-id="4b1cd-115">In the Cross docking quantity field, type a value to specify how much of the quantity being purchased of the selected product should be distributed.</span></span>
8. <span data-ttu-id="4b1cd-116">В поле "Дополнительное количество для кросс-докинга" введите значение для указания количеств для распределения доступных приобретенных продуктов</span><span class="sxs-lookup"><span data-stu-id="4b1cd-116">In the Additional cross docking quantity field, enter a value to specify the quantities to distribute for the available products being purchased</span></span>
9. <span data-ttu-id="4b1cd-117">В поле "Распределение" введите "Вес местоположения".</span><span class="sxs-lookup"><span data-stu-id="4b1cd-117">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="4b1cd-118">Можно выбрать другие типы для использования различных правил распределения.</span><span class="sxs-lookup"><span data-stu-id="4b1cd-118">You can select the other types to use different rules for the distribution.</span></span>  
10. <span data-ttu-id="4b1cd-119">В поле "Иерархия пополнения" выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4b1cd-119">In the Replenishment hierarchy field, select a value.</span></span>
11. <span data-ttu-id="4b1cd-120">Выберите "Да" в поле "Учитывать ассортименты".</span><span class="sxs-lookup"><span data-stu-id="4b1cd-120">Select Yes in the Respect assortments field.</span></span>
12. <span data-ttu-id="4b1cd-121">Щелкните "Вычисление количеств".</span><span class="sxs-lookup"><span data-stu-id="4b1cd-121">Click Calculate quantities.</span></span>
13. <span data-ttu-id="4b1cd-122">Щелкните "Создать заказ".</span><span class="sxs-lookup"><span data-stu-id="4b1cd-122">Click Create order.</span></span>
14. <span data-ttu-id="4b1cd-123">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="4b1cd-123">Click Yes.</span></span>
15. <span data-ttu-id="4b1cd-124">В списке найдите и выберите склад, который получил продукты</span><span class="sxs-lookup"><span data-stu-id="4b1cd-124">In the list, find and select a warehouse that received products</span></span>
16. <span data-ttu-id="4b1cd-125">Щелкните "Заказ" для просмотра заказов, который были созданы для выбранного склада</span><span class="sxs-lookup"><span data-stu-id="4b1cd-125">Click Order to view the orders that got created for the selected warehouse</span></span>


