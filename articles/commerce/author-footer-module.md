---
title: Модуль нижнего колонтитула
description: В этом разделе описываются модули нижнего колонтитула, а также описывается, как разрабатывать их в Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 7c253cd9620180b09f2f5cae232e46d236deabdd
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697321"
---
# <a name="footer-module"></a><span data-ttu-id="1d119-103">Модуль нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="1d119-103">Footer module</span></span>  

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="1d119-104">В этом разделе описываются модули нижнего колонтитула, а также описывается, как создавать их в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1d119-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1d119-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="1d119-105">Overview</span></span>

<span data-ttu-id="1d119-106">Модуль нижнего колонтитула — это специальный контейнер, который используется для размещения модулей, появляющихся в нижнем колонтитуле страницы.</span><span class="sxs-lookup"><span data-stu-id="1d119-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="1d119-107">Например, он может содержать ссылки на различные страницы сайта, такие как , такие как страницы **Свяжитесь с нами** и **Политики магазина**.</span><span class="sxs-lookup"><span data-stu-id="1d119-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

## <a name="footer-module-properties"></a><span data-ttu-id="1d119-108">Свойства модуля нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="1d119-108">Footer module properties</span></span> 

<span data-ttu-id="1d119-109">Как и большинство контейнеров, модуль нижнего колонтитула поддерживает свойства для заголовка и ширины.</span><span class="sxs-lookup"><span data-stu-id="1d119-109">Like most containers, a footer module support properties for the heading and the width.</span></span> <span data-ttu-id="1d119-110">Он также поддерживает добавление нескольких модулей категории нижних колонтитулов.</span><span class="sxs-lookup"><span data-stu-id="1d119-110">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="1d119-111">Каждый добавляемый модуль категорий нижнего колонтитула отображается как столбец в модуле нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="1d119-111">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="1d119-112">Модули, доступные в модуле нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="1d119-112">Modules available in a footer module</span></span>

<span data-ttu-id="1d119-113">**Элементы нижнего колонтитула** — модуль элементов нижнего колонтитула может содержать заголовок, изображение и ссылку.</span><span class="sxs-lookup"><span data-stu-id="1d119-113">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="1d119-114">Заголовок может использоваться как отдельно, так и в сочетании с изображением и ссылкой.</span><span class="sxs-lookup"><span data-stu-id="1d119-114">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="1d119-115">Каждую ссылку в нижнем колонтитуле можно настроить таким образом, чтобы она состояла только из текста (например, ссылки "Свяжитесь с нами" и "Конфиденциальность") или имела и текст, и изображение (например, ссылки на социальные сети).</span><span class="sxs-lookup"><span data-stu-id="1d119-115">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="1d119-116">**К началу** — модуль "К началу" содержит ссылку для быстрого перехода к верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="1d119-116">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="1d119-117">Требуется место назначения.</span><span class="sxs-lookup"><span data-stu-id="1d119-117">A destination is required.</span></span> <span data-ttu-id="1d119-118">По умолчанию значением места назначения является #, что переводит пользователя в верхнюю часть страницы.</span><span class="sxs-lookup"><span data-stu-id="1d119-118">The default destination value is #, which takes the user to the top of the page.</span></span>

## <a name="author-a-footer-module"></a><span data-ttu-id="1d119-119">Разработка модуля нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="1d119-119">Author a footer module</span></span>

1. <span data-ttu-id="1d119-120">В области переходов выберите **Фрагменты**, затем выберите **Создать фрагмент страницы**.</span><span class="sxs-lookup"><span data-stu-id="1d119-120">In the navigation pane, select **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="1d119-121">В диалоговом окне **Создание фрагмента страницы** выберите модуль нижнего колонтитула, введите имя для фрагмента страницы, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1d119-121">In the **New Page Fragment** dialog box, select the footer module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="1d119-122">В древовидной структуре слева выберите кнопку с многоточием (**...**) для модуля нижнего колонтитула, затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="1d119-122">In the outline tree on the left, select the ellipsis button (**...**) for the footer module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="1d119-123">В диалоговом окне **Добавить модуль** выберите модуль категории нижнего колонтитула, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1d119-123">In the **Add Module** dialog box, select the footer category module, and then select **OK**.</span></span>
1. <span data-ttu-id="1d119-124">В древовидной структуре выберите кнопку с многоточием для модуля категории нижнего колонтитула, затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="1d119-124">In the outline tree, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="1d119-125">В диалоговом окне **Добавить модуль** выберите модуль элемента нижнего колонтитула, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1d119-125">In the **Add Module** dialog box, select the footer item module, and then select **OK**.</span></span>
1. <span data-ttu-id="1d119-126">В древовидной структуре выберите модуль элемента нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="1d119-126">In the outline tree, select the footer item module.</span></span> <span data-ttu-id="1d119-127">Затем в области свойств справа настройте требуемые заголовок, ссылку и текст ссылки, а также изображение.</span><span class="sxs-lookup"><span data-stu-id="1d119-127">Then, in the properties pane on the right, configure the heading, link and link text, and image as you require.</span></span>
1. <span data-ttu-id="1d119-128">Повторите шаги 5–7, чтобы добавить другие элементы нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="1d119-128">To add more footer items, repeat steps 5 through 7.</span></span>
1. <span data-ttu-id="1d119-129">Чтобы добавить в нижний колонтитул ссылку "К началу", выберите кнопку с многоточием для модуля категории нижнего колонтитула, затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="1d119-129">To add a "back to top" link to your footer, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="1d119-130">В диалоговом окне **Добавить модуль** выберите модуль "К началу", затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1d119-130">In the **Add Module** dialog box, select the back to top module, and then select **OK**.</span></span>
1. <span data-ttu-id="1d119-131">В древовидной структуре выберите модуль "К началу".</span><span class="sxs-lookup"><span data-stu-id="1d119-131">In the outline tree, select the back to top module.</span></span> <span data-ttu-id="1d119-132">Затем в области свойств справа выполните настройку модуля "К началу" по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="1d119-132">Then, in the properties pane on the right, configure the back to top module as you require.</span></span>
1. <span data-ttu-id="1d119-133">Сохраните фрагмент страницы, верните его и опубликуйте.</span><span class="sxs-lookup"><span data-stu-id="1d119-133">Save the page fragment, check it in, and publish it.</span></span>

<span data-ttu-id="1d119-134">На всех шаблонах страниц, созданных для сайта, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1d119-134">On every page template that has been created for the site, follow these steps.</span></span>

1. <span data-ttu-id="1d119-135">В слоте **Главный** страницы по умолчанию в модуле нижнего колонтитула добавьте созданный фрагмент нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="1d119-135">In the **Main** slot of the default page, in the footer module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="1d119-136">Сохраните шаблон, верните его и опубликуйте.</span><span class="sxs-lookup"><span data-stu-id="1d119-136">Save the template, check it in, and publish it.</span></span>

<span data-ttu-id="1d119-137">Добавление фрагмента страницы в шаблоны страниц помогает гарантировать отображение нижнего колонтитула на каждой странице.</span><span class="sxs-lookup"><span data-stu-id="1d119-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1d119-138">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1d119-138">Additional resources</span></span>

[<span data-ttu-id="1d119-139">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="1d119-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1d119-140">Модуль контейнера</span><span class="sxs-lookup"><span data-stu-id="1d119-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="1d119-141">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="1d119-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="1d119-142">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="1d119-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="1d119-143">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="1d119-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="1d119-144">Модуль подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="1d119-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="1d119-145">Модуль заголовка</span><span class="sxs-lookup"><span data-stu-id="1d119-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="1d119-146">Модуль нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="1d119-146">Footer module</span></span>](author-footer-module.md)
