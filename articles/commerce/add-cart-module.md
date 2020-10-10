---
title: Модуль корзины
description: В этом разделе описываются модули корзины, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d9a15f85838849796d6ce4674712636251c75bf3
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818283"
---
# <a name="cart-module"></a><span data-ttu-id="91f15-103">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="91f15-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="91f15-104">В этом разделе описываются модули корзины, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="91f15-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="91f15-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="91f15-105">Overview</span></span>

<span data-ttu-id="91f15-106">Модуль корзины отображает элементы, которые были добавлены в корзину перед тем, как клиент переходит к оформлению заказа.</span><span class="sxs-lookup"><span data-stu-id="91f15-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="91f15-107">Модуль также показывает сводку заказа и позволяет клиенту применять коды рекламных акций или удалять их.</span><span class="sxs-lookup"><span data-stu-id="91f15-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="91f15-108">Модуль корзины поддерживает оформление заказа после входа в систему и оформление заказа для клиента-гостя.</span><span class="sxs-lookup"><span data-stu-id="91f15-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="91f15-109">Он также поддерживает ссылку **Назад к покупкам**.</span><span class="sxs-lookup"><span data-stu-id="91f15-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="91f15-110">Можно настроить маршрут для этой ссылки в **Параметры сайта \> Расширения \> Маршруты**.</span><span class="sxs-lookup"><span data-stu-id="91f15-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="91f15-111">Модуль корзины отображает данные на основе идентификатора корзины, который представляет собой файл cookie браузера, доступный на всем сайте.</span><span class="sxs-lookup"><span data-stu-id="91f15-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="91f15-112">На следующем рисунке показан пример страницы корзины на сайте Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="91f15-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Пример модуля корзины на сайте Fabrikam](./media/cart2.PNG)

<span data-ttu-id="91f15-114">На следующем рисунке показан пример страницы корзины на сайте Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="91f15-114">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="91f15-115">В этом примере имеется сбор за обработку для элемента строки.</span><span class="sxs-lookup"><span data-stu-id="91f15-115">In this example, there is a handling fee for a line item.</span></span>

![Пример модуля корзины со сбором за обслуживание для номенклатуры строки](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="91f15-117">Свойства и слоты модуля корзины</span><span class="sxs-lookup"><span data-stu-id="91f15-117">Cart module properties and slots</span></span>

| <span data-ttu-id="91f15-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="91f15-118">Property</span></span> | <span data-ttu-id="91f15-119">Значения</span><span class="sxs-lookup"><span data-stu-id="91f15-119">Values</span></span> | <span data-ttu-id="91f15-120">описание</span><span class="sxs-lookup"><span data-stu-id="91f15-120">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="91f15-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="91f15-121">Heading</span></span> | <span data-ttu-id="91f15-122">Текст заголовка и метка заголовка (**H1**, **H2**, **H3**, **H4**, **H5** или **H6**)</span><span class="sxs-lookup"><span data-stu-id="91f15-122">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="91f15-123">Заголовок для корзины, например "Корзина" или "Товары в корзине".</span><span class="sxs-lookup"><span data-stu-id="91f15-123">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="91f15-124">Показывать ошибки "Нет в наличии"</span><span class="sxs-lookup"><span data-stu-id="91f15-124">Show out of stock errors</span></span> | <span data-ttu-id="91f15-125">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="91f15-125">**True** or **False**</span></span> | <span data-ttu-id="91f15-126">Если это свойство имеет значение **Истина**, страница корзины отобразит ошибки, связанные с запасами.</span><span class="sxs-lookup"><span data-stu-id="91f15-126">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="91f15-127">Рекомендуется установить для этого свойства значение **Истина**, если для сайта установлены проверки запасов.</span><span class="sxs-lookup"><span data-stu-id="91f15-127">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="91f15-128">Показывать накладные расходы на поставку для номенклатур строки</span><span class="sxs-lookup"><span data-stu-id="91f15-128">Show shipping charges for line items</span></span> | <span data-ttu-id="91f15-129">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="91f15-129">**True** or **False**</span></span> | <span data-ttu-id="91f15-130">Если это свойство имеет значение **Истина**, для номенклатур строки корзины будут отображаться расходы на доставку, если эта информация доступна.</span><span class="sxs-lookup"><span data-stu-id="91f15-130">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="91f15-131">Эта функция не поддерживается в теме "Fabrikam", поскольку пользователи выбирают отгрузку только в потоке оформления заказа.</span><span class="sxs-lookup"><span data-stu-id="91f15-131">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="91f15-132">Однако эту возможность можно включить в другие workflow-процессы, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="91f15-132">However, this feature can be turned on in other workflows if it's applicable.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="91f15-133">Модули, которые могут быть использованы в модуле корзины</span><span class="sxs-lookup"><span data-stu-id="91f15-133">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="91f15-134">**Блок текста** — этот модуль поддерживает настраиваемые сообщения в модуле корзины.</span><span class="sxs-lookup"><span data-stu-id="91f15-134">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="91f15-135">Сообщения выдаются системой управления контентом (CMS).</span><span class="sxs-lookup"><span data-stu-id="91f15-135">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="91f15-136">Любое сообщение может быть добавлено, например "По вопросам, связанным с заказом, обращайтесь по телефону 1-800-Fabrikam."</span><span class="sxs-lookup"><span data-stu-id="91f15-136">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="91f15-137">**Выбор магазина** — этот модуль отображает список ближайших магазинов, в которых номенклатура доступна для получения.</span><span class="sxs-lookup"><span data-stu-id="91f15-137">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="91f15-138">Он позволяет пользователям вводить местоположение для поиска ближайших магазинов.</span><span class="sxs-lookup"><span data-stu-id="91f15-138">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="91f15-139">Дополнительные сведения об этом модуле см. в разделе [Модуль выбора магазина](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="91f15-139">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="91f15-140">Свойства модуля</span><span class="sxs-lookup"><span data-stu-id="91f15-140">Module properties</span></span>

<span data-ttu-id="91f15-141">Следующие параметры модуля корзины можно настроить в **Параметры сайта \> Расширения**:</span><span class="sxs-lookup"><span data-stu-id="91f15-141">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="91f15-142">**Максимальное количество** — это свойство используется для указания максимального количества каждой номенклатуры, которое может быть добавлено в корзину.</span><span class="sxs-lookup"><span data-stu-id="91f15-142">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="91f15-143">Например, розничная сеть может решить, что в одну проводку можно продать только 10 шт. каждого продукта.</span><span class="sxs-lookup"><span data-stu-id="91f15-143">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="91f15-144">**Запасы** — сведения о применении настроек запасов см. в разделе [Применение настроек запасов](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="91f15-144">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="91f15-145">**Назад к покупкам** — это свойство используется для указания маршрута для ссылки **Назад к покупкам**.</span><span class="sxs-lookup"><span data-stu-id="91f15-145">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="91f15-146">Маршрут может быть настроен на уровне сайта, что позволяет розничным продавцам вернуть клиента на домашнюю страницу или на любую другую страницу сайта.</span><span class="sxs-lookup"><span data-stu-id="91f15-146">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="91f15-147">Взаимодействие Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="91f15-147">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="91f15-148">Модуль корзины извлекает информацию о продукции с помощью интерфейсов API Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="91f15-148">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="91f15-149">Идентификатор корзины из cookie-файла браузера используется для получения всей информации о продукте из Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="91f15-149">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="91f15-150">Добавление модуля корзины на страницу</span><span class="sxs-lookup"><span data-stu-id="91f15-150">Add a cart module to a page</span></span>

<span data-ttu-id="91f15-151">Чтобы добавить модуль корзины на новую страницу и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="91f15-151">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="91f15-152">Перейдите к разделу **Фрагменты**, выберите **Создать**, чтобы создать фрагмент.</span><span class="sxs-lookup"><span data-stu-id="91f15-152">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="91f15-153">В диалоговом окне **Создать фрагмент** выберите модуль **Корзина**.</span><span class="sxs-lookup"><span data-stu-id="91f15-153">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="91f15-154">В области **Имя фрагмента** введите имя **Фрагмент корзины**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="91f15-154">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="91f15-155">Выберите слот **Корзина**.</span><span class="sxs-lookup"><span data-stu-id="91f15-155">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="91f15-156">В области свойств справа выберите символ карандаш, введите текст заголовка в поле, а затем выберите символ галочки.</span><span class="sxs-lookup"><span data-stu-id="91f15-156">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="91f15-157">В ячейке **Корзина** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="91f15-157">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="91f15-158">В диалоговом окне **Добавить модуль** выберите модуль **Выбор магазина**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="91f15-158">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="91f15-159">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата фрагмента, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="91f15-159">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="91f15-160">Перейдите к пункту **Шаблоны**, выберите **Создать**, чтобы создать шаблон.</span><span class="sxs-lookup"><span data-stu-id="91f15-160">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="91f15-161">В диалоговом окне **Создать шаблон** в разделе **Имя шаблона** введите имя шаблона.</span><span class="sxs-lookup"><span data-stu-id="91f15-161">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="91f15-162">В древовидной структуре выберите слот **Основной текст**, нажмите многоточие (**…**), затем выберите **Добавить фрагмент**.</span><span class="sxs-lookup"><span data-stu-id="91f15-162">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="91f15-163">В диалоговом окне **Выбор фрагмента** выберите созданный ранее **Фрагмент корзины** и нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="91f15-163">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="91f15-164">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="91f15-164">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="91f15-165">Перейдите к разделу **Страницы**, выберите **Создать**, чтобы создать страницу.</span><span class="sxs-lookup"><span data-stu-id="91f15-165">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="91f15-166">В диалоговом окне **Выбор шаблона** выберите созданный шаблон, введите имя страницы и нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="91f15-166">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="91f15-167">Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть страницу.</span><span class="sxs-lookup"><span data-stu-id="91f15-167">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="91f15-168">Выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="91f15-168">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="91f15-169">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="91f15-169">Additional resources</span></span>

[<span data-ttu-id="91f15-170">Модуль значка корзины</span><span class="sxs-lookup"><span data-stu-id="91f15-170">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="91f15-171">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="91f15-171">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="91f15-172">Модуль платежа</span><span class="sxs-lookup"><span data-stu-id="91f15-172">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="91f15-173">Модуль адреса доставки</span><span class="sxs-lookup"><span data-stu-id="91f15-173">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="91f15-174">Модуль параметров доставки</span><span class="sxs-lookup"><span data-stu-id="91f15-174">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="91f15-175">Модуль сведений о заказе</span><span class="sxs-lookup"><span data-stu-id="91f15-175">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="91f15-176">Модуль подарочных сертификатов</span><span class="sxs-lookup"><span data-stu-id="91f15-176">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="91f15-177">Расчет наличия запасов для розничных каналов</span><span class="sxs-lookup"><span data-stu-id="91f15-177">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
