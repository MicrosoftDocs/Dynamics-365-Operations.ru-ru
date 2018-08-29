---
title: "Поиск запасов в POS"
description: "В этом разделе описаны параметры, доступные для просмотра сведений о запасах в POS."
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: e40c558e03ef230fee6726994bc94979d40493c2
ms.contentlocale: ru-ru
ms.lasthandoff: 08/09/2018

---

# <a name="inventory-lookup-in-the-point-of-sale-pos"></a><span data-ttu-id="e8676-103">Поиск запасов в POS</span><span class="sxs-lookup"><span data-stu-id="e8676-103">Inventory lookup in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e8676-104">Поиск запасов в POS помогает предприятиям розничной торговли успешно работать в режиме реального времени и получать аналитические данные путем подключения магазинов, POS и бэк-офиса.</span><span class="sxs-lookup"><span data-stu-id="e8676-104">Inventory lookup in the point of sale (POS) helps retailers achieve real-time operational excellence and gain insights by connecting stores, the POS, and the back office.</span></span> <span data-ttu-id="e8676-105">Эта функция предоставляет точное представление в режиме реального времени запасов продуктов по магазинам и центрами распределения.</span><span class="sxs-lookup"><span data-stu-id="e8676-105">This functionality provides an accurate real-time view of product inventory across stores and distribution centers.</span></span> <span data-ttu-id="e8676-106">Она также помогает предприятиям розничной торговли обеспечивать дополнительную эффективность и снизить затраты, улучшая планирование запасов в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="e8676-106">It also helps retailers drive additional efficiencies and cost savings by improving inventory planning in real time.</span></span>

<span data-ttu-id="e8676-107">Точное представление в режиме реального времени запасов по всей организации помогает продавцам магазинов предоставлять отличное и своевременное обслуживания клиентов.</span><span class="sxs-lookup"><span data-stu-id="e8676-107">An accurate real-time view of inventory across an organization helps store associates provide timely, superior customer service.</span></span> <span data-ttu-id="e8676-108">Самый важный момент — это когда клиент готов принять решение о покупке.</span><span class="sxs-lookup"><span data-stu-id="e8676-108">The moment that matters most is the moment when the customer is ready to make a purchase decision.</span></span> <span data-ttu-id="e8676-109">Важно, чтобы кассирам в магазине была легко доступна информация о запасах в режиме реального времени, чтобы они могли точно гарантировать доставку и отправку продукта.</span><span class="sxs-lookup"><span data-stu-id="e8676-109">It's important that cashiers in the store have real-time inventory information at their fingertips, so that they can accurately promise product delivery and pickup.</span></span>

<span data-ttu-id="e8676-110">Можно открыть страницу **Поиск запасов** из рабочей области **Retail Modern POS** или **Retail Cloud POS**.</span><span class="sxs-lookup"><span data-stu-id="e8676-110">You can open the **Inventory lookup** page from the **Retail Modern POS** workspace or the **Retail Cloud POS** workspace.</span></span>

![Плитка поиска запасов на домашней странице POS](media/POSHomepage.png)

<span data-ttu-id="e8676-112">На странице **Поиск запасов** можно использовать цифровую клавиатуру для ввода номера продукта.</span><span class="sxs-lookup"><span data-stu-id="e8676-112">On the **Inventory lookup** page, you can use the numeric keyboard to enter a product number.</span></span> <span data-ttu-id="e8676-113">Затем можно просмотреть количество в наличии для нескольких магазинов и складов.</span><span class="sxs-lookup"><span data-stu-id="e8676-113">You can then view the on-hand quantity for multiple stores and warehouses.</span></span>

![Стандартная страница поиска запасов](media/InventoryLookUp.png)

<span data-ttu-id="e8676-115">Для каждого местонахождения также отображаются количества **Зарезервировано** и **Заказано**.</span><span class="sxs-lookup"><span data-stu-id="e8676-115">**Reserved** and **Ordered** quantities are also shown for each location.</span></span>

- <span data-ttu-id="e8676-116">**Зарезервировано** — это количество означает значение **Физически зарезервировано** из бэк-офиса для указанного номера продукта в местонахождении.</span><span class="sxs-lookup"><span data-stu-id="e8676-116">**Reserved** – This quantity refers to the **Physical reserved** value from the back office for the specified product number at the location.</span></span>
- <span data-ttu-id="e8676-117">**Заказано** — это количество означает значение **Всего заказано** из бэк-офиса для указанного номера продукта в местонахождении.</span><span class="sxs-lookup"><span data-stu-id="e8676-117">**Ordered** – This quantity refers to the **Ordered in total** value from the back office for the specified product number at the location.</span></span>

## <a name="locations-that-inventory-availability-information-is-shown-for"></a><span data-ttu-id="e8676-118">Местонахождения, для которых отображается информация о доступности запасов</span><span class="sxs-lookup"><span data-stu-id="e8676-118">Locations that inventory availability information is shown for</span></span>

<span data-ttu-id="e8676-119">Список местоположений включает в себя два вида объектов:</span><span class="sxs-lookup"><span data-stu-id="e8676-119">The list of locations includes two types of entities:</span></span>

- <span data-ttu-id="e8676-120">**Розничные магазины** — список магазинов, которые настраиваются с использованием группы указателей магазинов для текущего магазина в "Розничная сеть - Центральный офис".</span><span class="sxs-lookup"><span data-stu-id="e8676-120">**Retail stores** – The list shows stores that are configured by using the store locator group for the current store in the Retail headquarters.</span></span> 
- <span data-ttu-id="e8676-121">**Центры распределения** — различные типы центров распределения (такие как склады) могут быть настроены в Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="e8676-121">**Distribution centers** – Various types of distribution centers (such as warehouses) can be configured in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="e8676-122">Однако в списке отображаются сведения о доступности запасов только для центров распределения типа по умолчанию **Стандартный**.</span><span class="sxs-lookup"><span data-stu-id="e8676-122">However, the list shows inventory availability information only for distribution centers of the **Standard** default type.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="e8676-123">Сведения о доступности запасов не отображаются для складов типов **Транзитный**, **Карантинный** и **Товаров в пути** для POS.</span><span class="sxs-lookup"><span data-stu-id="e8676-123">Inventory availability information isn't shown for warehouses of the **Transit**, **Quarantine**, and **Goods in Route** types for the POS.</span></span>

<span data-ttu-id="e8676-124">На странице **Поиск запасов** можно просматривать доступные для резервирования (ATP) количества для каждого магазина, помимо текущих количеств в наличии, зарезервированных количеств и заказанных количеств.</span><span class="sxs-lookup"><span data-stu-id="e8676-124">On the **Inventory lookup** page, you can view available to promise (ATP) quantities for each store, in addition to the current on-hand quantities, reserved quantities, and ordered quantities.</span></span> <span data-ttu-id="e8676-125">Выберите магазин, для которого требуется просмотреть информацию о доступности для резервирования (ATP), затем выберите **Показать доступность магазина**.</span><span class="sxs-lookup"><span data-stu-id="e8676-125">Select the store to view the ATP information for, and then select **Show store availability**.</span></span>

![Количества ATP](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a><span data-ttu-id="e8676-127">Открытие аналитики на основе матричного представления для отображения всех вариантов</span><span class="sxs-lookup"><span data-stu-id="e8676-127">Opening the Dimension based matrix view to show all variants</span></span>

<span data-ttu-id="e8676-128">На странице **Сведения о продукте** шаблона продукта или на странице **Поиск запасов** выберите **Просмотр всех вариантов** на панели приложения в нижней части страницы.</span><span class="sxs-lookup"><span data-stu-id="e8676-128">On the **Product details** page of a product master, or on the **Inventory lookup** page, select **View all variants** from the app-bar at bottom of the page.</span></span> <span data-ttu-id="e8676-129">Представление **Матрица на основе аналитик** для исходного запуска с этих страниц содержит сведений о доступности запасов для всех вариантов продукта для текущего магазина.</span><span class="sxs-lookup"><span data-stu-id="e8676-129">The **Dimension based matrix** view for the initial launch from these pages shows the inventory availability information for all variants of a product for the current store.</span></span>

> [!NOTE]
> <span data-ttu-id="e8676-130">Кнопка **Просмотр всех вариантов** доступна только для шаблонов продуктов номенклатуры, которые имеют варианты продукта.</span><span class="sxs-lookup"><span data-stu-id="e8676-130">The **View all variants** button is available only for item product masters that have product variants.</span></span> <span data-ttu-id="e8676-131">Она недоступна для отдельных продуктов или наборов.</span><span class="sxs-lookup"><span data-stu-id="e8676-131">It isn't available for standalone products or kits.</span></span>

![Кнопка просмотра всех вариантов на странице поиска запасов](media/StandardToMatrix.png)

<span data-ttu-id="e8676-133">Выберите **Просмотр всех вариантов** на странице **Сведения о продукте** шаблона продукта или на странице **Поиск запасов** без выбора местоположения, чтобы перейти к представлению **Матрица на основе аналитик** для просмотра сведений о доступности запасов для всех вариантов продукта для текущего магазина.</span><span class="sxs-lookup"><span data-stu-id="e8676-133">Select **View all variants** on the **Product details** page of a product master, or on the **Inventory lookup** page, without selecting a location, to go to the **Dimension based matrix** view to view the inventory availability information for all variants of a product for the current store.</span></span>

![Представление матрицы на основе аналитик для страницы поиска запасов](media/Matrix.png)

> [!NOTE]
> <span data-ttu-id="e8676-135">На приведенном выше рисунке аналитики отображаются в алфавитном порядке, так как порядок отображения аналитик не был настроен для выбранного продукта.</span><span class="sxs-lookup"><span data-stu-id="e8676-135">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="e8676-136">В представлении **Матрица на основе аналитик** ячейки вариантов продукта включают значение в наличии в правом нижнем углу.</span><span class="sxs-lookup"><span data-stu-id="e8676-136">In the **Dimension based matrix** view, the cells for the product variants include an on-hand value in the lower-right corner.</span></span> <span data-ttu-id="e8676-137">В следующей таблице описывается значение различных значений.</span><span class="sxs-lookup"><span data-stu-id="e8676-137">The following table explains the meaning of the various values.</span></span>

| <span data-ttu-id="e8676-138">Стоимость запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="e8676-138">On-hand value</span></span>                            | <span data-ttu-id="e8676-139">описание</span><span class="sxs-lookup"><span data-stu-id="e8676-139">Description</span></span> |
|------------------------------------------|-------------|
| <span data-ttu-id="e8676-140">Числовое значение, которое больше 0 (нуля)</span><span class="sxs-lookup"><span data-stu-id="e8676-140">Numeric value that is more than 0 (zero)</span></span> | <span data-ttu-id="e8676-141">Вариант выпущен в выбранном местоположении, и вы можете выполнять дополнительные действия в ячейке.</span><span class="sxs-lookup"><span data-stu-id="e8676-141">A variant has been released to the selected location, and you can perform additional actions in the cell.</span></span> <span data-ttu-id="e8676-142">(Эти действия описаны более подробно ниже в этом разделе.)</span><span class="sxs-lookup"><span data-stu-id="e8676-142">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="e8676-143">**0** (ноль)</span><span class="sxs-lookup"><span data-stu-id="e8676-143">**0** (zero)</span></span>                             | <span data-ttu-id="e8676-144">Вариант был выпущен в выбранном местоположении, но номенклатура недоступна в указанном местоположении.</span><span class="sxs-lookup"><span data-stu-id="e8676-144">A variant has been released to the selected location, but the item isn't available in selected location.</span></span> <span data-ttu-id="e8676-145">Тем не менее можно выполнять дополнительные действия в ячейке.</span><span class="sxs-lookup"><span data-stu-id="e8676-145">However, you can perform additional actions in the cell.</span></span> <span data-ttu-id="e8676-146">(Эти действия описаны более подробно ниже в этом разделе.)</span><span class="sxs-lookup"><span data-stu-id="e8676-146">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="e8676-147">**н/д** или неактивная ячейка</span><span class="sxs-lookup"><span data-stu-id="e8676-147">**n/a** or an inactive cell</span></span>              | <span data-ttu-id="e8676-148">Вариант не был выпущен в выбранном местоположении, и вы не можете выполнять дополнительные действия в ячейке.</span><span class="sxs-lookup"><span data-stu-id="e8676-148">A variant hasn't been released to the selected location, and you can't perform additional actions in the cell.</span></span> |

<span data-ttu-id="e8676-149">Можно также изменить опорный элемент для аналитик, выбрав новую аналитику для использования.</span><span class="sxs-lookup"><span data-stu-id="e8676-149">You can also change the pivot for dimensions by selecting the new dimension to use.</span></span> 

![Изменение опорного элемента](media/ChangePivot.png)

![Опорный элемент изменен](media/PivotChanged.png)

> [!NOTE]
> <span data-ttu-id="e8676-152">На предыдущем рисунке порядок отображения аналитик для выбранного продукта является пользовательским (не по алфавиту).</span><span class="sxs-lookup"><span data-stu-id="e8676-152">In the preceding illustrations, the display order of the dimensions for the selected product is custom (non-alphabetic).</span></span> <span data-ttu-id="e8676-153">Он основан на порядке отображения аналитик, заданном в бэк-офисе.</span><span class="sxs-lookup"><span data-stu-id="e8676-153">It's based on the dimension display order that is set in the back office.</span></span>

<span data-ttu-id="e8676-154">Кроме того, в представлении **Матрица на основе аналитик** дополнительные действия могут выполняться для повышения производительности сотрудников магазина.</span><span class="sxs-lookup"><span data-stu-id="e8676-154">Additionally, in the **Dimension based matrix** view, more actions can be performed to help boost a store associate's productivity.</span></span> <span data-ttu-id="e8676-155">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="e8676-155">Here are some examples:</span></span>

- <span data-ttu-id="e8676-156">Изменение местоположения магазина для поиска доступности запасов всех вариантов продукта в других расположениях.</span><span class="sxs-lookup"><span data-stu-id="e8676-156">Change the store location to look up the inventory availability of all product variants at other locations.</span></span> <span data-ttu-id="e8676-157">Эти местоположения включают другие магазины в группе указателей магазина и центры распределения типа по умолчанию **Стандартный**.</span><span class="sxs-lookup"><span data-stu-id="e8676-157">These locations include other stores in the store locator group and distribution centers of the **Standard** default type.</span></span>
- <span data-ttu-id="e8676-158">Продажа индивидуального варианта продукта клиенту с помощью продажи без доставки при оплате наличными, получения в магазине или отгрузки в адрес.</span><span class="sxs-lookup"><span data-stu-id="e8676-158">Sell an individual product variant to a customer by using cash and carry, in-store pickup, or shipment to an address.</span></span>
- <span data-ttu-id="e8676-159">Сообщите клиенту сведений о доступности для резервирования для индивидуального варианта продукта в определенном местоположении.</span><span class="sxs-lookup"><span data-stu-id="e8676-159">Provide the customer with ATP information for an individual product variant at a specific location.</span></span>

![Дополнительные действия на плитках вариантов](media/VariantActions.png)

> [!NOTE]
> <span data-ttu-id="e8676-161">На приведенном выше рисунке аналитики отображаются в алфавитном порядке, так как порядок отображения аналитик не был настроен для выбранного продукта.</span><span class="sxs-lookup"><span data-stu-id="e8676-161">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="e8676-162">Следующая таблица содержит дополнительные сведения о дополнительных действий, которые доступны.</span><span class="sxs-lookup"><span data-stu-id="e8676-162">The following table provides more information about the additional actions that are available.</span></span>


|        <span data-ttu-id="e8676-163">Действие</span><span class="sxs-lookup"><span data-stu-id="e8676-163">Action</span></span>        |                                                                                                                    <span data-ttu-id="e8676-164">описание</span><span class="sxs-lookup"><span data-stu-id="e8676-164">Description</span></span>                                                                                                                    |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|       <span data-ttu-id="e8676-165">Продать сейчас</span><span class="sxs-lookup"><span data-stu-id="e8676-165">Sell now</span></span>       |                               <span data-ttu-id="e8676-166">Добавление выбранного варианта номенклатуры в проводку и перенаправление пользователя на экран проводки.</span><span class="sxs-lookup"><span data-stu-id="e8676-166">Add the selected item variant to the transaction, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="e8676-167">(Это действие недоступно, когда выбранное местоположение является центром распределения.)</span><span class="sxs-lookup"><span data-stu-id="e8676-167">(This action isn't available when the selected location is a distribution center.)</span></span>                               |
|   <span data-ttu-id="e8676-168">Самовывоз из магазина</span><span class="sxs-lookup"><span data-stu-id="e8676-168">Pick up in store</span></span>   |      <span data-ttu-id="e8676-169">Создание заказа клиента для варианта продукта, который клиент заберет из выбранного местонахождения, и перенаправление пользователя на экран проводки.</span><span class="sxs-lookup"><span data-stu-id="e8676-169">Create a customer order for the product variant that will be picked up from the selected location, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="e8676-170">(Это действие недоступно, когда выбранное местоположение является центром распределения.)</span><span class="sxs-lookup"><span data-stu-id="e8676-170">(This action isn't available when the selected location is a distribution center.)</span></span>       |
|     <span data-ttu-id="e8676-171">Отгрузить продукт</span><span class="sxs-lookup"><span data-stu-id="e8676-171">Ship product</span></span>     |                                                 <span data-ttu-id="e8676-172">Создание заказа клиента для варианта продукта, который будет отгружен из выбранного местонахождения, и перенаправление пользователя на экран проводки.</span><span class="sxs-lookup"><span data-stu-id="e8676-172">Create a customer order for the product variant that will be shipped from the selected location, and redirect the user to the transaction screen.</span></span>                                                 |
|     <span data-ttu-id="e8676-173">Доступность</span><span class="sxs-lookup"><span data-stu-id="e8676-173">Availability</span></span>     |                                                                             <span data-ttu-id="e8676-174">Отображение сведений о доступности для резервирования для выбранной комбинации вариантов для выбранного местонахождения.</span><span class="sxs-lookup"><span data-stu-id="e8676-174">Show the ATP information for the selected variant combination for the selected location.</span></span>                                                                              |
|  <span data-ttu-id="e8676-175">Показать все местоположения</span><span class="sxs-lookup"><span data-stu-id="e8676-175">Show all locations</span></span>  | <span data-ttu-id="e8676-176">Переключение на стандартное представление поиска запасов и выделение сведений о доступности запасов для варианта номенклатуры по всем магазинам в группе указателей магазинов, а также в центрах распределения типа <strong>Стандартный/По умолчанию</strong>.</span><span class="sxs-lookup"><span data-stu-id="e8676-176">Switch to the standard inventory lookup view, and highlight inventory availability information for the item variant across all stores in the store locator group, and also in distribution centers of the <strong>Standard/Default</strong> type.</span></span> |
| <span data-ttu-id="e8676-177">Просмотр сведений о продукте</span><span class="sxs-lookup"><span data-stu-id="e8676-177">View product details</span></span> |                                                                         <span data-ttu-id="e8676-178">Перенаправление пользователя на страницу <strong>Сведения о продукте</strong> связанного шаблона продукта.</span><span class="sxs-lookup"><span data-stu-id="e8676-178">Redirect the user to the <strong>Product details</strong> page of the associated product master.</span></span>                                                                          |


