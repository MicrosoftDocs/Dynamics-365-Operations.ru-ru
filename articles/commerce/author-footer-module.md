---
title: Модуль нижнего колонтитула
description: В этом разделе описываются модули нижнего колонтитула, а также описывается, как разрабатывать их в Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6dd9f214fbeeeaabadac4853916363c20a3288ca
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761210"
---
# <a name="footer-module"></a><span data-ttu-id="ffbfe-103">Модуль нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="ffbfe-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="ffbfe-104">В этом разделе описываются модули нижнего колонтитула, а также описывается, как создавать их в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ffbfe-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="ffbfe-105">Overview</span></span>

<span data-ttu-id="ffbfe-106">Модуль нижнего колонтитула — это специальный контейнер, который используется для размещения модулей, появляющихся в нижнем колонтитуле страницы.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="ffbfe-107">Например, он может содержать ссылки на различные страницы сайта, такие как , такие как страницы **Свяжитесь с нами** и **Политики магазина**.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="ffbfe-108">На следующем рисунке показан пример модуля нижнего колонтитула на странице сайта.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-108">The following image shows an example of a footer module on a site page.</span></span>

![Пример модуля нижнего колонтитула](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="ffbfe-110">Свойства модуля нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="ffbfe-110">Footer module properties</span></span> 

<span data-ttu-id="ffbfe-111">Как и большинство контейнеров, модуль нижнего колонтитула поддерживает свойства для заголовка и ширины.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-111">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="ffbfe-112">Он также поддерживает добавление нескольких модулей категории нижних колонтитулов.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-112">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="ffbfe-113">Каждый добавляемый модуль категорий нижнего колонтитула отображается как столбец в модуле нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-113">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="ffbfe-114">Модули, доступные в модуле нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="ffbfe-114">Modules available in a footer module</span></span>

<span data-ttu-id="ffbfe-115">**Элементы нижнего колонтитула** — модуль элементов нижнего колонтитула может содержать заголовок, изображение и ссылку.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-115">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="ffbfe-116">Заголовок может использоваться как отдельно, так и в сочетании с изображением и ссылкой.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-116">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="ffbfe-117">Каждую ссылку в нижнем колонтитуле можно настроить таким образом, чтобы она состояла только из текста (например, ссылки "Свяжитесь с нами" и "Конфиденциальность") или имела и текст, и изображение (например, ссылки на социальные сети).</span><span class="sxs-lookup"><span data-stu-id="ffbfe-117">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="ffbfe-118">**К началу** — модуль "К началу" содержит ссылку для быстрого перехода к верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-118">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="ffbfe-119">Требуется место назначения.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-119">A destination is required.</span></span> <span data-ttu-id="ffbfe-120">По умолчанию значением места назначения является \#, что переводит пользователя в верхнюю часть страницы.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-120">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="ffbfe-121">Создание модуля нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="ffbfe-121">Create a footer module</span></span>

1. <span data-ttu-id="ffbfe-122">Перейдите к разделу **Фрагменты**, выберите **Создать**, чтобы создать фрагмент.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-122">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="ffbfe-123">В диалоговом окне **Создание фрагмента** выберите модуль **Контейнер**, введите имя для фрагмента, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-123">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="ffbfe-124">В ячейке **Контейнер по умолчанию** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-124">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="ffbfe-125">В диалоговом окне **Добавить модуль** выберите модуль **Категория нижнего колонтитула**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-125">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="ffbfe-126">В ячейке **Категория нижнего колонтитула** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-126">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="ffbfe-127">В диалоговом окне **Добавить модуль** выберите модуль **Элемент нижнего колонтитула**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-127">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="ffbfe-128">Выберите ячейку **Элемент нижнего колонтитула**, затем в области свойств справа настройте требуемые заголовок, ссылку и текст ссылки, а также изображение.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-128">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="ffbfe-129">Повторите шаги 5–7, чтобы добавить другие элементы нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-129">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="ffbfe-130">Чтобы добавить в нижний колонтитул ссылку "К началу", выберите многоточие (**…**) в ячейке **Категория нижнего колонтитула**, затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-130">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="ffbfe-131">В диалоговом окне **Добавить модуль** выберите модуль **К началу**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-131">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="ffbfe-132">Выберите ячейку **К началу**, затем в области свойств справа настройте требуемые текст и другие свойства модуля.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-132">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="ffbfe-133">Выберите **Завершить редактирование** для возврата фрагмента, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-133">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="ffbfe-134">Чтобы гарантировать, что заголовок появляется на каждой странице, выполните следующие действия в каждом шаблоне страниц, созданном для сайта.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-134">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="ffbfe-135">В слоте **Нижний колонтитул** модуля **Страница по умолчанию** добавьте созданный фрагмент нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-135">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="ffbfe-136">Выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-136">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="ffbfe-137">Добавление фрагмента в шаблоны страниц помогает гарантировать отображение нижнего колонтитула на каждой странице.</span><span class="sxs-lookup"><span data-stu-id="ffbfe-137">By adding the fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ffbfe-138">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ffbfe-138">Additional resources</span></span>

[<span data-ttu-id="ffbfe-139">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="ffbfe-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ffbfe-140">Модуль контейнера</span><span class="sxs-lookup"><span data-stu-id="ffbfe-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="ffbfe-141">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="ffbfe-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="ffbfe-142">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="ffbfe-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="ffbfe-143">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="ffbfe-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="ffbfe-144">Модуль подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="ffbfe-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="ffbfe-145">Модуль заголовка</span><span class="sxs-lookup"><span data-stu-id="ffbfe-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="ffbfe-146">Модуль нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="ffbfe-146">Footer module</span></span>](author-footer-module.md)
