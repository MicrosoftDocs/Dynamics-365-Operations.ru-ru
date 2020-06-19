---
title: Модуль корзины
description: В этом разделе описываются модули корзины, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 3ba46fd90507a9cf8da92598c8449a2e553da352
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411281"
---
# <a name="cart-module"></a><span data-ttu-id="b6604-103">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="b6604-103">Cart module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b6604-104">В этом разделе описываются модули корзины, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b6604-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b6604-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="b6604-105">Overview</span></span>

<span data-ttu-id="b6604-106">Модуль корзины отображает элементы, которые были добавлены в корзину перед тем, как клиент переходит к оформлению заказа.</span><span class="sxs-lookup"><span data-stu-id="b6604-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="b6604-107">Модуль также показывает сводку заказа и позволяет клиенту применять коды рекламных акций или удалять их.</span><span class="sxs-lookup"><span data-stu-id="b6604-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="b6604-108">Модуль корзины поддерживает оформление заказа после входа в систему и оформление заказа для клиента-гостя.</span><span class="sxs-lookup"><span data-stu-id="b6604-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="b6604-109">Он также поддерживает ссылку **Назад к покупкам**.</span><span class="sxs-lookup"><span data-stu-id="b6604-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="b6604-110">Можно настроить маршрут для этой ссылки в **Параметры сайта \> Расширения \> Маршруты**.</span><span class="sxs-lookup"><span data-stu-id="b6604-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="b6604-111">Модуль корзины отображает данные на основе идентификатора корзины, который представляет собой файл cookie браузера, доступный на всем сайте.</span><span class="sxs-lookup"><span data-stu-id="b6604-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="b6604-112">На следующем рисунке показан пример страницы корзины на сайте Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="b6604-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Пример модуля корзины](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="b6604-114">Свойства и слоты модуля корзины</span><span class="sxs-lookup"><span data-stu-id="b6604-114">Cart module properties and slots</span></span>

<span data-ttu-id="b6604-115">В модуле корзины есть свойство **Заголовок**, для которого можно задать такие значения как **Корзина** и **Товары в корзине**.</span><span class="sxs-lookup"><span data-stu-id="b6604-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="b6604-116">Модули, которые могут быть использованы в модуле корзины</span><span class="sxs-lookup"><span data-stu-id="b6604-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="b6604-117">**Блок текста** — этот модуль поддерживает настраиваемые сообщения в модуле корзины.</span><span class="sxs-lookup"><span data-stu-id="b6604-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="b6604-118">Сообщения выдаются системой управления контентом (CMS).</span><span class="sxs-lookup"><span data-stu-id="b6604-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="b6604-119">Любое сообщение может быть добавлено, например "По вопросам, связанным с заказом, обращайтесь по телефону 1-800-Fabrikam."</span><span class="sxs-lookup"><span data-stu-id="b6604-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="b6604-120">**Выбор магазина** — этот модуль отображает список ближайших магазинов, в которых номенклатура доступна для получения.</span><span class="sxs-lookup"><span data-stu-id="b6604-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="b6604-121">Он позволяет пользователям вводить местоположение для поиска ближайших магазинов.</span><span class="sxs-lookup"><span data-stu-id="b6604-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="b6604-122">Дополнительные сведения об этом модуле см. в разделе [Модуль выбора магазина](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="b6604-122">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="b6604-123">Свойства модуля</span><span class="sxs-lookup"><span data-stu-id="b6604-123">Module properties</span></span>

<span data-ttu-id="b6604-124">Следующие параметры модуля корзины можно настроить в **Параметры сайта \> Расширения**:</span><span class="sxs-lookup"><span data-stu-id="b6604-124">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="b6604-125">**Максимальное количество** — это свойство используется для указания максимального количества каждой номенклатуры, которое может быть добавлено в корзину.</span><span class="sxs-lookup"><span data-stu-id="b6604-125">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="b6604-126">Например, розничная сеть может решить, что в одну проводку можно продать только 10 шт. каждого продукта.</span><span class="sxs-lookup"><span data-stu-id="b6604-126">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="b6604-127">**Запасы** — сведения о применении настроек запасов см. в разделе [Применение настроек запасов](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="b6604-127">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="b6604-128">**Назад к покупкам** — это свойство используется для указания маршрута для ссылки **Назад к покупкам**.</span><span class="sxs-lookup"><span data-stu-id="b6604-128">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="b6604-129">Маршрут может быть настроен на уровне сайта, что позволяет розничным продавцам вернуть клиента на домашнюю страницу или на любую другую страницу сайта.</span><span class="sxs-lookup"><span data-stu-id="b6604-129">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="b6604-130">Взаимодействие Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="b6604-130">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="b6604-131">Модуль корзины извлекает информацию о продукции с помощью интерфейсов API Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="b6604-131">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="b6604-132">Идентификатор корзины из cookie-файла браузера используется для получения всей информации о продукте из Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="b6604-132">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="b6604-133">Добавление модуля корзины на страницу</span><span class="sxs-lookup"><span data-stu-id="b6604-133">Add a cart module to a page</span></span>

<span data-ttu-id="b6604-134">Чтобы добавить модуль корзины на новую страницу и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b6604-134">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="b6604-135">Перейдите к разделу **Фрагменты страниц**, выберите **Создать**, чтобы создать фрагмент.</span><span class="sxs-lookup"><span data-stu-id="b6604-135">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="b6604-136">В диалоговом окне **Создать фрагмент страницы** выберите модуль **Корзина**.</span><span class="sxs-lookup"><span data-stu-id="b6604-136">In the **New Page Fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="b6604-137">В области **Имя фрагмента страницы** введите имя **Фрагмент корзины**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b6604-137">Under **Page Fragment Name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="b6604-138">Выберите слот **Корзина**.</span><span class="sxs-lookup"><span data-stu-id="b6604-138">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="b6604-139">В области свойств справа выберите символ карандаш, введите текст заголовка в поле, а затем выберите символ галочки.</span><span class="sxs-lookup"><span data-stu-id="b6604-139">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="b6604-140">В ячейке **Корзина** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="b6604-140">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b6604-141">В диалоговом окне **Добавить модуль** выберите модуль **Выбор магазина**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b6604-141">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b6604-142">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата фрагмента, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="b6604-142">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="b6604-143">Перейдите к пункту **Шаблоны**, выберите **Создать**, чтобы создать шаблон.</span><span class="sxs-lookup"><span data-stu-id="b6604-143">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="b6604-144">В диалоговом окне **Создать шаблон** в разделе **Имя шаблона** введите имя шаблона.</span><span class="sxs-lookup"><span data-stu-id="b6604-144">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="b6604-145">В древовидной структуре выберите слот **Основной текст**, нажмите многоточие (**…**), затем выберите **Добавить фрагмент**.</span><span class="sxs-lookup"><span data-stu-id="b6604-145">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="b6604-146">В диалоговом окне **Выбор фрагмента страницы** выберите созданный ранее **Фрагмент корзины** и нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b6604-146">In the **Select Page Fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="b6604-147">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="b6604-147">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="b6604-148">Перейдите к разделу **Страницы**, выберите **Создать**, чтобы создать страницу.</span><span class="sxs-lookup"><span data-stu-id="b6604-148">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="b6604-149">В диалоговом окне **Выбор шаблона** выберите созданный шаблон, введите имя страницы и нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b6604-149">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="b6604-150">Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть страницу.</span><span class="sxs-lookup"><span data-stu-id="b6604-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="b6604-151">Выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="b6604-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b6604-152">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b6604-152">Additional resources</span></span>

[<span data-ttu-id="b6604-153">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="b6604-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b6604-154">Модуль контейнера</span><span class="sxs-lookup"><span data-stu-id="b6604-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b6604-155">Модуль выбора магазина</span><span class="sxs-lookup"><span data-stu-id="b6604-155">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="b6604-156">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="b6604-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b6604-157">Модуль значка корзины</span><span class="sxs-lookup"><span data-stu-id="b6604-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="b6604-158">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="b6604-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b6604-159">Модуль подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="b6604-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b6604-160">Модуль верхнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="b6604-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="b6604-161">Модуль нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="b6604-161">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="b6604-162">Расчет наличия запасов для розничных каналов</span><span class="sxs-lookup"><span data-stu-id="b6604-162">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
