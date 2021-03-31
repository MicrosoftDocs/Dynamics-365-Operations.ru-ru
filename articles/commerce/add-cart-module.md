---
title: Модуль корзины
description: В этом разделе описываются модули корзины, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5b0ce69f57e6ba691803752280466b41ced7c521
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206495"
---
# <a name="cart-module"></a><span data-ttu-id="2a9b2-103">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="2a9b2-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2a9b2-104">В этом разделе описываются модули корзины, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2a9b2-105">Модуль корзины отображает элементы, которые были добавлены в корзину перед тем, как клиент переходит к оформлению заказа.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-105">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="2a9b2-106">Модуль также показывает сводку заказа и позволяет клиенту применять коды рекламных акций или удалять их.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-106">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="2a9b2-107">Модуль корзины поддерживает оформление заказа после входа в систему и оформление заказа для клиента-гостя.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-107">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="2a9b2-108">Он также поддерживает ссылку **Назад к покупкам**.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-108">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="2a9b2-109">Можно настроить маршрут для этой ссылки в **Параметры сайта \> Расширения \> Маршруты**.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-109">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="2a9b2-110">Модуль корзины отображает данные на основе идентификатора корзины, который представляет собой файл cookie браузера, доступный на всем сайте.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-110">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="2a9b2-111">На следующем рисунке показан пример страницы корзины на сайте Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-111">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Пример модуля корзины на сайте Fabrikam](./media/cart2.PNG)

<span data-ttu-id="2a9b2-113">На следующем рисунке показан пример страницы корзины на сайте Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-113">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="2a9b2-114">В этом примере имеется сбор за обработку для элемента строки.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-114">In this example, there is a handling fee for a line item.</span></span>

![Пример модуля корзины со сбором за обслуживание для номенклатуры строки](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="2a9b2-116">Свойства и слоты модуля корзины</span><span class="sxs-lookup"><span data-stu-id="2a9b2-116">Cart module properties and slots</span></span>

| <span data-ttu-id="2a9b2-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="2a9b2-117">Property</span></span> | <span data-ttu-id="2a9b2-118">Значения</span><span class="sxs-lookup"><span data-stu-id="2a9b2-118">Values</span></span> | <span data-ttu-id="2a9b2-119">описание</span><span class="sxs-lookup"><span data-stu-id="2a9b2-119">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="2a9b2-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2a9b2-120">Heading</span></span> | <span data-ttu-id="2a9b2-121">Текст заголовка и метка заголовка (**H1**, **H2**, **H3**, **H4**, **H5** или **H6**)</span><span class="sxs-lookup"><span data-stu-id="2a9b2-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="2a9b2-122">Заголовок для корзины, например "Корзина" или "Товары в корзине".</span><span class="sxs-lookup"><span data-stu-id="2a9b2-122">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="2a9b2-123">Показывать ошибки "Нет в наличии"</span><span class="sxs-lookup"><span data-stu-id="2a9b2-123">Show out of stock errors</span></span> | <span data-ttu-id="2a9b2-124">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="2a9b2-124">**True** or **False**</span></span> | <span data-ttu-id="2a9b2-125">Если это свойство имеет значение **Истина**, страница корзины отобразит ошибки, связанные с запасами.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-125">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="2a9b2-126">Рекомендуется установить для этого свойства значение **Истина**, если для сайта установлены проверки запасов.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-126">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="2a9b2-127">Показывать накладные расходы на поставку для номенклатур строки</span><span class="sxs-lookup"><span data-stu-id="2a9b2-127">Show shipping charges for line items</span></span> | <span data-ttu-id="2a9b2-128">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="2a9b2-128">**True** or **False**</span></span> | <span data-ttu-id="2a9b2-129">Если это свойство имеет значение **Истина**, для номенклатур строки корзины будут отображаться расходы на доставку, если эта информация доступна.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-129">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="2a9b2-130">Эта функция не поддерживается в теме "Fabrikam", поскольку пользователи выбирают отгрузку только в потоке оформления заказа.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-130">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="2a9b2-131">Однако эту возможность можно включить в другие workflow-процессы, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-131">However, this feature can be turned on in other workflows if it's applicable.</span></span> |
| <span data-ttu-id="2a9b2-132">Показывать доступные акции</span><span class="sxs-lookup"><span data-stu-id="2a9b2-132">Show available promotions</span></span>| <span data-ttu-id="2a9b2-133">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="2a9b2-133">**True** or **False**</span></span> | <span data-ttu-id="2a9b2-134">Если это свойство имеет значение **True**, в корзине отображаются доступные рекламные акции на основе номенклатур в корзине.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-134">If this property is set to **True**, the cart shows available promotions, based on items in the cart.</span></span> <span data-ttu-id="2a9b2-135">Эта возможность доступна в выпуске Dynamics 365 Commerce 10.0.16.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-135">This capability is available in the Dynamics 365 Commerce 10.0.16 release.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="2a9b2-136">Модули, которые могут быть использованы в модуле корзины</span><span class="sxs-lookup"><span data-stu-id="2a9b2-136">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="2a9b2-137">**Блок текста** — этот модуль поддерживает настраиваемые сообщения в модуле корзины.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-137">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="2a9b2-138">Сообщения выдаются системой управления контентом (CMS).</span><span class="sxs-lookup"><span data-stu-id="2a9b2-138">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="2a9b2-139">Любое сообщение может быть добавлено, например "По вопросам, связанным с заказом, обращайтесь по телефону 1-800-Fabrikam."</span><span class="sxs-lookup"><span data-stu-id="2a9b2-139">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="2a9b2-140">**Выбор магазина** — этот модуль отображает список ближайших магазинов, в которых номенклатура доступна для получения.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-140">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="2a9b2-141">Он позволяет пользователям вводить местоположение для поиска ближайших магазинов.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-141">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="2a9b2-142">Дополнительные сведения об этом модуле см. в разделе [Модуль выбора магазина](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="2a9b2-142">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="2a9b2-143">Свойства модуля</span><span class="sxs-lookup"><span data-stu-id="2a9b2-143">Module properties</span></span>

<span data-ttu-id="2a9b2-144">Следующие параметры модуля корзины можно настроить в **Параметры сайта \> Расширения**:</span><span class="sxs-lookup"><span data-stu-id="2a9b2-144">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="2a9b2-145">**Максимальное количество** — это свойство используется для указания максимального количества каждой номенклатуры, которое может быть добавлено в корзину.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-145">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="2a9b2-146">Например, розничная сеть может решить, что в одну проводку можно продать только 10 шт. каждого продукта.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-146">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="2a9b2-147">**Запасы** — сведения о применении настроек запасов см. в разделе [Применение настроек запасов](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="2a9b2-147">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="2a9b2-148">**Назад к покупкам** — это свойство используется для указания маршрута для ссылки **Назад к покупкам**.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-148">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="2a9b2-149">Маршрут может быть настроен на уровне сайта, что позволяет розничным продавцам вернуть клиента на домашнюю страницу или на любую другую страницу сайта.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-149">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2a9b2-150">В выпуске Dynamics 365 Commerce 10.0.14 и более поздних номенклатуры в корзине суммируются на основе настроек, определенных в интерактивном профиле функциональности для Интернет-магазина в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-150">In the Dynamics 365 Commerce 10.0.14 release and later, items in the cart are aggregated based on the settings that are defined in the online functionality profile for the online store in Commerce headquarters.</span></span> <span data-ttu-id="2a9b2-151">Дополнительные сведения о создании профиля функциональности онлайн-торговли и задании свойств, необходимых для агрегирования, см. в разделе [Создание профиля функциональности для онлайн-торговли](online-functionality-profile.md).</span><span class="sxs-lookup"><span data-stu-id="2a9b2-151">For more information about how to create an online functionality profile and set the properties that are required for aggregation, see [Create an online functionality profile](online-functionality-profile.md).</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="2a9b2-152">Взаимодействие Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="2a9b2-152">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="2a9b2-153">Модуль корзины извлекает информацию о продукции с помощью интерфейсов API Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-153">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="2a9b2-154">Идентификатор корзины из cookie-файла браузера используется для получения всей информации о продукте из Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-154">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="2a9b2-155">Добавление модуля корзины на страницу</span><span class="sxs-lookup"><span data-stu-id="2a9b2-155">Add a cart module to a page</span></span>

<span data-ttu-id="2a9b2-156">Чтобы добавить модуль корзины на новую страницу и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-156">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="2a9b2-157">Перейдите к разделу **Фрагменты**, выберите **Создать**, чтобы создать фрагмент.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-157">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="2a9b2-158">В диалоговом окне **Создать фрагмент** выберите модуль **Корзина**.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-158">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="2a9b2-159">В области **Имя фрагмента** введите имя **Фрагмент корзины**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-159">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="2a9b2-160">Выберите слот **Корзина**.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-160">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="2a9b2-161">В области свойств справа выберите символ карандаш, введите текст заголовка в поле, а затем выберите символ галочки.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-161">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="2a9b2-162">В ячейке **Корзина** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-162">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2a9b2-163">В диалоговом окне **Добавить модуль** выберите модуль **Выбор магазина**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-163">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2a9b2-164">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата фрагмента, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-164">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="2a9b2-165">Перейдите к пункту **Шаблоны**, выберите **Создать**, чтобы создать шаблон.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-165">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="2a9b2-166">В диалоговом окне **Создать шаблон** в разделе **Имя шаблона** введите имя шаблона.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-166">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="2a9b2-167">В древовидной структуре выберите слот **Основной текст**, нажмите многоточие (**…**), затем выберите **Добавить фрагмент**.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-167">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="2a9b2-168">В диалоговом окне **Выбор фрагмента** выберите созданный ранее **Фрагмент корзины** и нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-168">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="2a9b2-169">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-169">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="2a9b2-170">Перейдите к разделу **Страницы**, выберите **Создать**, чтобы создать страницу.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-170">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="2a9b2-171">В диалоговом окне **Выбор шаблона** выберите созданный шаблон, введите имя страницы и нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-171">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="2a9b2-172">Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть страницу.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-172">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="2a9b2-173">Выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="2a9b2-173">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2a9b2-174">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2a9b2-174">Additional resources</span></span>

[<span data-ttu-id="2a9b2-175">Модуль значка корзины</span><span class="sxs-lookup"><span data-stu-id="2a9b2-175">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="2a9b2-176">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="2a9b2-176">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="2a9b2-177">Модуль платежа</span><span class="sxs-lookup"><span data-stu-id="2a9b2-177">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="2a9b2-178">Модуль адреса доставки</span><span class="sxs-lookup"><span data-stu-id="2a9b2-178">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="2a9b2-179">Модуль параметров доставки</span><span class="sxs-lookup"><span data-stu-id="2a9b2-179">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="2a9b2-180">Модуль сведений о самовывозе</span><span class="sxs-lookup"><span data-stu-id="2a9b2-180">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="2a9b2-181">Модуль сведений о заказе</span><span class="sxs-lookup"><span data-stu-id="2a9b2-181">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="2a9b2-182">Модуль подарочных сертификатов</span><span class="sxs-lookup"><span data-stu-id="2a9b2-182">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="2a9b2-183">Расчет наличия запасов для розничных каналов</span><span class="sxs-lookup"><span data-stu-id="2a9b2-183">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="2a9b2-184">Создание профиля функциональности для онлайн-торговли</span><span class="sxs-lookup"><span data-stu-id="2a9b2-184">Create an online functionality profile</span></span>](online-functionality-profile.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]