---
title: Модуль нижнего колонтитула
description: В этом разделе описываются модули нижнего колонтитула, а также описывается, как разрабатывать их в Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d6e7b0ad4fe0723575a0ec55a9b02d110568db58
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797241"
---
# <a name="footer-module"></a><span data-ttu-id="3c996-103">Модуль нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="3c996-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="3c996-104">В этом разделе описываются модули нижнего колонтитула, а также описывается, как создавать их в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3c996-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3c996-105">Модуль нижнего колонтитула — это специальный контейнер, который используется для размещения модулей, появляющихся в нижнем колонтитуле страницы.</span><span class="sxs-lookup"><span data-stu-id="3c996-105">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="3c996-106">Например, он может содержать ссылки на различные страницы сайта, такие как , такие как страницы **Свяжитесь с нами** и **Политики магазина**.</span><span class="sxs-lookup"><span data-stu-id="3c996-106">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="3c996-107">На следующем рисунке показан пример модуля нижнего колонтитула на странице сайта.</span><span class="sxs-lookup"><span data-stu-id="3c996-107">The following image shows an example of a footer module on a site page.</span></span>

![Пример модуля нижнего колонтитула](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties&quot;></a><span data-ttu-id=&quot;3c996-109&quot;>Свойства модуля нижнего колонтитула</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3c996-109&quot;>Footer module properties</span></span> 

<span data-ttu-id=&quot;3c996-110&quot;>Как и большинство контейнеров, модуль нижнего колонтитула поддерживает свойства для заголовка и ширины.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3c996-110&quot;>Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id=&quot;3c996-111&quot;>Он также поддерживает добавление нескольких модулей категории нижних колонтитулов.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3c996-111&quot;>It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id=&quot;3c996-112&quot;>Каждый добавляемый модуль категорий нижнего колонтитула отображается как столбец в модуле нижнего колонтитула.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3c996-112&quot;>Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name=&quot;modules-available-in-a-footer-module&quot;></a><span data-ttu-id=&quot;3c996-113&quot;>Модули, доступные в модуле нижнего колонтитула</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3c996-113&quot;>Modules available in a footer module</span></span>

<span data-ttu-id=&quot;3c996-114&quot;>**Элементы нижнего колонтитула** — модуль элементов нижнего колонтитула может содержать заголовок, изображение и ссылку.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3c996-114&quot;>**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id=&quot;3c996-115&quot;>Заголовок может использоваться как отдельно, так и в сочетании с изображением и ссылкой.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;3c996-115&quot;>The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id=&quot;3c996-116&quot;>Каждую ссылку в нижнем колонтитуле можно настроить таким образом, чтобы она состояла только из текста (например, ссылки &quot;Свяжитесь с нами&quot; и &quot;Конфиденциальность") или имела и текст, и изображение (например, ссылки на социальные сети).</span><span class="sxs-lookup"><span data-stu-id="3c996-116">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="3c996-117">**К началу** — модуль "К началу" содержит ссылку для быстрого перехода к верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="3c996-117">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="3c996-118">Требуется место назначения.</span><span class="sxs-lookup"><span data-stu-id="3c996-118">A destination is required.</span></span> <span data-ttu-id="3c996-119">По умолчанию значением места назначения является \#, что переводит пользователя в верхнюю часть страницы.</span><span class="sxs-lookup"><span data-stu-id="3c996-119">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="3c996-120">Создание модуля нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="3c996-120">Create a footer module</span></span>

1. <span data-ttu-id="3c996-121">Перейдите к разделу **Фрагменты**, выберите **Создать**, чтобы создать фрагмент.</span><span class="sxs-lookup"><span data-stu-id="3c996-121">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="3c996-122">В диалоговом окне **Создание фрагмента** выберите модуль **Контейнер**, введите имя для фрагмента, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3c996-122">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="3c996-123">В ячейке **Контейнер по умолчанию** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="3c996-123">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3c996-124">В диалоговом окне **Добавить модуль** выберите модуль **Категория нижнего колонтитула**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3c996-124">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3c996-125">В ячейке **Категория нижнего колонтитула** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="3c996-125">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3c996-126">В диалоговом окне **Добавить модуль** выберите модуль **Элемент нижнего колонтитула**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3c996-126">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3c996-127">Выберите ячейку **Элемент нижнего колонтитула**, затем в области свойств справа настройте требуемые заголовок, ссылку и текст ссылки, а также изображение.</span><span class="sxs-lookup"><span data-stu-id="3c996-127">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="3c996-128">Повторите шаги 5–7, чтобы добавить другие элементы нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="3c996-128">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="3c996-129">Чтобы добавить в нижний колонтитул ссылку "К началу", выберите многоточие (**…**) в ячейке **Категория нижнего колонтитула**, затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="3c996-129">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="3c996-130">В диалоговом окне **Добавить модуль** выберите модуль **К началу**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3c996-130">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3c996-131">Выберите ячейку **К началу**, затем в области свойств справа настройте требуемые текст и другие свойства модуля.</span><span class="sxs-lookup"><span data-stu-id="3c996-131">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="3c996-132">Выберите **Завершить редактирование** для возврата фрагмента, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="3c996-132">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="3c996-133">Чтобы гарантировать, что заголовок появляется на каждой странице, выполните следующие действия в каждом шаблоне страниц, созданном для сайта.</span><span class="sxs-lookup"><span data-stu-id="3c996-133">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="3c996-134">В слоте **Нижний колонтитул** модуля **Страница по умолчанию** добавьте созданный фрагмент нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="3c996-134">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="3c996-135">Выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="3c996-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="3c996-136">Добавление фрагмента в шаблоны страниц помогает гарантировать отображение нижнего колонтитула на каждой странице.</span><span class="sxs-lookup"><span data-stu-id="3c996-136">By adding the fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3c996-137">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3c996-137">Additional resources</span></span>

[<span data-ttu-id="3c996-138">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="3c996-138">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3c996-139">Модуль контейнера</span><span class="sxs-lookup"><span data-stu-id="3c996-139">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="3c996-140">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="3c996-140">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="3c996-141">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="3c996-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="3c996-142">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="3c996-142">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="3c996-143">Модуль подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="3c996-143">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="3c996-144">Модуль заголовка</span><span class="sxs-lookup"><span data-stu-id="3c996-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="3c996-145">Модуль нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="3c996-145">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]