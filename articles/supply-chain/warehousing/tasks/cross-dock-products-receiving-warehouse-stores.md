---
title: Кросс-докинг продуктов со склада приемки в магазины
description: Эта процедура содержит инструкции по созданию и обработке кросс-докинга для распределения продуктов из получающего местоположения заказа на покупку между одним или несколькими магазинами.
author: ShylaThompson
manager: tfehr
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailBuyersPushPerPackage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac93806bc85be92840548e160ddf803e63adbbc4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977196"
---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a><span data-ttu-id="11c3f-103">Кросс-докинг продуктов со склада приемки в магазины</span><span class="sxs-lookup"><span data-stu-id="11c3f-103">Cross-dock products from receiving warehouse to stores</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="11c3f-104">Эта процедура содержит инструкции по созданию и обработке кросс-докинга для распределения продуктов из получающего местоположения заказа на покупку между одним или несколькими магазинами.</span><span class="sxs-lookup"><span data-stu-id="11c3f-104">This procedure walks through the steps to create and process a Cross-dock to distribute products from the receiving location of a purchase order to one or many stores.</span></span> <span data-ttu-id="11c3f-105">Пользователь может определить несколько конфигураций и получать о системы предложения по распределению продуктов или вручную указывать, куда нужно распределять продукты и какое количество должно быть распределено в каждый из магазинов.</span><span class="sxs-lookup"><span data-stu-id="11c3f-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="11c3f-106">Процедура не включает настройку данных, которые можно использовать в кросс-докинге, например правила пополнения, организационные иерархии и веса магазинов.</span><span class="sxs-lookup"><span data-stu-id="11c3f-106">The procedure doesn't include setup of data that can be used in the Cross-dock, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="11c3f-107">В данной процедуре используется демонстрационная компания USRT.</span><span class="sxs-lookup"><span data-stu-id="11c3f-107">The procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="11c3f-108">Перейдите в раздел "Все заказы на покупку".</span><span class="sxs-lookup"><span data-stu-id="11c3f-108">Go to All purchase orders.</span></span>
2. <span data-ttu-id="11c3f-109">Выберите в списке заказ на покупку и щелкните ссылку, чтобы открыть заказ.</span><span class="sxs-lookup"><span data-stu-id="11c3f-109">Select a purchase order in the list and click the link to open the order.</span></span>
3. <span data-ttu-id="11c3f-110">В области действий щелкните Retail и Commerce.</span><span class="sxs-lookup"><span data-stu-id="11c3f-110">On the Action Pane, click Retail and Commerce.</span></span>
4. <span data-ttu-id="11c3f-111">Щелкните "Кросс-докинг".</span><span class="sxs-lookup"><span data-stu-id="11c3f-111">Click Cross docking.</span></span>
5. <span data-ttu-id="11c3f-112">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="11c3f-112">Click Edit.</span></span>
    * <span data-ttu-id="11c3f-113">Категории можно использовать для фильтрации номенклатуры в разделе "Строки".</span><span class="sxs-lookup"><span data-stu-id="11c3f-113">The category can be used to filter the items in the Lines section.</span></span>  
6. <span data-ttu-id="11c3f-114">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="11c3f-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="11c3f-115">В поле "Количество для кросс-докинга" введите значение для определения того, какое количество приобретенного выбранного продукта будет распределено.</span><span class="sxs-lookup"><span data-stu-id="11c3f-115">In the Cross docking quantity field, type a value to specify how much of the quantity being purchased of the selected product should be distributed.</span></span>
8. <span data-ttu-id="11c3f-116">В поле "Дополнительное количество для кросс-докинга" введите значение для указания количеств для распределения доступных приобретенных продуктов</span><span class="sxs-lookup"><span data-stu-id="11c3f-116">In the Additional cross docking quantity field, enter a value to specify the quantities to distribute for the available products being purchased</span></span>
9. <span data-ttu-id="11c3f-117">В поле "Распределение" введите "Вес местоположения".</span><span class="sxs-lookup"><span data-stu-id="11c3f-117">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="11c3f-118">Можно выбрать другие типы для использования различных правил распределения.</span><span class="sxs-lookup"><span data-stu-id="11c3f-118">You can select the other types to use different rules for the distribution.</span></span>  
10. <span data-ttu-id="11c3f-119">В поле "Иерархия пополнения" выберите значение.</span><span class="sxs-lookup"><span data-stu-id="11c3f-119">In the Replenishment hierarchy field, select a value.</span></span>
11. <span data-ttu-id="11c3f-120">Выберите "Да" в поле "Учитывать ассортименты".</span><span class="sxs-lookup"><span data-stu-id="11c3f-120">Select Yes in the Respect assortments field.</span></span>
12. <span data-ttu-id="11c3f-121">Щелкните "Вычисление количеств".</span><span class="sxs-lookup"><span data-stu-id="11c3f-121">Click Calculate quantities.</span></span>
13. <span data-ttu-id="11c3f-122">Щелкните "Создать заказ".</span><span class="sxs-lookup"><span data-stu-id="11c3f-122">Click Create order.</span></span>
14. <span data-ttu-id="11c3f-123">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="11c3f-123">Click Yes.</span></span>
15. <span data-ttu-id="11c3f-124">В списке найдите и выберите склад, который получил продукты</span><span class="sxs-lookup"><span data-stu-id="11c3f-124">In the list, find and select a warehouse that received products</span></span>
16. <span data-ttu-id="11c3f-125">Щелкните "Заказ" для просмотра заказов, который были созданы для выбранного склада</span><span class="sxs-lookup"><span data-stu-id="11c3f-125">Click Order to view the orders that got created for the selected warehouse</span></span>

